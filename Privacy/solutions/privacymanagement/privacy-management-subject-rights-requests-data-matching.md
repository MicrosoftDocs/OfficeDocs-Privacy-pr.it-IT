---
title: Gestire la corrispondenza dei dati per le richieste di diritti dell'oggetto nella gestione della privacy
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: Scopri come caricare informazioni aggiuntive sulla gestione della privacy sugli interessati.
ms.openlocfilehash: 00a902705336d766993e805d78609a48334b2bf6
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478273"
---
# <a name="manage-data-matching-for-subject-rights-requests"></a>Gestire la corrispondenza dei dati per le richieste di diritti dell'oggetto

Con la corrispondenza dei dati, le organizzazioni possono consentire la gestione della privacy per identificare gli interessati in base ai valori dei dati forniti. Ciò consente di aumentare l'accuratezza dell'individuazione del contenuto dell'oggetto dei dati che corrisponde a tali valori sia per il personale interno che per gli utenti esterni con cui si interagisce. Semplifica inoltre la necessità di fornire manualmente i campi durante la creazione delle richieste di diritti dell'oggetto e fornisce il contesto all'interno delle richieste di diritti dell'oggetto e per il riquadro Panoramica che mostra gli elementi con il maggior numero di contenuti dell'oggetto dati. Per ulteriori informazioni su tale visualizzazione, vedere [Trovare e visualizzare i dati.](privacy-management-data-profile.md#items-with-the-most-data-subject-content)

Per utilizzare la funzionalità di corrispondenza dei dati, è necessario essere membri del gruppo di ruoli Gestione privacy. Dall'interno della gestione della privacy [nella](https://compliance.microsoft.com/)Centro conformità Microsoft 365 , **selezionare** Impostazioni nella barra di spostamento superiore e quindi **Corrispondenza dati**. Da qui, sarà necessario definire lo schema dei dati personali e fornire un caricamento dei dati personali come illustrato di seguito. Tieni presente che puoi aggiungere elementi e puoi eliminare gli elementi aggiunti tramite l'interfaccia utente. Tuttavia, al momento non puoi modificare un elemento sul posto dall'interfaccia utente.

## <a name="prepare-for-data-import"></a>Preparare l'importazione dei dati

Prima di definire lo schema o caricare i dati, è necessario identificare l'origine delle informazioni sull'oggetto dei dati. Il formato di file richiesto è .csv, che può essere letto da un'applicazione, ad esempio Microsoft Excel. Strutturare l'esportazione in modo che le intestazioni di colonna vengano visualizzate nella prima riga. Queste intestazioni devono includere i nomi degli attributi per lo schema dei dati personali. Controllare il formato dei dati in ogni campo. Se uno dei dati contiene virgole, racchiudere questi valori tra virgolette doppie per assicurarsi che non siano analizzati in campi separati.

## <a name="define-the-personal-data-schema"></a>Definire lo schema dei dati personali

Lo schema dei dati personali descrive gli attributi per gli interessati. Upload questo schema nella prima scheda dell'area delle impostazioni di corrispondenza dei dati. I file necessari includono un file XML **dello schema** dei dati personali e un file XML **del pacchetto** di regole.

### <a name="personal-data-schema-xml"></a>XML dello schema dei dati personali

Il file dello schema dei dati personali è un file XML che definisce i nomi di colonna previsti.

- Assegnare a questo file di schema *il nomepdm.xml*.
- Definire ogni nome di colonna utilizzando il tag Nome campo, come illustrato nell'esempio seguente.
- Utilizzare searchable = "true" per i campi che si desidera siano disponibili per la ricerca, fino a un massimo di cinque campi. Almeno uno dei nomi di campo deve essere ricercabile. Sintassi di esempio: `\<Field name="" searchable=""/>` .
- Lo schema dei dati personali include una sezione tag DataStore. È necessario mappare quattro campi obbligatori ai nomi dei campi: primaryKeyField, upnField, firstNameField, lastNameField.

Ad esempio, il file XML seguente definisce uno schema di esempio, con cinque campi specificati come ricercabili: PatientID, MRN, SSN, Telefono e DOB. PrimaryKeyField è mappato a PatientID, upnField è mappato a MRN, firstNameField è mappato a FirstName e lastNameField è mappato a LastName.

È possibile copiare, modificare e usare l'esempio.

 ```xml
<PdmSchema xmlns="http://schemas.microsoft.com/office/2020/pdm">
      <DataStore name="Patientrecords" description="Schema for patient records" version="1" primaryKeyField="PatientID" upnField="MRN" firstNameField="FirstName" lastNameField="LastName">
            <Field name="PatientID" searchable="true"/>
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</PdmSchema>
 ```

### <a name="rule-package-xml"></a>XML del pacchetto di regole

Quando si configura il pacchetto di regole, assicurarsi di fare riferimento correttamente al file dello schema dei dati personali creato in precedenza: pdm.xml. Nel codice XML del pacchetto di regole di esempio seguente, i campi seguenti devono essere personalizzati per creare il tipo di corrispondenza dati sensibile:

- **RulePack id**  &  **PrivacyMatch id:** utilizzare New-GUID per generare un GUID.
- **Archivio dati**: questo campo specifica l'archivio dati di ricerca di corrispondenza dei dati personali da utilizzare. Specificare il nome datastore definito di uno schema di dati personali configurato.
- **idMatch:** questo campo punta all'elemento principale per la corrispondenza dei dati personali.
  - **Corrisponde** a : Specifica il campo da utilizzare nella ricerca esatta. Specificare un nome di campo ricercabile dallo schema dei dati personali.
  - **Classificazione:** questo campo specifica la corrispondenza del tipo sensibile che attiva la ricerca della corrispondenza dei dati personali. È possibile specificare il nome o il GUID di un tipo di informazioni sensibili predefinito o personalizzato esistente. Per evitare problemi di prestazioni, se si utilizza un tipo di informazioni riservate personalizzato come elemento Classification nei dati personali, non utilizzare un tipo di informazioni riservate personalizzato che corrisponderà a una grande percentuale di contenuto (ad esempio "qualsiasi numero" o "qualsiasi parola di cinque lettere"). È consigliabile aggiungere parole chiave di supporto o includere la formattazione nella definizione del tipo di informazioni riservate per la classificazione personalizzata.
- **Match**: questo campo punta a prove aggiuntive trovate in prossimità di idMatch.
  - **Corrisponde** a : specificare qualsiasi nome di campo nello schema dei dati personali per DataStore.
- **Risorsa:** questa sezione specifica il nome e la descrizione per il tipo sensibile in più impostazioni locali.
  - **idRef:** specificare il GUID per l'ID ExactMatch.
  - **Nome & descrizioni**: personalizzare in base alle esigenze.

Nell'esempio XML del pacchetto di regole seguente si fa riferimento al file di esempio pdm.xml del passaggio precedente che crea l'XML dello schema dei dati personali:

- **Datastore**: il nome dataStore fa riferimento al file di schema creato in precedenza: dataStore = "PatientRecords".
- **idMatch**: il valore idMatch fa riferimento a un campo ricercabile elencato nel file pdm.xml creato in precedenza: idMatch matches = "SSN".
  - **Classificazione**: il valore di classificazione fa riferimento a un tipo di informazioni riservate esistente o personalizzato: classification = "U.S. Social Security Number (SSN)". In questo caso, viene usato il tipo di informazioni sensibili esistente del Numero di previdenza sociale degli Stati Uniti.

Crea un pacchetto di regole in formato XML (con codifica Unicode), come nel codice di esempio seguente. È possibile copiare, modificare e utilizzare questo esempio.

 ```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2020/pdm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b21">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care PDM Rulepack</Name>
        <Description>This rule package contains the Personal Data Match sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <PrivacyMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB381" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="6">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </PrivacyMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB381">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">PDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
 ```

## <a name="upload-personal-data"></a>Upload personali
Dopo aver definito lo schema dei dati personali, è possibile eseguire il caricamento dei dati **personali** nella seconda scheda della pagina delle impostazioni di corrispondenza dei dati. Quando si seleziona **Aggiungi**, scegliere lo schema personale definito nel primo passaggio, quindi caricare il file contenente i dati personali.

È possibile caricare questi dati personali scegliendo un file locale o fornendo un URL della firma di accesso condiviso a un percorso Archiviazione di Microsoft Azure esistente contenente il file di dati personali.
Se è stato preparato un file come primo passaggio di questo processo conforme allo schema creato, è possibile utilizzare tale file per il caricamento.

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

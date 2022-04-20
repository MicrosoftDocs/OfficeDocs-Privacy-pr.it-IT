---
title: Corrispondenza dei dati per le richieste di diritti dell'interessato
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: Informazioni su come caricare informazioni aggiuntive in Microsoft Priva sugli interessati.
ms.openlocfilehash: 76bd16f99a4a8ff9733c37a5787113e96c76c31c
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930583"
---
# <a name="data-matching-for-subject-rights-requests"></a>Corrispondenza dei dati per le richieste di diritti dell'interessato

Con la corrispondenza dei dati, le organizzazioni possono consentire a Microsoft Priva di identificare gli interessati in base a valori di dati forniti esatti. Ciò consente di aumentare l'accuratezza dell'individuazione del contenuto dell'interessato che corrisponde a tali valori di dati sia per il personale interno che per gli utenti esterni con cui si interagisce. Semplifica anche la necessità di fornire manualmente i campi durante la creazione delle richieste di diritti dell'oggetto e fornisce il contesto all'interno delle richieste di diritti dell'oggetto e per il riquadro Panoramica che mostra gli elementi con il maggior contenuto dell'interessato. Per altre informazioni su tale visualizzazione, vedere [Trovare e visualizzare i dati personali in Priva](priva-data-profile.md#items-with-the-most-data-subject-content).

Per usare la funzionalità di corrispondenza dei dati, è necessario essere membri del gruppo di ruoli Gestione privacy. Da Priva nel portale di [conformità di Microsoft Purview](https://compliance.microsoft.com/) selezionare **Impostazioni** nel riquadro di spostamento superiore e quindi **Corrispondenza dei dati**. Da qui, sarà necessario definire lo schema dei dati personali e fornire un caricamento dei dati personali come illustrato di seguito. Si noti che è possibile aggiungere elementi ed eliminare gli elementi aggiunti tramite l'interfaccia utente. Al momento, tuttavia, non è possibile modificare un elemento sul posto dall'interfaccia utente.

## <a name="prepare-for-data-import"></a>Preparare l'importazione dei dati

Prima di definire lo schema o caricare i dati, è necessario identificare l'origine delle informazioni dell'interessato. Il formato di file richiesto è .csv, che può essere letto da un'applicazione, ad esempio Microsoft Excel. Strutturare l'esportazione in modo che le intestazioni di colonna vengano visualizzate nella prima riga. Queste intestazioni devono includere i nomi degli attributi per lo schema dei dati personali. Controllare il formato dei dati in ogni campo. Se uno dei dati contiene virgole, racchiudere questi valori tra virgolette doppie per assicurarsi che non vengano analizzati in campi separati.

## <a name="define-the-personal-data-schema"></a>Definire lo schema dei dati personali

Lo schema dei dati personali descriverà gli attributi per gli interessati. Upload questo schema nella prima scheda dell'area delle impostazioni di corrispondenza dei dati. I file necessari includono un file XML **dello schema dei dati personali** e un file XML **del pacchetto di regole** .

### <a name="personal-data-schema-xml"></a>XML dello schema dei dati personali

Il file di schema dei dati personali è un file XML che definirà quali nomi di colonna sono previsti.

- Assegnare a questo file di schema *il nomepdm.xml*.
- Definire ogni nome di colonna usando il tag Nome campo come illustrato nell'esempio seguente.
- Usare ricercabile = "true" per i campi di cui si vuole eseguire la ricerca, fino a un massimo di cinque campi. Almeno uno dei nomi dei campi deve essere ricercabile. Sintassi di esempio: `\<Field name="" searchable=""/>`.
- Lo schema dei dati personali include una sezione tag DataStore. È necessario eseguire il mapping di quattro campi obbligatori ai nomi dei campi: primaryKeyField, upnField, firstNameField, lastNameField.

Ad esempio, il file XML seguente definisce uno schema di esempio, con cinque campi specificati come ricercabili: PatientID, MRN, SSN, Telefono e DOB. Il parametro primaryKeyField viene mappato a PatientID, upnField viene mappato a MRN, firstNameField viene mappato a FirstName e lastNameField viene mappato a LastName.

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

Quando si configura il pacchetto di regole, assicurarsi di fare riferimento correttamente al file di schema dei dati personali creato in precedenza: pdm.xml. Nel codice XML del pacchetto di regole di esempio seguente, è necessario personalizzare i campi seguenti per creare il tipo sensibile di corrispondenza dei dati:

- **ID** &  RulePack **ID PrivacyMatch**: usare New-GUID per generare un GUID.
- **Archivio dati**: questo campo specifica l'archivio dati di ricerca delle corrispondenze dei dati personali da usare. Specificare il nome datastore definito di uno schema di dati personali configurato.
- **idMatch**: questo campo punta all'elemento primario per la corrispondenza dei dati personali.
  - **Corrispondenze**: specifica il campo da utilizzare nella ricerca esatta. Specificare un nome di campo ricercabile dallo schema dei dati personali.
  - **Classificazione**: questo campo specifica la corrispondenza del tipo sensibile che attiva la ricerca della corrispondenza dei dati personali. È possibile specificare il nome o il GUID di un tipo di informazioni sensibili predefinito o personalizzato esistente. Per evitare di causare problemi di prestazioni, se si usa un tipo di informazioni sensibili personalizzato come elemento classificazione nella corrispondenza dei dati personali, non usare un tipo di informazioni sensibili personalizzato che corrisponderà a una grande percentuale di contenuto (ad esempio "qualsiasi numero" o "qualsiasi parola di cinque lettere"). È consigliabile aggiungere parole chiave di supporto o includere la formattazione nella definizione del tipo di informazioni riservate per la classificazione personalizzata.
- **Corrispondenza**: questo campo punta a prove aggiuntive trovate in prossimità di idMatch.
  - **Corrispondenze**: specificare qualsiasi nome di campo nello schema dei dati personali per DataStore.
- **Risorsa**: questa sezione specifica il nome e la descrizione per il tipo sensibile in più impostazioni locali.
  - **idRef**: specificare il GUID per l'ID ExactMatch.
  - **Nome & descrizioni**: personalizzare in base alle esigenze.

Nell'esempio XML del pacchetto di regole seguente viene fatto riferimento al file di esempio pdm.xml del passaggio precedente che crea il codice XML dello schema dei dati personali:

- **Archivio dati**: il nome dell'archivio dati fa riferimento al file di schema creato in precedenza: dataStore = "PatientRecords".
- **idMatch**: il valore idMatch fa riferimento a un campo ricercabile elencato nel file pdm.xml creato in precedenza: idMatch corrisponde a = "SSN".
  - **Classificazione**: il valore di classificazione fa riferimento a un tipo di informazioni riservate esistente o personalizzato: classification = "U.S. Social Security Number (SSN)". In questo caso, viene usato il tipo di informazioni sensibili esistente del Numero di previdenza sociale degli Stati Uniti.

Creare un pacchetto di regole in formato XML (con codifica Unicode), come nel codice di esempio seguente. È possibile copiare, modificare e usare questo esempio.

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

## <a name="upload-personal-data"></a>Upload dati personali
Dopo aver definito lo schema dei dati personali, è possibile eseguire il **caricamento dei dati personali** nella seconda scheda della pagina delle impostazioni di corrispondenza dei dati. Quando si seleziona **Aggiungi**, scegliere lo schema personale definito nel primo passaggio, quindi caricare il file contenente i dati personali.

È possibile caricare questi dati personali scegliendo un file locale o fornendo un URL di firma di accesso condiviso a un percorso di Archiviazione di Microsoft Azure esistente contenente il file di dati personali.
Se è stato preparato un file come primo passaggio di questo processo conforme allo schema creato, è possibile usare tale file per il caricamento.

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

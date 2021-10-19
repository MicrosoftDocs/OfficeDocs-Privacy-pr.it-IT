---
title: Creare e personalizzare criteri nella gestione della privacy
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
description: Informazioni su come creare e personalizzare i criteri di privacy per la gestione dei dati personali dell'organizzazione in Microsoft 365.
ms.openlocfilehash: 2e130e59cc860094f64a0b09fbbdf8c565ebf167
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478261"
---
# <a name="create-and-customize-privacy-management-policies"></a>Creare e personalizzare i criteri di gestione della privacy

È possibile creare nuovi criteri nella gestione della privacy per affrontare gli scenari di rischio per la privacy importanti per l'organizzazione. Per una guida introduttiva, usare i modelli predefiniti per creare nuovi criteri per la sovraesposizione dei dati, i trasferimenti di dati e la riduzione dei dati e gli scenari. Puoi anche personalizzare i tuoi criteri, usando uno qualsiasi di questi modelli come punto di partenza.

Durante la creazione o la modifica dei criteri, è possibile configurare le notifiche di posta elettronica o, se disponibili, suggerimenti sui criteri per Teams per portare le corrispondenze dei criteri all'attenzione degli utenti per la correzione.

## <a name="create-a-policy-from-a-template"></a>Creare un criterio da un modello

Seguire questa procedura per creare un criterio utilizzando uno dei modelli predefiniti.

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/), passare alla sezione Gestione della privacy e selezionare **Criteri**.
1. Selezionare **Crea un criterio**.
1. Scegliere il tipo di modello desiderato. Verrà aperto un riquadro a comparsa con informazioni sul modello.
1. Per esaminare le impostazioni predefinite del modello, inclusi i tipi di dati, i percorsi dei dati e le condizioni che attivano le corrispondenze dei criteri, selezionare **Visualizza impostazioni.**
     - È possibile selezionare Modifica **impostazioni** per apportare modifiche. Questo ti inserirà nella procedura guidata per la personalizzazione delle impostazioni.
1. Se si è pronti a utilizzare le impostazioni predefinite, assegnare un nome descrittivo al criterio e selezionare **Crea criterio.**

Quando si crea un criterio direttamente da un modello, verranno scelte automaticamente molte impostazioni. Verrà inoltre avviato in modalità test per impostazione predefinita, il che significa che non verranno generati avvisi o notifiche. Se si è pronti per attivare completamente il criterio dopo l'esecuzione in modalità test e la revisione dei risultati del criterio, è possibile trovarlo nell'elenco dei criteri e modificare il criterio per attivarlo.

## <a name="create-a-custom-privacy-management-policy"></a>Creare criteri di gestione della privacy personalizzati

Per assumere un controllo granulare delle impostazioni di un criterio, è possibile creare un criterio personalizzato utilizzando uno dei modelli esistenti come base. La gestione della privacy fornisce una procedura guidata per guidare l'utente attraverso questi passaggi.

Tutti i tipi di criteri seguono questo flusso di base. Alcune impostazioni e opzioni cambieranno a seconda del criterio scelto.

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/), passare alla sezione Gestione della privacy e selezionare **Criteri**.
1. Selezionare **Crea un criterio**.
1. Scegliere **l'opzione** Personalizzata per iniziare a usare la procedura guidata.
1. Scegli il tipo di modello di base: **sovraesposizione** dei dati, trasferimenti di **dati** o **minimizzazione dei dati.** Ognuno di essi offrirà alcune opzioni durante la creazione dei criteri.
1. Assegnare un nome e descrivere i criteri. È consigliabile usare nomi descrittivi chiari per identificare i criteri, poiché questi nomi verranno visualizzati in un secondo momento negli avvisi sulle corrispondenze dei criteri.
1. Procedere con la procedura guidata e scegliere le impostazioni desiderate. Le opzioni disponibili sono:
    - **Dati da monitorare:** selezionare il tipo di dati personali che verranno monitorati dal criterio.
    - **Utenti e gruppi**: applicare i criteri a tutti gli utenti o a utenti selezionati.
    - **Posizioni**: applica i criteri alle aree selezionate in Microsoft 365.
    - **Condizioni**: impostare le condizioni per i criteri. Queste opzioni variano a seconda del tipo di criterio.
    - **Risultati**: definire i risultati quando viene trovata una corrispondenza dei criteri, ad esempio le notifiche degli utenti.
    - **Avvisi**: decidere la frequenza degli avvisi per gli amministratori quando viene trovata una corrispondenza dei criteri.
    - **Mode:** scegli se eseguire o meno il criterio prima in modalità test.
1. Al termine di tutte le impostazioni, rivedere le scelte effettuate, apportare le modifiche desiderate e quindi selezionare **Invia** per creare il criterio.

## <a name="learn-about-key-settings-for-all-policies"></a>Informazioni sulle impostazioni chiave per tutti i criteri

### <a name="choose-data-to-monitor"></a>Scegliere i dati da monitorare

Quando si modifica o si configura qualsiasi tipo di criterio personalizzato, verrà richiesto di selezionare i tipi di dati da monitorare. Le opzioni sono le seguenti:

- **Gruppi di classificazione:** elenco di set di dati ricercabili in base alle normative chiave sulla privacy, ad esempio GDPR o HIPAA. Visualizza i dettagli di qualsiasi gruppo per sapere quali tipi di informazioni riservate copre. Seleziona uno o più di questi set per usarli così come sono.
- **Tipi di informazioni** riservate individuali: scegliendo tipi di informazioni riservate specifici, ad esempio numeri di previdenza sociale o informazioni sulla patente di guida, è possibile personalizzare il proprio gruppo o gruppi di dati da cercare. Questa procedura guidata consente di selezionare dall'elenco completo dei tipi di informazioni riservate all'interno della gestione della privacy. Ogni tipo di informazioni dispone di proprietà specifiche. Usa il pulsante info accanto a uno di essi per informazioni dettagliate e note sulle impostazioni consigliate. Se si creano più gruppi, la procedura guidata consente di applicare operatori booleani per correlarli e definire l'ordine delle operazioni.

Se si seleziona uno dei gruppi di classificazione esistenti, non è inoltre possibile selezionare singoli tipi o creare gruppi personalizzati. Per la massima flessibilità, scegli singoli tipi di informazioni riservate. Per utilizzare gli standard più comuni, scegliere tra i gruppi di classificazione.

### <a name="set-user-email-notifications"></a>Impostare le notifiche di posta elettronica degli utenti

Con [le notifiche tramite posta](privacy-management-policies-notifications.md)elettronica, è possibile inviare notifiche sulle corrispondenze dei criteri direttamente ai proprietari del contenuto. Questi messaggi di posta elettronica riepilogano quali dati devono essere esaminati e le possibili azioni da eseguire, ad esempio rendere privati i documenti, mantenerli nei file, segnalare eventuali corrispondenze false positive e aggiungere note per riferimento futuro. Questi messaggi di posta elettronica includono anche collegamenti per i destinatari della formazione su come gestire questi casi. La fornitura di questi collegamenti è necessaria e deve puntare alla propria documentazione interna su processi e procedure consigliate.

Le notifiche possono essere abilitate per singoli criteri durante la creazione di criteri personalizzati o durante la modifica di qualsiasi criterio. Imposta le preferenze nella **sezione** Risultati.

Le impostazioni obbligatorie includono la frequenza delle notifiche e il collegamento alla formazione sulla privacy.

Le impostazioni facoltative includono alcuni campi personalizzabili per i messaggi di posta elettronica. Seleziona **l'opzione Anteprima e modifica messaggio di** notifica per aprire un riquadro a comparsa che mostra una notifica di esempio. Qui puoi modificare la riga dell'oggetto del messaggio di posta elettronica, l'intestazione e il corpo del testo, il nome visualizzato e l'URL per la formazione sulla privacy.

Tieni presente che la capacità complessiva della gestione della privacy di inviare notifiche tramite posta elettronica è controllata in **Impostazioni**. È disabilitato per impostazione predefinita. La disattivazione di questa impostazione arresterà tutti i messaggi di posta elettronica anche se le notifiche sono state configurate a livello di singolo criterio.

## <a name="learn-about-settings-for-data-minimization-policies"></a>Informazioni sulle impostazioni per i criteri di minimizzazione dei dati

I criteri di minimizzazione dei dati si concentrano sull'età del contenuto e sulla durata dell'ultima modifica. Il monitoraggio dei dati personali ancora conservati in contenuti inutilizzati meno recenti consente di gestire meglio i dati archiviati e ridurre i rischi. Questa impostazione viene gestita nella **schermata** Condizioni.

Per impostazione predefinita, i criteri di minimizzazione dei dati ricercano il contenuto contenente dati personali creati o modificati per l'ultima volta almeno 60 giorni fa. Quando si modifica o si crea un criterio personalizzato, è possibile scegliere tra altri tempi preimpostati.

## <a name="learn-about-settings-for-data-transfer-policies"></a>Informazioni sulle impostazioni per i criteri di trasferimento dei dati

I criteri di trasferimento dei dati consentono di monitorare i dati trasferiti tra determinate aree geografiche del mondo o tra diversi reparti dell'organizzazione. Nella schermata **Condizioni** è possibile scegliere quali tipi di trasferimenti devono essere cercati dalla gestione della privacy.

Per impostazione predefinita, i criteri di trasferimento dei dati ricercano i trasferimenti tra il Nord America e altre aree geografiche. Quando si modifica o si crea un criterio personalizzato, è possibile scegliere il tipo di trasferimento e quindi effettuare selezioni per le aree o i reparti del mittente e del destinatario.

I criteri di trasferimento dei dati supportano anche la fornitura di suggerimenti e suggerimenti per i criteri agli utenti in Teams, in modo che possano rimanere informati sulle procedure consigliate per la gestione dei dati. Questa opzione può essere attivata/disattivata **nella schermata** Risultati.

## <a name="learn-about-settings-for-data-overexposure-policies"></a>Informazioni sulle impostazioni per i criteri di sovraesposizione dei dati

L'organizzazione può archiviare contenuto a vari livelli di accesso, incluse le aree accessibili pubblicamente e altre con restrizioni. Nella schermata **Condizioni** puoi scegliere di fare in modo che la gestione della privacy possa cercare potenziali sovraesposizione dei dati per il contenuto archiviato in uno dei livelli di accesso seguenti:

- **Pubblico:** chiunque abbia un collegamento può visualizzare questo contenuto.
- **Esterno:** persone specifiche esterne all'organizzazione hanno accesso.
- **Interno**: gli utenti dell'organizzazione hanno accesso.

Per impostazione predefinita, i criteri di sovraesposizione dei dati valutano tutti e tre i livelli di accesso. Quando si modifica o si crea un criterio personalizzato, è possibile scegliere tutti o uno di questi livelli.

## <a name="next-steps"></a>Passaggi successivi

Per ulteriori informazioni su come gestire i criteri e apportare modifiche dopo la creazione, vedere [Manage policies](privacy-management-policies-manage.md).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

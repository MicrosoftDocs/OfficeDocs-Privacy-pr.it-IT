---
title: Creare criteri in Gestione dei rischi per la privacy
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Informazioni su come creare e personalizzare criteri di privacy per la gestione dei dati personali dell'organizzazione in Microsoft 365.
ms.openlocfilehash: 2b655d778e73e2107c289988966fb491bf3ebb2e
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930507"
---
# <a name="create-policies-in-privacy-risk-management"></a>Creare criteri in Gestione dei rischi per la privacy

È possibile creare nuovi criteri in Gestione dei rischi per la privacy per affrontare gli scenari di rischio importanti per l'organizzazione. Per una guida introduttiva, usare i modelli predefiniti per creare nuovi criteri per la sovraesposizione dei dati, i trasferimenti di dati, la riduzione al minimo dei dati e gli scenari. È anche possibile personalizzare i propri criteri, usando uno di questi modelli come punto di partenza.

Durante la creazione o la modifica di criteri, è possibile configurare le notifiche tramite posta elettronica o, se disponibile, i suggerimenti per i criteri per Teams per portare le corrispondenze dei criteri all'attenzione degli utenti per la correzione.

## <a name="create-a-policy-from-a-template"></a>Creare un criterio da un modello

Seguire questa procedura per creare un criterio usando uno dei modelli predefiniti.

1. Nel [portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) passare alla sezione Priva Privacy Risk Management e selezionare **Criteri**.
1. Selezionare **Crea un criterio**.
1. Scegliere il tipo di modello desiderato. Verrà aperto un riquadro a comparsa con informazioni sul modello.
1. Per esaminare le impostazioni predefinite del modello, inclusi i tipi di dati, i percorsi dei dati e le condizioni corrispondenti ai criteri di attivazione, selezionare **Visualizza impostazioni**.
     - È possibile selezionare **Modifica impostazioni** per apportare modifiche. Verrà visualizzata la procedura guidata per la personalizzazione delle impostazioni.
1. Se si è pronti a usare le impostazioni predefinite, assegnare al criterio un nome descrittivo e selezionare **Crea criterio.**

Quando si crea un criterio direttamente da un modello, verranno scelte automaticamente molte impostazioni. Verrà inoltre avviata in modalità test per impostazione predefinita, il che significa che non verranno generati avvisi o notifiche. Se si è pronti per attivare completamente i criteri dopo l'esecuzione in modalità test e la revisione dei risultati dei criteri, è possibile trovarli nell'elenco dei criteri e modificare i criteri per attivarli.

## <a name="create-a-custom-policy"></a>Creare un criterio personalizzato

Per assumere un controllo granulare delle impostazioni di un criterio, è possibile creare un criterio personalizzato usando uno dei modelli esistenti come baseline. Priva offre una procedura guidata che illustra questi passaggi.

Tutti i tipi di criteri seguono questo flusso di base. Alcune impostazioni e opzioni cambieranno a seconda dei criteri scelti.

1. Nel [portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) passare alla sezione Priva Privacy Risk Management e selezionare **Criteri**.
1. Selezionare **Crea un criterio**.
1. Scegliere l'opzione **Personalizzata** per iniziare a usare la procedura guidata.
1. Scegliere il tipo di modello di base: **sovraesposizione dei dati,** **trasferimenti di dati** o **minimizzazione dei dati**. Ognuna di esse fornirà determinate opzioni durante la creazione dei criteri.
1. Denominare e descrivere i criteri. È consigliabile usare nomi descrittivi chiari per identificare i criteri, poiché questi nomi verranno visualizzati più avanti negli avvisi sulle corrispondenze dei criteri.
1. Procedere con la procedura guidata e scegliere le impostazioni desiderate. Le opzioni disponibili sono:
    - **Dati da monitorare**: selezionare il tipo di dati personali che i criteri monitoreranno.
    - **Utenti e gruppi**: applicare i criteri a tutti gli utenti o agli utenti selezionati.
    - **Località**: applicare i criteri alle aree selezionate in Microsoft 365.
    - **Condizioni**: impostare le condizioni per i criteri. Queste opzioni variano a seconda del tipo di criterio.
    - **Risultati**: definire i risultati quando viene trovata una corrispondenza di criteri, ad esempio le notifiche utente.
    - **Avvisi**: decidere la frequenza degli avvisi per gli amministratori quando viene trovata una corrispondenza dei criteri.
    - **Modalità**: scegliere se eseguire o meno i criteri prima in modalità test.
1. Al termine di tutte le impostazioni, esaminare le scelte, apportare le modifiche desiderate e quindi selezionare **Invia** per creare il criterio.

## <a name="learn-about-key-settings-for-all-policies"></a>Informazioni sulle impostazioni chiave per tutti i criteri

### <a name="choose-data-to-monitor"></a>Scegliere i dati da monitorare

Durante la modifica o la configurazione di qualsiasi tipo di criterio personalizzato, verrà richiesto di selezionare i tipi di dati che i criteri devono monitorare. Le opzioni sono le seguenti:

- **Gruppi di classificazione**: elenco ricercabile di set di dati in base alle principali normative sulla privacy, ad esempio GDPR o HIPAA. Visualizzare i dettagli di qualsiasi gruppo per vedere quali tipi di informazioni riservate vengono illustrati. Selezionare uno o più di questi set per usarli così come sono.
- **Singoli tipi di informazioni sensibili**: scegliendo manualmente tipi di informazioni sensibili specifici, ad esempio i numeri di previdenza sociale o le informazioni sulla patente di guida, è possibile personalizzare il proprio gruppo o gruppi di dati da cercare. Questa procedura guidata consente di selezionare dall'elenco completo dei tipi di informazioni sensibili in Gestione dei rischi per la privacy. Ogni tipo di informazioni ha le proprie proprietà. Usare il pulsante info accanto a uno di essi per informazioni dettagliate e note sulle impostazioni consigliate. Se si creano più gruppi, la procedura guidata consente di applicare operatori booleani per correlarli e definire l'ordine delle operazioni.

Se si seleziona tra i gruppi di classificazione esistenti, non è possibile selezionare i singoli tipi o creare gruppi personalizzati. Per la massima flessibilità, scegli i singoli tipi di informazioni sensibili. Per utilizzare gli standard più comuni, scegliere tra i gruppi di classificazione.

### <a name="set-user-email-notifications"></a>Impostare le notifiche di posta elettronica utente

Con [le notifiche tramite posta elettronica](risk-management-notifications.md), è possibile inviare notifiche sulle corrispondenze dei criteri direttamente ai proprietari del contenuto. Questi messaggi di posta elettronica riepilogano quali dati devono essere esaminati e le possibili azioni da intraprendere, ad esempio rendere privati i documenti, mantenerli in archivio, segnalare eventuali corrispondenze false positive e aggiungere note per riferimenti futuri. Questi messaggi di posta elettronica includono anche collegamenti per i destinatari del training su come gestire questi casi. La fornitura di questi collegamenti è necessaria e deve puntare alla propria documentazione interna sui processi e sulle procedure consigliate.

Le notifiche possono essere abilitate per i singoli criteri durante la creazione di criteri personalizzati o durante la modifica di qualsiasi criterio. Impostare le preferenze nella sezione **Risultati** .

Le impostazioni necessarie includono la frequenza delle notifiche e il collegamento alla formazione sulla privacy.

Le impostazioni facoltative includono alcuni campi personalizzabili per i messaggi di posta elettronica. Selezionare l'opzione **Anteprima e modifica messaggio di notifica** per aprire un riquadro a comparsa che mostra una notifica di esempio. Qui è possibile modificare la riga dell'oggetto del messaggio di posta elettronica, l'intestazione e il testo del corpo e il nome visualizzato e l'URL per il training sulla privacy.

Si noti che la funzionalità complessiva di Gestione dei rischi per la privacy di inviare notifiche tramite posta elettronica è controllata in **Impostazioni**. È disabilitato per impostazione predefinita. Se si disattiva questa impostazione, tutti i messaggi di posta elettronica verranno arrestati anche se le notifiche sono state configurate a livello di singolo criterio.

## <a name="learn-about-settings-for-data-minimization-policies"></a>Informazioni sulle impostazioni per i criteri di minimizzazione dei dati

I criteri di minimizzazione dei dati si concentrano sull'età del contenuto e sul tempo trascorso dall'ultima modifica. Il monitoraggio dei dati personali che vengono ancora conservati nei contenuti inutilizzati meno recenti consente di gestire meglio i dati archiviati e ridurre i rischi. Questa impostazione viene gestita nella schermata **Condizioni** .

Per impostazione predefinita, i criteri di riduzione dei dati cercano contenuti contenenti dati personali creati o modificati per l'ultima volta almeno 30 giorni fa. Quando si modifica o si crea un criterio personalizzato, è possibile selezionare tra altri intervalli di tempo preimpostati.

## <a name="learn-about-settings-for-data-transfer-policies"></a>Informazioni sulle impostazioni per i criteri di trasferimento dati

I criteri di trasferimento dei dati consentono di monitorare i trasferimenti di dati personali all'esterno dell'organizzazione, nonché i trasferimenti interni tra reparti, paesi o aree geografiche diversi. Nella schermata **Condizioni** è possibile scegliere i tipi di trasferimenti che devono essere cercati da Gestione dei rischi per la privacy.

Per impostazione predefinita, i criteri di trasferimento dei dati rilevano quando i dati personali all'interno dell'organizzazione vengono trasferiti o condivisi con un destinatario o una posizione all'esterno dell'organizzazione. Quando si modifica o si crea un criterio personalizzato, è possibile scegliere il tipo di trasferimento, quindi effettuare selezioni per le aree o i reparti del mittente e del destinatario.

I criteri di trasferimento dei dati supportano anche la fornitura di suggerimenti e raccomandazioni per i criteri agli utenti in Teams, in modo che possano rimanere informati sulle procedure consigliate per la gestione dei dati. Questa opzione può essere attivata o disattivata nella schermata **Risultati** .

## <a name="learn-about-settings-for-data-overexposure-policies"></a>Informazioni sulle impostazioni per i criteri di sovraesposizione dei dati

L'organizzazione può archiviare contenuti a vari livelli di accesso, incluse le aree accessibili pubblicamente e altre limitate. Nella schermata **Condizioni** è possibile scegliere di fare in modo che Gestione dei rischi per la privacy cerchi potenziali sovraesplosi dei dati per il contenuto archiviato in uno dei livelli di accesso seguenti:

- **Pubblico**: chiunque abbia un collegamento può visualizzare questo contenuto.
- **Esterno**: persone specifiche all'esterno dell'organizzazione hanno accesso.
- **Interno**: gli utenti dell'organizzazione hanno accesso.

Per impostazione predefinita, i criteri di sovraesposizione dei dati valutano tutti e tre i livelli di accesso. Quando si modifica o si crea un criterio personalizzato, è possibile scegliere tutti o uno di questi livelli.

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni su come gestire i criteri e apportare modifiche dopo che sono stati creati, vedere [Gestire i criteri](risk-management-policies-manage.md).

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

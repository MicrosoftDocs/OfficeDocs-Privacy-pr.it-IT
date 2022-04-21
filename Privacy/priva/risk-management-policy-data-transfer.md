---
title: Criteri di trasferimento dei dati in Gestione dei rischi per la privacy
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
description: Informazioni su come creare criteri di gestione dei dati in Microsoft Priva Privacy Risk Management per arginare i trasferimenti di dati personali all'interno o all'esterno dell'organizzazione.
ms.openlocfilehash: 6d491a7a65035aa1e3a405f36ef30b95f9c29245
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014485"
---
# <a name="data-transfer-policies-in-privacy-risk-management"></a>Criteri di trasferimento dei dati in Gestione dei rischi per la privacy

## <a name="whats-new"></a>Novità
I criteri di trasferimento dei dati possono ora rilevare quando gli elementi contenenti dati personali vengono trasferiti all'esterno dell'organizzazione. I trasferimenti esterni saranno lo scenario di trasferimento predefinito quando si crea un nuovo criterio di trasferimento dei dati usando [l'opzione di configurazione rapida](#quick-setup-use-a-template-with-default-settings). Ciò non influirà né modificherà le impostazioni per i criteri di trasferimento dei dati già creati.

## <a name="overview"></a>Panoramica

Il trasferimento dei dati personali presenta rischi, in particolare se trasferiti all'esterno dell'organizzazione o inviati tra determinati reparti o posizioni geografiche all'interno dell'organizzazione. Ad esempio, se i dati vengono inviati tramite messaggi di posta elettronica non crittografati o a destinatari non autorizzati, i dati potrebbero non essere più sicuri. Le attività di trasferimento dei dati come queste possono avere un impatto normativo o violare le procedure di privacy dell'organizzazione stabilite.

I criteri di trasferimento dei dati in Gestione dei rischi per la privacy consentono di monitorare i trasferimenti di dati personali all'esterno dell'organizzazione, nonché i trasferimenti interni tra reparti, paesi o aree geografiche diversi. Quando viene rilevata una corrispondenza dei criteri, è possibile inviare agli utenti notifiche tramite posta elettronica che consentono loro di intraprendere azioni correttive direttamente nel messaggio di posta elettronica, ad esempio rendere privati gli elementi di contenuto, notificare i proprietari del contenuto o contrassegnare gli elementi per un'ulteriore revisione.

Il processo di configurazione dei criteri semplifica l'impostazione delle condizioni dei criteri. Hai il controllo completo sulla tempistica degli avvisi e sulla frequenza dei messaggi di posta elettronica e suggerimenti in-the-moment in Microsoft Teams che portano l'attenzione degli utenti alle procedure di gestione dei dati sicure.

Esistono due modi per creare un criterio: da un **modello**, che è l'opzione rapida "predefinita" usando le impostazioni predefinite; o l'opzione **personalizzata** , che è un processo guidato per l'impostazione di condizioni, avvisi e notifiche.

## <a name="quick-setup-use-a-template-with-default-settings"></a>Configurazione rapida: usare un modello con le impostazioni predefinite

I criteri di trasferimento dei dati predefiniti rilevano quando i dati personali vengono inviati a destinatari esterni all'organizzazione. Ad esempio, viene visualizzato quando un utente dell'organizzazione invia un messaggio di posta elettronica Exchange a un destinatario esterno nei campi **A**, **Cc** o **Ccn**.

Seguire questa procedura per creare un criterio di trasferimento dati predefinito:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare **Crea un criterio** nell'angolo in alto a destra della schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Nella casella **Trasferimenti dati** selezionare **Crea**.

4. Un riquadro a comparsa contiene i dettagli dei criteri. Selezionando **Visualizza impostazioni** verranno visualizzate le [impostazioni predefinite](#default-data-transfer-policy-settings). È possibile modificare le impostazioni da qui, che consente di accedere al processo guidato descritto di seguito. Per continuare a creare i criteri usando le impostazioni predefinite, immettere semplicemente un nome descrittivo e quindi selezionare **Crea criterio**.

I criteri verranno creati e saranno elencati nella pagina **Criteri** . Inizia in [modalità test](risk-management-policies.md#testing-a-policy) in modo da poter monitorare le prestazioni prima di attivarlo.

#### <a name="default-data-transfer-policy-settings"></a>Impostazioni predefinite dei criteri di trasferimento dati

Un criterio di trasferimento dati creato dal modello rileverà:
- Quando i dati personali all'interno dell'organizzazione vengono trasferiti o condivisi con un destinatario o una posizione all'esterno dell'organizzazione.
- Quando i dati personali vengono condivisi esternamente da una di queste posizioni all'interno dell'organizzazione:
    - **Exchange**. Esempio: invio di un messaggio di posta elettronica contenente dati personali a un indirizzo di posta elettronica del destinatario esterno all'organizzazione.
    - **OneDrive** e **SharePoint**. Esempi: invio di un collegamento a un file o a un sito che contiene dati personali a un utente esterno all'organizzazione; copiare o spostare un file in un percorso OneDrive o SharePoint che si trova all'esterno dell'organizzazione.
    - **Teams**. Esempio: invio di un Teams messaggio di chat contenente dati personali a un destinatario esterno all'organizzazione.
- Tipi di dati basati sui gruppi di [classificazione](risk-management-policies.md#classification-groups) seguenti:
    - Regolamento generale sulla protezione dei dati (GDPR) dell'UE
    - Informazioni personali degli Stati Uniti
    - US Patriot Act
    - Legge sulla notifica di violazione dello stato degli Stati Uniti
    - US Gramm-Leach-Bliley Act (GLBA)
    - US Health Insurance Portability and Accountability Act (HIPAA)
    - Australia Health Records Act (HRIP)
    - Legge sulla privacy in Australia
    - Informazioni personali del Giappone
    - Protezione dei dati personali in Giappone

## <a name="custom-setup-guided-policy-creation-process"></a>Configurazione personalizzata: processo di creazione guidata dei criteri

L'opzione dei criteri personalizzati è un processo guidato per creare un nuovo criterio impostando condizioni, designando la gravità e la frequenza degli avvisi e attivando le notifiche di posta elettronica dell'utente.

Completare i passaggi seguenti per creare un nuovo criterio di trasferimento dei dati:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare il pulsante **Crea un criterio** in alto a destra nella schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Nella casella **Personalizzato** selezionare **Crea**.

4. Nella pagina **Nome e tipo** selezionare il modello di criterio **Trasferimenti di dati** . Immettere un nome di criterio che consente di identificarlo facilmente dall'elenco nella pagina **Criteri** e immettere una descrizione facoltativa, quindi selezionare **Avanti**.

5. Nella pagina **Dati da monitorare** scegliere il tipo di dati personali da monitorare. Esistono due opzioni:
    - **Gruppi di classificazione**: raggruppamenti di tipi di informazioni sensibili usati per rilevare contenuti correlati a dati personali o normative specifiche. Se si seleziona questa opzione, sarà necessario selezionare **+Aggiungi gruppi di classificazione** per scegliere uno o più gruppi dall'elenco fornito.
    - **Singoli tipi di informazioni sensibili**: selezionare questa opzione per scegliere da un elenco di singoli [tipi di informazioni riservate](/microsoft-365/compliance/sensitive-information-type-entity-definitions).

    Altre informazioni sulla [scelta dei dati da monitorare](risk-management-policies.md#choose-data-to-monitor). Al termine della selezione dei dati da monitorare, selezionare **Avanti**.

6. Nella pagina **Utenti e gruppi** scegliere a quali utenti dell'organizzazione verranno applicati i criteri. È possibile selezionare tutti i singoli utenti e tutti i gruppi di distribuzione Office 365 oppure selezionare utenti e gruppi specifici. Altre informazioni sulla [scelta di utenti e gruppi](risk-management-policies.md#choose-users-and-groups). Al termine, scegli **Avanti**.

7. Nella pagina **Percorsi** selezionare tutte le posizioni dei dati in Microsoft 365 che devono essere trattati dai criteri. Scegliere tra Exchange account di posta elettronica, account OneDrive, messaggi di chat e canali Teams e siti di SharePoint.

    All'interno di SharePoint è possibile designare tutti i siti o siti specifici. Se si seleziona **Siti SharePoint specifici**, è possibile immettere l'URL del sito nel campo URL. È anche possibile selezionare **+Scegli siti**, quindi nel riquadro a comparsa selezionare la casella a sinistra del nome del sito da selezionare.

    Altre informazioni sulla [scelta delle posizioni](risk-management-policies.md#choose-locations). Al termine della selezione delle posizioni, selezionare **Avanti**.

8. Nella pagina **Condizioni** selezionare il tipo di condizione di trasferimento dei dati che i criteri rileveranno:
    - **Trasferimenti all'esterno dell'organizzazione**: rileva i trasferimenti da utenti o gruppi all'interno dell'organizzazione a utenti esterni o guest all'esterno dell'organizzazione.
    - **Trasferimenti tra i reparti dell'organizzazione**: per questa opzione si selezioneranno un reparto mittente e un reparto destinatari. Scegliere i reparti dagli elenchi nei riquadri a comparsa visualizzati, quindi selezionare **Aggiungi**.
    - **Trasferimenti tra i confini o le aree** geografiche del paese: per questa opzione si selezioneranno un'area del mittente e un'area del destinatario. Scegliere i paesi o le aree designati dai riquadri a comparsa visualizzati, quindi selezionare **Aggiungi**.

9. Nella pagina **Risultati** decidere se inviare una notifica agli utenti quando corrispondono alle condizioni impostate dai criteri. È possibile scegliere una o entrambe le opzioni seguenti oppure scegliere nessuna delle due lasciando vuote le caselle di controllo:
    - **Suggerimenti inviati in Microsoft Teams**: i suggerimenti per la gestione dei dati verranno visualizzati nell'istanza di Teams di un utente quando hanno eseguito un'azione che corrisponde alle condizioni dei criteri. Sarà necessario aggiungere un URL per il training sulla privacy preferito, che verrà visualizzato anche nel suggerimento.
    - **Notifiche tramite posta elettronica**: gli utenti riceveranno una notifica tramite posta elettronica quando le azioni corrispondono alle condizioni dei criteri. I messaggi di posta elettronica contengono istruzioni per eseguire azioni correttive direttamente dal messaggio di posta elettronica, insieme a un collegamento alla formazione sulla privacy. Si designerà la frequenza dei messaggi di posta elettronica e l'URL per il training sulla privacy preferito.
     
    Altre informazioni sulla configurazione delle [notifiche utente](risk-management-notifications.md). Al termine della selezione dei risultati, selezionare **Avanti**.

10. Nella pagina **Avvisi** usare l'interruttore attiva/disattiva per attivare gli avvisi che un amministratore visualizzerà nella pagina **Avvisi** nella sezione **Criteri** di Gestione dei rischi per la privacy. Si designerà la frequenza di generazione degli avvisi, le soglie per le corrispondenze prima della generazione degli avvisi e la gravità degli avvisi. Altre informazioni [sull'impostazione degli avvisi per le corrispondenze dei criteri](risk-management-policies.md#set-alerts). Al termine, scegli **Avanti**.

11. Nella pagina **Modalità** decidere se eseguire o meno i criteri in modalità di test al momento della prima creazione, ovvero non verranno inviati avvisi o notifiche. Per mantenere i criteri in modalità di test, che è consigliabile, selezionare l'interruttore di attivazione/disattivazione nella posizione **Sì** . Altre informazioni sul [test di un criterio](risk-management-policies.md#testing-a-policy).

> [!NOTE]
> Se si attiva l'interruttore **Esegui in modalità test** sulla posizione **Disattivata** , *i criteri verranno attivati* al termine della creazione. Ciò significa che eventuali avvisi o notifiche utente configurati inizieranno a generare una volta rilevata una corrispondenza.

12. Nella pagina **Fine** esaminare le scelte. Selezionare **Modifica** sotto una delle sezioni per modificare le impostazioni. Quando si è soddisfatti delle impostazioni dei criteri, selezionare **Invia** per creare il criterio.

Dopo alcuni secondi, verrà visualizzata una conferma della creazione del criterio. Selezionare **Fine** nella pagina di conferma, che consente di passare alla pagina **Criteri** in cui verranno visualizzati i nuovi criteri nella parte superiore della tabella.

## <a name="next-steps"></a>Passaggi successivi

Per informazioni dettagliate su come modificare e gestire i criteri, visitare [Criteri di gestione dei rischi](risk-management-policies.md) per la privacy.

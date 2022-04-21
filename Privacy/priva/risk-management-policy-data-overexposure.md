---
title: Criteri di sovraesposizione dei dati in Gestione dei rischi per la privacy
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
description: Informazioni su come creare criteri di sovraesposizione dei dati in Microsoft Priva Privacy Risk Management per identificare e proteggere i dati personali che potrebbero essere eccessivamente accessibili.
ms.openlocfilehash: a0c87a84a78206862d9a79e1c16d17a90de5f040
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014506"
---
# <a name="data-overexposure-policies-in-privacy-risk-management"></a>Criteri di sovraesposizione dei dati in Gestione dei rischi per la privacy

L'organizzazione può archiviare contenuti a vari livelli di accesso, incluse le aree accessibili pubblicamente e altre limitate. I criteri di sovraesposizione dei dati consentono di rilevare e gestire le situazioni in cui i dati archiviati dall'organizzazione non sono sufficientemente sicuri. Ad esempio, se l'accesso a un sito interno è aperto a un numero eccessivo di persone o le impostazioni delle autorizzazioni non sono state mantenute, i dati personali archiviati in tale sito potrebbero essere vulnerabili a una violazione. I criteri di sovraesposizione dei dati possono valutare i dati per questi rischi e segnalare potenziali problemi.

Quando viene rilevata una corrispondenza dei criteri, è possibile inviare agli utenti notifiche tramite posta elettronica che includono opzioni di correzione per risolvere i problemi. Per la sovraesposizione dei dati, questi includono la creazione di elementi di contenuto privati, la notifica dei proprietari del contenuto o l'assegnazione di tag agli elementi per un'ulteriore revisione.

Il processo di configurazione dei criteri semplifica l'impostazione delle condizioni dei criteri. Hai il controllo completo sulla tempistica degli avvisi e sulla frequenza dei messaggi di posta elettronica che portano l'attenzione degli utenti alle procedure di gestione dei dati sicure.

Esistono due modi per creare un criterio: da un **modello**, che è l'opzione rapida "predefinita" usando le impostazioni predefinite; o l'opzione **personalizzata** , che è un processo guidato per l'impostazione di condizioni, avvisi e notifiche.

## <a name="quick-setup-use-a-template-with-default-settings"></a>Configurazione rapida: usare un modello con le impostazioni predefinite

I criteri di sovraesposizione dei dati predefiniti valutano i dati personali a tutti e tre i livelli di accesso: pubblico, esterno e interno.

Seguire questa procedura per creare un criterio di trasferimento dati predefinito:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare **Crea un criterio** nell'angolo in alto a destra della schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Nella casella **Sovraesposizione dati** selezionare **Crea**.

4. Un riquadro a comparsa contiene i dettagli dei criteri. Selezionando **Visualizza impostazioni** verranno visualizzate le impostazioni predefinite. È possibile modificare le impostazioni da qui, che consente di accedere al processo guidato descritto di seguito. Per continuare a creare i criteri usando le impostazioni predefinite, immettere semplicemente un nome descrittivo e quindi selezionare **Crea criterio**.

I criteri verranno creati e saranno elencati nella pagina **Criteri** . Inizia in [modalità test](risk-management-policies.md#testing-a-policy) in modo da poter monitorare le prestazioni prima di attivarlo.

#### <a name="default-data-overexposure-policy-settings"></a>Impostazioni predefinite dei criteri di sovraesposizione dei dati

Un criterio di sovraesposizione dei dati creato dal modello rileverà:

- Quando un utente fornisce un accesso troppo ampio agli elementi contenenti dati personali archiviati nella OneDrive o nella SharePoint dell'organizzazione. Ad esempio, i criteri rileveranno la condivisione dei dati personali nei modi seguenti:
    - Tramite un collegamento a cui chiunque nel pubblico può accedere
    - Tramite un collegamento o a causa di autorizzazioni che consentono a tutti gli utenti dell'organizzazione di accedere
    - Concessione dei diritti di accesso a utenti esterni o guest a file OneDrive o SharePoint
- Tipi di dati basati sui [gruppi di classificazione](risk-management-policies.md#classification-groups) seguenti:
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

Completare i passaggi seguenti per creare un nuovo criterio di sovraesposizione dei dati:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare il pulsante **Crea un criterio** in alto a destra nella schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Nella casella **Personalizzato** selezionare **Crea**.

4. Nella pagina **Nome e tipo** selezionare il modello di criteri **di sovraesposizione dei dati** . Immettere un nome di criterio che consente di identificarlo facilmente dall'elenco nella pagina **Criteri** e immettere una descrizione facoltativa, quindi selezionare **Avanti**.

5. Nella pagina **Dati da monitorare** scegliere il tipo di dati personali da monitorare. Esistono due opzioni:
    - **Gruppi di classificazione**: raggruppamenti di tipi di informazioni sensibili usati per rilevare contenuti correlati a dati personali o normative specifiche. Se si seleziona questa opzione, sarà necessario selezionare **+Aggiungi gruppi di classificazione** per scegliere uno o più gruppi dall'elenco fornito.
    - **Singoli tipi di informazioni sensibili**: selezionare questa opzione per scegliere da un elenco di singoli [tipi di informazioni riservate](/microsoft-365/compliance/sensitive-information-type-entity-definitions).

    Altre informazioni sulla [scelta dei dati da monitorare](risk-management-policies.md#choose-data-to-monitor). Al termine della selezione dei dati da monitorare, selezionare **Avanti**.

6. Nella pagina **Utenti e gruppi** scegliere a quali utenti dell'organizzazione verranno applicati i criteri. È possibile selezionare tutti i singoli utenti e tutti i gruppi di distribuzione Office 365 oppure selezionare utenti e gruppi specifici. Altre informazioni sulla [scelta di utenti e gruppi](risk-management-policies.md#choose-users-and-groups). Al termine, scegli **Avanti**.

7. Nella pagina **Percorsi** selezionare tutte le posizioni dei dati in Microsoft 365 che devono essere trattati dai criteri. Scegliere tra account OneDrive e siti SharePoint.

    All'interno di SharePoint è possibile designare tutti i siti o siti specifici. Se si seleziona **Siti SharePoint specifici**, è possibile immettere l'URL del sito nel campo URL. È anche possibile selezionare **+Scegli siti**, quindi nel riquadro a comparsa selezionare la casella a sinistra del nome del sito da selezionare.

    Altre informazioni sulla [scelta delle posizioni](risk-management-policies.md#choose-locations). Al termine della selezione delle posizioni, selezionare **Avanti**.

8. Nella pagina **Condizioni** selezionare il tipo di condizione di sovraesposizione dei dati che il criterio rileverà:
    - **Pubblico**: chiunque abbia un collegamento può accedere al contenuto.
    - **Esterno**: persone specifiche all'esterno dell'organizzazione hanno accesso.
    - **Interno**: tutti gli utenti dell'organizzazione hanno accesso.
    
    La selezione di più livelli di accesso amplierà l'ambito dei dati e potrebbe generare quantità notevolmente maggiori di avvisi e notifiche utente.

    Inserire un segno di spunta nella casella accanto alle scelte, quindi selezionare **Avanti**.

9. Nella pagina **Risultati** decidere se inviare una notifica agli utenti quando corrispondono alle condizioni impostate dai criteri. Se si seleziona la casella notifiche tramite posta elettronica, gli utenti riceveranno una notifica tramite posta elettronica quando le azioni corrispondono alle condizioni dei criteri. I messaggi di posta elettronica contengono istruzioni per eseguire azioni correttive direttamente dal messaggio di posta elettronica, insieme a un collegamento alla formazione sulla privacy. Si designerà la frequenza dei messaggi di posta elettronica e l'URL per il training sulla privacy preferito.
     
    Altre informazioni sulla configurazione delle [notifiche utente](risk-management-notifications.md). Al termine della selezione dei risultati, selezionare **Avanti**.

10. Nella pagina **Avvisi** usare l'interruttore attiva/disattiva per attivare gli avvisi che un amministratore visualizzerà nella pagina **Avvisi** nella sezione **Criteri** di Gestione dei rischi per la privacy. Si designerà la frequenza di generazione degli avvisi, le soglie per le corrispondenze prima della generazione degli avvisi e la gravità degli avvisi. Altre informazioni [sull'impostazione degli avvisi per le corrispondenze dei criteri](risk-management-policies.md#set-alerts). Al termine, scegli **Avanti**.

11. Nella pagina **Modalità** decidere se eseguire o meno i criteri in modalità di test al momento della prima creazione, ovvero non verranno inviati avvisi o notifiche. Per mantenere i criteri in modalità di test, che è consigliabile, selezionare l'interruttore di attivazione/disattivazione nella posizione **Sì** . Altre informazioni sul [test di un criterio](risk-management-policies.md#testing-a-policy).

> [!NOTE]
> Se si attiva l'interruttore **Esegui in modalità test** sulla posizione **Disattivata** , *i criteri verranno attivati* al termine della creazione. Ciò significa che eventuali avvisi o notifiche utente configurati inizieranno a generare una volta rilevata una corrispondenza.

12. Nella pagina **Fine** esaminare le scelte. Selezionare **Modifica** sotto una delle sezioni per modificare le impostazioni. Quando si è soddisfatti delle impostazioni dei criteri, selezionare **Invia** per creare il criterio.

Dopo alcuni secondi, verrà visualizzata una conferma della creazione del criterio. Selezionare **Fine** nella pagina di conferma, che consente di passare alla pagina **Criteri** in cui verranno visualizzati i nuovi criteri nella parte superiore della tabella.

## <a name="next-steps"></a>Passaggi successivi

Per informazioni dettagliate su come modificare e gestire i criteri, visitare [Criteri di gestione dei rischi](risk-management-policies.md) per la privacy.
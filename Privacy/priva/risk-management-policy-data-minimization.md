---
title: Criteri di riduzione dei dati in Gestione dei rischi per la privacy
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
description: Informazioni su come creare criteri di minimizzazione dei dati in Microsoft Priva Privacy Risk Management per ridurre la quantità di dati personali inutilizzati nell'organizzazione.
ms.openlocfilehash: c5a883de696923e4453ed28739e9bf68b618f8d1
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014477"
---
# <a name="data-minimization-policies-in-privacy-risk-management"></a>Criteri di riduzione dei dati in Gestione dei rischi per la privacy

I criteri di minimizzazione dei dati si concentrano sull'età del contenuto e sul tempo trascorso dall'ultima modifica. Il monitoraggio dei dati personali che vengono ancora conservati nei contenuti inutilizzati meno recenti consente di gestire meglio i dati archiviati e ridurre i rischi.

Gestione dei rischi per la privacy consente di creare criteri per monitorare i dati che non sono stati modificati entro un intervallo di tempo selezionato. Quando viene rilevata una corrispondenza dei criteri, è possibile inviare agli utenti notifiche tramite posta elettronica con opzioni di correzione, tra cui contrassegnare gli elementi per l'eliminazione, notificare i proprietari del contenuto o contrassegnare gli elementi per un'ulteriore revisione.

Il processo di configurazione dei criteri semplifica l'impostazione delle condizioni dei criteri. Hai il controllo completo sulla tempistica degli avvisi e sulla frequenza dei messaggi di posta elettronica che portano l'attenzione degli utenti alle procedure di gestione dei dati sicure.

Esistono due modi per creare un criterio: da un **modello**, che è l'opzione rapida "predefinita" usando le impostazioni predefinite; o l'opzione **personalizzata** , che è un processo guidato per l'impostazione di condizioni, avvisi e notifiche.

## <a name="quick-setup-use-a-template-with-default-settings"></a>Configurazione rapida: usare un modello con le impostazioni predefinite

Il criterio di minimizzazione dei dati predefinito rileva il contenuto contenente dati personali creati o modificati almeno 30 giorni fa.

Seguire questa procedura per creare un criterio di trasferimento dati predefinito:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare **Crea un criterio** nell'angolo in alto a destra della schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Nella casella **Minimizzazione dati** selezionare **Crea**.

4. Un riquadro a comparsa contiene i dettagli dei criteri. Selezionando **Visualizza impostazioni** verranno visualizzate le impostazioni predefinite. È possibile modificare le impostazioni da qui, che consente di accedere al processo guidato descritto di seguito. Per continuare a creare i criteri usando le impostazioni predefinite, immettere semplicemente un nome descrittivo e quindi selezionare **Crea criterio**.

I criteri verranno creati e saranno elencati nella pagina **Criteri** . Inizia in [modalità test](risk-management-policies.md#testing-a-policy) in modo da poter monitorare le prestazioni prima di attivarlo.

#### <a name="default-data-minimization-policy-settings"></a>Impostazioni predefinite dei criteri di minimizzazione dei dati

Un criterio di minimizzazione dei dati creato dal modello rileverà:
- Elementi di contenuto contenenti dati personali che non sono stati modificati almeno negli ultimi 30 giorni.
- Dati archiviati in una di queste posizioni all'interno dell'organizzazione: Exchange, OneDrive, SharePoint, Teams.
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

Completare i passaggi seguenti per creare un nuovo criterio di trasferimento dei dati:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare il pulsante **Crea un criterio** in alto a destra nella schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Nella casella **Personalizzato** selezionare **Crea**.

4. Nella pagina **Nome e tipo** selezionare il modello di **criteri di minimizzazione dei dati** . Immettere un nome di criterio che consente di identificarlo facilmente dall'elenco nella pagina **Criteri** e immettere una descrizione facoltativa, quindi selezionare **Avanti**.

5. Nella pagina **Dati da monitorare** scegliere il tipo di dati personali da monitorare. Esistono due opzioni:
    - **Gruppi di classificazione**: raggruppamenti di tipi di informazioni sensibili usati per rilevare contenuti correlati a dati personali o normative specifiche. Se si seleziona questa opzione, sarà necessario selezionare **+Aggiungi gruppi di classificazione** per scegliere uno o più gruppi dall'elenco fornito.
    - **Singoli tipi di informazioni sensibili**: selezionare questa opzione per scegliere da un elenco di singoli [tipi di informazioni riservate](/microsoft-365/compliance/sensitive-information-type-entity-definitions).

    Altre informazioni sulla [scelta dei dati da monitorare](risk-management-policies.md#choose-data-to-monitor). Al termine della selezione dei dati da monitorare, selezionare **Avanti**.

6. Nella pagina **Utenti e gruppi** scegliere a quali utenti dell'organizzazione verranno applicati i criteri. È possibile selezionare tutti i singoli utenti e tutti i gruppi di distribuzione Office 365 oppure selezionare utenti e gruppi specifici. Altre informazioni sulla [scelta di utenti e gruppi](risk-management-policies.md#choose-users-and-groups). Al termine, scegli **Avanti**.

7. Nella pagina **Percorsi** selezionare tutte le posizioni dei dati in Microsoft 365 che devono essere trattati dai criteri. Scegliere tra Exchange account di posta elettronica, account OneDrive, messaggi di chat e canali Teams e siti di SharePoint.

    All'interno di SharePoint è possibile designare tutti i siti o siti specifici. Se si seleziona **Siti SharePoint specifici**, è possibile immettere l'URL del sito nel campo URL. È anche possibile selezionare **+Scegli siti**, quindi nel riquadro a comparsa selezionare la casella a sinistra del nome del sito da selezionare.

    Altre informazioni sulla [scelta delle posizioni](risk-management-policies.md#choose-locations). Al termine della selezione delle posizioni, selezionare **Avanti**.

8. Nella pagina **Condizioni** usare il menu a discesa per scegliere quanti giorni dopo l'ultima modifica di un elemento che il criterio rileverà:
    - 30 giorni
    - 60 giorni
    - 90 giorni
    - 120 giorni
    
     Al termine, scegli **Avanti**.

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
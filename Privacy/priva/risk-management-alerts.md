---
title: Analizzare e correggere gli avvisi in Gestione dei rischi per la privacy
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
description: Informazioni su come gestire gli avvisi e i problemi generati dalle corrispondenze dei criteri nella gestione dei rischi per la privacy.
ms.openlocfilehash: 26b30082d4f7122e113d38e8357af26b3850fda2
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248963"
---
# <a name="investigate-and-remediate-alerts-in-privacy-risk-management"></a>Analizzare e correggere gli avvisi in Gestione dei rischi per la privacy

Microsoft Priva può contribuire a fornire visibilità su importanti scoperte dalla sovraesposizione dei dati, dalla minimizzazione dei dati o dai criteri di trasferimento dei dati. All'interno della soluzione Di gestione dei rischi per la privacy, gli amministratori **possono esaminare gli** avvisi relativi al contenuto che soddisfano le condizioni dei criteri. La revisione degli avvisi consente di identificare i casi che necessitano di follow-up. A tale scopo, è possibile creare **problemi**. I problemi offrono agli utenti un modo strutturato per esaminare il contenuto, assegnare la gravità del problema e lavorare in modo collaborativo per risolvere i problemi.

Se i criteri sono stati impostati per inviare notifiche agli utenti, i proprietari del contenuto possono anche eseguire determinate azioni correttive direttamente da questi messaggi di posta elettronica o da Teams. Per ulteriori informazioni, vedere [Send user notifications in Privacy Risk Management](risk-management-notifications.md).

## <a name="view-current-alerts-and-issues"></a>Visualizzare gli avvisi e i problemi correnti

La pagina **Panoramica** di Priva fornisce una panoramica dei risultati recenti con aggiornamenti sulle aree di interesse chiave, ad esempio i criteri con il maggior numero di corrispondenze e gli avvisi dei criteri attualmente attivi. Per ulteriori informazioni sulle informazioni fornite da questa visualizzazione, vedere [Trovare e visualizzare i dati personali in Priva](priva-data-profile.md).

È inoltre possibile accedere alle visualizzazioni e ai dettagli relativi agli avvisi e ai problemi tramite la pagina **criteri** principale. Seleziona **Visualizza avvisi e** **Visualizza problemi** per visualizzare i dettagli.

## <a name="manage-alerts"></a>Gestire gli avvisi

Per valutare gli avvisi attivi e specificare quali richiedono il follow-up, accedere alla **pagina Avvisi** . Fornisce un elenco filtrabile di avvisi generati dai criteri. Puoi esaminarli singolarmente per determinare le circostanze in cui sono stati attivati.

Se si seleziona un avviso, verrà aperto un riquadro a comparsa con ulteriori dettagli, ad esempio il numero di elementi corrispondenti e la gravità secondo le impostazioni dei criteri. Nella scheda **Contenuto** è possibile esaminare i file coinvolti in questo avviso. Queste informazioni possono fornire ulteriori informazioni sull'evento specifico che ha attivato l'avviso, sulla posizione dei file e sui tipi di dati personali coinvolti. I trigger per gli avvisi sono determinati dalle condizioni specifiche di ogni criterio. Ad esempio, un avviso potrebbe essere attivato su un criterio di trasferimento dei dati se Priva rileva un trasferimento tra i reparti o le aree geografiche specificati del criterio.

Dopo aver valutato qualsiasi avviso nell'elenco, è possibile selezionare **Crea** problema per richiedere ulteriori indagini e azioni da parte degli utenti. Verrà richiesto di assegnare un nome al problema e di aggiungere eventuali commenti rilevanti per il contesto. Puoi anche ignorare gli avvisi qui se non richiedono un follow-up.

## <a name="manage-issues"></a>Gestire i problemi

I problemi vengono creati dagli amministratori durante la valutazione degli avvisi sulle corrispondenze dei criteri. Per seguire e risolvere i problemi indicati, gli utenti possono visitare la **pagina Problemi** . Da qui è possibile esaminare i singoli problemi, analizzare le condizioni di istigazione, esaminare i dati ed eseguire i passaggi necessari per chiudere il caso.

Questa pagina fornisce un elenco di tutti i problemi aperti. Sono elencati per nome e ordinati in base alla gravità per aiutarti a definire la priorità dei casi, incluse le categorie alta, media e bassa, insieme a quelle non assegnate. Selezionare qualsiasi problema nell'elenco per esaminarne il contenuto ed eseguire un'azione per risolverlo. Puoi assegnare un livello di gravità ai problemi non assegnati durante la revisione.

### <a name="review-issue-details"></a>Esaminare i dettagli del problema

Le pagine dei dettagli del problema guidano l'utente nel processo di gestione dei rischi per la privacy identificati e della gestione dei file indicati.

Le schede nelle pagine dei dettagli del problema forniscono informazioni sugli avvisi e sul contenuto associati, tra cui:

- **Panoramica**: mostra le informazioni essenziali sul problema. Vedi lo stato corrente del problema e le azioni consigliate seguenti da eseguire. Puoi anche visualizzare una panoramica del contenuto, dei criteri associati, dei dettagli dell'avviso e della sequenza temporale. La sequenza temporale mostrerà la posizione in cui stai recuperando il contenuto. Il contenuto scaricato verrà conservato temporaneamente per la revisione.
- **Avvisi**: elenco dettagliato degli avvisi associati al problema.
- **Content**: elenco filtrabile di elementi di contenuto associati. Selezionare un elemento per visualizzare i dettagli, incluse le attività che si sono verificate e la cronologia delle correzioni, se qualcuno ha già effettuato azioni in Priva per gestire i dati. È inoltre possibile scegliere di eseguire nuove azioni di correzione.
- **Note**: selezionare questa opzione per aggiungere o visualizzare le note relative al problema per il team.
- **Collaboratori**: consente di visualizzare e gestire l'elenco dei collaboratori che possono contribuire alla risoluzione del problema.

### <a name="share-the-issue"></a>Condividere il problema

L'aggiunta di persone come collaboratori consente di condividere il problema con altri membri dell'organizzazione tramite un canale Microsoft Teams sicuro, un messaggio di posta elettronica aziendale o condividendo un collegamento direttamente alla pagina del problema in Priva. Queste opzioni sono disponibili nel **pulsante** Condividi. Quando si condivide tramite Teams, verrà richiesto di selezionare tra i team disponibili nell'organizzazione, selezionare il canale specifico e lasciare un messaggio sul problema, che verrà condiviso con il canale specificato.

## <a name="review-content-and-remediate-issues"></a>Esaminare il contenuto e risolvere i problemi

Per esaminare il contenuto associato a un problema, scegliere **l'azione** Rivedi contenuto se richiesto o aprire la **scheda** Contenuto. Selezionare un file nell'elenco per visualizzarlo per intero. Qui è possibile visualizzare i dettagli relativi al file, alle attività nel record e alla cronologia delle correzioni, se sono stati evasi passaggi precedenti per gestire il file.

Usa il **pulsante Correzione** per prendere decisioni di gestione dei dati per questo contenuto in Priva. La selezione del pulsante consente di scegliere tra una o più azioni di correzione. Le opzioni disponibili sono:

**Tutti i criteri**

- **Notifica al proprietario**: notifica al proprietario del contenuto il problema rilevato.
- **Applica etichetta di conservazione**: aggiungere un'etichetta sulla conservazione dei dati per questo elemento. [Ulteriori informazioni sulle etichette di conservazione](/microsoft-365/compliance/create-apply-retention-labels).
- **Applica etichetta di riservatezza**: aggiungi un'etichetta sulla riservatezza dei dati di questo elemento. [Altre informazioni sulle etichette di riservatezza](/microsoft-365/compliance/sensitivity-labels).
- **Contrassegna come non corrispondente**: identificare un risultato di ricerca come falso positivo per rimuovere l'elemento di contenuto dalla considerazione.

**Riduzione dei dati**

- **Elimina**: utilizzare questa opzione per un'eliminazione recidiva dei dati. Il contenuto viene spostato nella cartella degli elementi eliminati o nel Cestino (Exchange, SharePoint, OneDrive) o eliminato con un'opzione per il ripristino (Teams messaggi). L'eliminazione può essere annullata entro un determinato periodo di tempo, a seconda delle impostazioni del servizio.

**Sovraesposizione dei dati e trasferimento dei dati**

- **Rendi privato**: rimuovi l'accesso aperto per questo elemento di contenuto.

Ogni opzione ti chiederà di lasciare commenti e altre informazioni di supporto necessarie per il proprietario del contenuto prima di confermare la scelta.

Dopo aver intrapreso tutti i passaggi di correzione (incluse le azioni che ritieni consigliabili oltre alle opzioni disponibili in Priva) e il problema è pronto per la chiusura, usa il pulsante  Risolvi e aggiungi i commenti finali prima di inviarlo.

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

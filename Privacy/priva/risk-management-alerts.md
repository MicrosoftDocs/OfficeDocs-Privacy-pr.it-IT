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
description: Informazioni su come gestire avvisi e problemi generati dalle corrispondenze dei criteri in Microsoft Priva Privacy Risk Management.
ms.openlocfilehash: cc24342bc86bf327892b34ed26650070a7addbf0
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014386"
---
# <a name="investigate-and-remediate-alerts-in-privacy-risk-management"></a>Analizzare e correggere gli avvisi in Gestione dei rischi per la privacy

Microsoft Priva consente di fornire visibilità sulle individuazioni importanti derivanti dalla sovraesposizione dei dati, dalla riduzione al minimo dei dati o dai criteri di trasferimento dei dati. All'interno della soluzione Gestione dei rischi per la privacy, gli amministratori possono esaminare **gli avvisi** relativi al contenuto corrispondente alle condizioni dei criteri. La revisione degli avvisi consente di identificare i casi che richiedono un follow-up. A tale scopo, è possibile creare **problemi**. I problemi offrono agli utenti un modo strutturato per esaminare il contenuto, assegnare la gravità del problema e collaborare per risolvere i problemi.

Se i criteri sono stati configurati per inviare notifiche agli utenti, i proprietari dei contenuti possono anche intraprendere determinate azioni correttive direttamente da questi messaggi di posta elettronica o da Teams. Per altre informazioni, vedere [Inviare notifiche utente in Gestione dei rischi per la privacy](risk-management-notifications.md).

## <a name="view-current-alerts-and-issues"></a>Visualizzare gli avvisi e i problemi correnti

**La pagina Panoramica** di Priva offre una visualizzazione dei risultati recenti con aggiornamenti sulle aree principali di interesse, ad esempio i criteri con il maggior numero di corrispondenze e gli avvisi dei criteri attualmente attivi. Per altre informazioni sulle informazioni fornite da questa visualizzazione, vedere [Trovare e visualizzare i dati personali in Priva](priva-data-profile.md).

È anche possibile accedere alle visualizzazioni e ai dettagli relativi agli avvisi e ai problemi tramite la pagina **Criteri** principale. Selezionare **Visualizza avvisi** e **Visualizza problemi** per visualizzare i dettagli.

## <a name="manage-alerts"></a>Gestire gli avvisi

Per valutare gli avvisi attivi e specificare quali richiedono il completamento, accedere alla pagina **Avvisi** . Fornisce un elenco filtrabile degli avvisi generati dai criteri. È possibile esaminarli singolarmente per determinare le circostanze in cui sono stati attivati.

Se si seleziona un avviso, verrà aperto un riquadro di riquadro a comparsa con dettagli aggiuntivi, ad esempio il numero di elementi corrispondenti e la gravità in base alle impostazioni dei criteri. Nella scheda **Contenuto** è possibile esaminare i file coinvolti in questo avviso. Queste informazioni possono fornire informazioni dettagliate aggiuntive sull'evento specifico che ha attivato l'avviso, la posizione dei file e i tipi di dati personali coinvolti. I trigger per gli avvisi sono determinati dalle condizioni specifiche di ogni criterio. Ad esempio, un avviso potrebbe essere attivato su un criterio di trasferimento dei dati se Priva rileva un trasferimento tra i reparti o le aree specificati del criterio.

Dopo aver valutato qualsiasi avviso nell'elenco, è possibile selezionare **Crea problema** per richiedere ulteriori indagini e azioni da parte degli utenti. Verrà richiesto di denominare il problema e aggiungere eventuali commenti pertinenti per il contesto. È anche possibile ignorare gli avvisi qui se non richiedono un follow-up.

## <a name="manage-issues"></a>Gestire i problemi

I problemi vengono creati dagli amministratori durante la valutazione degli avvisi sulle corrispondenze dei criteri. Per completare e risolvere i problemi indicati, gli utenti possono visitare la pagina **Problemi** . Da qui è possibile esaminare i singoli problemi, analizzare le condizioni di istigazione, esaminare i dati e seguire i passaggi necessari per chiudere il caso.

Questa pagina fornisce un elenco di tutti i problemi aperti. Sono elencati per nome e ordinati in base alla gravità per facilitare la definizione della priorità dei casi, incluse le categorie alta, media e bassa, insieme a non assegnati. Selezionare qualsiasi problema nell'elenco per esaminarne il contenuto e intervenire per risolverlo. È possibile assegnare ai problemi non assegnati una classificazione di gravità durante la revisione.

### <a name="review-issue-details"></a>Esaminare i dettagli del problema

Le pagine dei dettagli del problema consentono di affrontare i rischi per la privacy identificati e di gestire i file indicati.

Le schede nelle pagine dei dettagli del problema forniscono informazioni sugli avvisi e sul contenuto associati, tra cui:

- **Panoramica**: mostra informazioni essenziali sul problema. Vedere lo stato corrente del problema e le azioni consigliate successive da eseguire. È anche possibile visualizzare una panoramica del contenuto, dei criteri associati, dei dettagli sull'avviso e della sequenza temporale. La sequenza temporale mostrerà dove si sta recuperando il contenuto. Il contenuto scaricato verrà conservato temporaneamente per la revisione.
- **Avvisi**: elenco dettagliato degli avvisi associati al problema.
- **Contenuto**: elenco filtrabile di elementi di contenuto associati. Selezionare qualsiasi elemento per visualizzarne i dettagli, incluse le attività che si sono verificate e la relativa cronologia di correzione, se qualcuno ha già intrapreso azioni in Priva per gestire i dati. È anche possibile scegliere di eseguire nuove azioni correttive.
- **Note**: selezionare per aggiungere o visualizzare eventuali note per il team sul problema.
- **Collaboratori**: consente di visualizzare e gestire l'elenco di collaboratori che possono contribuire alla risoluzione del problema.

### <a name="share-the-issue"></a>Condividere il problema

L'aggiunta di persone come collaboratori consente di condividere il problema con altri membri dell'organizzazione tramite un canale di Microsoft Teams sicuro, un messaggio di posta elettronica aziendale o condividendo un collegamento direttamente alla pagina del problema in Priva. Queste opzioni sono disponibili sotto il pulsante **Condividi** . Quando si condivide tramite Teams, verrà chiesto di selezionare i team disponibili nell'organizzazione, selezionare il canale specifico e lasciare un messaggio sul problema, che verrà condiviso con il canale specificato.

## <a name="review-content-and-remediate-issues"></a>Esaminare il contenuto e correggere i problemi

Per esaminare il contenuto associato a un problema, scegliere l'azione **Rivedi contenuto** se richiesto o aprire la scheda **Contenuto** . Selezionare qualsiasi file nell'elenco per visualizzarlo per intero. Qui è possibile visualizzare i dettagli sul file, le eventuali attività nel record e la relativa cronologia di correzione, se sono stati eseguiti i passaggi precedenti per gestire questo file. Selezionare **Correzione** per eseguire una o più delle azioni elencate di seguito.

- **Notifica al proprietario**: notificare al proprietario del contenuto il problema rilevato.

- **Applica etichetta di conservazione**: aggiungere un'etichetta sulla conservazione dei dati per questo elemento. [Altre informazioni sulle etichette di conservazione](/microsoft-365/compliance/create-apply-retention-labels).

- **Applica etichetta di riservatezza**: aggiungere un'etichetta sulla riservatezza dei dati di questo elemento. [Altre informazioni sulle etichette di riservatezza](/microsoft-365/compliance/sensitivity-labels).

- **Contrassegna come non corrispondente**: identificare un risultato di ricerca come falso positivo per rimuovere l'elemento di contenuto dalla considerazione.

- **Elimina** (solo per i criteri di minimizzazione dei dati): usare questa opzione per un'eliminazione temporanea dei dati. L'elemento viene spostato nella cartella degli elementi eliminati o nel contenitore di riciclo (Exchange, SharePoint, OneDrive) o eliminato con un'opzione per il ripristino (Teams messaggi). L'eliminazione può essere annullata entro un determinato periodo di tempo, a seconda delle impostazioni del servizio.

- **Rendi privato** (solo per i criteri di sovraesposizione e trasferimento dei dati): rimuovere l'accesso aperto per questo elemento di contenuto.

Ogni opzione richiederà di lasciare commenti e tutte le altre informazioni di supporto necessarie per il proprietario del contenuto prima di confermare la scelta.

Dopo aver eseguito tutti i passaggi di correzione (incluse le azioni che si ritiene consigliabile oltre alle opzioni disponibili in Priva) e il problema è pronto per la chiusura, usare il pulsante **Risolvi** e aggiungere i commenti finali prima di inviarlo.

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

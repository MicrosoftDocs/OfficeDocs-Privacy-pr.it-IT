---
title: Esaminare i dati per una richiesta di diritti dell'oggetto
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
description: Informazioni su come esaminare i dati delle richieste di diritti dell'oggetto raccolti da Microsoft Priva e collaborare al completamento della richiesta.
ms.openlocfilehash: 0e1e3e4573730a0cc799f0fa30812eb45d74528b
ms.sourcegitcommit: 875a7df5c2562eac6395e71c5bf83ba1d0a067d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2022
ms.locfileid: "62768430"
---
# <a name="review-data-for-a-subject-rights-request"></a>Esaminare i dati per una richiesta di diritti dell'oggetto

Dopo aver creato una richiesta di diritti dell'oggetto [(ulteriori](subject-rights-requests-create.md) informazioni) in Microsoft Priva, la soluzione Subject Rights Requests utilizzerà gli input per cercare corrispondenze sull'oggetto dati nell'ambiente di Microsoft 365 dell'organizzazione. Dopo aver compilato questi dati, è possibile esaminare i risultati, effettuare scelte sugli elementi da includere e redigere le informazioni in base alle esigenze. Questi passaggi possono essere collaborati da più utenti tramite l'interfaccia Priva.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Passaggio 1: esaminare i dettagli della richiesta e monitorare lo stato

Per visualizzare i risultati iniziali della ricerca, passare all'area Priva del [Centro conformità Microsoft 365 e aprire](https://compliance.microsoft.com/) **Richieste di diritti dell'oggetto**. In questa pagina principale è disponibile un elenco di tutte le richieste di diritti dell'oggetto aperte.

Seleziona la richiesta nell'elenco per visualizzare i dettagli della richiesta. Qui puoi trovare altre informazioni sulle proprietà della richiesta, sui risultati della ricerca e sullo stato della richiesta. Questa pagina diventerà il tuo hub per lavorare e collaborare alla gestione dei file trovati, alla creazione di report ed esportazioni e al completamento della richiesta.

I riquadri nella pagina dei dettagli della richiesta includono:

- **Dettagli**: dettagli essenziali sulla richiesta, inclusa la data di scadenza e la data della richiesta, la descrizione e la normativa sulla privacy correlata.
- **Progress**: sequenza temporale che indica i passaggi completati e tutte le attività ancora da completare.
- Statistiche sulla fase di avanzamento corrente. Questo riquadro può mostrare informazioni come un riepilogo della stima dei dati, il numero di elementi trovati nella ricerca e le relative posizioni in Microsoft 365 o lo stato delle esportazioni.
- **Elementi con priorità da esaminare**: questo riquadro mostrerà informazioni sugli elementi importanti rilevati automaticamente da Priva. Ad esempio, questo potrebbe includere informazioni riservate che già recano un'etichetta di riservatezza Microsoft o elementi con dati su più utenti che potrebbero richiedere una redazione. Ciò consente agli amministratori di sapere da dove iniziare la revisione. Gli elementi di priorità sono disponibili in Dati raccolti filtrando in base alla colonna "Tipi di priorità".

### <a name="understand-progress-stages"></a>Comprendere le fasi di avanzamento

Le richieste di diritti dell'oggetto vengono sottoposte a più fasi. Alcuni avanzano automaticamente mentre Priva esegue la valutazione dei dati e altri avanzano quando gli amministratori e i collaboratori richiedono diritti dell'oggetto completano passaggi essenziali come la revisione, la selezione e la redazione dei file.

Poiché potrebbe essere necessario lavorare sulle richieste nel tempo o da più collaboratori, Priva fornisce aggiornamenti continui sullo stato e indicazioni sui passaggi successivi da eseguire. Questi aggiornamenti possono essere visualizzati nella pagina panoramica della richiesta di diritti dell'oggetto.

#### <a name="data-estimate"></a>Stima dei dati
Dopo aver creato una richiesta, Priva inizia immediatamente a cercare potenziali corrispondenze all'oggetto dei dati nell'ambiente Microsoft 365 locale. Dopo aver identificato tutti gli elementi che pensiamo corrispondano ai criteri, vedrai la stima nella scheda riepilogo Stima dati  nella pagina **Panoramica della** richiesta. La quantità di dati nell'ambito della ricerca influirà sul tempo necessario per completare la stima.

La richiesta verrà spostata automaticamente alla fase successiva del recupero dei dati, in cui tutti gli elementi di contenuto vengono raccolti insieme in modo che le parti interessate possano collaborare alla revisione dei dati. In alcuni casi la stima dei dati verrà sospesa prima di passare al recupero e verranno notificati i passaggi successivi da eseguire prima di continuare.

Puoi anche scegliere di sospendere automaticamente nella fase di stima dei dati quando crei per la prima volta una richiesta di diritti dell'oggetto. Durante il processo di creazione, selezionare **l'opzione Ottieni prima** una stima durante il **passaggio Impostazioni di** ricerca. Esaminare i dettagli sul passaggio [delle impostazioni di ricerca](subject-rights-requests-create.md#define-search-settings).

#### <a name="pause-in-data-estimate-for-large-search-results"></a>Sospendere la stima dei dati per risultati di ricerca di grandi dimensioni

Priva noterà se la stima dei dati è proiettata per restituire una grande quantità di elementi da rivedere (oltre 10.000 elementi). La stima verrà sospesa in modo da poter visualizzare in anteprima i risultati e decidere se modificare la [query di ricerca](subject-rights-requests-create.md#refine-your-search) in modo che punti a posizioni o condizioni più specifiche o continuare a recuperare gli elementi identificati.  Ti mostreremo sullo schermo il numero di elementi e il volume di dati che corrispondono alla tua ricerca. Nella barra dei messaggi nella parte superiore dello schermo sono disponibili una o entrambe le opzioni seguenti:

- Un **pulsante Modifica query** di ricerca consente di accedere direttamente alle impostazioni di ricerca della richiesta per impostare parametri più rigorosi e generare una nuova stima.
- Se la query di ricerca non è più di 300.000 elementi, verrà visualizzata anche l'opzione **Recupera dati**. In questo modo è possibile scegliere di non modificare la ricerca e di continuare a raccogliere i dati.

#### <a name="retrieve-data"></a>Recuperare i dati
La fase di recupero dei dati si verifica quando tutti i file, i messaggi di posta elettronica, le chat, le immagini e altri elementi di contenuto contenenti i dati personali dell'oggetto dati vengono recuperati e messi insieme in un contenitore di archiviazione BLOB di Azure per la revisione. Il recupero dei dati può richiedere alcuni minuti o molto più a seconda del volume di dati. Al termine di questa fase, la richiesta passa automaticamente alla fase successiva della **verifica dei dati**.

#### <a name="review-data"></a>Esaminare i dati
 In questa fase, i collaboratori devono esaminare i risultati nella scheda Dati  raccolti ed eseguire tutte le attività applicabili come la redazione, l'applicazione di tag e l'aggiunta di note. Al termine della revisione, selezionare **Completa revisione**.

#### <a name="generate-reports"></a>Generare report
I report vengono generati in questa fase. Al termine, questi elementi sono disponibili nella **scheda** Report. I file finiti possono essere esportati per la revisione finale e la consegna all'utente che ha effettuato la richiesta.

#### <a name="close-the-request"></a>Chiudere la richiesta
Una richiesta chiusa indica che tutto il lavoro è stato completato per soddisfare questa richiesta di diritti dell'oggetto. Tutti i dati raccolti e i report verranno conservati in base alle impostazioni [di conservazione dei dati.](priva-settings.md#data-retention-periods)

## <a name="step-2-optional-view-and-edit-search-queries"></a>Passaggio 2 (facoltativo): visualizzare e modificare le query di ricerca

Per visualizzare informazioni dettagliate sulla ricerca di dati alla base di una richiesta di diritti dell'oggetto, selezionare **Visualizza dettagli query di ricerca**. Verrà visualizzato un riquadro che riepiloga la query e mostra ulteriori dettagli su ciò che è stato trovato.

È possibile visualizzare in **anteprima i risultati** della ricerca per vedere il tipo di contenuto che verrà restituito per la query. Se si desidera modificare le proprietà di questa ricerca e non è stata avviata la fase Recupera dati, è possibile utilizzare **l'opzione Modifica query di** ricerca.

Il processo guidato per la query di ricerca di modifica consente di modificare o aggiungere proprietà per l'identificazione dell'oggetto dati, i filtri e le condizioni di ricerca e le posizioni in cui cercare i dati (inclusi Exchange, SharePoint, OneDrive e/o Teams). Usa queste opzioni per raggiungere il livello di specificità desiderato. È possibile esaminare la versione finale della nuova query prima di premere **Salva**.

Al termine della modifica della query di ricerca, verrà eseguita una nuova ricerca per sostituire i risultati della ricerca precedenti. In questo modo lo stato nella sezione **Stato** viene reimpostato sul primo passaggio, **Stima dati**. Il completamento della nuova ricerca può richiedere fino a 60 minuti. Al termine, vedrai i risultati aggiornati nella pagina dei dettagli della richiesta.

## <a name="step-3-review-data"></a>Passaggio 3: esaminare i dati

In questa fase, i collaboratori devono esaminare i risultati nella **scheda Dati raccolti** . Le attività essenziali includono:

1. Esaminare l'elenco degli elementi identificati e scegliere se includere ogni file nei riepiloghi e/o nelle esportazioni. Se non è necessario includere una corrispondenza segnalata, selezionare l'opzione "Escludi". Se il contenuto sembra essere un falso positivo, puoi scegliere "Non una corrispondenza" per escludere il file dai rapporti finali e contrassegnare l'elemento come elemento che non dovrebbe essere stato raccolto dalla richiesta. Per impostare lo stato di un elemento, usa il menu azione (puntini di sospensione verticali) accanto al nome e seleziona la scelta desiderata. Se richiesto, aggiungere una nota per il riferimento interno per spiegare la decisione. Le note sono necessarie quando si escludono i file.
1. Usa **l'opzione Applica** tag per identificare gli elementi che necessitano di attenzione. I tag disponibili includono le opzioni fornite dal sistema, ad esempio il tagging di un elemento per il follow-up, e possono includere tag personalizzati come definito nelle impostazioni globali.
1. Usa **Annota** per creare contrassegni in linea o modificare i dati in un file selezionato. Ad esempio, se è necessario includere un file per una persona che contiene anche le informazioni personali di altri utenti, è possibile utilizzare la **redazione** Area (sotto il pulsante Disegno nella barra dei comandi) per black out tutte le informazioni che non riguardano la persona che ha effettuato la richiesta. Al termine delle modifiche, selezionare **Includi** per aggiungere il file redatto alla richiesta. L'annotazione crea una copia del file, in modo che nulla nel file originale sia modificato e rimanga nella posizione originale. La copia viene archiviata nel BLOB di Azure.
1. Per rivedere le note su un elemento, selezionarlo e passare alla **scheda Note** file. Puoi anche usare **l'opzione Aggiungi nota file** per creare un nuovo commento. Per rivedere o aggiungere note a livello di caso generale, passare alla scheda **Note** principale sopra e usare **Aggiungi nota caso**. Queste note saranno visibili per gli utenti che lavorano alla richiesta, ma non verranno incluse nel report finale o condivise in altro modo con l'oggetto dei dati.
1. Dopo aver esaminato tutti gli elementi e impostato i relativi stati, selezionare **Completa revisione**. Verrà aperto un riquadro a comparsa in cui è possibile esaminare un riepilogo dei dati e aggiungere eventuali note rilevanti. Queste note sono per la conservazione dei record interni e non vengono condivise con l'oggetto dei dati.
1. Selezionare di nuovo Completa revisione per continuare. I riepiloghi delle decisioni verranno forniti in un secondo momento nella **scheda** Report.

### <a name="collaborate-on-data-review"></a>Collaborare alla revisione dei dati

Priva supporta la collaborazione tramite Microsoft Teams per consentire al gruppo di collaborare alle richieste di diritti dell'oggetto. Quando crei una nuova richiesta, per impostazione Teams viene creato automaticamente un canale di Teams associato alla richiesta. Qui puoi discutere la richiesta e condividere in modo sicuro input e contributi. Per partecipare alla conversazione, apri la richiesta e usa **l'opzione Chat con i** collaboratori. Verrà aperta la Microsoft Teams e verrà posizionata all'interno del canale Generale per il sito del team della richiesta di diritti dell'oggetto.

Per esaminare l'elenco dei collaboratori attivi che possono visualizzare e contribuire al sito del team, all'interno della richiesta di diritti dell'oggetto aprire la **scheda** Collaboratori. Per aggiungere altri utenti per collaborare a questa richiesta, selezionare l'opzione **Aggiungi un collaboratore**.

Per modificare il comportamento predefinito della generazione di siti Teams durante la creazione di una richiesta di diritti dell'oggetto, passare a **Impostazioni** nella barra di spostamento superiore e selezionare Teams **collaborazione** per modificare l'impostazione.

Puoi anche usare l'opzione Condividi in alto a destra all'interno di una richiesta a destra dell'oggetto per eseguire un ciclo di utenti tramite Teams o posta elettronica o per copiare il collegamento alla pagina in Priva. La condivisione tramite Teams consente di selezionare un sito e un canale di Teams esistenti disponibili per il tuo account, in cui verrà pubblicato un collegamento a questo caso insieme a qualsiasi messaggio fornito.

## <a name="step-4-close-the-request"></a>Passaggio 4: Chiudere la richiesta

Dopo aver eseguito tutte le azioni necessarie per risolvere la richiesta di diritti dell'oggetto, selezionare **Chiudi la richiesta**. Verrà creato il report finale, disponibile nella **scheda Report**. Il completamento potrebbe richiedere del tempo a seconda del numero di file nella richiesta.

## <a name="next-steps"></a>Passaggi successivi
Per ulteriori informazioni sull'utilizzo dei report e sul completamento delle richieste di diritti dell'oggetto, vedere [Generare report ed eseguire una richiesta di diritti dell'oggetto](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

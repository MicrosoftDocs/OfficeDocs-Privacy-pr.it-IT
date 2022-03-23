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
ms.openlocfilehash: 5a72208894ff699675dcde230a7413b20c0b0a1e
ms.sourcegitcommit: a9ad5185174a9e8a7eea7583d257e8535c96a2ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/23/2022
ms.locfileid: "63746766"
---
# <a name="review-data-for-a-subject-rights-request"></a>Esaminare i dati per una richiesta di diritti dell'oggetto

Dopo aver creato una richiesta per i diritti dell'oggetto [(ulteriori](subject-rights-requests-create.md) informazioni) in Microsoft Priva, la soluzione Subject Rights Requests utilizzerà gli input per cercare corrispondenze sull'oggetto dati nell'ambiente di Microsoft 365 dell'organizzazione. Dopo aver compilato questi dati, è possibile esaminare i risultati, effettuare scelte sugli elementi da includere e redigere le informazioni in base alle esigenze. Questi passaggi possono essere collaborati da più utenti tramite l'interfaccia Priva.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Passaggio 1: esaminare i dettagli della richiesta e monitorare lo stato

Per visualizzare i risultati iniziali della ricerca, passare all'area Priva del [Centro conformità Microsoft 365 e aprire](https://compliance.microsoft.com/) **Le richieste di diritti dell'oggetto**. In questa pagina principale è disponibile un elenco di tutte le richieste di diritti dell'oggetto aperte.

Seleziona la richiesta nell'elenco per visualizzare i dettagli della richiesta. Qui puoi trovare altre informazioni sulle proprietà della richiesta, sui risultati della ricerca e sullo stato della richiesta. Questa pagina diventerà il tuo hub per lavorare e collaborare alla gestione dei file trovati, alla creazione di report ed esportazioni e al completamento della richiesta.

I riquadri nella pagina dei dettagli della richiesta includono:

- **Dettagli**: dettagli essenziali sulla richiesta, inclusa la data di scadenza e la data della richiesta, la descrizione e la normativa sulla privacy correlata.
- **Progress**: sequenza temporale che indica i passaggi completati e tutte le attività ancora da completare.
- Statistiche sulla fase di avanzamento corrente. Questo riquadro può mostrare informazioni come un riepilogo della stima dei dati, il numero di elementi trovati nella ricerca e le relative posizioni in Microsoft 365 o lo stato delle esportazioni.
- **Elementi con priorità da esaminare**: questo riquadro mostrerà informazioni sugli elementi importanti rilevati automaticamente da Priva. Ad esempio, questo potrebbe includere informazioni riservate che già recano un'etichetta di riservatezza Microsoft o elementi con dati su più utenti che potrebbero richiedere una redazione. Ciò consente agli amministratori di sapere da dove iniziare la revisione. Gli elementi di priorità sono disponibili in Dati raccolti filtrando in base alla colonna "Tipi di priorità".

### <a name="understand-progress-stages"></a>Comprendere le fasi di avanzamento

Le richieste di diritti dell'oggetto vengono sottoposte a più fasi. Alcuni stati avanzano automaticamente e altre fasi avanzano quando gli amministratori e i collaboratori richiedono diritti dell'oggetto completano passaggi essenziali come la revisione dei file.

Poiché potrebbe essere necessario lavorare sulle richieste nel tempo o da più collaboratori, Priva fornisce aggiornamenti continui sullo stato e indicazioni sui passaggi successivi da eseguire. Questi aggiornamenti possono essere visualizzati nella scheda **Panoramica** della pagina dei dettagli di una richiesta di diritti dell'oggetto.

#### <a name="data-estimate"></a>Stima dei dati
Dopo aver creato una richiesta, Priva inizia immediatamente a cercare potenziali corrispondenze all'oggetto dei dati nell'Microsoft 365 locale. Dopo aver identificato tutti gli elementi che pensiamo corrispondano ai criteri, vedrai la stima nella scheda riepilogo Stima dati  nella pagina **Panoramica della** richiesta. La quantità di dati nell'ambito della ricerca influirà sul tempo necessario per completare la stima.

La richiesta verrà spostata automaticamente alla fase successiva del recupero dei dati, in cui tutti gli elementi di contenuto vengono raccolti insieme in modo che le parti interessate possano collaborare alla revisione dei dati. In alcuni casi la stima dei dati verrà sospesa prima di passare al recupero e verranno notificati i passaggi successivi da eseguire prima di continuare.

Puoi anche scegliere di sospendere automaticamente nella fase di stima dei dati quando crei per la prima volta una richiesta di diritti dell'oggetto. Durante il processo di creazione, selezionare **l'opzione Ottieni prima** una stima durante il **passaggio Impostazioni di** ricerca. Esaminare i dettagli sul passaggio [delle impostazioni di ricerca](subject-rights-requests-create.md#define-search-settings).

#### <a name="pause-in-data-estimate-for-large-search-results"></a>Sospendere la stima dei dati per risultati di ricerca di grandi dimensioni

Priva noterà se la stima dei dati è proiettata per restituire un gran numero di elementi da rivedere (oltre 10.000 elementi). La stima verrà sospesa in modo da poter visualizzare in anteprima i risultati e decidere se modificare la [query di ricerca](subject-rights-requests-create.md#refine-your-search) in modo che punti a posizioni o condizioni più specifiche o continuare a recuperare gli elementi identificati.  Ti mostreremo sullo schermo il numero di elementi e il volume di dati che corrispondono alla tua ricerca. Nella barra dei messaggi nella parte superiore dello schermo sono disponibili una o entrambe le opzioni seguenti:

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

In questa fase, i collaboratori devono esaminare i risultati nella **scheda Dati raccolti**. Verrà Teams automaticamente un canale per facilitare la revisione del contenuto da parte di tutte le parti interessate. Per [altri dettagli, vedi Collaborare alla revisione](#collaborate-on-data-review) dei dati. Le attività essenziali per il passaggio di revisione dei dati sono descritte di seguito.

#### <a name="mark-items-as-include-or-exclude-and-add-notes"></a>Contrassegnare gli elementi come Includi o Escludi e aggiungi note

Esaminare l'elenco degli elementi identificati per determinare se i dati personali dell'oggetto dei dati si trova in ogni elemento. Se l'elemento contiene le informazioni dell'oggetto dati e appartiene come parte del report finale all'oggetto dati, contrassegnare l'elemento come **Includi** selezionando Includi  sulla barra dei comandi nella parte superiore dell'elenco di elementi. Puoi anche selezionare il pulsante blu **Includi** nell'area di revisione del contenuto a destra dell'elenco di elementi. Quando si seleziona **Includi**, viene visualizzato un riquadro a comparsa con un'opzione per aggiungere note. Al termine, **selezionare Invia per** salvare lo stato di revisione dell'elemento come **Includi**.

Se non è necessario includere un elemento come parte della richiesta, selezionare Escludi  sulla barra dei comandi o il pulsante  Escludi nell'area di revisione del contenuto. L'esclusione di un elemento significa che non è rilevante per la richiesta di diritti dell'oggetto e l'elemento non verrà incluso nei rapporti finali generati per [l'oggetto dei dati](subject-rights-requests-reports.md).

> [!NOTE]
> Se si contrassegna **un elemento Exclude**, è necessario aggiungere una nota come giustificazione del motivo per cui non riguarda la richiesta di diritti dell'oggetto. Le note sono per scopi interni e non sono incluse nei report finali.

Se il contenuto sembra essere un falso positivo, selezionare Non  corrisponde per escludere il file dai rapporti finali e contrassegnare l'elemento come elemento che non dovrebbe essere stato rilevato nella ricerca. Nel riquadro **a comparsa Contrassegna** come non corrispondente selezionare Conferma per  far sapere che l'elemento non corrisponde ai criteri di ricerca.

#### <a name="apply-tags"></a>Applicazione di tag

I tag possono essere usati per identificare gli elementi che necessitano di ulteriore attenzione. Priva fornisce tre tag predefiniti , **Follow-up**, **Delete** e **Update** , per i quali è possibile impostare una descrizione. Priva fornisce anche due tag personalizzati che puoi assegnare e descrivere.

Ad esempio, se si determina durante la revisione dei dati che un elemento di contenuto non deve essere conservato dall'organizzazione, è possibile applicare il tag **Delete** , quindi esportare un elenco di tutti i file con tag in modo da poter tornare indietro ed eliminare gli elementi identificati al termine della richiesta.

I cinque tag impostati e [gestiti in Impostazioni](priva-settings.md#data-review-tags) si applicano a tutte le richieste di diritti dell'oggetto.

**Per aggiungere o rimuovere tag:**

- Selezionare l'elemento dall'elenco nella **scheda Dati raccolti** della richiesta.
- Nell'area di anteprima dell'elemento a destra dell'elenco seleziona il **pulsante Applica** tag nella riga inferiore. Puoi anche selezionare i tre punti a destra del nome dell'elemento e selezionare **l'opzione Applica** tag.
- Verrà visualizzato un riquadro a comparsa con l'elenco di tag. Seleziona la casella accanto ai tag che vuoi applicare all'elemento. Se si deseleziona una casella selezionata, il tag verrà rimosso.
- Quando si è soddisfatti delle selezioni, selezionare **Salva**, che salva le selezioni di tag e chiude il riquadro a comparsa.

**Per aggiungere tag personalizzati o aggiornare le descrizioni dei tag:**
- Nella pagina Richieste di diritti dell'oggetto seleziona **Impostazioni** nell'angolo in alto a destra dello schermo per accedere alle impostazioni priva.
- Vai alla **pagina Tag revisione dati** e seleziona il tag per immettere una descrizione e, per i tag personalizzati, un nome. Altre informazioni sulle [impostazioni dei tag](priva-settings.md#data-review-tags).

**Per esportare un elenco di elementi contrassegnati:**
- Vai alla pagina **Dati raccolti** in una richiesta di diritti dell'oggetto.
- Sopra l'elenco di elementi, selezionare l'icona freccia giù che indica **Esporta** quando si passa su di esso.
- Verrà scaricato Excel file. Apri il file al termine del download.

Il file Excel scaricato mostra le proprietà di tutti gli elementi raccolti dalla ricerca per la richiesta. Trova la **colonna** Tag per identificare e ordinare gli elementi in base al tag.

#### <a name="use-the-annotate-command-to-redact-text"></a>Utilizzare il comando Annotate per redigere il testo
Usa **Annota** per creare contrassegni in linea o modificare i dati in un file selezionato. Ad esempio, se è necessario includere un file per una persona che contiene anche le informazioni personali di altri utenti, è possibile utilizzare la **redazione** Area (sotto il pulsante Disegno nella barra dei comandi) per black out tutte le informazioni che non riguardano la persona che ha effettuato la richiesta. Al termine delle modifiche, selezionare **Includi** per aggiungere il file redatto alla richiesta. L'annotazione crea una copia del file, in modo che nulla nel file originale sia modificato e rimanga nella posizione originale. La copia viene archiviata nel BLOB di Azure.

#### <a name="enter-notes-about-a-file"></a>Immettere note su un file
Per aggiungere o rivedere note su un elemento, selezionare l'elemento dalla relativa riga e passare alla scheda **Note** file nell'area di revisione del contenuto a destra. Puoi anche usare **l'opzione Aggiungi nota file** per creare un nuovo commento. Per rivedere o aggiungere note a livello di caso generale, passare alla scheda **Note** principale sopra e usare **Aggiungi nota caso**. Queste note saranno visibili per gli utenti che lavorano alla richiesta, ma non verranno incluse nel report finale o condivise in altro modo con l'oggetto dei dati.

#### <a name="complete-the-review"></a>Completare la revisione

Quando tutti gli elementi sono stati esaminati e ne hai impostato lo stato come **Includi,** Escludi o Non corrisponde, è il momento di chiudere il passaggio di revisione selezionando il pulsante  Completa revisione nell'angolo in alto **a** destra all'interno della richiesta.  Un riquadro a comparsa mostrerà un riepilogo dei dati e aggiungerà eventuali note correlate. Queste note sono per la conservazione dei record interni e non vengono condivise con l'oggetto dei dati.

Selezionare **Completa revisione** nel riquadro a comparsa per completare il passaggio di revisione. I riepiloghi delle decisioni verranno forniti in un secondo momento nella **scheda** Report.

### <a name="collaborate-on-data-review"></a>Collaborare alla revisione dei dati

Priva supporta la collaborazione tramite Microsoft Teams per consentire al gruppo di collaborare alle richieste di diritti dell'oggetto. Quando crei una nuova richiesta, per impostazione Teams viene creato automaticamente un canale di Teams associato alla richiesta. Qui puoi discutere la richiesta e condividere in modo sicuro input e contributi. Per partecipare alla conversazione, apri la richiesta e usa **l'opzione Chat con i** collaboratori. Verrà aperta la Microsoft Teams e verrà posizionata all'interno del canale Generale per il sito del team della richiesta di diritti dell'oggetto.

Per esaminare l'elenco dei collaboratori attivi che possono visualizzare e contribuire al sito del team, all'interno della richiesta di diritti dell'oggetto aprire la **scheda** Collaboratori. Per aggiungere altri utenti per collaborare a questa richiesta, selezionare l'opzione **Aggiungi un collaboratore**.

Per modificare il comportamento predefinito della generazione di siti Teams durante la creazione di una richiesta di diritti dell'oggetto, passare a **Impostazioni** nella barra di spostamento superiore e selezionare Teams **collaborazione** per modificare l'impostazione.

Puoi anche usare l'opzione Condividi in alto a destra all'interno di una richiesta a destra dell'oggetto per eseguire un ciclo di utenti tramite Teams o posta elettronica o per copiare il collegamento alla pagina in Priva. La condivisione tramite Teams consente di selezionare un sito e un canale di Teams esistenti disponibili per il tuo account, dove invierà un collegamento a questo caso insieme a qualsiasi messaggio fornito.

## <a name="step-4-close-the-request"></a>Passaggio 4: Chiudere la richiesta

Dopo aver eseguito tutte le azioni necessarie per risolvere la richiesta di diritti dell'oggetto, selezionare **Chiudi la richiesta**. Verrà creato il report finale, disponibile nella **scheda Report**. Il completamento potrebbe richiedere del tempo a seconda del numero di file nella richiesta.

## <a name="next-steps"></a>Passaggi successivi
Per ulteriori informazioni sull'utilizzo dei report e sul completamento delle richieste di diritti dell'oggetto, vedere [Generare report ed eseguire una richiesta di diritti dell'oggetto](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

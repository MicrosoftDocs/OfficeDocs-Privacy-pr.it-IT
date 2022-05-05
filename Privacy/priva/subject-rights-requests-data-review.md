---
title: Esaminare i dati per una richiesta di diritti dell'interessato
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
description: Informazioni su come esaminare i dati delle richieste di diritti degli interessati raccolti da Microsoft Priva e collaborare al completamento della richiesta.
ms.openlocfilehash: 3a1211d391ee196ad431fe19ab9134386c9803a4
ms.sourcegitcommit: 6b88d22d0250cbb9a4ba1f71665f29cb67939851
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2022
ms.locfileid: "65059760"
---
# <a name="review-data-for-a-subject-rights-request"></a>Esaminare i dati per una richiesta di diritti dell'interessato

Dopo aver creato una richiesta di diritti dell'interessato ([altre informazioni](subject-rights-requests-create.md)) in Microsoft Priva, la soluzione Subject Rights Requests userà gli input per cercare corrispondenze sull'interessato nell'ambiente Microsoft 365 dell'organizzazione. Dopo aver compilato questi dati, è possibile esaminare i risultati, scegliere cosa includere e redigere le informazioni in base alle esigenze. Questi passaggi possono essere collaborati da più utenti tramite l'interfaccia Priva.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Passaggio 1: Esaminare i dettagli della richiesta e monitorare lo stato di avanzamento

Per visualizzare i risultati iniziali della ricerca, passare all'area Priva del portale di [conformità di Microsoft Purview](https://compliance.microsoft.com/) e aprire **Richieste di diritti dell'oggetto**. In questa pagina principale è disponibile un elenco di tutte le richieste di diritti dell'oggetto aperte.

Selezionare la richiesta nell'elenco per visualizzare i dettagli della richiesta. Qui è possibile ottenere altre informazioni sulle proprietà della richiesta, sui risultati della ricerca e sullo stato della richiesta. Questa pagina diventerà l'hub per lavorare e collaborare alla gestione dei file trovati, alla creazione di report ed esportazioni e al completamento della richiesta.

La scheda **Panoramica** della pagina dei dettagli della richiesta fornisce dettagli sulla richiesta, un indicatore di stato che mostra il passaggio corrente e informazioni chiave sui dati trovati. I riquadri in questa pagina includono quanto segue:

##### <a name="details"></a>Dettagli

La scheda **Dettagli** visualizza informazioni di base per orientarti verso la richiesta, ad esempio la scadenza, la data di creazione, la descrizione e il regolamento sulla privacy correlati alla richiesta.

##### <a name="progress"></a>Progresso

La scheda **Stato** elenca ogni passaggio del processo: stima dei dati, recupero dei dati, revisione dei dati, generazione di report e chiusura della richiesta. Un cerchio blu pieno accanto al passaggio indica il passaggio attualmente in corso. Un segno di spunta all'interno del cerchio blu indica che il passaggio è completo e il cerchio non riempito indica che il passaggio non è ancora iniziato.

##### <a name="total-number-of-items-found"></a>Numero totale di elementi trovati

Statistiche sulla fase di avanzamento corrente. Questo riquadro può visualizzare informazioni come un riepilogo della stima dei dati, il numero di elementi trovati nella ricerca e le relative posizioni in Microsoft 365 o lo stato delle esportazioni.

##### <a name="priority-items-to-review"></a>Elementi di priorità da esaminare

Il riquadro **Elementi di priorità da rivedere** mostra gli elementi che è possibile assegnare priorità all'avvio della revisione. Il riquadro visualizza un conteggio degli elementi appartenenti alle categorie seguenti:
- **Riservato**: si tratta di elementi a cui è applicata [un'etichetta di riservatezza Microsoft](/microsoft-365/compliance/sensitivity-labels) . Ad esempio, un documento di Word con un'etichetta "Altamente riservato". 
- **Dati multi-persona**: questi elementi contengono i dati personali di più persone. Se si desidera includere questi elementi come parte del pacchetto di dati finale, è necessario redigere i dati irrilevanti nei file. Per informazioni dettagliate, vedere [Passaggio 3: Esaminare i dati](#step-3-review-data) riportati di seguito. Si noti che per consentire a Priva di identificare gli elementi con dati multi-persona, l'organizzazione deve configurare la [corrispondenza dei dati per le richieste di diritti degli interessati](subject-rights-requests-data-match.md).

**Come individuare gli elementi di priorità:**

Prima di tutto, assicurarsi di aver abilitato la visualizzazione nella tabella di elementi **Raccolta** dati seguendo la procedura seguente:

- Nella scheda **Dati raccolti** selezionare **Personalizza colonne** nella parte superiore dell'elenco di elementi.
- Nel riquadro a comparsa **Modifica colonne** posizionare un controllo accanto a **Tipi di priorità**.
- Selezionare **Applica**. L'elenco di elementi avrà ora una colonna **Tipi di priorità** .

È ora possibile identificare gli elementi di priorità e trovarli ordinando la colonna **Tipo di priorità** per raggruppare tipi simili.

### <a name="understand-progress-stages"></a>Informazioni sulle fasi di avanzamento

Le richieste di diritti del soggetto passano attraverso più fasi. Alcuni stati avanzano automaticamente e altre fasi avanzano quando gli amministratori e i collaboratori delle richieste di diritti dell'oggetto completano i passaggi essenziali, ad esempio la revisione dei file.

Poiché le richieste potrebbero dover essere elaborate nel tempo o da più collaboratori, Priva fornisce aggiornamenti continui sullo stato e indicazioni sui passaggi successivi da eseguire. Questi aggiornamenti possono essere visualizzati nella scheda **Panoramica** della pagina dei dettagli di una richiesta di diritti dell'oggetto.

#### <a name="data-estimate"></a>Stima dei dati
Dopo aver creato una richiesta, Priva inizia immediatamente a cercare potenziali corrispondenze con l'interessato nell'ambiente Microsoft 365. Dopo aver identificato tutti gli elementi che riteniamo corrispondono ai criteri, la stima verrà visualizzata nella scheda **Riepilogo stima dati** nella pagina **Panoramica** della richiesta. La quantità di dati nell'ambito della ricerca influirà sul periodo di tempo necessario per completare la stima.

La richiesta passerà automaticamente alla fase successiva di recupero dei dati, in cui tutti gli elementi di contenuto vengono raccolti insieme in modo che gli stakeholder possano collaborare alla revisione dei dati. In alcuni casi, la stima dei dati verrà sospesa prima di passare al recupero e verrà visualizzata una notifica dei passaggi successivi da eseguire prima di continuare.

È anche possibile scegliere di sospendere automaticamente nella fase di stima dei dati quando si crea una richiesta di diritti dell'interessato per la prima volta. Durante il processo di creazione selezionare l'opzione **Ottieni una prima stima** durante il passaggio **Impostazioni di ricerca** . Esaminare i dettagli sul [passaggio delle impostazioni di ricerca](subject-rights-requests-create.md#define-search-settings).

#### <a name="pause-in-data-estimate-for-large-search-results"></a>Sospendere la stima dei dati per i risultati della ricerca di grandi dimensioni

Priva noterà se si prevede che la stima dei dati restituisca un numero elevato di elementi da esaminare (oltre 10.000 elementi). La stima verrà sospesa in modo che sia possibile visualizzare in anteprima i risultati e decidere se [modificare la query di ricerca](subject-rights-requests-create.md#refine-your-search) in base a posizioni o condizioni più specifiche o continuare a recuperare gli elementi identificati.  Verrà visualizzato sullo schermo il numero di elementi e il volume di dati corrispondenti alla ricerca. In una barra dei messaggi nella parte superiore dello schermo sono disponibili una o entrambe le opzioni seguenti:

- Un pulsante **Modifica query di ricerca** consente di accedere direttamente alle impostazioni di ricerca della richiesta per impostare parametri più severi e generare una nuova stima.
- Finché la query di ricerca non supera i 300.000 elementi, verrà anche visualizzata un'opzione **Per recuperare i dati**. In questo modo è possibile scegliere di non modificare la ricerca e continuare a raccogliere i dati.

#### <a name="retrieve-data"></a>Recuperare i dati
La fase di recupero dei dati si verifica quando tutti i file, i messaggi di posta elettronica, le chat, le immagini e altri elementi di contenuto contenenti i dati personali dell'interessato vengono recuperati e raggruppati in un contenitore di archiviazione BLOB di Azure per la revisione. Il recupero dei dati può richiedere alcuni minuti o molto più a seconda del volume di dati. Al termine di questa fase, la richiesta passa automaticamente alla fase successiva di **Revisione dei dati**.

#### <a name="review-data"></a>Esaminare i dati
 In questa fase, i collaboratori devono esaminare i risultati nella scheda **Dati raccolti** ed eseguire tutte le attività applicabili, ad esempio la redazione, l'applicazione di tag e l'aggiunta di note. Al termine della revisione, selezionare **Completa revisione**.

#### <a name="generate-reports"></a>Generare report
I report vengono generati in questa fase. Al termine, è possibile trovarli nella scheda **Report** . I file completati possono essere esportati per la revisione finale e il recapito all'interessato che ha effettuato la richiesta.

#### <a name="close-the-request"></a>Chiudere la richiesta
Una richiesta chiusa indica che tutto il lavoro è stato completato per soddisfare questa richiesta di diritti dell'oggetto. Tutti i dati raccolti e i report verranno conservati in base alle [impostazioni di conservazione dei dati](priva-settings.md#data-retention-periods).

## <a name="step-2-optional-view-and-edit-search-queries"></a>Passaggio 2 (facoltativo): Visualizzare e modificare le query di ricerca

Per visualizzare informazioni dettagliate sulla ricerca dei dati dietro una richiesta di diritti dell'interessato, selezionare **Visualizza dettagli query di ricerca**. Verrà aperto un riquadro che riepiloga la query e mostra altri dettagli sugli elementi trovati.

È possibile visualizzare **l'anteprima dei risultati della ricerca** per visualizzare il tipo di contenuto che verrà restituito per questa query. Se si desidera modificare le proprietà di questa ricerca e non è stata avviata la fase Recupera dati, è possibile usare l'opzione **Modifica query di ricerca** .

Il processo guidato per la modifica della query di ricerca consente di modificare o aggiungere proprietà per l'identificazione dell'interessato, i filtri e le condizioni di ricerca e le posizioni in cui cercare i dati (inclusi Exchange, SharePoint, OneDrive e/o Teams). Usare queste opzioni per raggiungere il livello di specificità desiderato. È possibile esaminare la versione finale della nuova query prima di premere **Salva**.

Al termine della modifica della query di ricerca, verrà eseguita una nuova ricerca per sostituire i risultati della ricerca precedente. In questo modo, lo stato nella sezione **Stato** viene ripristinato al primo passaggio, **Stima dati**. Il completamento della nuova ricerca potrebbe richiedere fino a 60 minuti. Al termine, verranno visualizzati i risultati aggiornati nella pagina dei dettagli della richiesta.

## <a name="step-3-review-data"></a>Passaggio 3: Esaminare i dati

In questa fase, i collaboratori devono esaminare i risultati nella scheda **Dati raccolti**. Verrà automaticamente configurato un canale Teams per facilitare la revisione dei contenuti da parte di tutti gli stakeholder. Per altri dettagli [, vedere Collaborare alla revisione dei dati](#collaborate-on-data-review) . Le attività essenziali per il passaggio di revisione dei dati sono descritte di seguito.

#### <a name="mark-items-as-include-or-exclude-and-add-notes"></a>Contrassegnare gli elementi come Includi o Escludi e aggiungere note

Esaminare l'elenco degli elementi identificati restituiti dalla ricerca. Se si decide di includere l'elemento come parte del report finale all'interessato, selezionare **Includi** sulla barra dei comandi nella parte superiore dell'elenco di elementi. È anche possibile selezionare il pulsante blu **Includi** nell'area di revisione del contenuto a destra dell'elenco di elementi. Quando si seleziona **Includi**, viene visualizzato un riquadro a comparsa con un'opzione per aggiungere note. Al termine, selezionare **Invia** per salvare lo stato di revisione dell'elemento come **Includi**.

Se l'elemento non appartiene come parte della richiesta, selezionare **Escludi** sulla barra dei comandi o il pulsante **Escludi** nell'area di revisione del contenuto. L'esclusione di un elemento significa che non verrà inclusa nei [report finali generati per l'interessato](subject-rights-requests-reports.md).

> [!NOTE]
> Se contrassegni un elemento come **Escludi**, devi aggiungere una nota come giustificazione per il motivo per cui non riguarda la richiesta di diritti dell'oggetto. Le note sono per scopi interni e non sono incluse nei report finali.

Se il contenuto sembra essere un falso positivo, selezionare **Non corrisponde** e nel riquadro a comparsa selezionare **Conferma**. Questa azione escluderà il file dai report finali e contrassegnerà l'elemento come qualcosa che non avrebbe dovuto essere rilevato nella ricerca.

#### <a name="apply-tags"></a>Applicazione di tag

I tag possono essere usati per identificare gli elementi che richiedono ulteriore attenzione. Priva fornisce tre tag predefiniti, **ovvero Completamento**, **Eliminazione** e **Aggiornamento** , per i quali è possibile impostare una descrizione. Priva fornisce anche due tag personalizzati che è possibile denominare e descrivere.

Ad esempio, se durante la verifica dei dati si determina che un elemento di contenuto non deve essere conservato dall'organizzazione, è possibile applicare il tag **Elimina** , quindi esportare un elenco di tutti i file con tag in modo da poter tornare indietro ed eliminare gli elementi identificati al termine della richiesta.

I cinque tag gestiti in **Impostazioni** si applicano a tutte le richieste di diritti dell'oggetto.

**Per aggiungere o rimuovere tag:**

- Selezionare l'elemento dall'elenco nella scheda **Dati raccolti** della richiesta.
- Nell'area di anteprima dell'elemento a destra dell'elenco selezionare il pulsante **Applica tag** nella riga inferiore. È anche possibile selezionare i tre punti a destra del nome dell'elemento e selezionare l'opzione **Applica tag** .
- Viene visualizzato un riquadro a comparsa con l'elenco di tag. Selezionare la casella accanto a uno dei tag da applicare all'elemento. L'annullamento del controllo di una casella di controllo rimuoverà il tag.
- Al termine, selezionare **Salva**, che salva le selezioni dei tag e chiude il riquadro a comparsa.

**Per aggiungere tag personalizzati o aggiornare le descrizioni dei tag:**
- Nella pagina Richieste di diritti dell'oggetto selezionare **Impostazioni** nell'angolo in alto a destra dello schermo per accedere alle impostazioni Priva.
- Passare alla pagina **Tag di revisione dei dati** e selezionare il tag per immettere una descrizione e, per i tag personalizzati, un nome. Altre informazioni sulle [impostazioni dei tag](priva-settings.md#data-review-tags).

**Per esportare un elenco di elementi con tag:**
- Passare alla pagina **Dati raccolti** in una richiesta di diritti dell'interessato.
- Sopra l'elenco di elementi, selezionare l'icona freccia giù che indica **Esporta** quando si passa il mouse su di esso.
- Verrà scaricato un file Excel che mostra le proprietà per tutti gli elementi raccolti dalla ricerca della richiesta. Trovare la colonna **Tag** per identificare e ordinare gli elementi in base al tag.

#### <a name="use-the-annotate-command-to-redact-text"></a>Usare il comando Annota per redigere il testo
Il comando **Annota** nell'area di revisione del contenuto consente di creare mark-up inline e redact dati all'interno di un elemento di contenuto. Ad esempio, se è necessario includere un file per un utente che contiene anche le informazioni personali di un altro interessato, è possibile utilizzare la **modifica dell'area** sotto il pulsante Disegno nella barra dei comandi per oscurare tutte le informazioni che non riguardano la persona che ha effettuato la richiesta. Al termine delle modifiche, selezionare **Includi** per aggiungere il file redacted alla richiesta. L'annotazione crea una copia del file, che viene archiviata nel BLOB di Azure. Il file originale rimane inalterato e archiviato nel percorso originale.

#### <a name="enter-notes-about-a-file"></a>Immettere note su un file
Per aggiungere o rivedere note su un elemento, selezionare l'elemento dalla relativa riga e passare alla scheda **Note file** nell'area di revisione del contenuto a destra. È anche possibile usare l'opzione **Aggiungi nota file** per creare un nuovo commento. Per esaminare o aggiungere note a livello di caso generale, passare alla scheda **Note** principale precedente e usare **Aggiungi nota caso**. Queste note saranno visibili agli utenti che lavorano alla richiesta, ma non saranno incluse nel report finale o altrimenti condivise con l'interessato.

#### <a name="complete-the-review"></a>Completare la revisione

Quando tutti gli elementi sono stati esaminati e il relativo stato è stato impostato su **Includi**, **Escludi** o **Non corrisponde,** è il momento di chiudere il passaggio di revisione selezionando il pulsante  **Completa revisione** nell'angolo in alto a destra all'interno della richiesta. Un riquadro a comparsa mostrerà un riepilogo dei dati e aggiungerà eventuali note correlate. Queste note sono destinate alla conservazione interna dei record e non vengono condivise con l'interessato.

Selezionare **Completa revisione** nel riquadro a comparsa per completare il passaggio di revisione. I riepiloghi delle decisioni verranno forniti più avanti nella scheda **Report** .

### <a name="collaborate-on-data-review"></a>Collaborare alla revisione dei dati

Priva supporta la collaborazione tramite Microsoft Teams per consentire al gruppo di collaborare alle richieste di diritti degli interessati. Quando si crea una nuova richiesta, un canale Teams viene creato e associato automaticamente alla richiesta per impostazione predefinita. Qui è possibile discutere della richiesta e condividere in modo sicuro input e contributi. Per partecipare alla conversazione, aprire la richiesta e usare l'opzione **Chat con i collaboratori** . Verrà aperto Microsoft Teams e verrà inserito all'interno del canale Generale per il sito del team della richiesta di diritti dell'oggetto.

Per esaminare l'elenco dei collaboratori attivi che possono visualizzare e contribuire al sito del team, all'interno della richiesta di diritti dell'oggetto aprire la scheda **Collaboratori** . Per aggiungere altri utenti per collaborare a questa richiesta, selezionare l'opzione **Aggiungi un collaboratore**.

Per modificare il comportamento predefinito della generazione di siti Teams durante la creazione di una richiesta di diritti dell'oggetto, passare a **Impostazioni** nel riquadro di spostamento superiore e selezionare **Teams collaborazione** per modificare l'impostazione.

È anche possibile usare l'opzione **Condividi** in alto a destra all'interno di una richiesta di diritto dell'oggetto per eseguire il ciclo degli utenti tramite Teams o posta elettronica o per copiare il collegamento alla pagina in Priva. La condivisione tramite Teams consente di selezionare un sito e un canale di Teams esistenti disponibili per l'account, in cui verrà inviato un collegamento a questo caso insieme a qualsiasi messaggio fornito.

## <a name="step-4-close-the-request"></a>Passaggio 4: Chiudere la richiesta

Dopo aver eseguito tutte le azioni necessarie per risolvere la richiesta di diritti **dell'oggetto, selezionare Chiudi la richiesta**. In questo modo viene creato il report finale, disponibile nella **scheda Report**. Il completamento potrebbe richiedere del tempo a seconda del numero di file nella richiesta.

## <a name="next-steps"></a>Passaggi successivi
Per altre informazioni sull'uso dei report e sul completamento delle richieste di diritti dell'oggetto, vedere [Generare report e soddisfare una richiesta di diritti dell'oggetto](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

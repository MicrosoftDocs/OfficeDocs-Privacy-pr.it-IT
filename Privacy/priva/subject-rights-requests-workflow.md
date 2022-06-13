---
title: Flusso di lavoro per le richieste di diritti dell'interessato
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
description: Comprendere i passaggi del flusso di lavoro e la pagina dei dettagli della richiesta in Richieste di diritti degli interessati Microsoft Priva.
ms.openlocfilehash: 389c587d8d8b56d0654a78281825c8f98a6244d3
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046740"
---
# <a name="understand-the-workflow-and-request-details-pages"></a>Informazioni sulle pagine dei dettagli del flusso di lavoro e della richiesta

**Questo articolo** illustra i passaggi di avanzamento durante la creazione e l'esecuzione di una richiesta. Informazioni su come usare le informazioni dettagliate e le funzionalità nella pagina dei dettagli di ogni richiesta.

Quando si [crea una richiesta](subject-rights-requests-create.md) nella soluzione Subject Rights Requests, le informazioni fornite vengono usate per cercare corrispondenze sull'interessato nell'ambiente Microsoft 365 dell'organizzazione. Gli elementi corrispondenti vengono rispettati per consentire all'utente di esaminare, scegliere cosa includere e redigere le informazioni in base alle esigenze. Più utenti possono collaborare a questi passaggi all'interno dell'interfaccia Subject Rights Requests. La pagina [Panoramica](#overview-tab) della richiesta fornisce lo stato delle fasi di avanzamento e le indicazioni sui passaggi successivi da eseguire.

## <a name="progress-stages-for-requests"></a>Fasi di avanzamento per le richieste

Ogni richiesta viene eseguita in più fasi. Alcune fasi vengono eseguite automaticamente e altre vengono avanzate manualmente dopo il completamento di alcuni passaggi, ad esempio la revisione dei file.

- **Stima dei dati**: prima di recuperare i dati, Priva stima la quantità di dati che si prevede di trovare. A seconda della quantità di dati, la richiesta può o meno passare automaticamente alla fase successiva di recupero dei dati. È possibile impostare una richiesta di sospensione nella fase di stima prima di raccogliere i dati; per altre informazioni, vedere [la stima e il recupero dei dati](subject-rights-requests-data-retrieval.md).

- **Recupera dati**: tutti i file, i messaggi di posta elettronica, le chat, le immagini e altri elementi di contenuto vengono raggruppati. Al termine di questa fase, la richiesta passa automaticamente alla fase successiva di revisione dei dati. Per altre informazioni, vedere [Stima e recupero dei dati](subject-rights-requests-data-retrieval.md).

- **Esaminare i dati**: i collaboratori esaminano tutti i dati raccolti, decidono quali riguardano la richiesta ed eseguono attività come la redazione di file e l'aggiunta di note del caso. Altre informazioni sulla [revisione dei dati per una richiesta di diritti dell'interessato](subject-rights-requests-data-review.md). Dopo aver completato la revisione dei dati, passare manualmente alla fase successiva per generare report.

- **Genera report**: al termine della revisione dei dati, un utente passa manualmente a questo passaggio. Priva genera i report finali, che includono il pacchetto di dati da condividere con l'interessato e i report interni per i record dell'organizzazione. Altre informazioni sulla [generazione di report](subject-rights-requests-reports.md).

- **Chiudere la richiesta**: al termine di tutto il lavoro, chiudere la richiesta per indicare che è considerata completata. Altre informazioni sulla [generazione di report](subject-rights-requests-reports.md) in modo che sia possibile soddisfare e chiudere la richiesta.

## <a name="understanding-the-request-details-page"></a>Informazioni sulla pagina dei dettagli della richiesta

Selezionare **Richieste di diritti degli interessati Priva** nel riquadro di spostamento a sinistra del portale di conformità di Microsoft Purview per accedere alle richieste create dall'organizzazione e visualizzarne lo stato. Le schede di stato nella pagina principale Richieste di diritti soggetto mostrano il numero di richieste attive, chiuse e scadute e i tipi di richiesta principali. La tabella sotto le schede di stato elenca tutte le richieste create dall'organizzazione, con la richiesta creata più di recente nella parte superiore.

Per aprire la pagina dei dettagli di una richiesta, selezionare il nome della richiesta dalla tabella. Qui è possibile ottenere altre informazioni sulle proprietà della richiesta, sui risultati della ricerca e sullo stato della richiesta. Questa pagina diventerà l'hub per lavorare e collaborare alla gestione dei file trovati, alla creazione di report ed esportazioni e al completamento della richiesta.

### <a name="overview-tab"></a>Scheda Panoramica

La scheda **Panoramica** della pagina dei dettagli della richiesta fornisce dettagli sulla richiesta, un indicatore di stato che mostra il passaggio corrente e informazioni chiave sui dati trovati. Questa pagina contiene le singole schede di stato illustrate di seguito.

##### <a name="details"></a>Dettagli

La scheda **Dettagli** visualizza le informazioni di base per orientarti verso la richiesta, ad esempio la scadenza, la data di creazione, la descrizione e il relativo regolamento sulla privacy.

##### <a name="progress"></a>Progresso

La scheda **Stato** elenca ogni passaggio del processo: stima dei dati, recupero dei dati, revisione dei dati, generazione di report e chiusura della richiesta. Un cerchio blu pieno accanto al passaggio indica il passaggio attualmente in corso. Un segno di spunta all'interno del cerchio blu indica che il passaggio è completo. Un cerchio vuoto vuoto indica che il passaggio non è ancora stato avviato.

##### <a name="data-estimate-summary"></a>Riepilogo della stima dei dati

La scheda **Riepilogo stima dati** viene visualizzata quando la richiesta viene sospesa nella [fase di stima dei dati](subject-rights-requests-data-retrieval.md#data-estimate). Mostra la posizione e il numero di elementi che la ricerca dovrebbe recuperare.

##### <a name="total-number-of-items-found"></a>Numero totale di elementi trovati

La scheda **Numero totale di elementi trovati** visualizza il numero di elementi di contenuto trovati e le relative posizioni in Microsoft 365.

##### <a name="priority-items-to-review"></a>Elementi di priorità da esaminare

Il riquadro **Elementi di priorità da rivedere** mostra gli elementi che è possibile assegnare priorità all'avvio della revisione. Il riquadro visualizza un conteggio degli elementi appartenenti alle categorie seguenti:
- **Riservato**: a questi elementi è applicata [un'etichetta di riservatezza Microsoft](/microsoft-365/compliance/sensitivity-labels) . Ad esempio, un documento di Word con un'etichetta "Altamente riservato". 
- **Dati multi-persona**: questi elementi contengono i dati personali di più persone. Se si desidera includere questi elementi come parte del pacchetto di dati finale, è necessario redigere i dati irrilevanti nei file. Ottenere [informazioni dettagliate sulla revisione dei dati](subject-rights-requests-data-review.md). Per consentire a Priva di identificare gli elementi con dati multi-persona, l'organizzazione deve configurare la [corrispondenza dei dati per le richieste di diritti degli interessati](subject-rights-requests-data-match.md).

**Come individuare gli elementi di priorità:**

Prima di tutto, assicurarsi di aver abilitato la visualizzazione nella tabella di elementi **Raccolta** dati seguendo la procedura seguente:

- Nella scheda **Dati raccolti** selezionare **Personalizza colonne** nella parte superiore dell'elenco di elementi.
- Nel riquadro a comparsa **Modifica colonne** posizionare un controllo accanto a **Tipi di priorità**.
- Selezionare **Applica**. L'elenco di elementi avrà ora una colonna **Tipi di priorità** .

È ora possibile identificare gli elementi di priorità e trovarli ordinando la colonna **Tipo di priorità** per raggruppare tipi simili.

### <a name="data-collected-tab"></a>Scheda Dati raccolti

Quando tutti gli elementi corrispondenti alle impostazioni di ricerca sono stati identificati, vengono raccolti e presentati nella scheda **Dati raccolti** . Accanto all'elenco di elementi è visualizzata una schermata di anteprima per esaminare ogni elemento, apportare modifiche e contrassegnare gli elementi come inclusi o esclusi come parte della richiesta. Altre informazioni sulla [revisione dei dati e sul passaggio di collaborazione](subject-rights-requests-data-review.md).

### <a name="notes-tab"></a>Scheda Note

La scheda **Note** consente ai collaboratori di immettere note sul lavoro svolto nella richiesta. Queste note sono visibili a tutti gli utenti che lavorano alla richiesta, ma non verranno incluse nel report finale o condivise in altro modo con l'interessato.

### <a name="collaborators-tab"></a>Scheda Collaboratori

Nella scheda Collaboratori vengono visualizzati tutti gli utenti che sono stati invitati a collaborare ai dati raccolti e qualsiasi canale Teams associato per la richiesta. L'autore della richiesta viene automaticamente elencato come collaboratore. Invitare nuovi collaboratori selezionando il comando **Aggiungi collaboratore** e immettendo il nome di un utente per selezionarli da un elenco. Altre informazioni sulla [collaborazione per la revisione dei dati](subject-rights-requests-data-review.md#collaboration-for-data-review)

### <a name="reports-tab"></a>Scheda Report

Nella scheda **Report** vengono visualizzati tutti i report generati automaticamente quando si passa alla fase **Genera report** . I report sono suddivisi in due categorie: i report da condividere con l'interessato e i report destinati all'uso interno dell'organizzazione. Ottenere informazioni dettagliate [sull'uso dei report](subject-rights-requests-reports.md).

### <a name="history-tab"></a>Scheda Cronologia

La scheda **Cronologia** riepiloga gli eventi di primo livello per la richiesta, incluse le modifiche alla fase di avanzamento e le aggregazioni per il numero di elementi inclusi, esclusi e redatti.

## <a name="next-steps"></a>Passaggi successivi

Per informazioni su come ottenere informazioni sulla prima richiesta, vedere [Creare una richiesta di diritti per l'oggetto](subject-rights-requests-create.md) .

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)
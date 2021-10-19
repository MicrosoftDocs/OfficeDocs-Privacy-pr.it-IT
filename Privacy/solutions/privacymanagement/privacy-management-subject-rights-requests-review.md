---
title: Esaminare i dati e collaborare alle richieste di diritti dell'oggetto nella gestione della privacy
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: Scopri come esaminare i dati delle richieste di diritti dell'oggetto raccolti dalla gestione della privacy e collaborare al completamento della richiesta.
ms.openlocfilehash: 7f0754007c70ef7836abf13ec0dbd50e9d9c8958
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478250"
---
# <a name="review-data-and-collaborate-on-subject-rights-requests"></a>Esaminare i dati e collaborare alle richieste di diritti dell'oggetto

Dopo aver creato una richiesta per i diritti dell'oggetto[(](privacy-management-subject-rights-requests-create.md)ulteriori informazioni), la gestione della privacy utilizzerà gli input sull'oggetto per cercare corrispondenze nell'ambiente Microsoft 365'organizzazione. Dopo aver compilato questi dati, è possibile esaminare i risultati, effettuare scelte sugli elementi da includere e redigere le informazioni in base alle esigenze. Questi passaggi possono essere collaborati da più utenti tramite l'interfaccia di gestione della privacy.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Passaggio 1: esaminare i dettagli della richiesta e monitorare lo stato

Per visualizzare i risultati iniziali della ricerca, passare all'area di gestione della privacy del Centro conformità Microsoft 365 [e](https://compliance.microsoft.com/) aprire Richieste di diritti **dell'oggetto.** In questa pagina principale è disponibile un elenco di tutte le richieste di diritti dell'oggetto aperte.

Seleziona la richiesta nell'elenco per visualizzare i dettagli della richiesta. Qui puoi trovare altre informazioni sulle proprietà della richiesta, sui risultati della ricerca e sullo stato della richiesta. Questa pagina diventerà il tuo hub per lavorare e collaborare alla gestione dei file trovati, alla creazione di report ed esportazioni e al completamento della richiesta.

I riquadri nella pagina dei dettagli della richiesta includono:

- **Dettagli**: dettagli essenziali sulla richiesta, inclusa la data di scadenza e la data della richiesta, la descrizione e la normativa sulla privacy correlata.
- **Progress**: sequenza temporale che indica i passaggi completati e tutte le attività ancora da completare.
- Statistiche sulla fase di avanzamento corrente. Questo riquadro può mostrare informazioni come un riepilogo della stima dei dati, il numero di elementi trovati nella ricerca e le relative posizioni in Microsoft 365 o lo stato delle esportazioni.
- **Elementi con priorità da esaminare:** questo riquadro mostrerà informazioni sugli elementi importanti rilevati automaticamente dalla gestione della privacy. Ad esempio, questo potrebbe includere informazioni riservate che già recano un'etichetta di riservatezza Microsoft o elementi con dati su più utenti che potrebbero richiedere una redazione. Ciò consente agli amministratori di sapere dove iniziare la revisione. Gli elementi di priorità sono disponibili in Dati raccolti filtrando in base alla colonna "Tipi di priorità".

### <a name="understand-progress-stages"></a>Comprendere le fasi di avanzamento

Le richieste di diritti dell'oggetto vengono sottoposte a più fasi. Alcuni avanzano automaticamente quando la gestione della privacy esegue la valutazione dei dati e altri avanzano quando gli amministratori e i collaboratori richiedono diritti dell'oggetto completano passaggi essenziali come la revisione, la selezione e la redazione dei file.

Dal momento che potrebbe essere necessario lavorare sulle richieste nel tempo o da più collaboratori, la gestione della privacy fornisce continui aggiornamenti sullo stato e indicazioni sui passaggi successivi da eseguire. Questi aggiornamenti possono essere visualizzati nella pagina panoramica della richiesta di diritti dell'oggetto.

1. **Stima dei dati:** dopo la creazione di una richiesta, la gestione della privacy identifica gli elementi che includono potenziali corrispondenze all'oggetto dei dati e annota le loro posizioni in Microsoft 365. Al termine della stima dei dati, si avanzerà automaticamente per recuperare i dati **,** a meno che non si siano verificati errori o la richiesta non sia impostata per la sospensione qui per la revisione dell'amministratore.
   - La richiesta potrebbe essere impostata per richiedere la revisione dell'amministratore in questa fase. Se l'amministratore determina che i risultati iniziali della query di ricerca sono soddisfacenti, è possibile procedere al recupero dei dati. Se si desidera apportare modifiche prima di procedere, è possibile scegliere di modificare prima la query di ricerca. Per informazioni dettagliate, vedere passaggio 2. Non sarà possibile modificare la query di ricerca dopo aver avviato la fase di recupero dei dati.
   - Se la query di ricerca restituisce una stima dei dati di grandi dimensioni, ovvero è al di sopra della soglia consigliata per la gestione della privacy per le dimensioni o il conteggio dei file, è possibile provare a rivedere la ricerca per affinare l'ambito. Tieni presente che i file associati a un elemento corrispondente (ad esempio, i file allegati in un messaggio di posta elettronica) possono essere conteggiati per il totale. Le stime dei dati superiori al massimo della stima dei dati di grandi dimensioni richiederanno una revisione della ricerca per procedere.
1. **Recupera dati**: questa fase indica che la gestione della privacy è in fase di recupero dei dati. Una volta completato, avanzerà automaticamente per esaminare **i dati.**
1. **Esaminare i** dati: in questa fase, i  collaboratori devono esaminare i risultati nella scheda Dati raccolti ed eseguire tutte le attività applicabili, ad esempio la redazione, l'applicazione di tag e l'aggiunta di note. Al termine della revisione, selezionare **Completa revisione.**
1. **Generare report**: i report vengono generati in questa fase. Al termine, questi elementi sono disponibili nella **scheda** Report. I file finiti possono essere esportati per la revisione finale e la consegna all'utente che ha effettuato la richiesta.

## <a name="step-2-optional-view-and-edit-search-queries"></a>Passaggio 2 (facoltativo): visualizzare e modificare le query di ricerca

Per visualizzare informazioni dettagliate sulla ricerca di dati dietro una richiesta di diritti dell'oggetto, selezionare **Visualizza dettagli query di ricerca.** Verrà visualizzato un riquadro che riepiloga la query e mostra ulteriori dettagli su ciò che è stato trovato.

È possibile visualizzare in anteprima **i** risultati della ricerca per vedere il tipo di contenuto che verrà restituito per la query. Se si desidera modificare le proprietà di questa ricerca e non è stata avviata la fase Recupera dati, è possibile utilizzare **l'opzione Modifica query di** ricerca.

La procedura guidata modifica query di ricerca offre la possibilità di modificare o aggiungere proprietà per l'identificazione dell'oggetto dati, i filtri e le condizioni di ricerca e le posizioni in cui cercare i dati (inclusi Exchange, SharePoint, OneDrive e/o Teams). Usa queste opzioni per raggiungere il livello di specificità desiderato. È possibile esaminare la versione finale della nuova query prima di premere **Salva.**

Al termine della modifica della query di ricerca, verrà eseguita una nuova ricerca per sostituire i risultati della ricerca precedenti. In questo modo lo stato nella sezione **Stato** viene reimpostato sul primo passaggio, **Stima dati**. Il completamento della nuova ricerca può richiedere fino a 60 minuti. Al termine, vedrai i risultati aggiornati nella pagina dei dettagli della richiesta.

## <a name="step-3-review-data"></a>Passaggio 3: esaminare i dati

In questa fase, i collaboratori devono esaminare i risultati nella **scheda Dati raccolti.** Le attività essenziali includono:

1. Esaminare l'elenco degli elementi identificati e scegliere se includere ogni file nei riepiloghi e/o nelle esportazioni. Se non è necessario includere una corrispondenza segnalata, selezionare l'opzione "Escludi". Se il contenuto sembra essere un falso positivo, puoi scegliere "Non una corrispondenza" per escludere il file dai rapporti finali e contrassegnare l'elemento come elemento che non dovrebbe essere stato raccolto dalla richiesta. Per impostare lo stato di un elemento, usa il menu azione (puntini di sospensione verticali) accanto al nome e seleziona la scelta desiderata. Se richiesto, aggiungere una nota per il riferimento interno per spiegare la decisione. Le note sono necessarie quando si escludono i file.
1. Usa **l'opzione Applica** tag per identificare gli elementi che necessitano di attenzione. I tag disponibili includono le opzioni fornite dal sistema, ad esempio il tagging di un elemento per il follow-up, e possono includere tag personalizzati come definito nelle impostazioni globali.
1. Usa **Annota** per creare contrassegni in linea o modificare i dati in un file selezionato. Ad esempio, se è necessario includere un file per una persona che contiene anche le informazioni personali di altri utenti, è possibile utilizzare la **redazione area** (sotto il pulsante Disegno nella barra dei comandi) per black out tutte le informazioni che non riguardano la persona che ha effettuato la richiesta. Al termine delle modifiche, selezionare **Includi** per aggiungere il file redatto alla richiesta. L'annotazione crea una copia del file, in modo che nulla nel file originale sia modificato e rimanga nella posizione originale. La copia viene archiviata nel BLOB di Azure.
1. Per rivedere le note su un elemento, selezionarlo e passare alla **scheda Note** file. Puoi anche usare **l'opzione Aggiungi nota file** per creare un nuovo commento. Per rivedere o aggiungere note a livello di caso generale, passare alla scheda **Note** principale sopra e usare **Aggiungi nota caso.** Queste note saranno visibili agli utenti che lavorano alla richiesta, ma non verranno incluse nel report finale o condivise in altro modo con l'oggetto dei dati.
1. Dopo aver esaminato tutti gli elementi e impostato i relativi stati, selezionare **Completa revisione.** Verrà aperto un riquadro a comparsa in cui è possibile esaminare un riepilogo dei dati e aggiungere eventuali note rilevanti. Queste note sono per la conservazione dei record interni e non vengono condivise con l'oggetto dei dati.
1. Selezionare di nuovo Completa revisione per continuare. I riepiloghi delle decisioni verranno forniti in un secondo momento nella **scheda** Report.

### <a name="collaborate-on-data-review"></a>Collaborare alla revisione dei dati

La gestione della privacy supporta la collaborazione Microsoft Teams per consentire al gruppo di collaborare alle richieste di diritti dell'oggetto. Quando crei una nuova richiesta, per impostazione Teams viene creato automaticamente un canale di Teams associato alla richiesta. Qui puoi discutere la richiesta e condividere in modo sicuro input e contributi. Per partecipare alla conversazione, apri la richiesta e usa **l'opzione Chat con i** collaboratori. Verrà aperta la Microsoft Teams e verrà posizionata all'interno del canale Generale per il sito del team della richiesta di diritti dell'oggetto.

Per esaminare l'elenco dei collaboratori attivi che possono visualizzare e contribuire al sito del team, all'interno della richiesta di diritti dell'oggetto aprire la **scheda** Collaboratori. Per aggiungere altri utenti per collaborare a questa richiesta, selezionare l'opzione **Aggiungi un collaboratore.**

Per modificare il comportamento predefinito della generazione di siti Teams durante la creazione di una richiesta di diritti dell'oggetto, passare a **Impostazioni** nella barra di spostamento superiore e selezionare Teams **collaborazione** per modificare l'impostazione.

Puoi anche usare  l'opzione Condividi in alto a destra all'interno di una richiesta di diritto dell'oggetto per eseguire un ciclo di utenti tramite Teams o posta elettronica o per copiare il collegamento alla pagina nella gestione della privacy. La condivisione tramite Teams consente di selezionare un sito e un canale di Teams esistenti disponibili per il tuo account, dove invierà un collegamento a questo caso insieme a qualsiasi messaggio fornito.

## <a name="step-4-close-the-request"></a>Passaggio 4: Chiudere la richiesta

Dopo aver eseguito tutte le azioni necessarie per risolvere la richiesta di diritti dell'oggetto, selezionare **Chiudi la richiesta.** Verrà creato il report finale, che verrà crittografato e reso disponibile nella **scheda Report.** Il completamento potrebbe richiedere del tempo a seconda del numero di file nella richiesta.

## <a name="next-steps"></a>Passaggi successivi
Per ulteriori informazioni sull'utilizzo dei report e sul completamento delle richieste di diritti [dell'oggetto,](privacy-management-subject-rights-requests-fulfill.md)vedere Fulfill subject rights requests .

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

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
ms.openlocfilehash: cac4064a1e0dc2860d061748793a91c0b86e0896
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249042"
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

Le richieste di diritti dell'oggetto vengono sottoposte a più fasi. Alcuni avanzano automaticamente mentre Priva esegue la valutazione dei dati e altri avanzano quando gli amministratori e i collaboratori richiedono diritti dell'oggetto completano passaggi essenziali come la revisione, la selezione e la redazione dei file.

Poiché potrebbe essere necessario lavorare sulle richieste nel tempo o da più collaboratori, Priva fornisce aggiornamenti continui sullo stato e indicazioni sui passaggi successivi da eseguire. Questi aggiornamenti possono essere visualizzati nella pagina panoramica della richiesta di diritti dell'oggetto.

1. **Data estimate**: After a request is created, Priva identifies items that include potential matches to your data subject and makes notes of their locations in Microsoft 365. Al termine della stima dei dati, avanzerai automaticamente per recuperare i **dati, a** meno che non si siano verificati errori o la richiesta non sia impostata per la sospensione qui per la revisione dell'amministratore.
   - La richiesta potrebbe essere impostata per richiedere la revisione dell'amministratore in questa fase. Se l'amministratore determina che i risultati iniziali della query di ricerca sono soddisfacenti, è possibile procedere al recupero dei dati. Se si desidera apportare modifiche prima di procedere, è possibile scegliere di modificare prima la query di ricerca. Per informazioni dettagliate, vedere passaggio 2. Non sarà possibile modificare la query di ricerca dopo aver avviato la fase di recupero dei dati.
   - Se la query di ricerca restituisce una stima dei dati di grandi dimensioni, ovvero è superiore alla soglia consigliata di Priva per le dimensioni o il conteggio dei file, è possibile provare a rivedere la ricerca per affinare l'ambito. Tieni presente che i file associati a un elemento corrispondente (ad esempio, i file allegati in un messaggio di posta elettronica) potrebbero essere conteggiati per il totale. Le stime dei dati superiori al massimo della stima dei dati di grandi dimensioni richiederanno una revisione della ricerca per procedere.
1. **Recuperare i** dati: questa fase indica che Priva è in fase di recupero dei dati. Al termine, avanzerà automaticamente per esaminare **i dati**.
1. **Esaminare i** dati: in questa fase, i collaboratori devono esaminare i risultati nella scheda  Dati raccolti ed eseguire tutte le attività applicabili come la redazione, l'applicazione di tag e l'aggiunta di note. Al termine della revisione, selezionare **Completa revisione**.
1. **Generare report**: i report vengono generati in questa fase. Al termine, questi elementi sono disponibili nella **scheda** Report. I file finiti possono essere esportati per la revisione finale e la consegna all'utente che ha effettuato la richiesta.

## <a name="step-2-optional-view-and-edit-search-queries"></a>Passaggio 2 (facoltativo): visualizzare e modificare le query di ricerca

Per visualizzare informazioni dettagliate sulla ricerca di dati alla base di una richiesta di diritti dell'oggetto, selezionare **Visualizza dettagli query di ricerca**. Verrà visualizzato un riquadro che riepiloga la query e mostra ulteriori dettagli su ciò che è stato trovato.

È possibile visualizzare in **anteprima i risultati** della ricerca per vedere il tipo di contenuto che verrà restituito per la query. Se si desidera modificare le proprietà di questa ricerca e non è stata avviata la fase Recupera dati, è possibile utilizzare **l'opzione Modifica query di** ricerca.

La procedura guidata modifica query di ricerca consente di modificare o aggiungere proprietà per l'identificazione dell'oggetto dati, i filtri e le condizioni di ricerca e le posizioni in cui cercare i dati (inclusi Exchange, SharePoint, OneDrive e/o Teams). Usa queste opzioni per raggiungere il livello di specificità desiderato. È possibile esaminare la versione finale della nuova query prima di premere **Salva**.

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

Priva supporta la collaborazione tramite Microsoft Teams per consentire al gruppo di collaborare sulle richieste di diritti dell'oggetto. Quando crei una nuova richiesta, per impostazione Teams viene creato automaticamente un canale di Teams associato alla richiesta. Qui puoi discutere la richiesta e condividere in modo sicuro input e contributi. Per partecipare alla conversazione, apri la richiesta e usa **l'opzione Chat con i** collaboratori. Verrà aperta la Microsoft Teams e verrà posizionata nel canale Generale per il sito del team della richiesta di diritti dell'oggetto.

Per esaminare l'elenco dei collaboratori attivi che possono visualizzare e contribuire al sito del team, all'interno della richiesta di diritti dell'oggetto aprire la **scheda** Collaboratori. Per aggiungere altri utenti per collaborare a questa richiesta, selezionare l'opzione **Aggiungi un collaboratore**.

Per modificare il comportamento predefinito della generazione di siti Teams durante la creazione di una richiesta di diritti dell'oggetto, passare a **Impostazioni** nella barra di spostamento superiore e selezionare Teams **collaborazione** per modificare l'impostazione.

Puoi anche usare l'opzione Condividi in alto a destra all'interno di una richiesta a destra dell'oggetto per eseguire un ciclo di utenti tramite Teams o posta elettronica o per copiare il collegamento alla pagina in Priva. La condivisione tramite Teams consente di selezionare un sito e un canale di Teams esistenti disponibili per il tuo account, dove invierà un collegamento a questo caso insieme a qualsiasi messaggio fornito.

## <a name="step-4-close-the-request"></a>Passaggio 4: Chiudere la richiesta

Dopo aver eseguito tutte le azioni necessarie per risolvere la richiesta di diritti dell'oggetto, selezionare **Chiudi la richiesta**. Verrà creato il report finale, che verrà crittografato e reso disponibile nella **scheda Report**. Il completamento potrebbe richiedere del tempo a seconda del numero di file nella richiesta.

## <a name="next-steps"></a>Passaggi successivi
Per ulteriori informazioni sull'utilizzo dei report e sul completamento delle richieste di diritti dell'oggetto, vedere [Generare report ed eseguire una richiesta di diritti dell'oggetto](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

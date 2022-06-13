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
ms.openlocfilehash: 0182be22efe224481625c121dc98ebe1d96a06ec
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046630"
---
# <a name="review-data-for-a-subject-rights-request"></a>Esaminare i dati per una richiesta di diritti dell'interessato

**Questo articolo** illustra come esaminare i dati raccolti per una richiesta di diritti dell'interessato usando strumenti di redazione, tag file. Informazioni su come usare la funzionalità di collaborazione, che include un canale Teams dedicato.

Dopo aver raccolto i dati per una richiesta di diritti dell'interessato, la fase successiva consiste nel esaminare gli elementi di contenuto, decidere quali elementi includere o escludere come parte della richiesta e, se necessario, redigere le informazioni.

## <a name="tasks-for-completing-the-data-review"></a>Attività per il completamento della revisione dei dati

In questa fase, i collaboratori devono esaminare i risultati nella scheda **Dati raccolti**. Verrà automaticamente configurato un canale Teams per facilitare la revisione dei contenuti da parte di tutti gli stakeholder. Per altri dettagli, vedere [Collaborazione per la revisione dei dati](#collaboration-for-data-review) riportata di seguito. Le attività essenziali per il passaggio di revisione dei dati sono descritte di seguito.

#### <a name="mark-items-as-include-or-exclude-and-add-notes"></a>Contrassegnare gli elementi come Includi o Escludi e aggiungere note

Esaminare l'elenco degli elementi identificati restituiti dalla ricerca. Se si decide di includere l'elemento come parte del report finale all'interessato, selezionare **Includi** sulla barra dei comandi nella parte superiore dell'elenco di elementi. È anche possibile selezionare il pulsante blu **Includi** nell'area di revisione del contenuto a destra dell'elenco di elementi. Quando si seleziona **Includi**, viene visualizzato un riquadro a comparsa con un'opzione per aggiungere note. Al termine, selezionare **Invia** per salvare lo stato di revisione dell'elemento come **Includi**.

Se l'elemento non appartiene come parte della richiesta, selezionare **Escludi** sulla barra dei comandi o il pulsante **Escludi** nell'area di revisione del contenuto. L'esclusione di un elemento significa che non verrà inclusa nei [report finali generati per l'interessato](subject-rights-requests-reports.md).

> [!NOTE]
> Se contrassegni un elemento come **Escludi**, devi aggiungere una nota come giustificazione per il motivo per cui non riguarda la richiesta di diritti dell'oggetto. Le note sono per scopi interni e non sono incluse nei report finali.

Se il contenuto sembra essere un falso positivo, selezionare **Non corrisponde** e nel riquadro a comparsa selezionare **Conferma**. Questa azione escluderà il file dai report finali e contrassegnerà l'elemento come qualcosa che non avrebbe dovuto essere rilevato nella ricerca.

#### <a name="apply-tags"></a>Applicazione di tag

I tag possono essere usati per identificare gli elementi che richiedono ulteriore attenzione. Priva fornisce tre tag predefiniti, **ovvero Completamento**, **Eliminazione** e **Aggiornamento**, per i quali è possibile impostare una descrizione. Priva fornisce anche due tag personalizzati che è possibile denominare e descrivere.

Ad esempio, se durante la verifica dei dati si determina che un elemento di contenuto non deve essere conservato dall'organizzazione, è possibile applicare il tag **Elimina** , quindi esportare un elenco di tutti i file con tag in modo da poter tornare indietro ed eliminare gli elementi identificati al termine della richiesta.

I cinque tag gestiti in **Impostazioni** si applicano a tutte le richieste di diritti dell'oggetto.

**Per aggiungere o rimuovere tag:**

- Selezionare l'elemento dall'elenco nella scheda **Dati raccolti** della richiesta.
- Nell'area di anteprima dell'elemento a destra dell'elenco selezionare il pulsante **Applica tag** nella riga inferiore. È anche possibile selezionare i tre punti a destra del nome dell'elemento e selezionare l'opzione **Applica tag** .
- Viene visualizzato un riquadro a comparsa con l'elenco di tag. Selezionare la casella accanto a uno dei tag da applicare all'elemento. Se si deseleziona una casella selezionata, il tag verrà rimosso.
- Al termine, selezionare **Salva**, che salva le selezioni dei tag e chiude il riquadro a comparsa.

**Per aggiungere tag personalizzati o aggiornare le descrizioni dei tag:**
- Nella pagina Richieste diritti soggetto selezionare **Impostazioni** nell'angolo superiore destro della schermata per accedere alle impostazioni di Priva.
- Passare alla pagina **Tag di revisione dei dati** e selezionare il tag per immettere una descrizione e, per i tag personalizzati, un nome. Altre informazioni sulle [impostazioni dei tag](priva-settings.md#data-review-tags).

**Per esportare un elenco di elementi con tag:**
- Passare alla pagina **Dati raccolti** in una richiesta di diritti dell'interessato.
- Sopra l'elenco di elementi selezionare il comando **Esporta** .
- Verrà scaricato un file Excel che mostra le proprietà per tutti gli elementi raccolti dalla ricerca della richiesta. Trovare la colonna **Tag** per identificare e ordinare gli elementi in base al tag.

#### <a name="use-the-annotate-command-to-redact-text"></a>Usare il comando Annota per redigere il testo
Il comando **Annota** nell'area di revisione del contenuto consente di creare mark-up inline e redact dati all'interno di un elemento di contenuto. Ad esempio, se è necessario includere un file per un utente che contiene anche le informazioni personali di un altro interessato, è possibile utilizzare la **modifica dell'area** sotto il pulsante Disegno nella barra dei comandi per oscurare tutte le informazioni che non riguardano la persona che ha effettuato la richiesta. Al termine delle modifiche, selezionare **Includi** per aggiungere il file redacted alla richiesta. L'annotazione crea una copia del file, che viene archiviata nel BLOB di Azure. Il file originale rimane inalterato e archiviato nel percorso originale.

#### <a name="enter-notes-about-a-file"></a>Immettere note su un file
Per aggiungere o rivedere note su un elemento, selezionare l'elemento dalla relativa riga e passare alla scheda **Note file** nell'area di revisione del contenuto a destra. È anche possibile usare l'opzione **Aggiungi nota file** per creare un nuovo commento. Per esaminare o aggiungere note a livello di caso generale, passare alla scheda **Note** principale precedente e usare **Aggiungi nota caso**. Queste note saranno visibili agli utenti che lavorano alla richiesta, ma non saranno incluse nel report finale o altrimenti condivise con l'interessato.

## <a name="collaboration-for-data-review"></a>Collaborazione per la revisione dei dati

Gli amministratori delle richieste di diritti dell'oggetto possono visualizzare tutte le richieste. È possibile aggiungere altri utenti per collaborare a una richiesta, che consentirà loro di visualizzare tale richiesta e lavorare con i dati raccolti al suo interno per facilitare lo spostamento della richiesta al completamento.

Quando si crea una richiesta, viene creato automaticamente un canale di Teams dedicato per gli stakeholder per discutere della richiesta e condividere in modo sicuro input e contributi. La scheda **Collaboratori** nella pagina dei dettagli della richiesta mostra tutti i collaboratori che possono visualizzare e contribuire alla richiesta e a qualsiasi canale Teams associato.

Per aggiungere altri collaboratori, selezionare **Aggiungi collaboratore**, iniziare a digitare il nome dell'utente, selezionare il nome una volta visualizzato e quindi selezionare **Aggiungi**.

Per avviare una chat Teams, qualsiasi collaboratore può selezionare **Chat con i collaboratori** in alto a destra nella pagina dei dettagli della richiesta. Questa azione si apre Teams e inserisce l'utente nel canale **Generale** per il sito del team della richiesta di diritti dell'oggetto.

È possibile modificare il comportamento predefinito della creazione di canali Teams per le richieste di diritti dell'oggetto passando a Priva **Impostazioni** nell'angolo in alto a destra di Richiesta diritti soggetto. Selezionare **Teams collaborazione**, quindi deselezionare la casella nella pagina per disattivare le funzionalità di Teams per tutti i requst di diritti dell'oggetto.

Il comando **Condividi** in alto a destra nella pagina dei dettagli di una richiesta crea un collegamento condivisibile che passa direttamente alla richiesta in Priva. Assegnare questo collegamento ai collaboratori in modo che possano accedere alla richiesta a cui sono stati aggiunti.

## <a name="complete-the-review"></a>Completare la revisione

Quando tutti gli elementi sono stati esaminati e il relativo stato è stato impostato su **Includi**, **Escludi** o **Non corrisponde,** è il momento di chiudere il passaggio di revisione. Qualsiasi collaboratore su una richiesta può completare la revisione.

Selezionare il pulsante **Completa revisione** nell'angolo in alto a destra della richiesta. Un riquadro a comparsa mostrerà un riepilogo dei dati e aggiungerà eventuali note correlate. Queste note sono destinate alla conservazione interna dei record e non vengono condivise con l'interessato.

Selezionare **Completa revisione** nel riquadro a comparsa per completare il passaggio di revisione. Questa azione prepara la richiesta per le fasi finali del processo: generazione di report e chiusura della richiesta. I riepiloghi delle decisioni verranno forniti più avanti nella scheda **Report** .

## <a name="next-steps"></a>Passaggi successivi
Informazioni su come generare il report finale e lavorare per il completamento della richiesta in [Generare report e chiudere una richiesta](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)

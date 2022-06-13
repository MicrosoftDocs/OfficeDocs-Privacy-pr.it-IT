---
title: Stima e recupero dei dati nelle richieste di diritti dell'interessato
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
description: Informazioni su come vengono recuperati i dati e su come modificare le impostazioni di ricerca in Richieste di diritti degli interessati Microsoft Priva.
ms.openlocfilehash: 9d35a7f37861d7d3ecc5d1bac7db92c75939b4c3
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046733"
---
# <a name="data-estimate-and-retrieval"></a>Stima e recupero dei dati

**In questo articolo**: Comprendere la stima dei dati e le fasi di recupero dei dati di una richiesta di diritti dell'interessato. Informazioni su come visualizzare la query di ricerca di una richiesta e apportare modifiche per perfezionare la ricerca.

## <a name="data-estimate"></a>Stima dei dati
Dopo aver creato una richiesta, Priva inizia immediatamente a cercare corrispondenze con l'interessato nel contenuto all'interno dell'ambiente Microsoft 365. Dopo aver identificato tutti gli elementi che riteniamo corrispondono ai criteri, la stima verrà visualizzata nella scheda **Riepilogo stima dati** nella pagina **Panoramica** della richiesta. La quantità di dati nell'ambito della ricerca influirà sul tempo necessario per completare la stima.

La richiesta passerà automaticamente alla fase successiva del **recupero dei dati**, in cui tutti gli elementi di contenuto vengono raccolti insieme per consentire agli stakeholder di collaborare alla revisione dei dati. In alcuni casi, la stima dei dati verrà sospesa prima di passare al recupero e verrà visualizzata una notifica dei passaggi successivi da eseguire prima di continuare.

### <a name="pause-in-data-estimate"></a>Sospendere la stima dei dati

Esistono due motivi per cui una richiesta verrà sospesa nella fase **di stima dei dati** :

1. Quando si crea una richiesta per la prima volta, è possibile scegliere di ottenere prima una stima. Per informazioni dettagliate, vedere il passaggio 5 in [Creare una richiesta](subject-rights-requests-create.md#create-a-request) .

2. Se si prevede che la stima restituisca un numero elevato di elementi da esaminare (oltre 10.000 elementi), il flusso di lavoro viene sospeso. A questo punto è possibile visualizzare in anteprima i risultati e decidere se [modificare la query di ricerca](subject-rights-requests-create.md#refining-your-search) o continuare a recuperare gli elementi identificati.

Quando la richiesta viene sospesa in **Data estimate**, verrà visualizzata una scheda nella pagina dei dettagli della richiesta con informazioni di riepilogo sul numero di elementi, il volume, la relativa posizione e un collegamento che consente di **visualizzare i dettagli della query di ricerca**.

![Scheda di stima dei dati.](../media/priva-srr-data-estimate.png)

## <a name="view-and-edit-search-queries"></a>Visualizzare e modificare le query di ricerca

Per visualizzare informazioni dettagliate sulla ricerca della richiesta, selezionare **Visualizza i dettagli della query di ricerca** nella scheda **Riepilogo stima dati** . Viene aperto un riquadro a comparsa che riepiloga la query e mostra altri dettagli sugli elementi trovati. Da qui sono disponibili le opzioni seguenti:

- Selezionare **Anteprima risultati** per ottenere un'anteprima del tipo di contenuto che verrà restituito nelle impostazioni di ricerca correnti.
- Selezionare **Modifica query di ricerca** per modificare le impostazioni di ricerca.

Quando si seleziona **Modifica query di ricerca**, si verrà guidati attraverso un processo guidato per modificare o aggiungere proprietà per identificare l'interessato, modificare le condizioni e modificare le posizioni che si vuole coprire la ricerca. Per informazioni più dettagliate, seguire le istruzioni riportate in [Affinamento della ricerca](subject-rights-requests-create.md#refining-your-search) . È possibile esaminare la versione finale della nuova query di ricerca, quindi selezionare **Salva** per avviare di nuovo la ricerca.

Verrà generata una nuova stima e lo stato della richiesta tornerà alla **stima dei dati**. Il completamento della nuova ricerca potrebbe richiedere fino a 60 minuti. Al termine, verranno visualizzati i risultati aggiornati nella pagina dei dettagli della richiesta.

Quando si è pronti per procedere, selezionare Recupera **dati** in alto a destra dello schermo per passare alla fase di recupero dei dati.

## <a name="retrieve-data"></a>Recuperare i dati

La fase di recupero dei dati si verifica quando vengono recuperati tutti i file, i messaggi di posta elettronica, le chat, le immagini e altri elementi di contenuto contenenti i dati personali dell'interessato. Gli elementi vengono raggruppati in un contenitore di archiviazione BLOB di Azure per la revisione. Il recupero dei dati può richiedere alcuni minuti o molto più a seconda del volume di dati.

Al termine di questa fase, la richiesta passa automaticamente alla fase successiva di **Revisione dei dati**.

## <a name="next-steps"></a>Passaggi successivi

Visitare [Esaminare i dati per una richiesta di diritti dell'interessato](subject-rights-requests-data-review.md) per informazioni sulle attività principali e collaborare con gli stakeholder per **il passaggio Rivedi i dati** .

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)
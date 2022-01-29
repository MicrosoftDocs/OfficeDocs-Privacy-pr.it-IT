---
title: Trovare e visualizzare i dati personali in Microsoft Priva
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
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: Informazioni sulla panoramica e sul profilo dati in Priva e su come ottenere informazioni dettagliate sui dati personali nell'ambiente Microsoft 365 aziendale.
ms.openlocfilehash: 57064821a1c118b955d1f5380886a349263c845c
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249023"
---
# <a name="find-and-visualize-personal-data-in-microsoft-priva"></a>Trovare e visualizzare i dati personali in Microsoft Priva

Microsoft Priva consente di comprendere i dati archiviati dall'organizzazione automatizzando l'individuazione delle risorse di dati personali e fornendo visualizzazioni delle informazioni essenziali. Queste visualizzazioni sono disponibili nelle pagine di **panoramica e** **del profilo** dati. È possibile agire in base alle informazioni dettagliate qui per rafforzare il livello di privacy dell'organizzazione e ridurre i rischi.

Per iniziare, passare alla sezione Priva del [Centro conformità Microsoft 365](https://compliance.microsoft.com/) e visualizzare queste pagine:

- **Panoramica**: offre una visualizzazione generale dei dati dell'organizzazione in Microsoft 365. Gli amministratori della privacy possono monitorare le tendenze e le attività, identificare e analizzare i potenziali rischi che coinvolgono dati personali e approfondire attività chiave come la gestione dei criteri o le azioni di richiesta dei diritti dell'oggetto.
- **Profilo dati**: fornisce uno snapshot dei dati personali archiviati dall'organizzazione in Microsoft 365. Questa pagina consente di visualizzare dove si trova la vita dei dati personali, quali tipi sono i più diffusi nell'organizzazione e quanti tipi diversi esistono in diverse posizioni nell'ambiente Microsoft 365 locale. È inoltre possibile esplorare i dati personali da questa posizione.

Quando i dati cambiano e Priva apporta nuovi risultati, le informazioni visualizzate in queste pagine verranno aggiornate. Si noti che potrebbero essere necessario fino a 24 ore prima che i nuovi dati siano rappresentati nei grafici.

## <a name="explore-the-overview-page"></a>Esplorare la pagina di panoramica

La pagina di panoramica è costituita da tre sezioni principali. I riquadri nella parte superiore della pagina forniscono statistiche recenti essenziali sui dati. La sezione informazioni chiave offre opportunità di indagine sulle tendenze e sulle aree di interesse chiave. Per ulteriori informazioni sull'ambiente dati, consultare i grafici delle linee di tendenza. Per ulteriori informazioni su queste aree, vedere le sezioni seguenti.

![Pagina panoramica di esempio.](../media/priva-overview.png)

### <a name="top-tiles"></a>Riquadri principali

#### <a name="policy-matches-over-past-7-days"></a>Corrispondenze dei criteri negli ultimi 7 giorni

Quando i criteri vengono impostati in Priva Privacy Risk Management, i dati verranno valutati in base ai criteri per determinate condizioni che potrebbero presentare rischi per la privacy. Le corrispondenze dei criteri indicano le individuazioni di dati che potrebbero richiedere ulteriori revisioni o correzioni. Questo riquadro mostra il numero di corrispondenze dei criteri verificatesi negli ultimi sette giorni. Le corrispondenze verranno eseguiti in questa sezione indipendentemente dal fatto che i criteri siano attivi o in esecuzione in modalità di test, in modo da poter visualizzare i risultati di tutti i criteri attivi. Selezionando questo riquadro si passa a una visualizzazione filtrata della pagina Criteri  di Gestione dei rischi per la privacy, che mostra i criteri che hanno avuto una corrispondenza negli ultimi sette giorni.

#### <a name="items-with-personal-data"></a>Elementi con dati personali

Per vedere le funzionalità di individuazione automatica di Priva sul lavoro, esamina il riquadro **Elementi con dati** personali. Questo riquadro mostra quanti nuovi elementi contenenti dati personali in base alle impostazioni sono stati individuati nell'ambiente di Microsoft 365 dell'organizzazione negli ultimi sette giorni. Selezionando questo riquadro verrà caricata una visualizzazione dei 100 elementi più recenti individuati.

#### <a name="subject-rights-requests"></a>Richieste di diritti dell'oggetto

La pagina di panoramica include un riquadro che mostra quante richieste di diritti oggetto sono state create negli ultimi sette giorni. Un secondo riquadro, se applicabile, mostra il numero di richieste scadute in base alle scadenze designate e potrebbe richiedere un'attenzione immediata. La selezione di questi riquadri consente agli utenti con le autorizzazioni appropriate di accedere alla pagina di richiesta dei diritti dell'oggetto priva.

### <a name="key-insights"></a>Informazioni dettagliate chiave

#### <a name="content-items-with-the-most-personal-data"></a>Elementi di contenuto con la maggior parte dei dati personali

I contenuti che contengono una grande quantità di dati personali possono presentare un rischio maggiore di esposizione. È possibile esaminare tali elementi per assicurarsi che siano coperti da un criterio di gestione dei rischi per la privacy. Per attirare l'attenzione di questi elementi, la pagina di panoramica fornisce una visualizzazione degli elementi di contenuto che contengono la maggior parte dei dati personali in base alle impostazioni. Qui è possibile visualizzare il numero di tipi di dati personali univoci rilevati, il numero di proprietari di contenuti univoci identificati e il numero di soggetti di dati identificati in base alle impostazioni di corrispondenza dei dati per le richieste di diritti dell'oggetto.

Selezionare **Visualizza riepilogo** per una visualizzazione riepilogata degli elementi trovati. Puoi anche scegliere di esplorare **questi risultati** per visualizzare l'anteprima di singoli file. Questa visualizzazione mostra un massimo di 100 elementi. Gli utenti nel gruppo di ruoli Gestione privacy possono selezionare i file per esaminare i dettagli e determinare la pertinenza ed esportare l'elenco in .csv per riferimento.

#### <a name="policies-with-the-most-matches-in-the-last-week"></a>Criteri con il maggior numero di corrispondenze nell'ultima settimana

Questa panoramica mostra quali criteri sono stati corrispondenti con maggiore frequenza negli ultimi sette giorni, in modalità "Attiva" o "Test". Aiuta a illustrare le prestazioni dei criteri e gli effetti del lavoro in corso mentre gli utenti Priva affinano i loro comportamenti di privacy.

Selezionare **Visualizza riepilogo** per un riepilogo dei primi 10 criteri corrispondenti e dei proprietari di contenuto del contenuto associato. Verrà inoltre visualizzato il numero di notifiche utente inviate a causa delle corrispondenze dei criteri e del numero di azioni eseguite dall'utente. Selezionare **Analizza** per visualizzare la pagina Criteri in Gestione dei rischi per la privacy, filtrata per visualizzare i criteri dalla visualizzazione riepilogo. Questa visualizzazione di indagine mostrerà le statistiche per l'intera durata del criterio. Selezionalo per visualizzare i dettagli, ad esempio quando gli elementi corrispondenti sono stati inizialmente rilevati.

#### <a name="users-with-the-most-policy-matched-in-the-last-week"></a>Utenti con il maggior numero di criteri corrispondenti nell'ultima settimana

Queste informazioni trattano anche le corrispondenze dei criteri in modalità "Test" o "Attiva". Consente di visualizzare un riepilogo degli utenti con il maggior numero di corrispondenze di criteri nell'ultima settimana e dei criteri corrispondenti. Sono inclusi i totali dei proprietari di contenuto univoci, le notifiche inviate a questi utenti e il numero di azioni eseguite da tali notifiche. Selezionando **Analizza** si visualizza la pagina dei criteri, filtrata per visualizzare i criteri dalla visualizzazione riepilogo. Nella visualizzazione investigativa non sono disponibili informazioni sull'utente, ma è possibile selezionare un criterio per visualizzare i dettagli dei criteri correlati a queste corrispondenze.

#### <a name="items-with-the-most-data-subject-content"></a>Elementi con la maggior parte del contenuto dell'oggetto dati

Questa panoramica fa riferimento alle informazioni della funzionalità di corrispondenza dei dati nelle richieste di diritti dell'oggetto e fa riferimento agli elementi di contenuto individuati all'interno di Microsoft 365 che contengono la maggior parte degli interessati. Per ulteriori informazioni su tale impostazione, vedere [Informazioni sulle richieste di diritti dell'oggetto](subject-rights-requests.md).

Questi elementi consentono di confermare la configurazione di corrispondenza dei dati e di ridurre i rischi per la privacy correlati a questi elementi. Selezionare **Visualizza riepilogo** per una visualizzazione di riepilogo. Selezionare **Esplora** per una visualizzazione dettagliata di un massimo di 100 di questi elementi. Qui puoi visualizzare in anteprima questi elementi e determinare la pertinenza ed esportare l'elenco .csv formato.

### <a name="trendline-graphs"></a>Grafici delle linee di tendenza

Per le visualizzazioni dinamiche delle tendenze presenti nei dati dell'organizzazione, consultare i grafici delle linee di tendenza. Questi grafici possono essere filtrati in base a caratteristiche quali intervalli di tempo, tipo di dati o posizioni dei dati. Usa gli elenchi a discesa forniti per modificare la visualizzazione. Posizionando il puntatore del mouse sulle linee del grafico, è possibile visualizzare le statistiche relative a quel punto specifico nel tempo.

I risultati relativi ai criteri includeranno i dati dei criteri sia in modalità "Test" che in modalità "Attiva". Se non sono attivi criteri di un determinato tipo, i grafici correlati non mostreranno alcun risultato.

#### <a name="active-policy-alerts"></a>Avvisi dei criteri attivi

In quest'area viene visualizzato uno snapshot degli avvisi attivi attivati dalle corrispondenze dei criteri. Nel corso del tempo, questa visualizzazione consente di rilevare più facilmente anomalie come picchi di volume di grandi dimensioni. Selezionare **Visualizza avvisi** per passare alla pagina dei criteri in Gestione dei rischi per la privacy, in cui è possibile analizzare ulteriormente gli avvisi e creare problemi per la correzione.

#### <a name="personal-data-found-in-organization"></a>Dati personali trovati nell'organizzazione

Questo grafico mostra le tendenze relative alla quantità di dati personali che corrispondono alle impostazioni individuate nel tempo nell'ambiente Microsoft 365 e dove si trovano. Inizierà la compilazione dopo che Priva è stato eseguito per un periodo di tempo sufficiente e dopo che il contenuto con i dati personali è stato trovato all'interno di SharePoint, OneDrive, Teams e/o Exchange.

#### <a name="data-transfers-detected-in-organization"></a>Trasferimenti di dati rilevati nell'organizzazione

Questo grafico è correlato ai criteri di trasferimento dei dati. Fornisce una visualizzazione del modo in cui i dati si spostano all'interno dell'organizzazione, tra reparti o tra aree geografiche per organizzazioni multi-geografiche.

#### <a name="unused-personal-data"></a>Dati personali inutilizzati

Questo grafico è correlato ai criteri di minimizzazione dei dati. Fornisce informazioni dettagliate sul modo in cui l'organizzazione archivia contenuto contenente dati personali e su come i criteri possono migliorare la gestione di tali dati nel tempo.

#### <a name="overexposed-personal-data"></a>Dati personali sovraesposizione

Questo grafico è correlato ai criteri di sovraesposizione dei dati. Può essere utile per identificare i comportamenti di condivisione nel tempo all'interno dell'organizzazione e delle posizioni in cui il contenuto con dati personali potrebbe essere sovraesposizione, ad esempio condividendo pubblicamente, condiviso con un utente esterno o ampiamente condiviso all'interno dell'organizzazione.

#### <a name="subject-rights-requests-by-regulation"></a>Richieste di diritti dell'oggetto per regolamento

Questa visualizzazione fornisce informazioni dettagliate sulle normative che più spesso guidano le richieste di diritti dell'oggetto nel tempo. La legenda di questo grafico mostra i nomi delle normative di tendenza. Posizionando il puntatore del mouse sulle linee di tendenza, verranno visualizzati i totali delle richieste di diritti dell'oggetto aperte per tale regolamento durante il periodo selezionato.

#### <a name="subject-rights-requests-by-status"></a>Richieste di diritti dell'oggetto per stato

Questo grafico mostra le attività dell'organizzazione per il completamento delle richieste di diritti dell'oggetto, suddivise in richieste **attive, chiuse** o **scadute**. I risultati qui disponibili possono essere utili per indicare dove è possibile trarre vantaggio dall'allocazione di più risorse alla chiusura delle richieste e alla riunione degli obiettivi.

### <a name="additional-data-views"></a>Visualizzazioni dati aggiuntive

#### <a name="subject-rights-requests-at-a-glance"></a>Richieste di diritti dell'oggetto a colpo d'occhio

Questa visualizzazione offre una visualizzazione di alto livello delle richieste di diritti dell'oggetto attive, incluso il tempo rimanente per completare le richieste entro le scadenze. Riepiloga il numero totale di richieste, quante sono attive e quante sono chiuse. Selezionare **Visualizza tutte le richieste** per passare alla pagina delle richieste di diritti dell'oggetto, in cui è possibile visualizzare ulteriori dettagli e lavorare sulle richieste attive per completarle.

#### <a name="subject-rights-requests-by-residency"></a>Richieste di diritti dell'oggetto per residenza

Questa visualizzazione mappa consente di visualizzare il volume di richieste di diritti dell'oggetto in base alla residenza degli interessati. Passando il puntatore del mouse su una bolla verrà identificata l'area geografica e il totale delle richieste di diritti dell'oggetto aperte per conto dei residenti.

## <a name="explore-the-data-profile-page"></a>Esplorare la pagina del profilo dati

La pagina del profilo dati in Priva offre una visualizzazione snapshot dei dati personali archiviati dall'organizzazione in Microsoft 365 e dove si trova. Fornisce inoltre informazioni dettagliate sui tipi di dati archiviati. I riquadri principali includono quanto segue.

![Pagina del profilo dati di esempio.](../media/priva-dataprofile.png)

### <a name="personal-data-type-instances-detected-in-microsoft-365"></a>Istanze del tipo di dati personali rilevate in Microsoft 365

Questo riquadro consente di visualizzare la quantità di dati personali presenti nell'ambiente di Microsoft 365 in base alle impostazioni e alla modalità di distribuzione dei dati tra Exchange, OneDrive, SharePoint e Teams.

Il grafico a barre mostra il conteggio approssimativo aggregato delle istanze del tipo di dati personali univoche trovate all'interno del contenuto. Esempi di tipi di dati possono includere elementi come i numeri di carta di credito e i numeri di previdenza sociale. Pertanto, un file individuato contenente tre numeri di carta di credito e un numero di previdenza sociale conterrà due tipi di dati personali univoci e quattro istanze. La parte inferiore di questo riquadro mostra i tipi di dati personali univoci all'interno di ogni Microsoft 365 posizione. Fornisce una visualizzazione della diversità dei tipi di dati personali rilevati nel contenuto dell'organizzazione.

### <a name="top-personal-data-types-across-your-organization"></a>Principali tipi di dati personali all'interno dell'organizzazione

Questo riquadro fornisce uno snapshot dei principali tipi di dati personali rilevati nell'ambiente, insieme a informazioni sul numero di elementi che contengono tale tipo di dati personali e in quali posizioni.

### <a name="personal-data-type-instances-by-region"></a>Istanze del tipo di dati personali per area geografica

Per ambienti multi-geografici, questo riquadro aggrega a livello regionale le istanze del tipo di dati personali presenti all'interno del contenuto, in base alle aree in cui è ospitato il contenuto. Per le organizzazioni con un'unica area geografica, questo riquadro mostrerà un punto che rappresenta la posizione Microsoft 365 geografica. Passando il puntatore del mouse sui punti sulla mappa verrà visualizzato il conteggio approssimativo delle istanze del tipo di dati personali individuate in tale area.

### <a name="exploring-content"></a>Esplorazione del contenuto

Selezionando **Esplora** in qualsiasi riquadro del profilo dati verrà aperto Esplora contenuto. Al momento, non è possibile cercare un elemento di contenuto specifico e i dati Teams in questa visualizzazione. Ciò significa che i numeri all'interno di Esplora contenuto potrebbero non corrispondere ai numeri visualizzati nella pagina del profilo dati, poiché la pagina del profilo dati include Teams contenuto. Gli amministratori della privacy che desiderano ulteriori approfondimenti sui propri dati sulla privacy possono farlo qui in base al tipo di dati personali (tipo di informazioni riservate) o in base alla posizione (Exchange, OneDrive o SharePoint).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

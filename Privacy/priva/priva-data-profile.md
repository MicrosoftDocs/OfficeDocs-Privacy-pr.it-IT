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
description: Informazioni sulla panoramica e sul profilo dati in Priva e su come ottenere informazioni dettagliate sui dati personali nell'ambiente Microsoft 365 dell'organizzazione.
ms.openlocfilehash: 13a27fde86abf87fa4c08528f41976fdc58fe02f
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930597"
---
# <a name="find-and-visualize-personal-data-in-microsoft-priva"></a>Trovare e visualizzare i dati personali in Microsoft Priva

Microsoft Priva consente di comprendere i dati archiviati dall'organizzazione automatizzando l'individuazione degli asset di dati personali e fornendo visualizzazioni di informazioni essenziali. Queste visualizzazioni sono disponibili nelle pagine **di panoramica** e **profilo dati** . È possibile agire sulle informazioni dettagliate qui per rafforzare il comportamento di privacy dell'organizzazione e ridurre i rischi.

Per iniziare, passare alla sezione Priva del portale di [conformità di Microsoft Purview](https://compliance.microsoft.com/) e visualizzare queste pagine:

- **Panoramica**: fornisce una visualizzazione complessiva dei dati dell'organizzazione in Microsoft 365. Gli amministratori della privacy possono monitorare tendenze e attività, identificare e analizzare i potenziali rischi che coinvolgono i dati personali e springboard in attività chiave come la gestione dei criteri o le azioni di richiesta dei diritti degli interessati.
- **Profilo dati**: fornisce uno snapshot dei dati personali archiviati dall'organizzazione in Microsoft 365. Questa pagina consente di visualizzare la posizione in cui si trovano i dati personali, i tipi più diffusi nell'organizzazione e il numero di tipi diversi esistenti tra le posizioni nell'ambiente Microsoft 365. È anche possibile esplorare i dati personali da questa posizione.

Man mano che i dati cambiano e Priva crea nuovi risultati, le informazioni visualizzate in queste pagine verranno aggiornate. Si noti che potrebbero essere richieste fino a 24 ore prima che i nuovi dati vengano rappresentati nei grafici.

## <a name="explore-the-overview-page"></a>Esplorare la pagina di panoramica

La pagina di panoramica è costituita da tre sezioni principali. I riquadri nella parte superiore della pagina forniscono statistiche recenti essenziali sui dati. La sezione informazioni dettagliate chiave offre opportunità investigative su tendenze e aree di interesse principale. Per altre informazioni sull'ambiente dati, vedere i grafici delle linee di tendenza. Per altre informazioni su queste aree, vedere le sezioni seguenti.

![Pagina di panoramica di esempio.](../media/priva-overview.png)

### <a name="top-tiles"></a>Riquadri principali

#### <a name="policy-matches-over-past-7-days"></a>Corrispondenze dei criteri negli ultimi 7 giorni

Quando i criteri vengono impostati in Priva Privacy Risk Management, i dati verranno valutati in base ai criteri per determinate condizioni che potrebbero presentare rischi per la privacy. Le corrispondenze dei criteri indicano individuazioni di dati che potrebbero richiedere ulteriori verifiche o correzioni. Questo riquadro mostra il numero di corrispondenze di criteri che si sono verificate negli ultimi sette giorni. Le corrispondenze verranno visualizzate qui indipendentemente dal fatto che i criteri siano attivi o in esecuzione in modalità di test, in modo da poter visualizzare i risultati di tutti i criteri attivi. Se si seleziona questo riquadro, verrà visualizzata una visualizzazione filtrata della pagina **Criteri** di Gestione dei rischi per la privacy, che mostra i criteri che hanno avuto una corrispondenza negli ultimi sette giorni.

#### <a name="items-with-personal-data"></a>Elementi con dati personali

Per visualizzare le funzionalità di individuazione automatizzata di Priva sul lavoro, vedere il riquadro **Elementi con dati personali** . Questo riquadro mostra quanti nuovi elementi contenenti dati personali in base alle impostazioni sono stati individuati nell'ambiente Microsoft 365 dell'organizzazione negli ultimi sette giorni. Selezionando questo riquadro verrà caricata una visualizzazione dei 100 elementi più recenti individuati.

#### <a name="subject-rights-requests"></a>Richieste di diritti dell'interessato

La pagina di panoramica include un riquadro che mostra il numero di richieste di diritti dell'oggetto create negli ultimi sette giorni. Un secondo riquadro, se applicabile, mostra il numero di richieste scadute in base alle scadenze designate e potrebbe richiedere un'attenzione immediata. Se si selezionano questi riquadri, gli utenti avranno le autorizzazioni appropriate per la pagina di richiesta dei diritti dell'oggetto di Priva.

### <a name="key-insights"></a>Informazioni dettagliate chiave

#### <a name="content-items-with-the-most-personal-data"></a>Elementi di contenuto con i dati più personali

Il contenuto che contiene una grande quantità di dati personali può presentare un rischio maggiore di esposizione. È possibile esaminare tali elementi per assicurarsi che siano coperti da un'informativa sulla gestione dei rischi per la privacy. Per aumentare l'attenzione di questi elementi, la pagina di panoramica fornisce una visualizzazione degli elementi di contenuto che contengono la maggior parte dei dati personali in base alle impostazioni. Qui è possibile visualizzare il numero di tipi di dati personali univoci rilevati, il numero di proprietari di contenuti univoci identificati e il numero di interessati identificati in base alle impostazioni di corrispondenza dei dati per le richieste di diritti degli interessati.

Selezionare **Visualizza riepilogo** per una visualizzazione di riepilogo degli elementi trovati. È anche possibile scegliere **di esplorare** questi risultati per visualizzare in anteprima i singoli file. Questa visualizzazione mostra un massimo di 100 elementi. Gli utenti del gruppo di ruoli Gestione privacy possono selezionare i file per esaminare i dettagli e determinare la pertinenza ed esportare l'elenco in formato .csv per riferimento.

#### <a name="policies-with-the-most-matches-in-the-last-week"></a>Criteri con il maggior numero di corrispondenze nell'ultima settimana

Questa panoramica illustra quali criteri sono stati confrontati più frequentemente negli ultimi sette giorni, in modalità "On" o "Testing". Consente di illustrare le prestazioni dei criteri e gli effetti del lavoro in corso man mano che gli utenti Priva affinano i comportamenti di privacy.

Selezionare **Visualizza riepilogo** per un riepilogo dei primi 10 criteri corrispondenti e dei proprietari del contenuto associato. Si vedrà anche quante notifiche utente sono state inviate a causa di queste corrispondenze di criteri e il numero di azioni eseguite dall'utente. Selezionare **Analizza** per visualizzare la pagina Criteri in Gestione dei rischi per la privacy, filtrata per visualizzare i criteri dalla visualizzazione di riepilogo. Questa visualizzazione investigativa mostrerà le statistiche per l'intera durata dei criteri. Selezionarlo per visualizzare i dettagli, ad esempio quando sono stati rilevati inizialmente elementi corrispondenti.

#### <a name="users-with-the-most-policy-matched-in-the-last-week"></a>Utenti con il maggior numero di criteri corrispondenti nell'ultima settimana

Queste informazioni dettagliate corrispondono anche alle corrispondenze dei criteri in modalità "Test" o "Attivato". Consente di visualizzare un riepilogo degli utenti con il maggior numero di corrispondenze di criteri nell'ultima settimana e i criteri corrispondenti. Sono inclusi i totali dei proprietari di contenuti univoci, le notifiche inviate a questi utenti e il numero di azioni eseguite da tali notifiche. Se si seleziona **Analizza** , si passa alla pagina dei criteri, filtrati per visualizzare i criteri dalla visualizzazione di riepilogo. Nella visualizzazione investigativa le informazioni sull'utente non vengono trovate, ma è possibile selezionare un criterio per visualizzare i dettagli dei criteri correlati a queste corrispondenze.

#### <a name="items-with-the-most-data-subject-content"></a>Elementi con la maggior parte del contenuto dell'interessato

Queste informazioni dettagliate fanno riferimento alle informazioni della funzionalità di corrispondenza dei dati nelle richieste di diritti degli interessati e visualizzano gli elementi di contenuto individuati all'interno di Microsoft 365 che contengono la maggior parte degli interessati. Per altre informazioni su questa impostazione, vedere [Informazioni sulle richieste di diritti dell'oggetto](subject-rights-requests.md).

Questi elementi consentono di confermare la configurazione della corrispondenza dei dati e di attenuare i rischi per la privacy correlati a questi elementi. Selezionare **Visualizza riepilogo** per una visualizzazione di riepilogo. Selezionare **Esplora** per una visualizzazione dettagliata di un massimo di 100 di questi elementi. Qui è possibile visualizzare in anteprima questi elementi e determinare la pertinenza ed esportare l'elenco in formato .csv.

### <a name="trendline-graphs"></a>Grafici delle linee di tendenza

Per le visualizzazioni dinamiche delle tendenze rilevate nei dati dell'organizzazione, consultare i grafici delle linee di tendenza. Questi grafici possono essere filtrati in base a caratteristiche come intervalli di tempo, tipo di dati o posizioni dei dati. Usare gli elenchi a discesa forniti per modificare la visualizzazione. Il passaggio del mouse sulle righe nel grafico consentirà di visualizzare le statistiche correlate a quel punto specifico nel tempo.

I risultati correlati ai criteri includeranno i dati dei criteri in modalità "Test" e "Attivato". Se non sono attivi criteri di un determinato tipo, i grafici correlati non visualizzeranno alcun risultato.

#### <a name="active-policy-alerts"></a>Avvisi dei criteri attivi

Questa area mostra uno snapshot degli avvisi attivi attivati dalle corrispondenze dei criteri. Nel corso del tempo, questa visualizzazione consente di rilevare più facilmente anomalie come picchi di volume elevati. Selezionare **Visualizza avvisi** per passare alla pagina criteri in Gestione rischi per la privacy, in cui è possibile analizzare ulteriormente gli avvisi e creare problemi per la correzione.

#### <a name="personal-data-found-in-organization"></a>Dati personali trovati nell'organizzazione

Questo grafico mostra le tendenze relative alla quantità di dati personali corrispondenti alle impostazioni individuate nel tempo nell'ambiente Microsoft 365 e nella posizione in cui si trovano. Inizierà a popolamento dopo che Priva è in esecuzione da tempo sufficiente e dopo che i contenuti con dati personali sono stati trovati all'interno di SharePoint, OneDrive, Teams e/o Exchange.

#### <a name="data-transfers-detected-in-organization"></a>Trasferimenti di dati rilevati nell'organizzazione

Questo grafico è correlato ai criteri di trasferimento dei dati. Offre una panoramica del trasferimento dei dati all'interno dell'organizzazione, tra reparti o tra aree per organizzazioni multi-geografiche.

#### <a name="unused-personal-data"></a>Dati personali inutilizzati

Questo grafico è correlato ai criteri di minimizzazione dei dati. Fornisce informazioni dettagliate sul modo in cui l'organizzazione archivia contenuti contenenti dati personali e su come i criteri possono migliorare la gestione di questi dati nel tempo.

#### <a name="overexposed-personal-data"></a>Dati personali sovraesposti

Questo grafico è correlato ai criteri di sovraesposizione dei dati. Può aiutare a identificare i comportamenti di condivisione nel tempo all'interno dell'organizzazione e le posizioni in cui il contenuto con dati personali può essere sovraesposto, ad esempio condividendo pubblicamente, condiviso con un utente esterno o condiviso ampiamente all'interno dell'organizzazione.

#### <a name="subject-rights-requests-by-regulation"></a>Richieste di diritti dell'interessato da parte della regolamentazione

Questa visualizzazione fornisce informazioni dettagliate sulle normative che determinano maggiormente le richieste di diritti dell'oggetto nel tempo. La legenda di questo grafico mostra i nomi delle normative di tendenza. Passando il puntatore del mouse sulle righe di tendenza verranno visualizzati i totali delle richieste di diritti dell'oggetto aperte per tale regolamento durante il periodo di tempo selezionato.

#### <a name="subject-rights-requests-by-status"></a>Richieste di diritti dell'oggetto in base allo stato

Questo grafico mostra come l'organizzazione sta completando le richieste di diritti dell'oggetto, suddivise in richieste **attive**, **chiuse** o **scadute**. I risultati qui possono aiutare a indicare dove è possibile trarre vantaggio dall'allocazione di più risorse per chiudere le richieste e soddisfare gli obiettivi.

### <a name="additional-data-views"></a>Visualizzazioni dati aggiuntive

#### <a name="subject-rights-requests-at-a-glance"></a>Richieste di diritti soggetto a colpo d'occhio

Questa visualizzazione offre una visione generale delle richieste di diritti soggetti attivi, incluso il tempo rimanente per completare le richieste in base alle scadenze. Riepiloga il numero totale di richieste, il numero di richieste attive e il numero di richieste chiuse. Selezionare **Visualizza tutte le richieste** per passare alla pagina relativa alla richiesta di diritti dell'oggetto, in cui è possibile visualizzare altri dettagli e lavorare sulle richieste attive per eseguirle fino al completamento.

#### <a name="subject-rights-requests-by-residency"></a>Richieste di diritti dell'oggetto per residenza

Questa visualizzazione mappa consente di visualizzare il volume di richieste di diritti dell'interessato in base alla residenza degli interessati. Passando il puntatore su una bolla si identificherà l'area e il totale delle richieste di diritti dell'oggetto aperte per conto dei residenti.

## <a name="explore-the-data-profile-page"></a>Esplorare la pagina del profilo dati

La pagina del profilo dati in Priva offre una visualizzazione snapshot dei dati personali archiviati dall'organizzazione in Microsoft 365 e dove si trovano. Fornisce anche informazioni dettagliate sui tipi di dati archiviati. I riquadri principali includono quanto segue.

![Pagina del profilo dati di esempio.](../media/priva-dataprofile.png)

### <a name="personal-data-type-instances-detected-in-microsoft-365"></a>Istanze del tipo di dati personali rilevate in Microsoft 365

Questo riquadro consente di visualizzare la quantità di dati personali presenti nell'ambiente Microsoft 365 in base alle impostazioni e alla modalità di distribuzione dei dati in Exchange, OneDrive, SharePoint e Teams.

Il grafico a barre mostra il conteggio aggregato approssimativo delle istanze univoche del tipo di dati personali trovate all'interno del contenuto. Esempi di tipi di dati possono includere elementi come i numeri di carta di credito e i numeri di previdenza sociale. Pertanto, un file individuato che contiene tre numeri di carta di credito e un numero di previdenza sociale conterrà due tipi di dati personali univoci e quattro istanze. La parte inferiore di questo riquadro mostra i tipi di dati personali univoci all'interno di ogni posizione Microsoft 365. Fornisce una visualizzazione della diversità dei tipi di dati personali rilevati nel contenuto dell'organizzazione.

### <a name="top-personal-data-types-across-your-organization"></a>Tipi di dati personali principali nell'organizzazione

Questo riquadro fornisce uno snapshot dei principali tipi di dati personali rilevati nell'ambiente, insieme alle informazioni sul numero di elementi che contengono tale tipo di dati personali e in quali posizioni.

### <a name="personal-data-type-instances-by-region"></a>Istanze del tipo di dati personali per area

Per gli ambienti multi-geo, questo riquadro aggrega a livello di area le istanze del tipo di dati personali presenti nel contenuto, in base alle aree in cui è ospitato il contenuto. Per le organizzazioni a area singola, questo riquadro mostrerà un punto che rappresenta la posizione Microsoft 365. Passando il puntatore del mouse sui punti sulla mappa verrà visualizzato il conteggio approssimativo delle istanze del tipo di dati personali individuate in tale area.

### <a name="exploring-content"></a>Esplorazione del contenuto

Se si seleziona **Esplora** in qualsiasi riquadro del profilo dati, verrà aperto esplora contenuto. Al momento, non è possibile cercare un elemento di contenuto specifico e non verranno visualizzati Teams dati in questa visualizzazione. Ciò significa che i numeri all'interno di Esplora contenuto potrebbero non corrispondere ai numeri visualizzati nella pagina del profilo dati, poiché la pagina del profilo dati include Teams contenuto. Gli amministratori della privacy che desiderano ulteriori informazioni sui dati sulla privacy possono farlo qui in base al tipo di dati personali (tipo di informazioni riservate) o alla posizione (Exchange, OneDrive o SharePoint).

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

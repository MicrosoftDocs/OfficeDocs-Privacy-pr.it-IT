---
title: Generare report per soddisfare una richiesta di diritti dell'oggetto
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
description: Informazioni su come gestire i pacchetti di dati creati da Microsoft Priva per le richieste di diritti dell'interessato e soddisfare la richiesta all'interessato.
ms.openlocfilehash: 999de2aecefab2c1685967d197839fbb72938f8a
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851662"
---
# <a name="generate-reports-to-fulfill-a-subject-rights-request"></a>Generare report per soddisfare una richiesta di diritti dell'oggetto

Dopo aver completato la verifica dei dati per una richiesta di diritti dell'interessato in Microsoft Priva, è possibile procedere per soddisfare la richiesta. Priva creerà report e raccoglierà i file contrassegnati come **Includi** durante il processo di revisione dei dati. I file selezionati da questi pacchetti di dati possono essere inviati all'interessato per completare la richiesta.

## <a name="understanding-reports"></a>Informazioni sui report

Dopo aver selezionato **Completa revisione** nella fase **Di revisione dei dati** della richiesta di diritti dell'interessato, i report finali per la richiesta inizieranno a generare automaticamente. Nella scheda **Report** della pagina dei dettagli delle richieste di diritti dell'oggetto, la colonna **Stato** indica quando è **in corso** la generazione del report e quando un report è **pronto per il download**. La creazione dei report può richiedere fino a 30 minuti.

I report sono suddivisi in due sezioni:
1. **Report per l'interessato**: questi report contengono informazioni che possono essere restituite all'interessato come parte dell'evasione della richiesta. Qui è possibile trovare il **pacchetto di dati** contenente i file da inviare all'interessato.
   > [!IMPORTANT]
   > Verrà generato un pacchetto di dati solo se gli elementi vengono contrassegnati come **Includi** durante la revisione dei dati.

   > [!IMPORTANT]
   > Verrà generato un pacchetto di dati solo per i tipi di richieste **di esportazione** e **accesso** . Non verrà generato un pacchetto di dati per un **elenco con tag per la richiesta di completamento** . Esaminare i dettagli sui [tipi di richiesta di diritti dell'oggetto](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard).

2. **Report per uso interno**: questi report si riferiscono ai record interni dell'organizzazione correlati alla richiesta di diritti dell'oggetto. Includono un log di controllo e un elenco di tutti i file a cui sono stati applicati i tag durante la revisione dei dati per completare o intraprendere ulteriori azioni.

> [!NOTE]
> Quando vengono generati report, l'organizzazione completa la richiesta inviando i report appropriati in modo sicuro all'interessato per soddisfare la richiesta di diritti dell'interessato. Se l'interessato ha richiesto l'eliminazione dei dati, è responsabilità dell'organizzazione identificare gli elementi da eliminare ed eseguire l'eliminazione.

## <a name="data-package"></a>Pacchetto di dati

Il pacchetto di dati della richiesta di diritti dell'interessato contiene elementi contrassegnati come **Include** durante la fase di revisione dei dati del processo. Il pacchetto di dati viene generato come file ZIP. Quando è pronto per il download, selezionare la riga del report nella scheda **Report** della pagina dei dettagli della richiesta di diritti dell'oggetto. Verrà aperto un pannello a comparsa con un pulsante per **scaricare** il report. Le istruzioni **sulle operazioni successive** nel riquadro a comparsa forniscono un riferimento rapido su come usare il contenuto.

Quando si è pronti per scaricare il pacchetto di dati, selezionare **Scarica**, trovare il download e quindi aprire il file ZIP scaricato.

### <a name="contents-of-the-data-package"></a>Contenuto del pacchetto di dati

Il file ZIP del pacchetto di dati contiene gli elementi seguenti:

- Una cartella denominata **Azure**: questa cartella contiene i materiali chiave per l'interessato. Vedere la spiegazione dettagliata seguente.
- File esterni alla cartella di **Azure** : questi possono includere due fogli di calcolo denominati **Risultati** e **Riepilogo**. Questi file all'esterno della cartella di Azure vengono forniti come riferimento e devono essere usati principalmente dagli amministratori dell'organizzazione.

Quando Priva identifica e recupera i file per una richiesta di diritti dell'interessato, i file esportati in questo processo vengono rinominati usando identificatori univoci per proteggere i dati personali. È possibile fare riferimento incrociato ai nomi univoci con i nomi di file originali usando il file **Export_load_file.csv** . Poiché i nomi di file originali possono includere informazioni riservate, è necessario seguire i criteri applicati a tali informazioni.

> [!NOTE]
> È consigliabile esaminare attentamente il contenuto di questa cartella e inviare solo i file necessari all'interessato. È consigliabile valutare la risposta per assicurarsi che sia personalizzata per soddisfare i requisiti della legge applicabile.

### <a name="azure-folder-contents"></a>Contenuto della cartella di Azure

Aprire la cartella **di Azure** , quindi aprire il file **AEDExport.zip** , che contiene un'altra cartella di file con un nome lungo costituito da numeri e lettere. Aprire la cartella con il nome lungo per visualizzare il contenuto descritto di seguito:

- **Extracted_text_files** cartella: contiene il testo estratto dai file nativi (dove supportato).
- **Cartella NativeFiles** : contiene tutti gli elementi contrassegnati durante la revisione dei dati come **Inclusi**, nel formato di file nativo. A ogni elemento di questa cartella viene assegnato un nome file univoco per proteggere i dati personali. È possibile fare riferimento incrociato a questi nomi univoci con il nome del file originale usando il file Export_load_file.csv, illustrato di seguito.
  - I file che sono stati redatti usando la funzione **Annotate** durante il processo di revisione dei dati si trovano nella cartella **NativeFiles** e hanno il suffisso "_burn.pdf".
- **Export_load_file.csv** file: contiene i nomi di file originali in modo che sia possibile farvi riferimento incrociato con i nomi di file univoci specificati nella cartella NativeFiles.
- File di testo **di riepilogo**: fornisce un riepilogo dei tipi di file nel pacchetto di dati, il numero di file e le relative dimensioni.

##### <a name="what-to-do-with-the-folder-contents"></a>Operazioni da eseguire con il contenuto della cartella

Aprire la cartella **di Azure** e i file ZIP come illustrato in precedenza. L'attività successiva consiste nell'esaminare gli elementi, determinare cosa inviare all'interessato e modificare il contenuto del file ZIP, se necessario.

Ad esempio, per una richiesta di esportazione in cui l'interessato vuole ricevere una copia di tutti gli elementi contenenti i dati personali contenuti nell'organizzazione, è consigliabile esaminare attentamente gli elementi nella cartella **NativeFiles** e rimuovere qualsiasi elemento che non si vuole inviare all'interessato.

Per una richiesta di accesso in cui l'interessato vuole ricevere un riepilogo di tutte le informazioni personali contenute nell'organizzazione, è necessario concentrarsi sul file di testo **Riepilogo** .

Modificare il file ZIP per rimuovere qualsiasi contenuto che non si vuole includere nel pacchetto finale. Al termine, inviare il file ZIP in modo sicuro all'interessato che ha effettuato la richiesta di diritti dell'interessato.

## <a name="audit-log"></a>Log di controllo

Il log di controllo è un file CSV che fornisce un record della progressione delle fasi per ogni richiesta di diritti dell'oggetto. Elenca ogni fase del processo insieme alla data e all'ora completate e al nome utente dell'utente che ha completato il passaggio.

## <a name="tagged-files-reports"></a>Report di file con tag

I report etichettati come **File contrassegnati come...** sono file CSV che elencano gli elementi di contenuto a cui sono stati applicati i tag durante il processo di revisione dei dati. I tag vengono usati per contrassegnare gli elementi di contenuto per un'ulteriore attenzione o azione da parte dell'organizzazione. Altre informazioni sulle [impostazioni per i tag](priva-settings.md#data-review-tags).

## <a name="retention-periods-for-reports-and-data"></a>Periodi di conservazione per report e dati

I report generati dalle richieste di diritti dell'interessato e dai dati associati, ad esempio i file con annotazioni salvati in Azure, vengono archiviati per un periodo di tempo specificato. Il periodo di conservazione predefinito è di 30 giorni dalla data in cui viene chiusa una richiesta di diritti dell'oggetto.

Il periodo di conservazione dei dati è definito in Priva **Impostazioni** e si applica a tutte le richieste di diritti dell'interessato. Per visualizzare o modificare il periodo di conservazione dei dati, seguire questa procedura:

1. In qualsiasi punto della Richieste di diritti degli interessati Priva selezionare **Impostazioni** (icona a ingranaggio) nell'angolo in alto a destra dello schermo.
2. Selezionare **Periodi di conservazione dei dati** nel riquadro di spostamento a sinistra.
3. Nel menu a discesa **Dati raccolti e report** selezionare 30 giorni o 90 giorni come periodo di conservazione.
4. Selezionare **Salva** per salvare le impostazioni.

Assicurarsi di verificare che i periodi di conservazione dei dati scelti siano conformi ai criteri e agli obblighi legali dell'organizzazione.

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)

---
title: Generare report ed soddisfare una richiesta di diritti dell'oggetto
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
description: Informazioni su come gestire i pacchetti di dati creati da Microsoft Priva per le richieste di diritti dell'oggetto ed eseguire la richiesta all'oggetto dei dati.
ms.openlocfilehash: a72dfb53e4f642cd2c567896c854af2beaedd416
ms.sourcegitcommit: beeb693075ef692e95d679f366301df8517b2ac3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/23/2022
ms.locfileid: "63765519"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>Generare report ed soddisfare una richiesta di diritti dell'oggetto

Dopo aver completato la revisione dei dati per una richiesta di diritti dell'oggetto in Microsoft Priva, puoi andare avanti per soddisfare la richiesta. Priva creerà report e raccoglierà i file contrassegnati come **Include** durante il processo di revisione dei dati. I file selezionati da questi pacchetti di dati possono essere inviati al soggetto dei dati per completare la richiesta. Priva supporta inoltre l'api per le richieste di diritti Microsoft 365 soggetto per introdurre funzionalità di automazione.

## <a name="understanding-reports"></a>Informazioni sui report

Dopo aver selezionato **Completa revisione** nella fase **Di** revisione dei dati della richiesta di diritti dell'oggetto, i report finali per la richiesta inizieranno a generare automaticamente. Nella scheda **Report** della pagina dei dettagli delle richieste di diritti oggetto, la colonna **Stato** indica quando la generazione del report è **in** corso e quando un report **è Pronto per il download**. La creazione dei report può richiedere fino a 30 minuti.

I report sono suddivisi in due sezioni:
1. **Report per l'oggetto dei** dati: questi report contengono informazioni che possono essere restituite all'oggetto dei dati come parte dell'evasione delle richieste. È qui che troverai il pacchetto **di dati** contenente i file da inviare all'oggetto dei dati.
   > [!IMPORTANT]
   > Un pacchetto di dati verrà generato solo se contrassegni gli elementi **come Includi durante** la revisione dei dati.

   > [!IMPORTANT]
   > Verrà generato un pacchetto di dati solo per i **tipi di** **richieste** di esportazione e accesso. Non verrà generato un pacchetto di dati per un elenco **con tag per la richiesta di follow-up** . Esaminare i dettagli sui [tipi di richieste di diritti oggetto](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard).

2. **Report per uso interno**: questi report sono relativi ai record interni dell'organizzazione correlati alla richiesta di diritti dell'oggetto. Includono un log di controllo e un elenco di tutti i file a cui sono stati applicati i tag durante la revisione dei dati per eseguire ulteriori operazioni.

> [!NOTE]
> Quando vengono generati report, l'organizzazione completa la richiesta inviando i report appropriati in modo sicuro all'oggetto dei dati per soddisfare la richiesta di diritti dell'oggetto. Se l'utente ha richiesto l'eliminazione dei propri dati, è responsabilità dell'organizzazione identificare gli elementi da eliminare ed eseguire l'eliminazione.

## <a name="data-package"></a>Pacchetto di dati

Il pacchetto di dati della richiesta di diritti dell'oggetto contiene elementi contrassegnati come **Includi** durante la fase di revisione dei dati del processo. Il pacchetto di dati viene generato come file ZIP. Quando è pronto per il download, selezionare la riga del report nella scheda **Report** della pagina dei dettagli della richiesta di diritti dell'oggetto. Verrà aperto un riquadro a comparsa con un pulsante per **scaricare** il report. Le **istruzioni sulle operazioni seguenti** nel riquadro a comparsa forniscono un riferimento rapido per l'utilizzo del contenuto.

Quando sei pronto per scaricare il pacchetto di dati, seleziona **Scarica**, trova il download e quindi apri il file ZIP scaricato.

### <a name="contents-of-the-data-package"></a>Contenuto del pacchetto di dati

Il file ZIP del pacchetto di dati contiene gli elementi seguenti:

- Una cartella denominata **Azure**: questa cartella contiene i materiali chiave per l'oggetto dei dati. Vedi la spiegazione dettagliata di seguito.
- File esterni alla **cartella di Azure** : possono includere due fogli di calcolo denominati **Risultati** e **Riepilogo**. Questi file esterni alla cartella di Azure sono forniti come riferimento e devono essere usati principalmente dagli amministratori dell'organizzazione.

Quando Priva identifica e recupera i file per una richiesta di diritti dell'oggetto, i file esportati in questo processo vengono rinominati utilizzando identificatori univoci per proteggere i dati personali. È possibile creare riferimenti incrociati ai nomi univoci con i nomi di file originali **utilizzando ilExport_load_file.csv** file. Poiché i nomi dei file originali possono includere informazioni riservate, è consigliabile seguire i criteri applicabili a tali informazioni.

> [!NOTE]
> È consigliabile esaminare attentamente il contenuto di questa cartella e inviare solo i file necessari all'oggetto dei dati. È consigliabile valutare la risposta per assicurarsi che sia personalizzata per soddisfare i requisiti della legge applicabile.

### <a name="azure-folder-contents"></a>Contenuto della cartella di Azure

Apri la **cartella di Azure** , quindi apri il file **AEDExport.zip** , che contiene un'altra cartella di file con un nome lungo costituito da numeri e lettere. Aprire la cartella con il nome lungo per visualizzare il contenuto descritto di seguito:

- **Extracted_text_files** cartella: contiene il testo estratto dai file nativi (se supportato).
- **Cartella NativeFiles** : contiene tutti gli elementi contrassegnati durante la revisione dei dati **come Inclusi**, nel formato di file nativo. A ogni elemento di questa cartella viene assegnato un nome file univoco per proteggere i dati personali. Puoi fare riferimento incrociato a questi nomi univoci con il nome del file originale usando il file Export_load_file.csv, illustrato di seguito.
  - I file che sono stati redatti utilizzando la funzione **Annotate** durante il processo di revisione dei dati si trova nella **cartella NativeFiles** e hanno il suffisso "_burn.pdf".
- **Export_load_file.csv** file: contiene i nomi di file originali in modo da poter fare riferimento incrociato con i nomi di file univoci forniti nella cartella NativeFiles.
- **File** di testo riepilogativo: fornisce un riepilogo dei tipi di file nel pacchetto di dati, del numero di file e delle relative dimensioni.

##### <a name="what-to-do-with-the-folder-contents"></a>Cosa fare con il contenuto della cartella

Apri la **cartella di Azure** e i file ZIP come spiegato in precedenza. L'attività successiva è esaminare gli elementi, determinare cosa inviare all'oggetto dati e modificare il contenuto del file ZIP, se necessario.

Ad esempio, per una richiesta di esportazione in cui l'oggetto dei dati desidera ricevere una copia di tutti gli elementi contenenti i dati personali dell'organizzazione, è necessario esaminare attentamente gli elementi nella cartella **NativeFiles** e rimuovere qualsiasi elemento che non si desidera inviare all'oggetto dei dati.

Per una richiesta di accesso in cui l'oggetto dei dati desidera ricevere un riepilogo di tutte le informazioni personali tenute dall'organizzazione, è necessario concentrarsi sul file **di testo Riepilogo** .

Modifica il file ZIP per rimuovere tutti i contenuti che non vuoi includere nel pacchetto finale. Al termine, inviare il file ZIP in modo sicuro all'oggetto dei dati che ha effettuato la richiesta di diritti dell'oggetto.

## <a name="audit-log"></a>Log di controllo

Il log di controllo è un file CSV che fornisce un record della progressione delle fasi per ogni richiesta di diritti dell'oggetto. Vengono elencate ogni fase del processo insieme alla data e all'ora di completamento e al nome utente della persona che ha completato il passaggio.

## <a name="tagged-files-reports"></a>Report di file con tag

I report etichettati come **File contrassegnati come...** sono file CSV che elencano gli elementi di contenuto a cui sono stati applicati i tag durante il processo di revisione dei dati. I tag vengono utilizzati per contrassegnare gli elementi di contenuto per un'ulteriore attenzione o azione da parte dell'organizzazione. Altre informazioni sulle [impostazioni per i tag](priva-settings.md#data-review-tags).

## <a name="retention-periods-for-reports-and-data"></a>Periodi di conservazione per report e dati

I report generati dalle richieste di diritti dell'oggetto e dai dati associati, ad esempio i file con annotazioni salvati in Azure, vengono archiviati per un periodo di tempo specificato. Il periodo di conservazione predefinito è 30 giorni dalla data in cui viene chiusa una richiesta di diritti dell'oggetto.

Il periodo di conservazione dei dati è definito in Priva **Impostazioni** e si applica a tutte le richieste di diritti dell'oggetto. Per visualizzare o modificare il periodo di conservazione dei dati, eseguire la procedura seguente:

1. Da qualsiasi punto in Priva Subject Rights Requests seleziona **Impostazioni** (l'icona a forma di ingranaggio) nell'angolo in alto a destra dello schermo.
2. Selezionare **Periodi di conservazione dei dati** nella barra di spostamento sinistra.
3. Dal menu **a discesa Dati raccolti e report** selezionare 30 o 90 giorni come periodo di conservazione.
4. Selezionare **Salva** per salvare le impostazioni.

Assicurarsi di verificare che i periodi di conservazione dei dati scelti siano conformi ai criteri e agli obblighi legali dell'organizzazione.

## <a name="integrate-with-partner-solutions"></a>Integrazione con soluzioni partner

Puoi integrare la soluzione Priva Subject Rights Requests con i processi e gli strumenti aziendali esistenti sfruttando l'API per le richieste di diritti Microsoft 365 soggetto. Questo offre un modo semplice ma potente per introdurre l'automazione nella strategia per i diritti dell'oggetto.

Quando gli interessati richiedono informazioni all'organizzazione, puoi sfruttare le API per creare tali richieste all'interno di Microsoft 365 in base ai criteri personalizzati per tale richiesta. Puoi creare la richiesta di diritti dell'oggetto in Microsoft 365, tenere traccia dell'avanzamento della richiesta attraverso le sue fasi e confermare quando la richiesta ha completato l'elaborazione e il contenuto è pronto per il recupero. Le NOSTRE API sono disponibili per tutti gli utenti per rendere le soluzioni più estensibile: che si tratta di ISV, partner che possono ospitare Microsoft 365 nelle proprie soluzioni o per le organizzazioni da usare con le applicazioni line-of-business.

Per altre informazioni, vedi [Usare l'API per la richiesta di diritti Graph microsoft](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

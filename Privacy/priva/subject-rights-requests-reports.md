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
ms.openlocfilehash: 8a6a41188de78508401b0dfffb3d7cdefb2320a5
ms.sourcegitcommit: 4965df24fdc907f7a6e397f2c78019aaf72c7580
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/17/2022
ms.locfileid: "63564446"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>Generare report ed soddisfare una richiesta di diritti dell'oggetto

Dopo aver completato la revisione dei dati per una richiesta di diritti dell'oggetto in Microsoft Priva, puoi passare alla richiesta di evasione. Priva creerà report e raccoglierà i file contrassegnati per **Include** durante il processo di revisione dei dati. I file selezionati da questi pacchetti di dati possono essere inviati al soggetto dei dati per completare la richiesta. Priva supporta inoltre l'api per le richieste di diritti Microsoft 365 soggetto per introdurre funzionalità di automazione.

## <a name="understanding-reports"></a>Informazioni sui report

Dopo aver selezionato **Completa revisione** nella fase **Di** revisione dei dati della richiesta di diritti dell'oggetto, i report finali per la richiesta inizieranno a generare automaticamente. Nella scheda **Report** della pagina dei dettagli delle richieste di diritti oggetto, la colonna **Stato** indica quando la generazione del report è **in** corso e quando un report **è Pronto per il download**. La creazione dei report può richiedere fino a 30 minuti.

I report sono suddivisi in due sezioni:
1. **Report per l'oggetto dei** dati: questi report contengono informazioni che possono essere restituite all'oggetto dei dati come parte dell'evasione delle richieste. È qui che troverai il pacchetto **di dati** contenente i file da inviare all'oggetto dei dati.
   > [!IMPORTANT]
   > Un pacchetto di dati verrà generato solo se contrassegni gli elementi **come Includi durante** la revisione dei dati.

   > [!IMPORTANT]
   > Verrà generato un pacchetto di dati solo per i **tipi di** **richieste** di esportazione e accesso. Non verrà generato un pacchetto di dati per un elenco **con tag per la richiesta di follow-up** . Esaminare i dettagli sui [tipi di richieste di diritti oggetto](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard).

2. **Report per uso interno**: questi report sono relativi ai record interni dell'organizzazione correlati alla richiesta di diritti dell'oggetto. Includono un log di controllo e un elenco di tutti i file a cui sono stati applicati i tag durante la revisione dei dati per eseguire ulteriori operazioni.

## <a name="prepare-final-reports-for-the-data-subject"></a>Preparare i report finali per l'oggetto dei dati

Il pacchetto di dati della richiesta di diritti dell'oggetto viene generato come file ZIP. La generazione del pacchetto può richiedere fino a 30 minuti. Quando è pronto, apri la richiesta di diritti dell'oggetto dalla pagina delle richieste di diritti dell'oggetto, apri la scheda Report, trova il download e apri il file ZIP.

Il pacchetto di dati contiene un insieme di file. I file esterni alla cartella di Azure vengono forniti come riferimento e devono essere usati principalmente dagli amministratori. I materiali chiave per l'oggetto dei dati sono contenuti nella **cartella azure** .

È consigliabile esaminare attentamente il contenuto di questa cartella e inviare solo i file necessari all'oggetto dei dati. È consigliabile valutare la risposta per assicurarsi che sia personalizzata per soddisfare i requisiti della legge applicabile.

### <a name="azure-folder-contents"></a>Contenuto della cartella di Azure

Apri questa cartella, quindi apri il file **AEDExport.zip** file. I contenuti includono:

- La **Extracted_text_files** contiene il testo estratto dai file nativi (se supportato).
- La **cartella NativeFiles** contiene tutti gli **elementi inclusi** nel formato di file nativo.
- I file redatti sono nella **cartella NativeFiles** e hanno il suffisso "_burn.pdf".
- I file esportati vengono rinominati utilizzando identificatori univoci per proteggere i dati personali. È possibile eseguire il cross-reference dei nomi univoci con i nomi di file originali utilizzando il metodo **Export_load_file.csv**. Poiché i nomi dei file originali possono includere informazioni riservate, è consigliabile seguire i criteri applicabili a tali informazioni.

Dopo aver esaminato il contenuto del file ZIP, modificarlo in base alle esigenze per rimuovere tutti i contenuti che non si desidera includere nel pacchetto finale. Al termine, inviarlo in modo sicuro all'oggetto dei dati.

## <a name="integrate-with-partner-solutions"></a>Integrazione con soluzioni partner

Puoi integrare la soluzione Priva Subject Rights Requests con i processi e gli strumenti aziendali esistenti usando l'API Microsoft 365 subject rights request. L'uso dell'API offre un modo semplice ma potente per introdurre l'automazione nella strategia per i diritti dell'oggetto.

Quando gli interessati richiedono informazioni all'organizzazione, le API possono contribuire a creare tali richieste entro Microsoft 365 in base ai criteri univoci della richiesta. Puoi creare la richiesta di diritti dell'oggetto in Microsoft 365, tenere traccia dell'avanzamento della richiesta attraverso le sue fasi e confermare quando la richiesta ha completato l'elaborazione e il contenuto è pronto per il recupero. Le NOSTRE API sono disponibili per tutti gli utenti per rendere le soluzioni più estensibile: che si tratta di ISV, partner che possono ospitare Microsoft 365 nelle proprie soluzioni o per le organizzazioni da usare con le applicazioni line-of-business.

Per altre informazioni, vedi [Usare l'API per la richiesta di diritti Graph microsoft](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="manage-data-retention"></a>Gestire la conservazione dei dati

I report generati tramite questo strumento e i dati associati, ad esempio i file con annotazioni salvati in Azure, vengono archiviati per un periodo di tempo specificato. Il periodo di conservazione dei dati è definito in Priva **Impostazioni** e si applica a tutte le richieste di diritti dell'oggetto. Per visualizzare o modificare i periodi di conservazione dei dati, eseguire la procedura seguente:

1. Da qualsiasi punto in Priva Subject Rights Requests seleziona **Impostazioni** (l'icona a forma di ingranaggio) nell'angolo in alto a destra dello schermo.
2. Selezionare **Periodi di conservazione dei dati** nella barra di spostamento sinistra.
3. Usando il menu a discesa, selezionare 30 o 90 giorni come periodo di conservazione.

Assicurarsi di verificare che i periodi di conservazione dei dati scelti siano conformi ai criteri e agli obblighi legali dell'organizzazione.

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

---
title: Gestire i report sulle richieste di diritti dell'oggetto e soddisfare le richieste nella gestione della privacy
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
description: Scopri come gestire i pacchetti di dati creati dalla gestione della privacy per le richieste di diritti dell'oggetto e come soddisfare la richiesta all'oggetto dei dati.
ms.openlocfilehash: 424bb4edc6ddcab86200d76cee767bc9699b281a
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478196"
---
# <a name="manage-subject-rights-requests-reports-and-fulfill-requests"></a>Gestire i report sulle richieste di diritti dell'oggetto e soddisfare le richieste

Dopo aver completato la revisione dei dati per una richiesta di diritti dell'oggetto, puoi passare alla richiesta di evasione. La gestione della privacy creerà report e raccoglierà i file contrassegnati per **Includi** durante il processo di revisione dei dati. I file selezionati da questi pacchetti di dati possono essere inviati al soggetto dei dati per completare la richiesta. La gestione della privacy supporta anche l'api per le richieste di diritti Microsoft 365 soggetto per introdurre funzionalità di automazione.

## <a name="prepare-final-reports-for-the-data-subject"></a>Preparare i report finali per l'oggetto dei dati

Il pacchetto di dati della richiesta di diritti dell'oggetto viene generato come file ZIP. La generazione del pacchetto può richiedere fino a 30 minuti. Quando è pronto, apri la richiesta di diritti dell'oggetto dalla pagina delle richieste di diritti dell'oggetto, apri la scheda Report, trova il download e apri il file ZIP. 

Il pacchetto di dati contiene un insieme di file. I file esterni alla cartella di Azure vengono forniti come riferimento e devono essere usati principalmente dagli amministratori. I materiali chiave per l'oggetto dei dati sono contenuti nella **cartella azure.**

È consigliabile esaminare attentamente il contenuto di questa cartella e inviare solo i file necessari all'oggetto dei dati. È consigliabile valutare la risposta per assicurarsi che sia personalizzata per soddisfare i requisiti della legge applicabile.

### <a name="azure-folder-contents"></a>Contenuto della cartella di Azure

Apri questa cartella, quindi apri il file **AEDExport.zip** file. I contenuti includono:

- La **Extracted_text_files** contiene testo estratto dai file nativi (se supportato).
- La **cartella NativeFiles** contiene tutti gli **elementi inclusi** nel formato di file nativo.
- I file redatti sono nella **cartella NativeFiles** e hanno il suffisso "_burn.pdf".
- I file esportati vengono rinominati utilizzando identificatori univoci per proteggere i dati personali. È possibile creare riferimenti incrociati ai nomi univoci con i nomi di file originali utilizzando il metodo **Export_load_file.csv**. Poiché i nomi dei file originali possono includere informazioni riservate, è consigliabile seguire i criteri applicabili a tali informazioni.

Dopo aver esaminato il contenuto del file ZIP, modificarlo in base alle esigenze per rimuovere qualsiasi contenuto che non si desidera includere nel pacchetto finale. Al termine, inviarlo in modo sicuro all'oggetto dei dati.

## <a name="integrate-with-partner-solutions"></a>Integrazione con soluzioni partner

Puoi integrare il modulo subject rights request Microsoft 365 con i processi e gli strumenti aziendali esistenti sfruttando l'API Microsoft 365 subject rights request. Questo offre un modo semplice ma potente per introdurre l'automazione nella strategia per i diritti dell'oggetto.

Quando gli interessati richiedono informazioni all'organizzazione, puoi sfruttare le API per creare tali richieste all'interno di Microsoft 365 in base ai criteri personalizzati per tale richiesta. Puoi creare la richiesta di diritti dell'oggetto in Microsoft 365, tenere traccia dell'avanzamento della richiesta attraverso le sue fasi e confermare quando la richiesta ha completato l'elaborazione e il contenuto è pronto per il recupero. Le NOSTRE API sono disponibili per chiunque possa usare per rendere le proprie soluzioni più estensibile: che si tratta di ISV, partner per ospitare Microsoft 365 nelle proprie soluzioni o per le organizzazioni da usare con le applicazioni line-of-business.

Per ulteriori informazioni, vedere [Use the Microsoft Graph subject rights request API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="manage-data-retention"></a>Gestire la conservazione dei dati

I report generati tramite questo strumento e i dati associati, ad esempio i file con annotazioni salvati in Azure, vengono archiviati per un periodo di tempo specificato. Questa durata viene definita a  livello globale tramite  Impostazioni nella sezione Periodi di conservazione dei dati, che consente di scegliere tra 30 e 90 giorni. Verificare che questi periodi di conservazione dei dati siano conformi ai criteri e agli obblighi legali.

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

---
title: Automatizzare le attività relative alle richieste di diritti dell'oggetto nella gestione della privacy
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
description: Scopri come usare Microsoft Power Automate per automatizzare le attività essenziali per le richieste di diritti dell'oggetto nella gestione della privacy.
ms.openlocfilehash: df76e87e3298b2ccc6c897d485e695d0f1ae35c9
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478190"
---
# <a name="automate-subject-rights-requests-tasks"></a>Automatizzare le attività relative alle richieste di diritti dell'oggetto

Microsoft Power Automate è un servizio di flusso di lavoro che automatizza le azioni tra applicazioni e servizi. Quando si abilitano flussi di Power Automate per la gestione della privacy per Microsoft 365, è possibile automatizzare attività importanti per casi e utenti, ad esempio la creazione di ticket in ServiceNow o l'aggiunta di promemoria del calendario sulle date di scadenza. Per ulteriori informazioni sulle Power Automate, visitare il sito [della documentazione.](/power-automate/getting-started)

I clienti con Microsoft 365 che includono la gestione della privacy non hanno bisogno di altre licenze Power Automate per usare i modelli di gestione della privacy Power Automate consigliati. Questi modelli possono essere personalizzati per supportare l'organizzazione e coprire gli scenari di gestione della privacy di base. Se si sceglie di utilizzare le funzionalità di Power Automate premium in questi modelli, creare un modello personalizzato utilizzando il connettore di conformità di Microsoft 365 o utilizzare modelli Power Automate per altre aree di conformità in Microsoft 365, potrebbero essere necessarie più licenze Power Automate.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>Creare un nuovo Power Automate flusso di lavoro da un modello

1. Nel riquadro [Centro conformità Microsoft 365](https://compliance.microsoft.com/), passare alla sezione gestione della privacy della struttura di spostamento e selezionare **Richieste di diritti dell'oggetto**.
1. Aprire la richiesta di diritti dell'oggetto che si desidera utilizzare nell'elenco e selezionare **Automate**, quindi **Manage Power Automate flows**. Verrà aperto il riquadro a comparsa Flussi.
1. Usa **l'opzione** Nuovo e scegli il modello che vuoi usare tra le opzioni disponibili. Seguire le istruzioni della procedura guidata per completare l'installazione. Le opzioni variano a seconda del tipo di modello.

Dopo aver salvato un'istanza del modello, è necessario eseguirla dalla pagina dei dettagli della richiesta di diritti dell'oggetto in modo che l'istanza del flusso abbia il contesto e l'ID appropriati. Aprire la richiesta, tornare al menu **Automate,** selezionare il modello e selezionare **Esegui flusso.** È possibile visualizzare le attività passate selezionando Visualizza **attività di esecuzione del flusso.**

### <a name="power-automate-templates-in-privacy-management"></a>Power Automate modelli nella gestione della privacy

- Creare un record per il caso di gestione della **privacy in ServiceNow**: questo modello è per le organizzazioni che desiderano utilizzare la soluzione ServiceNow per tenere traccia dei casi di richiesta di diritti dell'oggetto. Verrà richiesto di immettere i dettagli dell'istanza serviceNow, inclusi un account per connettersi a ServiceNow. Questo account deve avere la possibilità di creare un evento imprevisto in ServiceNow e compilare i dettagli dell'evento imprevisto. Dopo la connessione all'istanza, gli amministratori delle richieste di diritti dell'oggetto potranno creare un record per il caso in ServiceNow e, se necessario, possono personalizzare ciò che verrà inserito nel modello nei campi selezionati. Per ulteriori informazioni sul connettore, vedere la [pagina di riferimento ServiceNow Connector.](/connectors/service-now/)
- **Creare un promemoria del calendario:** questo modello consente di impostare i promemoria della data di scadenza nel Outlook calendario per le richieste di diritti dell'oggetto. Lo strumento popolerà alcuni dettagli dalle proprietà della richiesta, ad esempio il nome della richiesta e la data di scadenza. È possibile aggiungere dettagli descrittivi, specificare i destinatari e modificare altre impostazioni avanzate.
- **Ottenere i file per tag per una** richiesta di diritti dell'oggetto: questo modello consente di cercare i file per la richiesta di diritti dell'oggetto a cui è stato assegnato un tag specifico. È possibile modificare il flusso per eseguire azioni personalizzate o visualizzare l'elenco dei file restituiti da sfruttare per i processi o gli strumenti interni.

## <a name="share-a-power-automate-flow"></a>Condividere un Power Automate flusso

Condividendo un Power Automate, è possibile aggiungere un altro proprietario e consentire loro di modificare, aggiornare ed eliminare il flusso. Tutti i proprietari possono inoltre accedere alla cronologia di esecuzione e aggiungere o rimuovere altri proprietari. Per condividere un flusso, aprire la richiesta di diritti **dell'oggetto** che si desidera utilizzare, selezionare **Automate** e quindi selezionare Manage Power Automate flows . In questo riquadro è possibile selezionare un flusso esistente e quindi utilizzare l'opzione Condividi per aggiungere un utente o un gruppo.

Questo riquadro offre inoltre la possibilità di gestire le connessioni incorporate ai servizi utilizzati nel Power Automate flusso. La modifica di queste impostazioni può influire sulla capacità di eseguire il flusso.

## <a name="edit-or-delete-power-automate-flow"></a>Modificare o eliminare Power Automate flusso

Per modificare i dettagli di un Power Automate flusso di lavoro, aprire la richiesta di diritti **dell'oggetto,** selezionare **Automate** e selezionare Manage Power Automate flows . In questo riquadro è possibile selezionare un flusso esistente per visualizzare i dettagli. Utilizzare Modifica in qualsiasi sezione per modificare le proprietà e quindi salvare.

Per rimuovere completamente il flusso, utilizzare **l'opzione** Elimina. Rimuoverà il flusso per tutti i proprietari e lo disinstallerà per tutti gli utenti. Le istanze del flusso precedente continueranno a essere eseguite per evitare la perdita di dati. Puoi confermare la scelta prima che l'eliminazione sia definitiva.

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

---
title: "Automatizzare le attività nelle richieste di diritti dell'oggetto "
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
description: Scopri come usare Microsoft Power Automate per automatizzare le attività essenziali per le richieste di diritti dell'oggetto in Priva.
ms.openlocfilehash: 2e1fa97b9e2cc5889471fa163dec26a5a5e37d56
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248951"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>Automatizzare le attività nelle richieste di diritti dell'oggetto 

Microsoft Power Automate è un servizio di flusso di lavoro che automatizza le azioni tra applicazioni e servizi. Quando si abilitano Power Automate per le richieste di diritti dell'oggetto di Microsoft Priva, è possibile automatizzare attività importanti per casi e utenti, ad esempio la creazione di ticket in ServiceNow o l'aggiunta di promemoria del calendario sulle date di scadenza. Per ulteriori informazioni sulle Power Automate, visitare il sito [della documentazione](/power-automate/getting-started).

I clienti con sottoscrizioni di richieste di diritti soggetto non necessitano di un'altra licenza Power Automate per usare i modelli Power Automate consigliati per Priva. Questi modelli possono essere personalizzati per supportare l'organizzazione e coprire gli scenari di richiesta dei diritti dell'oggetto di base. Se si sceglie di utilizzare le funzionalità di Power Automate premium in questi modelli, creare un modello personalizzato utilizzando il connettore di conformità Microsoft 365 o utilizzare modelli Power Automate per altre aree di conformità in Microsoft 365, potrebbero essere necessarie più licenze Power Automate.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>Creare un nuovo Power Automate flusso di lavoro da un modello

1. Nel riquadro [Centro conformità Microsoft 365](https://compliance.microsoft.com/) passare alla sezione Priva della struttura di spostamento e selezionare **Priva Subject Rights Requests**.
1. Aprire la richiesta di diritti dell'oggetto che si desidera utilizzare nell'elenco e selezionare **Automate**, quindi **Manage Power Automate flows**. Verrà aperto il riquadro a comparsa Flussi.
1. Usa **l'opzione** Nuovo e scegli il modello che vuoi usare tra le opzioni disponibili. Seguire le istruzioni della procedura guidata per completare l'installazione. Le opzioni variano a seconda del tipo di modello.

Dopo aver salvato un'istanza del modello, è necessario eseguirla dalla pagina dei dettagli della richiesta di diritti dell'oggetto in modo che l'istanza del flusso abbia il contesto e l'ID appropriati. Apri la richiesta, torna al menu **Automate** , seleziona il modello e seleziona **Esegui flusso**. È possibile visualizzare le attività passate selezionando Visualizza **attività di esecuzione del flusso**.

### <a name="power-automate-templates-in-priva"></a>Power Automate modelli in Priva

- **Creare un record per il caso di gestione della privacy in ServiceNow**: questo modello è per le organizzazioni che desiderano utilizzare la soluzione ServiceNow per tenere traccia dei casi di richiesta di diritti dell'oggetto. Verrà richiesto di immettere i dettagli dell'istanza serviceNow, inclusi un account per connettersi a ServiceNow. Questo account deve avere la possibilità di creare un evento imprevisto in ServiceNow e compilare i dettagli dell'evento imprevisto. Una volta connessi all'istanza, gli amministratori delle richieste di diritti dell'oggetto saranno in grado di creare un record per il caso in ServiceNow e, se necessario, potranno personalizzare ciò che verrà inserito nel modello nei campi selezionati. Per ulteriori informazioni sul connettore, vedere la [pagina di riferimento ServiceNow Connector](/connectors/service-now/).
- **Creare un promemoria del calendario**: questo modello consente di impostare promemoria della data di scadenza nel Outlook calendario per le richieste di diritti dell'oggetto. Lo strumento popolerà alcuni dettagli dalle proprietà della richiesta, ad esempio il nome della richiesta e la data di scadenza. È possibile aggiungere dettagli descrittivi, specificare i destinatari e modificare altre impostazioni avanzate.
- **Ottenere i file per tag per una richiesta di** diritti dell'oggetto: questo modello consente di cercare i file per la richiesta di diritti dell'oggetto a cui è stato assegnato un tag specifico. È possibile modificare il flusso per eseguire azioni personalizzate o visualizzare l'elenco dei file restituiti da sfruttare per i processi o gli strumenti interni.

## <a name="share-a-power-automate-flow"></a>Condividere un Power Automate flusso

Condividendo un Power Automate, è possibile aggiungere un altro proprietario e consentire loro di modificare, aggiornare ed eliminare il flusso. Tutti i proprietari possono inoltre accedere alla cronologia di esecuzione e aggiungere o rimuovere altri proprietari. Per condividere un flusso, aprire la richiesta di diritti dell'oggetto che si desidera utilizzare, selezionare **Automatizzare** e quindi selezionare **Gestisci Power Automate flussi**. In questo riquadro è possibile selezionare un flusso esistente, quindi utilizzare l'opzione Condividi per aggiungere un utente o un gruppo.

Questo riquadro offre inoltre la possibilità di gestire le connessioni incorporate ai servizi utilizzati nel Power Automate flusso. La modifica di queste impostazioni può influire sulla capacità di eseguire il flusso.

## <a name="edit-or-delete-power-automate-flow"></a>Modificare o eliminare Power Automate flusso

Per modificare i dettagli di un flusso Power Automate, aprire la richiesta di diritti dell'oggetto, selezionare **Automate** e **selezionare Manage Power Automate flows**. In questo riquadro è possibile selezionare un flusso esistente per visualizzare i dettagli. Utilizzare Modifica in qualsiasi sezione per modificare le proprietà e quindi salvare.

Per rimuovere completamente il flusso, utilizzare **l'opzione** Elimina. Rimuoverà il flusso per tutti i proprietari e lo disinstallerà per tutti gli utenti. Le istanze del flusso precedente continueranno a essere eseguite per evitare la perdita di dati. Puoi confermare la scelta prima che l'eliminazione sia definitiva.

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

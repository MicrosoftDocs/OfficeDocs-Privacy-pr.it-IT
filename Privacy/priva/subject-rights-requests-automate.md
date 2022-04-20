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
description: Informazioni su come usare Microsoft Power Automate per automatizzare le attività essenziali per le richieste di diritti degli interessati in Priva.
ms.openlocfilehash: ec9edde16b60c2326ca899e587dfe5dc7a1e32f5
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930497"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>Automatizzare le attività nelle richieste di diritti dell'oggetto 

Microsoft Power Automate è un servizio del flusso di lavoro che automatizza le azioni tra applicazioni e servizi. Quando si abilitano i flussi di Power Automate per microsoft Priva Subject Rights Requests, è possibile automatizzare attività importanti per case e utenti, ad esempio la creazione di ticket in ServiceNow o l'aggiunta di promemoria del calendario sulle date di scadenza. Per altre informazioni su Power Automate, visitare il [sito della documentazione](/power-automate/getting-started).

Per i clienti con sottoscrizioni con richieste di diritti soggetto non è necessaria un'altra licenza Power Automate per usare i modelli di Power Automate consigliati per Priva. Questi modelli possono essere personalizzati per supportare l'organizzazione e coprire gli scenari principali di richiesta di diritti dell'oggetto. Se si sceglie di usare le funzionalità di Power Automate Premium in questi modelli, creare un modello personalizzato usando il connettore di conformità Microsoft 365 o usare modelli di Power Automate per altre aree di conformità in Microsoft 365, potrebbero essere necessarie licenze più Power Automate.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>Creare un nuovo flusso di Power Automate da un modello

1. Nel [portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) passare alla sezione Priva del riquadro di spostamento e selezionare **Priva Subject Rights Requests (Richieste di diritti soggetti privati**).
1. Aprire la richiesta di diritti per l'oggetto che si vuole usare dall'elenco e selezionare **Automatizza**, quindi **Gestisci flussi di Power Automate**. Verrà aperto il riquadro a comparsa Flussi.
1. Usare l'opzione **Nuovo** e scegliere il modello da usare tra le opzioni disponibili. Da qui seguire le istruzioni della procedura guidata per completare l'installazione. Le opzioni variano a seconda del tipo di modello.

Dopo aver salvato un'istanza del modello, è necessario eseguirla dalla pagina dei dettagli della richiesta di diritti dell'oggetto in modo che l'istanza del flusso abbia il contesto e l'ID corretti. Aprire la richiesta, tornare al menu **Automatizza** , selezionare il modello e selezionare **Esegui flusso**. È possibile visualizzare le attività precedenti selezionando **Visualizza attività di esecuzione del flusso**.

### <a name="power-automate-templates-in-priva"></a>modelli Power Automate in Priva

- **Creare un record per il caso di gestione della privacy in ServiceNow**: questo modello è destinato alle organizzazioni che vogliono usare la soluzione ServiceNow per tenere traccia dei casi di richiesta di diritti soggetti. Verrà richiesto di immettere i dettagli dell'istanza di ServiceNow, inclusi un account per connettersi a ServiceNow. Questo account deve avere la possibilità di creare un evento imprevisto in ServiceNow e compilare i dettagli dell'evento imprevisto. Dopo aver eseguito la connessione all'istanza, gli amministratori potranno creare un record per il caso in ServiceNow e, se necessario, personalizzare ciò che il modello popola nei campi selezionati. Per altre informazioni sul connettore, vedere la [pagina di riferimento del connettore ServiceNow](/connectors/service-now/).
- **Creare un promemoria del calendario**: questo modello consente di impostare i promemoria per la data di scadenza nel calendario Outlook per le richieste di diritti dell'oggetto. Lo strumento popola automaticamente alcuni dettagli dalle proprietà della richiesta, ad esempio il nome della richiesta e la relativa data di scadenza. È possibile aggiungere dettagli descrittivi, specificare i destinatari e modificare altre impostazioni avanzate.
- **Ottenere i file per tag per una richiesta di diritti dell'oggetto**: questo modello consente di cercare i file per la richiesta di diritti dell'oggetto a cui è stato assegnato un tag specifico. È possibile modificare il flusso per eseguire azioni personalizzate o visualizzare l'elenco dei file restituiti da sfruttare per i processi o gli strumenti interni.

## <a name="share-a-power-automate-flow"></a>Condividere un flusso di Power Automate

Condividendo un flusso Power Automate, è possibile aggiungere un altro proprietario e consentire loro di modificare, aggiornare ed eliminare il flusso. Tutti i proprietari possono anche accedere alla cronologia di esecuzione e aggiungere o rimuovere altri proprietari. Per condividere un flusso, aprire la richiesta di diritti dell'oggetto con cui si vuole lavorare, selezionare **Automatizza** e quindi selezionare **Gestisci flussi di Power Automate**. Da questo riquadro è possibile selezionare un flusso esistente, quindi usare l'opzione Condividi per aggiungere un utente o un gruppo.

Questo riquadro offre anche la possibilità di gestire le connessioni incorporate ai servizi usati nel flusso di Power Automate. La modifica di queste impostazioni può influire sulla capacità di eseguire il flusso.

## <a name="edit-or-delete-power-automate-flow"></a>Modificare o eliminare Power Automate flusso

Per modificare i dettagli di un flusso di Power Automate, aprire la richiesta di diritti dell'oggetto, selezionare **Automatizza** e selezionare **Gestisci flussi Power Automate**. Da questo riquadro è possibile selezionare un flusso esistente per visualizzare i dettagli. Usare Modifica in qualsiasi sezione per modificare le proprietà e quindi salvare.

Per rimuovere completamente il flusso, usare l'opzione **Elimina** . Rimuoverà il flusso per tutti i proprietari e lo disinstallerà per tutti gli utenti. Le istanze del flusso precedenti continueranno a essere eseguite per evitare la perdita di dati. È possibile confermare la scelta prima che l'eliminazione sia definitiva.

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

---
title: Integrazione con Microsoft API Graph e Power Automate
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
description: Informazioni su come estendere le funzionalità di Richieste di diritti degli interessati Priva integrando con Microsoft API Graph e Power Automate.
ms.openlocfilehash: e4fcad2067ece3d1a6338e6d4891c59d91205a33
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851641"
---
# <a name="integrate-and-extend-through-microsoft-graph-api-and-power-automate"></a>Integrare ed estendere tramite Microsoft API Graph e Power Automate

È possibile integrare Richieste di diritti degli interessati Priva con i processi e gli strumenti aziendali esistenti usando l'API Microsoft Graph Subject Rights Request. È anche possibile estendere le funzionalità di automazione delle richieste di diritti dell'oggetto usando flussi di Power Automate predefiniti per attività quali l'impostazione di promemoria del calendario e la creazione di casi in ServiceNow.

## <a name="microsoft-graph-subject-rights-requests-api"></a>API Microsoft Graph Subject Rights Requests

L'API Microsoft 365 Subject Rights Request offre un modo semplice ma potente per introdurre l'automazione nella strategia esistente per i diritti dei soggetti. Quando una singola persona richiede informazioni all'organizzazione, le API consentono di creare tali richieste all'interno di Microsoft 365 in base ai criteri per tale richiesta. È possibile creare la richiesta di diritti dell'oggetto in Microsoft 365, tenere traccia dello stato di avanzamento e confermare quando la richiesta ha completato l'elaborazione e il contenuto è pronto per il recupero.

Le API sono disponibili per chiunque sia in grado di usare per rendere le soluzioni più estendibili, ad esempio ISV, partner che desiderano soddisfare Microsoft 365 nelle proprie soluzioni e organizzazioni che desiderano usare le API con le proprie applicazioni line-of-business.

Visualizzare la documentazione completa in [Usare l'API Microsoft Graph per la richiesta di diritti dell'oggetto](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="power-automate-templates-for-subject-rights-requests"></a>modelli di Power Automate per le richieste di diritti dell'oggetto

Microsoft Power Automate è un servizio del flusso di lavoro che automatizza le azioni tra applicazioni e servizi. Subject Rights Requests include modelli di Power Automate predefiniti per consentire agli utenti di gestire le richieste di diritti dell'interessato. Gli utenti possono configurare flussi di automazione per processi come la creazione di ticket in ServiceNow e l'aggiunta di promemoria del calendario sulle date di scadenza. Per altre informazioni su Power Automate, vedere la [documentazione di Power Automate](/power-automate/getting-started).

Se è stata acquistata una sottoscrizione di Richieste di diritti soggetto, non è necessaria una licenza Power Automate separata per usare i modelli di Power Automate consigliati. Questi modelli possono essere personalizzati per supportare l'organizzazione e coprire gli scenari principali di richiesta di diritti dell'oggetto. Tuttavia, potrebbero essere necessarie licenze aggiuntive per usare le funzionalità premium Power Automate in questi modelli o per creare un modello personalizzato.

### <a name="available-templates"></a>Modelli disponibili

- **Creare un record per Priva caso di gestione della privacy in ServiceNow**: questo modello è destinato alle organizzazioni che vogliono usare la soluzione ServiceNow per tenere traccia dei casi di richiesta di diritti degli interessati. Verrà richiesto di immettere i dettagli dell'istanza di ServiceNow, incluso un account per connettersi a ServiceNow. Questo account deve avere la possibilità di creare un evento imprevisto in ServiceNow e compilare i dettagli dell'evento imprevisto. Dopo aver eseguito la connessione all'istanza, gli amministratori potranno creare un record per il caso in ServiceNow e, se necessario, personalizzare ciò che il modello popola nei campi selezionati. Per altre informazioni sul connettore, vedere la [documentazione del connettore ServiceNow](/connectors/service-now/).

- **Aggiungere un promemoria del calendario per completare un caso di gestione della privacy Priva**: questo modello consente di impostare promemoria per la data di scadenza nel calendario Outlook per le richieste di diritti dell'oggetto. Lo strumento popola automaticamente alcuni dettagli dalle proprietà della richiesta, ad esempio il nome della richiesta e la relativa data di scadenza. È possibile aggiungere dettagli descrittivi, specificare i destinatari e modificare altre impostazioni avanzate.

- **Ottenere i file per tag per una richiesta di diritti dell'oggetto Priva**: questo modello consente di cercare i file per la richiesta di diritti dell'oggetto a cui è stato assegnato un tag specifico. È possibile modificare il flusso per eseguire azioni personalizzate o visualizzare l'elenco dei file restituiti da usare per i processi o gli strumenti interni.

### <a name="create-a-new-power-automate-flow-from-a-template"></a>Creare un nuovo flusso di Power Automate da un modello

1. Nel [Portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) selezionare **Richieste di diritti degli interessati Priva** nel riquadro di spostamento a sinistra.

2. Trovare la richiesta di diritti dell'oggetto su cui si vuole lavorare e selezionarla dall'elenco per aprire la pagina dei dettagli.

3. Nell'angolo in alto a destra selezionare **Automatizza**, quindi selezionare **Gestisci flussi Power Automate** per aprire il riquadro a comparsa dei flussi.

4. Selezionare **Nuovo** e scegliere il modello da usare tra le opzioni disponibili. Da qui seguire le istruzioni per personalizzare e aggiungere i passaggi per completare la compilazione del flusso. Le opzioni variano a seconda del modello usato (vedere i tipi di modello riportati di seguito).

5. Al termine, scegliere **Salva**.

Dopo aver salvato un'istanza del modello, è necessario eseguirla dalla pagina dei dettagli della richiesta in modo che l'istanza del flusso abbia il contesto e l'ID corretti. Aprire la richiesta, tornare al menu **Automatizza** , selezionare il modello e selezionare **Esegui flusso**. È possibile visualizzare le attività precedenti selezionando **Visualizza attività di esecuzione del flusso**.

### <a name="share-a-power-automate-flow"></a>Condividere un flusso di Power Automate

La condivisione di un flusso di Power Automate consente di aggiungere un altro proprietario e di modificare, aggiornare ed eliminare il flusso. Tutti i proprietari possono accedere alla cronologia di esecuzione e aggiungere o rimuovere altri proprietari. 

Per condividere un flusso, aprire la richiesta di diritti dell'oggetto con cui si vuole lavorare, selezionare **Automatizza** e quindi selezionare **Gestisci flussi di Power Automate**. Da questo riquadro è possibile selezionare un flusso esistente, quindi usare l'opzione **Condividi** per aggiungere un utente o un gruppo.

Questo riquadro offre anche la possibilità di gestire le connessioni incorporate ai servizi usati nel flusso di Power Automate. La modifica di queste impostazioni può influire sulla capacità di eseguire il flusso.

### <a name="edit-or-delete-power-automate-flow"></a>Modificare o eliminare Power Automate flusso

Per modificare i dettagli di un flusso di Power Automate, selezionare **Automatizza** nell'angolo superiore destro della pagina dei dettagli di una richiesta e quindi selezionare **Gestisci flussi di Power Automate**.

Nel riquadro **flussi Power Automate** selezionare il flusso da modificare e selezionare **Modifica** dalla barra dei comandi per modificare o aggiungere passaggi. Al termine, selezionare **Salva**.

Per eliminare un flusso, selezionarlo dall'elenco nel riquadro **flussi di Power Automate** e selezionare **Elimina** dalla barra dei comandi. Il flusso verrà rimosso per tutti i proprietari e disinstallato per tutti gli utenti. Le istanze del flusso precedenti continueranno a essere eseguite per evitare la perdita di dati. Verrà chiesto di confermare prima che l'eliminazione sia definitiva.

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)

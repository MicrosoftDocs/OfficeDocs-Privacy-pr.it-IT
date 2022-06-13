---
title: Configurare le impostazioni di Priva
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Informazioni sulle opzioni delle impostazioni globali per Microsoft Priva.
ms.openlocfilehash: a6f2fe55600d6cc3018c9d15f05a6d9e459a1486
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046600"
---
# <a name="configure-priva-settings"></a>Configurare le impostazioni di Priva

È possibile gestire le impostazioni per Microsoft Priva selezionando l'icona a ingranaggio nell'angolo superiore destro dello schermo. Le opzioni qui consentono di impostare preferenze di alto livello e personalizzare le proprietà delle chiavi. Questa pagina offre una panoramica delle principali categorie di Impostazioni.

## <a name="anonymization"></a>Anonimizzazione

È possibile mostrare agli utenti in determinati ruoli le versioni anonime dei nomi utente all'interno delle funzionalità di Gestione dei rischi per la privacy. La funzionalità di anonimizzazione sostituisce i nomi visualizzati identificabili con un'etichetta generica per mascherare le identità degli utenti durante la revisione dei dati sensibili. Questa opzione non si applica alla soluzione Subject Rights Requests.

## <a name="user-notification-emails"></a>Messaggi di posta elettronica di notifica utente  

I criteri in Gestione dei rischi per la privacy consentono di impostare parametri per la valutazione dei potenziali rischi per la privacy nell'ambiente. Quando viene rilevata una corrispondenza dei criteri, Gestione dei rischi per la privacy può inviare un messaggio di posta elettronica agli utenti con raccomandazioni sulle azioni correttive da intraprendere e un collegamento alla formazione sulla privacy. In **Impostazioni** è possibile abilitare o disabilitare la funzionalità di notifica tramite posta elettronica di Gestione dei rischi per la privacy nel suo complesso. Se la funzionalità di notifica è disattivata in Impostazioni, tutti i messaggi di posta elettronica verranno disabilitati. Per altre informazioni sui criteri, vedere [Creare criteri in Gestione dei rischi per la privacy](risk-management-policies.md).

## <a name="teams-collaboration"></a>Collaborazione in Teams  

Integrare le funzionalità Microsoft Teams con Richieste di diritti degli interessati Priva per migliorare la collaborazione con gli stakeholder. Se si seleziona la casella di controllo **Attiva funzionalità Microsoft Teams per le richieste di diritti dell'interessato**, verrà creato automaticamente un canale di Teams associato per ogni richiesta. Gli utenti possono essere aggiunti al canale Teams dalla scheda **Collaboratori** della richiesta.

L'attivazione di questa funzionalità si applica Teams funzionalità a tutte le richieste. Se si deseleziona la casella, queste funzionalità verranno disattivate per tutte le richieste. Altre informazioni sulla [collaborazione durante il processo di revisione dei dati](subject-rights-requests-data-review.md#collaboration-for-data-review).

## <a name="data-matching"></a>Corrispondenza dei dati  

Usare questa sezione per caricare schemi di dati che descrivono gli attributi degli interessati, che consentono di identificare l'interessato corretto durante la ricerca di dati personali all'interno dell'ambiente Microsoft 365. Gli schemi e i pacchetti di regole vengono creati e caricati in formato XML. In **Caricamento dati personali** è anche possibile inviare dati personali corrispondenti a uno schema specificato. È possibile creare e caricare il proprio file o scegliere di caricare dati personali da Azure. Altre informazioni sulla [corrispondenza dei dati per le richieste di diritti dell'interessato](subject-rights-requests-data-match.md).

## <a name="data-retention-periods"></a>Periodi di conservazione dei dati

Questa impostazione è correlata a Richieste di diritti degli interessati Priva. Consente di controllare le preferenze per quanto tempo si desidera conservare i dati raccolti e i report generati dopo la chiusura della richiesta. Può essere impostato su 30 o 90 giorni e si applica a tutte le richieste di diritti dell'oggetto create. È consigliabile verificare che i periodi di conservazione dei dati siano conformi ai criteri e agli obblighi legali dell'organizzazione. Altre informazioni sulla [conservazione dei dati per le richieste di diritti degli interessati](subject-rights-requests-reports.md#retention-periods-for-reports-and-data).

## <a name="data-review-tags"></a>Tag di revisione dei dati

I tag di revisione dei dati possono essere usati per contrassegnare gli elementi di contenuto recuperati in una richiesta di diritti dell'interessato. Questa area di impostazioni consente di gestire i tag. Priva fornisce tre tag predefiniti: **Completamento**, **Eliminazione** e **Aggiornamento**. Questi nomi di tag non possono essere modificati, ma è possibile fornire una descrizione per questi tag significativa per l'organizzazione.

Priva fornisce anche due tag personalizzati che è possibile denominare e definire per l'uso dell'organizzazione. Verranno visualizzati come **Tag personalizzato 1** e **Tag personalizzato 2** fino a quando non si modificano i nomi.

Seguire la procedura seguente per modificare i nomi e le descrizioni dei tag:

- Nella pagina Impostazioni **Priva** selezionare **Tag di revisione dei dati**.
- Trovare il tag nell'elenco che si vuole modificare e selezionare l'icona **Modifica** matita accanto al relativo nome.
- Nel riquadro a comparsa apportare le modifiche nei campi disponibili. Per i tag di sistema, è possibile modificare solo la descrizione. Per i tag personalizzati, è possibile modificare il nome e la descrizione.
- Al termine, selezionare **Invia** per salvare le modifiche.

Le impostazioni dei tag si applicano a tutte le richieste di diritti del soggetto.

Altre informazioni [sull'applicazione di tag quando si esaminano i dati per una richiesta di diritti dell'interessato](subject-rights-requests-data-review.md#apply-tags).
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
ms.openlocfilehash: 9b59dcd875f248dd4a15be47d2f4383e8f656155
ms.sourcegitcommit: 1f3f2757f456628ec904bc3df985b00ffba8f892
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2022
ms.locfileid: "62542824"
---
# <a name="configure-priva-settings"></a>Configurare le impostazioni di Priva

Puoi gestire le impostazioni per Microsoft Priva selezionando l'icona a forma di ingranaggio nell'angolo in alto a destra dello schermo. Le opzioni qui consentono di impostare preferenze di alto livello e personalizzare le proprietà chiave. In questa pagina viene fornita una panoramica delle categorie Impostazioni principali.

## <a name="anonymization"></a>Anonimizzazione

Questa funzionalità consente di mostrare versioni anonime dei nomi utente nelle funzionalità di gestione dei rischi per la privacy agli utenti in determinati ruoli. Sostituirà i nomi visualizzati identificabili con un'etichetta generica per mascherare le identità degli utenti durante la revisione dei dati sensibili. Questa opzione non si applica alla soluzione Richieste diritti oggetto.

## <a name="user-notification-emails"></a>Messaggi di posta elettronica di notifica utente  

I criteri in Gestione dei rischi per la privacy consentono di impostare i parametri per la valutazione dei potenziali rischi per la privacy nell'ambiente. Quando viene rilevata una corrispondenza ai criteri, La gestione dei rischi per la privacy può inviare un messaggio di posta elettronica agli utenti con suggerimenti sulle azioni correttive da intraprendere e un collegamento alla formazione sulla privacy. In Impostazioni, è possibile abilitare o disabilitare la funzionalità di notifica tramite posta elettronica di Gestione dei rischi per la privacy nel suo complesso. Se la funzionalità di notifica è disattivata in Impostazioni, tutti i messaggi di posta elettronica verranno disabilitati. Per ulteriori informazioni sui criteri, vedere [Create policies in Privacy Risk Management](risk-management-policies.md).

## <a name="teams-collaboration"></a>Collaborazione in Teams  

Integrare Microsoft Teams funzionalità con Priva Subject Rights Requests per migliorare la collaborazione con gli stakeholder. Ogni volta che viene creata una richiesta di diritti dell'oggetto, verrà creato un team associato Teams. Gli utenti possono essere aggiunti a un team dalla scheda Collaboratori della richiesta. Per altre informazioni sulle richieste di diritti dell'oggetto, vedi [Informazioni su Priva Subject Rights Requests](subject-rights-requests.md).

## <a name="data-matching"></a>Corrispondenza dati  

Utilizzare questa sezione per caricare schemi di dati che descrivono gli attributi degli interessati, che consentono di identificare l'oggetto dei dati corretto durante la ricerca di dati personali all'interno dell'Microsoft 365 locale. Gli schemi e i pacchetti di regole vengono creati e caricati in formato XML. In **Caricamento dati personali** è inoltre possibile inviare dati personali che corrispondono a uno schema fornito. Puoi creare e caricare il tuo file o scegliere di caricare i dati personali da Azure. Per altre informazioni sulle richieste di diritti dell'oggetto, vedi [Informazioni su Priva Subject Rights Requests](subject-rights-requests.md).

## <a name="data-retention-periods"></a>Periodi di conservazione dei dati

Questa impostazione è correlata a Priva Subject Rights Requests. Consente di controllare la preferenza per quanto tempo si desidera conservare i dati raccolti e i report generati dopo la chiusura della richiesta. Può essere impostato su 30 o 90 giorni e si applica a tutte le richieste di diritti dell'oggetto create. È consigliabile verificare che i periodi di conservazione dei dati siano conformi ai criteri e agli obblighi legali dell'organizzazione. Ulteriori informazioni [sull'impostazione della conservazione dei dati per le richieste di diritti dell'oggetto](subject-rights-requests-reports.md#manage-data-retention).

## <a name="data-review-tags"></a>Tag di revisione dei dati

Gestisci i tag che userai per contrassegnare i file recuperati in una richiesta di diritti dell'oggetto. Questi tag possono essere usati per indicare il contenuto che avrà bisogno di ulteriore attenzione, ad esempio il contenuto che potrebbe essere necessario eliminare manualmente. In questa sezione delle impostazioni è possibile modificare i nomi e le descrizioni dei tag personalizzati. Puoi anche modificare le descrizioni dei tag per i tag predefiniti forniti dal sistema. I nomi dei tag di sistema non possono essere modificati. Per altre informazioni sulle richieste di diritti dell'oggetto, vedi [Esaminare i dati per una richiesta di diritti dell'oggetto](subject-rights-requests-data-review.md#step-3-review-data).

---
title: Inviare notifiche utente in Gestione dei rischi per la privacy
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Informazioni su come inviare notifiche ai proprietari dei contenuti sulle corrispondenze dei criteri trovate dalla gestione dei rischi per la privacy e su come usare queste notifiche di posta elettronica per risolvere i problemi.
ms.openlocfilehash: 2215224adf932f806f16429560d4a694cd47a859
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248957"
---
# <a name="send-user-notifications-in-privacy-risk-management"></a>Inviare notifiche utente in Gestione dei rischi per la privacy

La gestione dei rischi per la privacy in Microsoft Priva può informare direttamente i proprietari dei contenuti delle corrispondenze per la sovraesposizione dei dati, la minimizzazione dei dati e i criteri di trasferimento dei dati. Con le notifiche tramite posta elettronica, gli utenti possono facilmente trovare informazioni sul contenuto che devono esaminare e possono usare le istruzioni direttamente nel messaggio di posta elettronica per applicare le azioni correttive appropriate. Questi messaggi di posta elettronica includono anche collegamenti alla propria formazione sulla privacy. Per i criteri di trasferimento dei dati, puoi anche condividere notifiche e suggerimenti sui criteri nei Teams canali.

## <a name="prepare-training-content-for-policy-notifications"></a>Preparare il contenuto di formazione per le notifiche dei criteri

L'inclusione di un collegamento alla formazione sulla privacy è necessaria per i criteri che generano notifiche. L'accesso alle linee guida sulla privacy dell'organizzazione consente di mantenere gli utenti informati sulle proprie procedure consigliate e sui criteri. Può anche fornire contesto per le azioni di correzione suggerite nel messaggio di posta elettronica e aiutare gli utenti a prepararsi per buone decisioni di gestione dei dati in futuro.

Prima di configurare i criteri, decidi l'URL di formazione che vuoi includere. È possibile specificare un collegamento per ogni criterio, pertanto è consigliabile scegliere riferimenti specifici per ogni scenario.

## <a name="set-up-email-notifications-for-policies"></a>Configurare le notifiche di posta elettronica per i criteri

Le notifiche tramite posta elettronica possono essere configurate quando si crea un criterio personalizzato o si modifica qualsiasi criterio. Per [le istruzioni complete, vedere Creare criteri in Gestione](risk-management-policies.md) dei rischi per la privacy. Le impostazioni di notifica tramite posta elettronica sono disponibili nella **scheda Risultati** della procedura guidata dei criteri. Qui puoi decidere con quale frequenza inviare notifiche, impostare l'URL di formazione sulla privacy e immettere qualsiasi testo personalizzato per l'oggetto o il corpo del messaggio di posta elettronica.

## <a name="remediate-issues-from-email-notifications"></a>Risolvere i problemi dalle notifiche di posta elettronica

Quando gli utenti ricevono notifiche tramite posta elettronica sulle corrispondenze dei criteri, possono seguire le istruzioni nei messaggi di posta elettronica per intraprendere immediatamente un'azione correttiva. Ad esempio, se un criterio di sovraesposizione dei dati trova una corrispondenza per i dati personali che potrebbe essere troppo accessibile, il messaggio di posta elettronica risultante potrebbe fornire istruzioni per rendere privato l'elemento. Se l'elemento indicato deve essere conservato così come è, gli utenti possono anche scegliere di mantenere l'elemento. Le azioni suggerite fornite saranno rilevanti per ogni tipo di criterio diverso.

## <a name="send-notifications-in-teams"></a>Inviare notifiche in Teams

Per i criteri di trasferimento dei dati, gli utenti possono ricevere suggerimenti e suggerimenti per i criteri nei canali Teams quando viene rilevata una corrispondenza dei criteri. Questi suggerimenti informano gli utenti sull'uso responsabile dei dati personali. Suggerimenti includerà anche collegamenti alla formazione correlata.

Per altre informazioni sulla configurazione di queste notifiche, vedi [Creare criteri in Gestione dei rischi per la privacy](risk-management-policies.md#set-user-email-notifications).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

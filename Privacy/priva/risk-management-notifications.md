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
description: Informazioni su come notificare ai proprietari dei contenuti le corrispondenze ai criteri trovate da Microsoft Priva Privacy Risk Management e come possono usare queste notifiche tramite posta elettronica per risolvere i problemi.
ms.openlocfilehash: 8969e1cd4d5859102b18bd46723d1be6e85d35f6
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014376"
---
# <a name="user-notifications-in-privacy-risk-management"></a>Notifiche utente in Gestione dei rischi per la privacy

Quando si configura un criterio in Gestione dei rischi per la privacy, è possibile scegliere di notificare agli utenti quando le loro azioni soddisfano le condizioni impostate nei criteri. Esistono due tipi di notifiche: i messaggi di posta elettronica, disponibili per tutti e tre i tipi di criteri, e i suggerimenti visualizzati in Teams, disponibili solo per il tipo di criterio di trasferimento dei dati. Quando si crea o si modifica un criterio, è possibile decidere se attivare queste notifiche, la frequenza di invio e personalizzare il contenuto.

L'invio di notifiche agli utenti può essere un componente importante per aiutare l'organizzazione a raggiungere gli obiettivi di privacy. Le notifiche sono progettate per:

- Sensibilizzare immediatamente gli utenti quando le loro azioni potrebbero esporre i dati personali a rischi per la privacy.
- Fornire metodi di correzione direttamente all'interno dei messaggi di posta elettronica, in modo che gli utenti possano intraprendere azioni rapide per proteggere i dati a rischio.
- Indirizzare gli utenti alle linee guida e alle procedure consigliate per la privacy dell'organizzazione.

Informare gli utenti dei potenziali problemi in questo momento e consentire loro di correggere i problemi e aggiornare le proprie competenze, può essere uno strumento potente per la creazione di procedure di gestione dei dati audio in tutta l'organizzazione.

Esaminare le sezioni seguenti per preparare e gestire le notifiche utente per le corrispondenze dei criteri.

## <a name="prepare-training-content-for-notifications"></a>Preparare il contenuto di training per le notifiche

Se si sceglie di inviare notifiche utente quando vengono rilevate corrispondenze ai criteri, è necessario includere un collegamento al training sulla privacy. Fornire l'accesso alle linee guida sulla privacy dell'organizzazione consente di mantenere gli utenti informati sulle procedure consigliate e sui criteri. Può anche fornire un contesto per le azioni correttive suggerite nel messaggio di posta elettronica e aiutare gli utenti a prepararsi per decisioni di gestione dei dati valide in futuro.

Prima di configurare i criteri, decidere l'URL di training da includere. È possibile specificare un collegamento per ogni criterio, quindi è consigliabile scegliere riferimenti specifici per ogni scenario.

## <a name="set-user-email-notifications"></a>Impostare le notifiche di posta elettronica utente

È possibile configurare le notifiche tramite posta elettronica per tutti i tipi di criteri quando si crea un nuovo criterio o si modifica un criterio esistente. Queste impostazioni sono disponibili nella pagina **Risultati** della creazione guidata criteri. Vedere [Definire i risultati: notifiche utente e suggerimenti](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips) per le istruzioni complete.

> [!NOTE]
> La capacità complessiva di Gestione dei rischi per la privacy di inviare notifiche tramite posta elettronica è controllata in Priva **Impostazioni**. È disabilitato per impostazione predefinita. Se si disattiva questa impostazione, tutti i messaggi di posta elettronica verranno arrestati anche se le notifiche sono state configurate a livello di singolo criterio. Altre informazioni sulle [impostazioni di posta elettronica per le notifiche utente](priva-settings.md#user-notification-emails).

## <a name="send-notifications-in-teams"></a>Inviare notifiche in Teams

Per i criteri di trasferimento dei dati, è possibile scegliere agli utenti di ricevere suggerimenti e consigli sui criteri in canali di Teams sicuri quando viene rilevata una corrispondenza dei criteri. Questi suggerimenti informano gli utenti sull'uso responsabile dei dati personali. Suggerimenti includerà anche collegamenti alla formazione correlata.

Per altre informazioni sulla configurazione di queste notifiche, vedere [Definire i risultati: notifiche utente e suggerimenti](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips).

## <a name="preview-and-customize-email-content"></a>Visualizzare in anteprima e personalizzare il contenuto della posta elettronica

Quando gli utenti ricevono notifiche tramite posta elettronica sulle corrispondenze dei criteri, possono seguire le richieste nei messaggi di posta elettronica per intraprendere immediatamente azioni correttive. Ad esempio, se un criterio di sovraesposizione dei dati trova una corrispondenza per i dati personali che potrebbero essere troppo accessibili, il messaggio di posta elettronica di notifica include un collegamento all'elemento di contenuto in modo che l'utente possa esaminarlo e pulsanti per contrassegnare l'elemento come privato o mantenere il livello di accesso corrente. Le azioni suggerite saranno rilevanti per ogni tipo di criterio.

È possibile visualizzare in anteprima il contenuto del messaggio di posta elettronica e apportare modifiche personalizzate durante la modifica di questa impostazione nel processo di creazione o modifica dei criteri. Per visualizzare in anteprima e modificare il contenuto della posta elettronica di notifica, seguire questa procedura:

1. Creare o modificare i criteri avviando i passaggi descritti nel [processo di creazione guidata dei criteri](risk-management-policies.md#custom-setup-guided-process-to-choose-all-settings).

2. Nel passaggio **Risultati** del processo selezionare la casella accanto a **Invia un messaggio di posta elettronica di notifica agli utenti quando si verifica una corrispondenza dei criteri**.

3. Selezionare il pulsante **Anteprima e modifica messaggio di posta elettronica di notifica** visualizzato sotto la casella di controllo messaggio di posta elettronica di notifica.

4. Viene visualizzato un riquadro a comparsa con campi di testo prepopolato con il contenuto di posta elettronica predefinito. È possibile modificare uno o tutti i campi, tra cui la riga dell'oggetto del messaggio di posta elettronica, l'intestazione del corpo, il contenuto del corpo, il nome visualizzato del training sulla privacy e l'URL di training. L'anteprima del messaggio di posta elettronica si trova nella parte inferiore del riquadro a comparsa e verrà modificata quando si apportano modifiche al testo predefinito. Quando si è soddisfatti del contenuto del messaggio di posta elettronica, selezionare **Salva** per salvare le impostazioni. Per eliminare eventuali modifiche al messaggio di posta elettronica predefinito, selezionare la **X** nell'angolo superiore destro del riquadro a comparsa per chiuderla e ripristinare il contenuto predefinito.

5. Nella pagina **Risultati** selezionare **Avanti**. Continuare con la procedura guidata e quando si arriva alla pagina **Finale** finale, esaminare le impostazioni e selezionare **Invia**.

Le impostazioni di notifica saranno ora valide per questo criterio. Se i criteri vengono testati, le notifiche non verranno inviate. Se i criteri sono attivati, verranno inviate notifiche. Visualizzare altri dettagli sulla [creazione e la gestione dei criteri](risk-management-policies.md).


## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

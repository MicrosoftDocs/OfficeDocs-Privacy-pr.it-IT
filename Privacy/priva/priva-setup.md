---
title: Introduzione a Chat
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
- MET150fcf
description: Informazioni su come configurare Microsoft Priva per l'organizzazione, impostare ruoli e autorizzazioni e configurare impostazioni importanti.
ms.openlocfilehash: 945cbfd2625be50cb89eeaa8fe09e0effaea79d5
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678213"
---
# <a name="get-started-with-priva"></a>Introduzione a Chat

Se si è pronti a iniziare a usare Microsoft Priva per aiutare l'organizzazione a identificare e attenuare i rischi per la privacy, seguire questa procedura per configurare.

## <a name="confirm-subscriptions-and-licensing"></a>Confermare le sottoscrizioni e le licenze

Priva è disponibile all'interno del [Portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) e può essere acquistato dalle organizzazioni con le licenze seguenti:

- Microsoft 365 E3, E5, A3, A5
- Office 365 E1, E3, E5, A1, A3, A5

Priva offre opzioni di licenza per due soluzioni diverse: Gestione dei rischi per la privacy Priva e Richieste di diritti degli interessati Priva. Questi possono essere acquistati singolarmente o insieme. Quando si ottengono licenze per le richieste di diritti dell'oggetto, è possibile scegliere il livello di licenza appropriato per il numero di richieste che è necessario gestire. È possibile acquistare richieste aggiuntive in qualsiasi momento.

Per indicazioni dettagliate sulle licenze, vedere [Indicazioni dettagliate sulle licenze di Microsoft 365 per la sicurezza e la conformità](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva).

> [!Note]
> Priva non è disponibile per i clienti di Us Government Community (GCC) Moderate, GCC High o Department of Defense (DoD).

### <a name="start-a-free-trial"></a>Avviare una versione di versione di valutazione gratuita

Usare una sottoscrizione di valutazione gratuita per esplorare tutte le funzionalità e le funzionalità di entrambe le soluzioni Priva. Informazioni su come iscriversi alla versione di [valutazione Priva](priva-trial.md).

## <a name="enable-the-microsoft-365-audit-log"></a>Abilitare il log di controllo Microsoft 365

Microsoft 365 log di controllo sono un riepilogo di tutte le attività all'interno dell'organizzazione. I criteri di gestione dei rischi per la privacy possono usare queste attività per generare informazioni dettagliate sui criteri.

È possibile che i log di controllo dell'organizzazione siano già attivati. Se è necessario iniziare a usarli per la prima volta, vedere [Attivare o disattivare la ricerca nei log di controllo](/microsoft-365/compliance/turn-audit-log-search-on-or-off) per istruzioni dettagliate sull'attivazione del controllo. Dopo l'abilitazione, verrà visualizzato un messaggio che indica che è in corso la preparazione del log di controllo e che sarà possibile eseguire una ricerca in un paio d'ore, dopo il completamento della preparazione. Questa procedura deve essere eseguita una sola volta. Per altre informazioni sull'uso del log di controllo Microsoft 365, vedere [Cercare nel log di controllo](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

## <a name="set-user-permissions-and-assign-roles"></a>Impostare le autorizzazioni utente e assegnare ruoli

Priva usa un modello di autorizzazione del controllo degli accessi in base al ruolo. Solo gli utenti a cui è assegnato un ruolo possono accedere a Priva e le azioni consentite da ogni utente sono limitate in base al tipo di ruolo.

L'amministratore globale ha le autorizzazioni per accedere a Priva e assegnare altri utenti ai ruoli. Possono accedere e impostare le autorizzazioni utente nel [Portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) per Priva. Per una guida introduttiva, il gruppo di ruoli Gestione privacy ha le autorizzazioni per accedere a tutte le funzionalità di Priva. Questo gruppo può essere adatto alle organizzazioni in cui lo stesso individuo può svolgere tutti i compiti. Altri ruoli di privacy consentono di assumere un controllo più granulare e assegnare gli utenti a funzioni o funzionalità selezionate.

Per altre informazioni sui gruppi di ruoli e su come concedere [l'accesso, vedere Impostare le autorizzazioni utente e assegnare ruoli in Priva](priva-permissions.md).

## <a name="start-finding-and-visualizing-your-data"></a>Iniziare a trovare e visualizzare i dati

Dopo aver eseguito l'accesso a Priva, verrà **visualizzata** la pagina Panoramica. Questa pagina fornisce informazioni dinamiche sull'evoluzione dei dati personali nell'ambiente Microsoft 365 per individuare rapidamente i problemi, identificare gli indicatori di rischio e intervenire per risolvere i problemi. La panoramica deve essere popolata con informazioni dettagliate iniziali entro le prime 24 ore dall'iscrizione. Mentre si continua a usare Priva, la pagina di panoramica verrà aggiornata per continuare a fornire informazioni correnti.

Per altre informazioni dettagliate sui dati nel tempo, la pagina **Profilo dati** fornirà più visualizzazioni e analisi e offrirà una visione olistica dei dati dell'organizzazione in base alla posizione geografica e alla posizione Microsoft 365.

Per altre informazioni su queste pagine, vedere [Trovare e visualizzare i dati personali in Priva](priva-data-profile.md).

## <a name="start-managing-risks-with-default-policies"></a>Iniziare a gestire i rischi con i criteri predefiniti

Gestione dei rischi per la privacy inizierà a valutare i dati e a esaminare gli scenari di rischio chiave per la riduzione al minimo dei dati, la sovraesposizione dei dati e il trasferimento dei dati. Questi criteri sono attivati per impostazione predefinita. È possibile usare questi criteri per valutare dove si trovano i rischi, quindi attivare le notifiche tramite posta elettronica per gli utenti per segnalare problemi alla loro attenzione e guidare la correzione di questi rischi. Inoltre, è possibile creare e personalizzare criteri personalizzati dai modelli di criteri forniti. È possibile personalizzare i criteri per soddisfare le esigenze di conformità legale e normativa dell'organizzazione, come può essere identificato in consultazione con il consulente legale. Per altre informazioni, vedere [Creare criteri in Gestione dei rischi per la privacy](risk-management-policies.md).

## <a name="get-started-with-subject-rights-requests"></a>Attività iniziali con richieste di diritti dell'interessato

Richieste di diritti degli interessati Priva automatizza il processo di evasione delle richieste di diritti degli interessati, offrendo un facile accesso ai dati e ai flussi di lavoro personalizzabili che si adattano ai processi aziendali esistenti. È possibile trovare facilmente i dati rilevanti, esaminare i risultati e produrre report. Lungo il percorso, è possibile collaborare in modo sicuro con altri esperti dell'organizzazione per completare la richiesta di diritti dell'oggetto. È anche possibile gestire e personalizzare i flussi di lavoro aziendali con modelli predefiniti. Per altre informazioni sull'uso di queste funzionalità, vedere [Informazioni su Richieste di diritti degli interessati Priva](subject-rights-requests.md).

## <a name="priva-availability"></a>disponibilità Priva

Microsoft Priva è disponibile per i clienti di tutto il mondo. Se l'organizzazione ha effettuato il provisioning del tenant in uno dei data center locali elencati di seguito per soddisfare i requisiti di residenza dei dati, le soluzioni Priva non saranno disponibili nel riquadro di spostamento a sinistra del Portale di conformità di Microsoft Purview:

- Norvegia
- Polonia
- Qatar
- Singapore
- Sudafrica
- Corea del Sud
- Spagna
- Svezia
- Svizzera
- Emirati Arabi Uniti

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)

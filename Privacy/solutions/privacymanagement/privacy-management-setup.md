---
title: Introduzione alla gestione della privacy
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
- MET150fcf
description: Informazioni su come configurare la gestione della privacy per l'organizzazione, impostare ruoli e autorizzazioni e configurare impostazioni importanti.
ms.openlocfilehash: 0f64c581fbeb13726ee9ca2a0f695a5d4f55eb97
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478193"
---
# <a name="get-started-with-privacy-management"></a>Introduzione alla gestione della privacy

Se si è pronti a iniziare a usare la gestione della privacy Microsoft per assistenza nell'identificazione e nella mitigazione dei rischi per la privacy, seguire questa procedura per configurare i prerequisiti e iniziare a esplorare le informazioni dettagliate sulla privacy.

## <a name="step-1-confirm-subscriptions-and-licensing"></a>Passaggio 1: Confermare le sottoscrizioni e le licenze

La gestione della privacy è disponibile [nell'Centro conformità Microsoft 365](https://compliance.microsoft.com/) e può essere acquistata dalle organizzazioni con le licenze seguenti:

- Microsoft 365 E3, E5, A3, A5
- Office 365 E1, E3, E5, A1, A3, A5

La gestione della privacy offre opzioni di licenza per due diversi moduli della soluzione: richieste di rischi e diritti oggetto. Questi possono essere acquistati singolarmente o insieme. Quando si ottengono licenze per le richieste di diritti oggetto, è possibile scegliere il livello di licenza appropriato per il numero di richieste che è necessario gestire. È possibile acquistare richieste aggiuntive in qualsiasi momento.

Per indicazioni dettagliate sulle licenze, vedere [Indicazioni dettagliate sulle licenze di Microsoft 365 per la sicurezza e la conformità](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management).

> [!Note]
> La gestione della privacy non è disponibile per i clienti Community (GCC) Moderate, GCC High o Department of Defense (DoD).

### <a name="get-free-trial-license"></a>Ottenere la licenza di valutazione gratuita

È disponibile una licenza di valutazione gratuita per iniziare a usare la gestione della privacy. Per informazioni sull'idoneità e su come partecipare, vedi Informazioni sulla versione di valutazione gratuita per la [gestione della privacy.](privacy-management-trial.md)

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>Passaggio 2: Abilitare il Microsoft 365 di controllo

Microsoft 365 log di controllo sono un riepilogo di tutte le attività all'interno dell'organizzazione. I criteri di gestione della privacy possono usare queste attività per generare informazioni dettagliate sui criteri.

L'organizzazione potrebbe avere già attivato i log di controllo. Se è necessario iniziare a usarli per la prima volta, vedere Attivare o disattivare la ricerca nel [log](/microsoft-365/compliance/turn-audit-log-search-on-or-off) di controllo per istruzioni dettagliate per attivare il controllo. Dopo l'abilitazione, verrà visualizzato un messaggio che indica che è in corso la preparazione del log di controllo e che sarà possibile eseguire una ricerca in un paio d'ore, dopo il completamento della preparazione. Questa procedura deve essere eseguita una sola volta. Per ulteriori informazioni sull'utilizzo del Microsoft 365 di controllo, vedere [Search the audit log](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

## <a name="step-3-set-user-permissions-and-assign-roles"></a>Passaggio 3: Impostare le autorizzazioni utente e assegnare ruoli

La gestione della privacy utilizza un modello di autorizzazione RBAC (Role-Based Access Control). Solo gli utenti assegnati a un ruolo possono accedere alla gestione della privacy e le azioni consentite da ogni utente sono limitate per tipo di ruolo.

L'amministratore globale dispone delle autorizzazioni per accedere alla gestione della privacy e assegnare altri utenti ai ruoli. Possono accedere e impostare le autorizzazioni utente nella [Centro conformità Microsoft 365](https://compliance.microsoft.com/) per la gestione della privacy. Per iniziare rapidamente, il gruppo di ruoli Gestione privacy dispone delle autorizzazioni per accedere a tutte le funzionalità di gestione della privacy. Questo gruppo può essere adatto alle organizzazioni in cui lo stesso individuo può eseguire tutti i compiti all'interno della soluzione di gestione della privacy. Altri ruoli di privacy consentono di assumere un controllo più granulare e assegnare gli utenti a funzionalità o funzioni selezionate.

Per ulteriori informazioni sui gruppi di ruoli e su come concedere l'accesso, vedere [Set user permissions and assign roles](privacy-management-permissions.md).

## <a name="step-4-start-finding-and-visualizing-your-data"></a>Passaggio 4: iniziare a trovare e visualizzare i dati

Dopo l'accesso alla gestione della privacy, verrà visualizzata la **pagina Panoramica.** Questa pagina fornisce informazioni dettagliate dinamiche sull'evoluzione dei dati personali nell'ambiente Microsoft 365 per individuare rapidamente i problemi, identificare gli indicatori di rischio e intervenire per risolvere i problemi. La panoramica dovrebbe essere popolata con informazioni dettagliate iniziali entro le prime 24 ore dalla registrazione. Continuando a usare la gestione della privacy, la pagina di panoramica verrà aggiornata per continuare a fornire informazioni aggiornate.

Per ulteriori approfondimenti sui dati  nel tempo, la pagina del profilo dati fornirà più visualizzazioni e analisi e fornirà una visualizzazione olistica dei dati dell'organizzazione in base alla posizione geografica e Microsoft 365 geografica.

Per altre informazioni su queste pagine, vedi [Trovare e visualizzare i dati.](privacy-management-data-profile.md)

## <a name="step-5-start-managing-risks-with-default-policies"></a>Passaggio 5: iniziare a gestire i rischi con i criteri predefiniti

La gestione della privacy inizierà a valutare i dati e darà un'occhiata agli scenari di rischio chiave per la minimizzazione dei dati, la sovraesposizione dei dati e i trasferimenti di dati. Questi criteri sono attivati per impostazione predefinita. È possibile utilizzare questi criteri per valutare la posizione dei rischi, quindi attivare le notifiche tramite posta elettronica degli utenti per attirare l'attenzione degli utenti e guidare la correzione di tali rischi. Inoltre, è possibile creare e personalizzare i propri criteri dai modelli di criteri forniti. È possibile personalizzare i criteri per soddisfare le esigenze di conformità legale e normativa dell'organizzazione, come potrebbe essere identificato in consultazione con i consulenti legali. Per ulteriori informazioni, vedere [Gestire i rischi per la privacy con i criteri nella gestione della privacy.](privacy-management-policies.md)

## <a name="step-6-get-started-with-subject-rights-requests"></a>Passaggio 6: Introduzione alle richieste di diritti dell'oggetto

La gestione della privacy automatizza il processo di evasione delle richieste di diritti dell'oggetto con un facile accesso ai dati e ai flussi di lavoro personalizzabili che rientrano nei processi aziendali esistenti. È possibile trovare facilmente i dati rilevanti, esaminare i risultati e produrre report. Lungo il percorso, è possibile collaborare in modo sicuro con altri esperti dell'organizzazione per completare la richiesta di diritti dell'oggetto. È inoltre possibile gestire e personalizzare i flussi di lavoro aziendali con modelli predefiniti. Per ulteriori informazioni sull'utilizzo di queste funzionalità, vedere [Manage subject rights requests.](privacy-management-subject-rights-requests.md)

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

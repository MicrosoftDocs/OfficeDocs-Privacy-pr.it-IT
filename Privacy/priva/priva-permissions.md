---
title: Impostare le autorizzazioni utente e assegnare ruoli in Microsoft Priva
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
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: Informazioni su come configurare le autorizzazioni Microsoft Priva e assegnare gli utenti ai gruppi di ruoli.
ms.openlocfilehash: eca08327e2db909475dbf4c072b8f6843de3d57b
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678223"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>Impostare le autorizzazioni utente e assegnare ruoli in Microsoft Priva

Per concedere ai membri dell'organizzazione le autorizzazioni per l'uso di Microsoft Priva, assegnarli ai gruppi di ruoli appropriati nel Portale di conformità di Microsoft Purview.

> [!NOTE]
> La maggior parte dei ruoli Priva è attualmente designata come "gestione della privacy". Per un elenco completo, vedere di seguito. I ruoli specifici di Priva non verranno visualizzati in Azure Active Directory.

## <a name="sign-in-and-set-permissions"></a>Accedere e impostare le autorizzazioni

1. Passare alla [Portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) e selezionare **Autorizzazioni** nel riquadro di spostamento a sinistra.  
2. Nell'elenco a discesa **soluzioni Microsoft Purview** selezionare **Ruoli**. Verrà visualizzato l'elenco completo dei gruppi di ruoli.
3. Trovare il gruppo di ruoli a cui si desidera aggiungere uno o più utenti (vedere le descrizioni del gruppo di ruoli di seguito) e selezionare la casella a sinistra del nome del gruppo.
4. Nel riquadro a comparsa per il gruppo selezionare **Modifica** nell'intestazione **Membri**.  
5. Nel riquadro a comparsa selezionare **Scegli membri** nel riquadro di spostamento sinistro. Verrà visualizzata un'altra finestra a comparsa.
6. Selezionare **+ Aggiungi** per scegliere uno o più utenti da aggiungere al gruppo.  
7. Selezionare la casella di controllo accanto ai nomi da aggiungere e quindi selezionare il pulsante **Aggiungi** nella parte inferiore.  
8. Al termine dell'assegnazione degli utenti, selezionare **Fine**, quindi **Salva** e quindi **Chiudi**.

## <a name="learn-more-about-role-groups-and-roles"></a>Altre informazioni su gruppi di ruoli e ruoli

A seconda della struttura del team, è possibile assegnare gli utenti a gruppi di ruoli specifici per gestire diversi set di funzionalità Priva. I membri devono essere assegnati ai gruppi di ruoli a seconda delle attività che devono eseguire e del livello di accesso ai file appropriato. Ogni gruppo di ruoli include uno o più ruoli. Questi ruoli possono riguardare attività di Priva specifiche o funzioni chiave abilitate o limitate per i membri del gruppo. Utenti diversi possono quindi avere diversi livelli di visibilità e accesso a determinate funzionalità di Priva.

I gruppi di ruoli possono essere personalizzati, se necessario. Per evitare la perdita accidentale dell'accesso, è consigliabile creare una copia del gruppo di ruoli esistente da personalizzare, assegnare alla copia un nome identificabile, apportare e verificare le modifiche apportate al nuovo gruppo e assegnarvi le persone in base alle esigenze.

## <a name="privacy-management-role-group"></a>Gruppo di ruoli Gestione privacy

Questo gruppo contiene tutti i ruoli di autorizzazione Priva in un singolo gruppo. Questo gruppo di ruoli può essere adatto alle organizzazioni in cui lo stesso individuo può svolgere tutti i compiti. L'appartenenza a questo gruppo di ruoli concederà a tale account l'accesso completo a tutte le funzionalità di Priva per cui si dispone di una licenza.

È consigliabile assicurarsi che sia sempre presente almeno un membro attivo di questo gruppo.

I ruoli includono:

- Gestione dei casi  
- Visualizzatore contenuto classificazione dati  
- Visualizzatore elenco classificazione dati  
- Amministrazione gestione della privacy  
- Analisi della gestione della privacy  
- Indagine sulla gestione della privacy  
- Contributo permanente alla gestione della privacy  
- Contributo temporaneo alla gestione della privacy  
- Visualizzatore gestione privacy  
- Amministrazione di richiesta di diritti dell'interessato  
- caso View-Only

## <a name="privacy-management-administrators-role-group"></a>Gruppo di ruoli Amministratori gestione privacy

I membri di questo gruppo di ruoli hanno un ampio accesso alle funzioni di Priva, tra cui la creazione, la lettura, l'aggiornamento e l'eliminazione di criteri di gestione dei rischi per la privacy, richieste di diritti dell'interessato, autorizzazioni e impostazioni.

I ruoli includono:

- Gestione dei casi  
- Amministrazione gestione della privacy  
- caso View-Only

## <a name="privacy-management-analysts-role-group"></a>Gruppo di ruoli Analisti di gestione della privacy

I membri di questo gruppo di ruoli fungono da analisti del caso. Possono analizzare le corrispondenze dei criteri, visualizzare i metadati dei file ed eseguire azioni correttive. Questo gruppo non può accedere ai file completi tramite Esplora contenuto.

I ruoli includono:

- Gestione dei casi  
- Visualizzatore elenco classificazione dati  
- Analisi della gestione della privacy  
- caso View-Only

### <a name="privacy-management-investigators-role-group"></a>Gruppo di ruoli Investigatori per la gestione della privacy

I membri di questo gruppo agiscono come investigatori dei dati. Possono analizzare le corrispondenze dei criteri, visualizzare il contenuto del file associato ed eseguire azioni correttive. Questo gruppo può accedere ai file tramite Esplora contenuto.

I ruoli includono:

- Gestione dei casi  
- Visualizzatore contenuto classificazione dati  
- Visualizzatore elenco classificazione dati  
- Indagine sulla gestione della privacy  
- caso View-Only

## <a name="privacy-management-viewer-role-group"></a>Gruppo di ruoli Visualizzatore gestione privacy

I membri di questo gruppo possono visualizzare informazioni analitiche in Priva, ad esempio la panoramica, il profilo dati e i report sulle richieste dell'interessato.

I ruoli includono:

- Visualizzatore gestione privacy

## <a name="subject-rights-request-administrators-role-group"></a>Gruppo di ruoli Subject Rights Request Administrators

I membri di questo gruppo hanno accesso completo per amministrare e creare richieste di diritti dell'oggetto.

I ruoli includono:

- Amministrazione di richiesta di diritti dell'interessato

## <a name="privacy-management-contributors-role-group"></a>Gruppo di ruoli Collaboratori alla gestione della privacy

I membri di questo gruppo hanno accesso alle richieste di diritti soggetti per cui sono stati aggiunti come collaboratore.  

I ruoli includono:

- Contributo temporaneo alla gestione della privacy  
- Contributo permanente alla gestione della privacy

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)
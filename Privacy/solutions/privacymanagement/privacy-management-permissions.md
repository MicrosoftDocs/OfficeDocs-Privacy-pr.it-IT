---
title: Impostare le autorizzazioni utente e assegnare ruoli nella gestione della privacy
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
- MET150
description: Informazioni su come configurare le autorizzazioni di gestione della privacy e assegnare gli utenti ai gruppi di ruoli.
ms.openlocfilehash: 52ffb6ee47aea93f906e1356abf61979eca34787
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478258"
---
# <a name="set-user-permissions-and-assign-roles-in-privacy-management"></a>Impostare le autorizzazioni utente e assegnare ruoli nella gestione della privacy

Per concedere ai membri dell'organizzazione le autorizzazioni per l'utilizzo della gestione della privacy, assegnarli ai gruppi di ruoli appropriati nella Centro conformità Microsoft 365. Tieni presente che i ruoli specifici per la gestione della privacy non verranno visualizzati Azure Active Directory.

## <a name="sign-in-and-set-permissions"></a>Accedere e impostare le autorizzazioni

1. Vai al riquadro [Centro conformità Microsoft 365](https://compliance.microsoft.com/) e seleziona **Autorizzazioni** nel riquadro di spostamento a sinistra.  
2. **Nell'elenco a discesa Centro** conformità selezionare **Ruoli**. Verrà visualizzato l'elenco completo dei gruppi di ruoli.
3. Individuare il gruppo di ruoli a cui si desidera aggiungere uno o più utenti e selezionare la casella a sinistra del nome del gruppo. Vedi di seguito per un elenco dei ruoli di gestione della privacy.  
4. Nel riquadro a comparsa del gruppo selezionare **Modifica nell'intestazione** Membri.   
5. Selezionare **Scegli membri**. Verrà visualizzata un'altra finestra a comparsa.
6. Selezionare **+ Aggiungi** per scegliere uno o più utenti da aggiungere al gruppo.  
7. Seleziona la casella di controllo accanto ai nomi che vuoi aggiungere, quindi seleziona il **pulsante** Aggiungi nella parte inferiore.  
8. Al termine dell'assegnazione degli utenti, selezionare **Fine,** **quindi Salva** e **chiudi.**

## <a name="learn-more-about-role-groups-and-roles"></a>Ulteriori informazioni sui gruppi di ruoli e sui ruoli

A seconda della struttura del team, sono disponibili opzioni per assegnare utenti a gruppi di ruoli specifici per gestire set diversi di funzionalità di gestione della privacy. I membri devono essere assegnati ai gruppi di ruoli a seconda delle attività da eseguire e del livello di accesso ai file appropriato. Ogni gruppo di ruoli include uno o più ruoli. Questi ruoli possono riguardare specifiche attività di gestione della privacy o funzioni chiave abilitate o limitate per i membri del gruppo. Utenti diversi possono pertanto avere diversi livelli di visibilità e accesso a determinate funzionalità di gestione della privacy.

I gruppi di ruoli possono essere personalizzati, se necessario. Per evitare la perdita accidentale dell'accesso, è consigliabile creare una copia del gruppo di ruoli esistente che si desidera personalizzare, assegnare alla copia un nome identificabile, apportare e verificare le modifiche apportate al nuovo gruppo e assegnare le persone a tale gruppo nel modo appropriato.

## <a name="privacy-management-role-group"></a>Gruppo di ruoli Gestione privacy

Questo gruppo contiene tutti i ruoli di autorizzazione per la gestione della privacy in un singolo gruppo. Questo gruppo di ruoli può essere adatto alle organizzazioni in cui lo stesso individuo può eseguire tutti i compiti all'interno della soluzione di gestione della privacy. Se si fornisce l'appartenenza a questo gruppo di ruoli, all'account verrà concesso l'accesso completo a tutte le funzionalità della soluzione di gestione della privacy.

È consigliabile verificare che vi sia sempre almeno un membro attivo di questo gruppo.

I ruoli includono:

- Gestione dei casi  
- Visualizzatore contenuto classificazione dati  
- Visualizzatore elenco classificazione dati  
- Amministratore gestione privacy  
- Analisi della gestione della privacy  
- Indagine sulla gestione della privacy  
- Contributo permanente per la gestione della privacy  
- Contributo temporaneo sulla gestione della privacy  
- Visualizzatore gestione privacy  
- Amministratore richiesta diritti soggetto  
- View-Only caso

## <a name="privacy-management-administrators-role-group"></a>Gruppo di ruoli Amministratori gestione privacy

I membri di questo gruppo di ruoli dispongono di un ampio accesso alle funzioni di gestione della privacy, tra cui la creazione, la lettura, l'aggiornamento e l'eliminazione dei criteri di gestione della privacy, le richieste di diritti dell'oggetto, le autorizzazioni per la gestione della privacy e le impostazioni di gestione della privacy.

I ruoli includono:

- Gestione dei casi  
- Amministratore gestione privacy  
- View-Only caso

## <a name="privacy-management-analysts-role-group"></a>Gruppo di ruoli Privacy Management Analysts

I membri di questo gruppo di ruoli fungono da analisti dei casi di gestione della privacy. Possono analizzare le corrispondenze dei criteri, visualizzare i metadati dei file ed eseguire azioni correttive. Questo gruppo non può accedere ai file completi tramite Esplora contenuto.

I ruoli includono:

- Gestione dei casi  
- Visualizzatore elenco classificazione dati  
- Analisi della gestione della privacy  
- View-Only caso

### <a name="privacy-management-investigators-role-group"></a>Gruppo di ruoli Privacy Management Investigators

I membri di questo gruppo agiscono come investigatori dei dati di gestione della privacy. Possono analizzare le corrispondenze dei criteri, visualizzare il contenuto del file associato ed eseguire azioni correttive. Questo gruppo può accedere ai file tramite Esplora contenuto.

I ruoli includono:

- Gestione dei casi  
- Visualizzatore contenuto classificazione dati  
- Visualizzatore elenco classificazione dati  
- Indagine sulla gestione della privacy  
- View-Only caso

## <a name="privacy-management-viewer-role-group"></a>Gruppo di ruoli Visualizzatore gestione privacy

I membri di questo gruppo possono visualizzare le informazioni analitiche nella gestione della privacy, ad esempio la panoramica, il profilo dati e i report sulle richieste dell'oggetto.

I ruoli includono:

- Visualizzatore gestione privacy

## <a name="subject-rights-request-administrators-role-group"></a>Gruppo di ruoli Subject Rights Request Administrators

I membri di questo gruppo hanno accesso completo per amministrare e creare richieste di diritti dell'oggetto.

I ruoli includono:

- Amministratore richiesta diritti soggetto

## <a name="privacy-management-contributors-role-group"></a>Gruppo di ruoli Privacy Management Contributors

I membri di questo gruppo hanno accesso alle richieste di diritti dell'oggetto per le quali sono stati aggiunti come collaboratori.  

I ruoli includono:

- Contributo temporaneo sulla gestione della privacy  
- Contributo permanente per la gestione della privacy

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)
---
title: Creare una richiesta di diritti dell'oggetto nella gestione della privacy
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
description: Scopri come creare una nuova richiesta di diritti dell'oggetto nella gestione della privacy.
ms.openlocfilehash: 316d515be454b6aceed95f68c6f3da6fa0e7567c
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478247"
---
# <a name="create-a-subject-rights-request"></a>Creare una richiesta di diritti dell'oggetto

Gli amministratori di Subject Rights Management possono aprire nuove richieste di diritti dell'oggetto tramite la pagina principale delle richieste di diritti dell'oggetto della gestione della privacy. Una procedura guidata guiderà l'utente attraverso il processo di ricerca dei dati personali su un soggetto di dati e l'avvio del processo di evasione della richiesta.

Puoi anche scegliere di caricare materiale aggiuntivo per consentire la gestione della privacy per identificare gli interessati in base a valori di dati forniti esatti. Per ulteriori informazioni, vedere [Manage data matching.](privacy-management-subject-rights-requests-data-matching.md)

## <a name="use-the-subject-rights-request-creation-wizard"></a>Usare la procedura guidata per la creazione di richieste di diritti dell'oggetto

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/), passare alla sezione Gestione della privacy e selezionare **Richieste di diritti dell'oggetto**.
1. Per avviare una nuova richiesta, selezionare **Crea una richiesta.**
1. Identificare l'utente che ha effettuato la richiesta e specificare la relazione con l'azienda.
1. Verrà eseguita una ricerca predefinita per gli elementi correlati all'oggetto dati. Se si desidera affinare la ricerca o ottenere una stima prima di recuperare i dati, è possibile effettuare queste selezioni in questa fase. Puoi anche lasciare vuoti tutti gli elementi e passare al passaggio successivo. Per ulteriori informazioni sulle opzioni, vedere [Definire le impostazioni di ricerca](#define-search-settings) e [Perfezionare la ricerca.](#refine-your-search)
1. Scegli un tipo di richiesta in base alle attività che l'utente vuole che tu faccia con i loro dati. Se la richiesta si riferisce a una specifica normativa sulla privacy dei dati, puoi anche selezionarla da un elenco fornito per aggiungere altro contesto. L'impostazione di una scadenza (obbligatoria) semplifica l'ordinamento delle richieste in arrivo o scadute e la risoluzione delle richieste in modo rapido. I tipi di richiesta includono:
   - **Access**: fornisce un riepilogo delle informazioni personali dell'utente tenuto dall'organizzazione in Microsoft 365.
   - **Export**: fornisce un riepilogo e un'esportazione delle informazioni personali dell'oggetto dati, come raccolto e annotato durante la revisione.
   - **Elenco con tag per il follow-up**: genera un riepilogo di tutti i file tag dagli utenti durante la revisione che potrebbero richiedere ulteriori azioni al di fuori della gestione della privacy. Ad esempio, potrebbe essere necessario facilitare l'eliminazione delle informazioni personali dell'oggetto dei dati in base alla loro richiesta. I tag di revisione dei dati personalizzati per le richieste di diritti dell'oggetto possono essere gestiti in **Impostazioni.**
1. Confermare il nome della richiesta e aggiungere una descrizione facoltativa come riferimento.
1. Esaminare il riepilogo degli elementi immessi durante i passaggi precedenti. È possibile modificare qualsiasi campo prima di selezionare **Crea richiesta.**

### <a name="define-search-settings"></a>Definire le impostazioni di ricerca

Durante la creazione di una richiesta di diritti dell'oggetto, è possibile scegliere una o tutte queste opzioni di ricerca per trovare i dati relativi all'oggetto:

- **Includere il contenuto creato dall'oggetto dei** dati: include il contenuto creato dall'oggetto dei dati e può restituire un volume di dati superiore.
- **Affinare la ricerca:** in questo modo è possibile specificare proprietà aggiuntive che consentono di identificare l'oggetto dei dati. Qui puoi impostare l'ambito della ricerca su Microsoft 365 o risorse specifiche oppure selezionare altre condizioni per modificare l'ambito della richiesta. Dopo aver scelto questa opzione, verrà richiesto di immettere i parametri di ricerca personalizzati.
- **Ottenere prima una stima:** in questo modo è possibile visualizzare la quantità di dati che ci si aspetta di trovare prima che i dati vengono recuperati automaticamente.

### <a name="refine-your-search"></a>Perfezionare la ricerca

Se si è scelto di perfezionare la ricerca durante la definizione delle impostazioni di ricerca, verrà richiesto di immettere i parametri di ricerca avanzati. Puoi aggiungere **identificatori, impostare condizioni**  **e** scegliere posizioni specifiche all'interno Microsoft 365 ricerca.

- **Aggiungere identificatori:** fornire ulteriori informazioni di identificazione sull'oggetto dei dati, ad esempio nomi, indirizzi di posta elettronica e/o altre opzioni. Separare più valori in ogni campo con un punto e virgola.
- **Condizioni**: iniziare ad aggiungere condizioni per la ricerca scegliendo un tipo nell'elenco a discesa. Questi tipi corrispondono alle possibili proprietà dei dati, ad esempio l'intervallo di tempo, le dimensioni, le etichette di conservazione, i mittenti e i destinatari e molti altri. Selezionare un tipo per aggiungerlo e quindi impostare le proprietà desiderate. Per le voci di campo di testo, è possibile aggiungere più parole chiave separate da punti e virgola. È possibile aggiungere tutti i tipi di contenuto che si desidera.
- **Percorsi**: è possibile impostare l'ambito della ricerca in modo da SharePoint siti, Teams canali e OneDrive for Business specifici. Per ogni posizione è possibile selezionare tutte le istanze, ad esempio tutte Exchange cassette postali, o istanze specifiche, ad esempio la cassetta postale di un utente. Selezionare il **collegamento Scegli...** per ogni posizione per immettere informazioni su istanze specifiche. Per informazioni sull'identificazione dei termini di ricerca appropriati, vedere quanto segue:
  - [Manage sites in the new SharePoint admin center](/sharepoint/manage-sites-in-new-admin-center): Vengono fornite indicazioni su come ordinare e filtrare i siti e su come cercare un SharePoint sito. Usa questa opzione per trovare gli URL per il SharePoint di ricerca.
  - [Get-Team](/powershell/module/teams/get-team): fornisce informazioni su come trovare i team in Microsoft Teams in base a proprietà/informazioni specifiche. Utilizzare questa opzione per identificare Teams chat e canali.
  - [Informazioni OneDrive URL:](/onedrive/list-onedrive-urls#about-onedrive-urls)fornisce informazioni sul formato e sulle proprietà appropriate per l'URL di OneDrive di un utente. Utilizzare questa opzione per identificare OneDrive siti nella ricerca.

Ti consigliamo di esaminare attentamente le selezioni per assicurarti di identificare l'oggetto dei dati corretto. Ad esempio, se si ricercano le cassette postali per nome e si trovano più persone con nomi simili, verificare quella corretta prima di aggiungerle alla richiesta.

## <a name="next-steps"></a>Passaggi successivi

Dopo aver creato la richiesta, la vedrai elencata nella pagina della richiesta di diritti dell'oggetto. Per ulteriori informazioni su come procedere con la revisione, vedere [Esaminare i dati e collaborare alle richieste.](privacy-management-subject-rights-requests-review.md)

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale sulla gestione della privacy](privacy-management-disclaimer.md)

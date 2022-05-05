---
title: Creare una richiesta di diritti dell'oggetto
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
description: Informazioni su come creare una nuova richiesta di diritti soggetto in Microsoft Priva.
ms.openlocfilehash: af772d585e3e9b554f42f6adde99bba19173ee03
ms.sourcegitcommit: 6b88d22d0250cbb9a4ba1f71665f29cb67939851
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2022
ms.locfileid: "65059730"
---
# <a name="create-a-subject-rights-request"></a>Creare una richiesta di diritti dell'oggetto

Gli amministratori di Subject Rights Management possono aprire nuove richieste tramite la pagina principale di Priva Subject Rights Requests. Una procedura guidata guiderà l'utente nel processo di ricerca dei dati personali relativi a un interessato e di avvio del processo di esecuzione della richiesta.

È anche possibile scegliere di caricare materiale aggiuntivo per consentire a Priva di identificare gli interessati in base a valori di dati specificati esatti. Per altre informazioni, vedere [Corrispondenza dei dati per le richieste di diritti dell'interessato](subject-rights-requests-data-match.md).

## <a name="request-types"></a>Tipi di richiesta

Priva Subject Rights Requests supporta tre diversi tipi di richieste:

1. **Accesso**: fornisce un riepilogo delle informazioni personali dell'interessato contenute nell'organizzazione in Microsoft 365.

2. **Esportazione**: fornisce un riepilogo e un file esportato di elementi di contenuto che contengono le informazioni personali dell'interessato. Questi sono gli elementi esaminati e contrassegnati come **Inclusi** durante la revisione dei dati raccolti dalle impostazioni di ricerca.

3. **Elenco con tag per il completamento**: genera un riepilogo di tutti i file contrassegnati durante la revisione dei dati che potrebbero richiedere un'azione aggiuntiva all'esterno di Priva. Ad esempio, potrebbe essere necessario facilitare l'eliminazione delle informazioni personali dell'interessato in base alla richiesta. È possibile visualizzare i tag inclusi e configurare tag personalizzati per l'organizzazione in [Impostazioni Priva](priva-settings.md).

## <a name="getting-started-with-your-first-request"></a>Introduzione alla prima richiesta

Quando si avvia una versione di valutazione o una sottoscrizione di Richieste di diritti dell'oggetto, viene offerta una configurazione semplice e predefinita per la prima richiesta che usa le impostazioni predefinite. Questa configurazione consente di esplorare il flusso di lavoro della richiesta di diritti dell'oggetto e acquisire familiarità con le relative funzionalità.

La prima volta che si arriva alla pagina Richieste di diritti dell'oggetto, verrà visualizzato un banner nella parte superiore con un pulsante **di Attività iniziali**. Quando un utente seleziona questo pulsante, viene visualizzato un riquadro a comparsa con le informazioni dell'utente prepopolato nei campi nome e posta elettronica e vengono visualizzate tutte le impostazioni predefinite.

**Esplorazione della funzionalità di richiesta con le informazioni**: provare una richiesta di diritti dell'oggetto in base alle proprie informazioni può aiutare a acquisire familiarità e comfort nello spostamento in ogni fase del processo. Si vedrà quale yeilds di ricerca predefinita e può esercitarsi a perfezionare i risultati modificando le impostazioni di ricerca. Nella scheda **Dati raccolti** è possibile esaminare gli elementi nell'area di anteprima a destra e praticare la redazione di testo, l'applicazione di tag, l'immissione di note e l'contrassegno di elementi da includere o escludere per il report finale.Trovare i dettagli in [Rivedi i dati per una richiesta di diritti dell'interessato](subject-rights-requests-data-review.md).

- Non è necessario usare le informazioni per creare la prima richiesta. Se si è pronti per avviare una richiesta per un interessato, sostituire semplicemente il nome e l'indirizzo di posta elettronica con le informazioni dell'interessato.

Per accettare tutte le impostazioni e creare la richiesta, selezionare **Crea**. Il riquadro verrà chiuso e la nuova richiesta verrà visualizzata nella pagina **Richieste di diritti dell'oggetto** . Per modificare una delle impostazioni predefinite prima di creare la richiesta, selezionare **Modifica dettagli richiesta**, che consente di accedere alla [creazione guidata della richiesta con diritti dell'oggetto](#use-the-subject-rights-request-creation-wizard).

> [!NOTE]
> Qualsiasi richiesta creata verrà conteggiata per l'assegnazione della sottoscrizione di valutazione o a pagamento, indipendentemente dalle informazioni dell'interessato usate per la richiesta. Il periodo di conservazione dei dati standard di 30 giorni si applica dopo la chiusura della richiesta. Informazioni su come modificare i [periodi di conservazione per le richieste di diritti dell'oggetto](subject-rights-requests-reports.md#retention-periods-for-reports-and-data).

## <a name="use-the-subject-rights-request-creation-wizard"></a>Usare la creazione guidata della richiesta di diritti dell'oggetto

1. Nel [portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) passare alla sezione Priva e selezionare **Priva Subject Rights Requests (Richieste di diritti soggetti privati**).
1. Per avviare una nuova richiesta, selezionare **Crea una richiesta**.
1. Identificare l'interessato che ha effettuato la richiesta e specificare la relazione con l'azienda.
1. Verrà eseguita una ricerca predefinita per gli elementi correlati all'interessato. Se si vuole perfezionare la ricerca o ottenere una stima prima di recuperare i dati, è possibile effettuare queste selezioni in questa fase. È anche possibile lasciare vuoti tutti gli elementi e passare al passaggio successivo. Per altre informazioni sulle opzioni, vedere [Definire le impostazioni di ricerca](#define-search-settings) e [Perfezionare la ricerca](#refine-your-search).
1. Scegliere un tipo di richiesta in base alle operazioni che l'interessato vuole eseguire con i dati. Se la richiesta riguarda un regolamento specifico sulla privacy dei dati, è anche possibile selezionarla da un elenco specificato per aggiungere altro contesto. L'impostazione di una scadenza (obbligatoria) semplifica l'ordinamento per l'avvicinamento o la scadenza delle richieste e la risoluzione tempestiva delle richieste. I tipi di richiesta includono:
   - **Accesso**: fornisce un riepilogo delle informazioni personali dell'interessato contenute nell'organizzazione in Microsoft 365.
   - **Esportazione**: fornisce un riepilogo e un'esportazione delle informazioni personali dell'interessato, raccolte e annotate durante la revisione.
   - **Elenco con tag per il completamento**: genera un riepilogo di tutti i file contrassegnati dagli utenti durante la revisione che potrebbero richiedere un'azione aggiuntiva all'esterno di Priva. Ad esempio, potrebbe essere necessario facilitare l'eliminazione delle informazioni personali dell'interessato in base alla richiesta. I tag di revisione dei dati personalizzati per le richieste di diritti degli interessati possono essere gestiti in **Impostazioni globali.**
1. Confermare il nome di questa richiesta e aggiungere una descrizione facoltativa per riferimento.
1. Esaminare il riepilogo degli elementi immessi durante i passaggi precedenti. È possibile modificare qualsiasi campo prima di selezionare **Crea richiesta**.

Per ogni richiesta di diritti dell'oggetto, è possibile impostare la ricerca per cercare i dati in tutte le posizioni o in posizioni specifiche all'interno di Exchange e Sharepoint. Scegliere una posizione spostando il relativo interruttore di attivazione/disattivazione nella posizione **Sì** . È possibile scegliere di cercare tutti gli account e i siti o di designare account o siti specifici all'interno di ogni posizione. Leggere i dettagli seguenti su ciò che viene trattato in ogni posizione.

- **Exchange**: questa opzione cercherà i dati nelle cassette postali Exchange e nelle chat Teams individuali o di gruppo. È possibile scegliere di cercare tutti gli account Exchange nell'organizzazione oppure selezionare **Scegli account** per selezionare singoli utenti nel riquadro a comparsa **Exchange cassette postali**.

- **SharePoint**: questa opzione cercherà i dati in siti SharePoint, siti OneDrive for Business e canali di Teams. È possibile scegliere di eseguire ricerche in tutti i siti SharePoint dell'organizzazione oppure selezionare **Scegli siti** per selezionare singoli utenti nel riquadro a comparsa **SharePoint siti**.

Per informazioni sull'identificazione dei termini di ricerca appropriati, vedere gli argomenti seguenti:

- **SharePoint siti e URL**: [Gestire i siti nell'interfaccia di amministrazione SharePoint](/sharepoint/manage-sites-in-new-admin-center) fornisce indicazioni su come ordinare e filtrare i siti e su come cercare un sito SharePoint. Usare questa opzione per trovare gli URL da immettere nel campo di ricerca nel riquadro a comparsa **SharePoint siti**.

- **Teams chat e canali**: [Get-Team](/powershell/module/teams/get-team) mostra come trovare i team in Microsoft Teams fornendo proprietà o informazioni specifiche.

- **OneDrive siti e URL**: [Informazioni sugli URL OneDrive](/onedrive/list-onedrive-urls#about-onedrive-urls) fornisce informazioni sul formato e sulle proprietà appropriati per l'URL di OneDrive di un utente. Usare questa opzione per identificare OneDrive siti nella ricerca.

È consigliabile esaminare attentamente le selezioni per assicurarsi di identificare l'interessato corretto. Ad esempio, se si esegue una ricerca nelle cassette postali per nome e si trovano più persone con nomi simili, verificare quella corretta prima di aggiungerle alla richiesta.

## <a name="define-search-settings"></a>Definire le impostazioni di ricerca

Quando si crea una richiesta di diritti dell'oggetto, verrà eseguita una ricerca predefinita in base alle selezioni nella pagina **Percorsi** della creazione guidata. Se si vuole eseguire una ricerca più mirata o se si vuole ottenere una stima dei dati prima del recupero degli elementi di contenuto, è possibile effettuare tali selezioni nella pagina **Impostazioni di ricerca** della creazione guidata richiesta.

### <a name="advanced-search-options"></a>Opzioni di ricerca avanzate

- **Perfezionare la ricerca**: questa opzione consente di specificare proprietà aggiuntive per identificare l'interessato tra i dati dell'organizzazione. Dopo aver scelto questa opzione, verrà richiesto di aggiungere altri parametri di ricerca, illustrati di seguito in [Perfezionare la ricerca](#refine-your-search).
- **Includi contenuto creato dall'interessato**: questa opzione cercherà il contenuto creato dall'interessato. Gli esempi includono i file creati dall'interessato o caricati in SharePoint dall'interessato. La selezione di questa opzione può aumentare significativamente la quantità di dati restituiti.
- **Includi tutte le versioni degli elementi**: se è stato selezionato SharePoint come percorso di ricerca, la query di ricerca predefinita restituirà solo la versione corrente degli elementi SharePoint. Se si seleziona questa casella, verranno restituite le versioni correnti e tutte le versioni precedenti degli elementi SharePoint, generando una quantità di dati significativamente maggiore da esaminare.

### <a name="data-estimate"></a>Stima dei dati

L'opzione **Ottieni una prima stima** presenterà una stima della quantità di dati che si prevede di trovare prima che i dati vengano recuperati automaticamente. Quando la stima viene visualizzata nella pagina dei dettagli della richiesta, è possibile scegliere di visualizzare i risultati della ricerca e visualizzare in anteprima un campionamento degli elementi individuati. Se gli elementi rappresentano i risultati previsti, è necessario selezionare **Recupera dati** per procedere con il recupero effettivo degli elementi di contenuto.

## <a name="refine-your-search"></a>Perfezionare la ricerca

Se si sceglie **Affina la ricerca** nella pagina **Impostazioni di ricerca** , quando si seleziona **Avanti** verrà richiesto di specificare i dettagli per gli attributi e le condizioni personali per indirizzare ulteriormente i risultati della ricerca. È possibile aggiungere aggiunte in una o in entrambe le categorie. Al termine delle selezioni in questa sezione, il recupero dei dati per la richiesta si baserà sulle impostazioni di ricerca.

#### <a name="add-personal-attributes"></a>Aggiungere attributi personali

Immettere i valori nei campi di testo per i nomi, i nomi alternativi, gli indirizzi di posta elettronica e l'indirizzo dell'interessato. È possibile aggiungere altri identificatori, ad esempio la data di nascita o il numero di telefono, e i campi di testo supportano più voci separate da un punto e virgola. Al termine, selezionare **Avanti** per continuare con la pagina **Condizioni** .

#### <a name="conditions"></a>Condizioni

Selezionare il pulsante **Aggiungi condizione** per scegliere tra un intervallo di condizioni per indirizzare ulteriormente la ricerca, tra cui il nome dell'elemento, i nomi del mittente e del destinatario, il tipo di dati personali e se l'elemento è stato condiviso esternamente all'esterno dell'organizzazione. I campi di testo supportano più voci separate da un punto e virgola. Al termine, selezionare **Avanti** per salvare le impostazioni di ricerca e passare all'impostazione del tipo di richiesta.

## <a name="next-steps"></a>Passaggi successivi

Dopo aver creato la richiesta, verrà visualizzata nella pagina relativa alla richiesta di diritti dell'oggetto. Per altre informazioni su come procedere con la revisione, vedere [Esaminare i dati e collaborare alle richieste](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

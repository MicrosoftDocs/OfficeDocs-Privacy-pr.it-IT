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
description: Informazioni su come creare una nuova richiesta di diritti dell'oggetto in Microsoft Priva.
ms.openlocfilehash: 9de1047950a556b4456fd4453ea8d860a0a01c38
ms.sourcegitcommit: 16dd1c0320bf1c58ad75edbbe2113fc79013f504
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/25/2022
ms.locfileid: "64404610"
---
# <a name="create-a-subject-rights-request"></a>Creare una richiesta di diritti dell'oggetto

Gli amministratori di Subject Rights Management possono aprire nuove richieste tramite la pagina principale Richieste diritti oggetto di Priva. Una procedura guidata guiderà l'utente attraverso il processo di ricerca dei dati personali su un soggetto di dati e l'avvio del processo di evasione della richiesta.

Puoi anche scegliere di caricare materiale aggiuntivo per consentire a Priva di identificare gli interessati in base ai valori dei dati forniti. Per altre informazioni, vedi [Corrispondenza dei dati per le richieste di diritti dell'oggetto](subject-rights-requests-data-match.md).

## <a name="request-types"></a>Tipi di richiesta

Priva Subject Rights Requests supporta tre diversi tipi di richieste:

1. **Accesso**: fornisce un riepilogo delle informazioni personali dell'oggetto dei dati tenute dall'organizzazione in Microsoft 365.

2. **Export**: fornisce un riepilogo e un file esportato di elementi di contenuto che contengono le informazioni personali dell'oggetto dei dati. Questi sono gli elementi esaminati e contrassegnati come **inclusi** durante la revisione dei dati raccolti dalle impostazioni di ricerca.

3. **Elenco con tag per il follow-up**: genera un riepilogo di tutti i file contrassegnati durante la revisione dei dati che potrebbero richiedere un'azione aggiuntiva al di fuori di Priva. Ad esempio, potrebbe essere necessario facilitare l'eliminazione delle informazioni personali dell'oggetto dei dati in base alla loro richiesta. È possibile visualizzare i tag inclusi e configurare tag personalizzati per l'organizzazione nelle [impostazioni priva](priva-settings.md).

## <a name="use-the-subject-rights-request-creation-wizard"></a>Usare la procedura guidata per la creazione di richieste di diritti dell'oggetto

1. Nel riquadro [Centro conformità Microsoft 365](https://compliance.microsoft.com/), selezionare **Priva Subject Rights Requests** dal riquadro di spostamento sinistro.

2. Nell'angolo in alto a destra seleziona **Crea una richiesta**.

3. Nella pagina **Informazioni sull'oggetto** dei dati aggiungere il nome e cognome dell'oggetto dei dati, l'indirizzo di posta elettronica, il paese di residenza e specificare la relazione con l'azienda. Quindi, scegliere **Avanti**.

4. Nella pagina **Posizioni** scegliere le posizioni Microsoft 365 in cui si desidera cercare i dati personali dell'oggetto dei dati. Ottenere informazioni dettagliate sulle [impostazioni della posizione](#choose-locations). Al termine della scelta delle posizioni, selezionare **Avanti.**

5. Nella pagina **Impostazioni di** ricerca è possibile modificare le impostazioni di ricerca per perfezionare la ricerca e scegliere se ottenere una stima prima di recuperare i dati. Non è necessario scegliere alcuna opzione in questa pagina, che determina una ricerca predefinita in base alle posizioni specificate nel passaggio precedente. Per altre informazioni sulle opzioni qui, vedi [Definire le impostazioni di ricerca](#define-search-settings). Quando si è pronti per continuare, selezionare **Avanti**.

6. Nella pagina **Tipo di** richiesta scegliere un tipo di richiesta in [base alle operazioni](#request-types) che l'oggetto dati desidera eseguire con i relativi dati: **Accesso****, Esportazione** o Elenco con tag per il **follow-up**. Se la richiesta si riferisce a una specifica normativa sulla privacy dei dati, puoi anche selezionarla da un elenco fornito per aggiungere altro contesto. L'impostazione di una scadenza (obbligatoria) semplifica l'ordinamento delle richieste in arrivo o scadute e la risoluzione delle richieste in modo rapido. Al termine, selezionare **Avanti**.

7. In **Nome richiesta** confermare o modificare il nome della richiesta e aggiungere una descrizione facoltativa come riferimento. Quindi, scegliere **Avanti**.

8. Nella pagina **Revisione e** fine rivedere le selezioni. È possibile modificare qualsiasi sezione. Al termine, selezionare **Crea richiesta**.

La richiesta avrà una propria pagina dei dettagli e verrà elencata nella pagina principale Richiesta diritti oggetto. Dopo aver creato la richiesta, Priva inizierà a cercare corrispondenze alle informazioni dell'oggetto dati fornite nelle posizioni specificate. La visualizzazione di una stima dei dati nella pagina dei dettagli della richiesta potrebbe richiedere alcuni minuti a seconda dell'ambito della ricerca.

## <a name="choose-locations"></a>Scegliere le posizioni

Per ogni richiesta di diritti dell'oggetto, è possibile impostare la ricerca per cercare dati in tutte le posizioni o in posizioni specifiche all'interno di Exchange e Sharepoint. Scegliere una posizione spostando l'interruttore interruttore sulla **posizione** Attivato. È possibile scegliere di eseguire ricerche in tutti gli account e siti oppure di designare account o siti specifici all'interno di ogni posizione. Leggi i dettagli di seguito su ciò che è trattato in ogni posizione.

- **Exchange**: questa opzione consente di cercare i dati nelle cassette postali Exchange e nelle chat individuali o Teams gruppo. È possibile scegliere di cercare tutti Exchange account nell'organizzazione oppure selezionare Scegli account per  selezionare singoli utenti nel riquadro a comparsa Exchange **cassette** postali.

- **SharePoint**: questa opzione consente di cercare i dati in SharePoint siti, OneDrive for Business siti e Teams canali. È possibile scegliere di eseguire ricerche in SharePoint siti nell'organizzazione oppure selezionare Scegli siti  per selezionare singoli utenti nel riquadro a comparsa  SharePoint siti.

Per informazioni sull'identificazione dei termini di ricerca appropriati, fare riferimento ai seguenti argomenti:

- **SharePoint** siti e URL: Gestire i siti nell'interfaccia di amministrazione di [SharePoint](/sharepoint/manage-sites-in-new-admin-center) fornisce indicazioni su come ordinare e filtrare i siti e su come cercare un sito SharePoint sito. Utilizzare questa opzione per trovare gli URL da immettere nel campo di ricerca nel **riquadro SharePoint riquadro** a comparsa dei siti.

- **Teams chat e** canali: [Get-Team](/powershell/module/teams/get-team) mostra come trovare team in Microsoft Teams fornendo proprietà o informazioni specifiche.

- **OneDrive siti e URL**[: informazioni](/onedrive/list-onedrive-urls#about-onedrive-urls) sugli URL di OneDrive fornisce informazioni sul formato e sulle proprietà corrette per l'URL di OneDrive di un utente. Utilizzare questa opzione per identificare OneDrive siti nella ricerca.

Ti consigliamo di esaminare attentamente le selezioni per assicurarti di identificare l'oggetto dei dati corretto. Ad esempio, se si ricercano le cassette postali per nome e si trovano più persone con nomi simili, verificare quella corretta prima di aggiungerle alla richiesta.

## <a name="define-search-settings"></a>Definire le impostazioni di ricerca

Quando si crea una richiesta di diritti dell'oggetto, verrà eseguita una ricerca predefinita in base alle selezioni  nella pagina Percorsi della creazione guidata. Se si desidera eseguire una ricerca più mirata o se si desidera scegliere di ottenere una stima dei dati prima del recupero degli elementi di contenuto, è possibile effettuare tali selezioni nella pagina Impostazioni di  ricerca della procedura guidata per la creazione della richiesta.

### <a name="advanced-search-options"></a>Opzioni di ricerca avanzate

- **Affinare la ricerca**: questa opzione consente di specificare proprietà aggiuntive per identificare l'oggetto dei dati tra i dati dell'organizzazione. Dopo aver scelto questa opzione, verrà richiesto di aggiungere altri parametri di ricerca, illustrati di seguito in [Affinare la ricerca](#refine-your-search).
- **Includi contenuto creato dall'oggetto dati**: questa opzione consente di cercare il contenuto creato dall'oggetto dati. Tra gli esempi sono inclusi i file creati dall'SharePoint o caricati dall'oggetto dati. La selezione di questa opzione può aumentare in modo significativo la quantità di dati restituiti.
- **Includi tutte le versioni degli** elementi: se è stato selezionato SharePoint come percorso di ricerca, la query di ricerca predefinita restituirà solo la versione corrente SharePoint elementi. Selezionando questa casella verranno restituite la versione corrente e tutte le versioni precedenti degli elementi SharePoint, con una quantità di dati significativamente maggiore da esaminare.

### <a name="data-estimate"></a>Stima dei dati

**L'opzione Ottieni prima una** stima presenta una stima della quantità di dati che ci aspettiamo di trovare prima che i dati vengono recuperati automaticamente. Quando la stima viene visualizzata nella pagina dei dettagli della richiesta, è possibile scegliere di visualizzare i risultati della ricerca e visualizzare in anteprima un campionamento di elementi individuati. Se gli elementi rappresentano i risultati previsti, è necessario selezionare Recupera **dati per procedere** con il recupero effettivo degli elementi di contenuto.

## <a name="refine-your-search"></a>Perfezionare la ricerca

Se si sceglie **Affina** la ricerca nella  pagina Impostazioni di ricerca, quando si  seleziona Avanti verrà richiesto di specificare i dettagli per gli attributi e le condizioni personali per definire ulteriormente i risultati della ricerca. È possibile aggiungere aggiunte in una o in entrambe le categorie. Al termine delle selezioni in questa sezione, il recupero dei dati per la richiesta si baserà sulle impostazioni di ricerca.

#### <a name="add-personal-attributes"></a>Aggiungere attributi personali

Immettere i valori nei campi di testo per i nomi, i nomi, i nomi alternativi, gli indirizzi di posta elettronica e l'indirizzo dell'oggetto dei dati. È possibile aggiungere altri identificatori, ad esempio la data di nascita o il numero di telefono, e i campi di testo supportano più voci separate da un punto e virgola. Al termine, selezionare **Avanti** per passare alla **pagina** Condizioni.

#### <a name="conditions"></a>Condizioni

Selezionare il  pulsante Aggiungi condizione per scegliere tra una serie di condizioni di destinazione della ricerca, inclusi il nome dell'elemento, i nomi dei mittenti e dei destinatari, il tipo di dati personali e se l'elemento è stato condiviso esternamente all'esterno dell'organizzazione. I campi di testo supportano più voci separate da un punto e virgola. Al termine, selezionare Avanti per salvare  le impostazioni di ricerca e l'avanzamento nell'impostazione del tipo di richiesta.

## <a name="next-steps"></a>Passaggi successivi

Dopo aver creato la richiesta, la vedrai elencata nella pagina della richiesta di diritti dell'oggetto. Per ulteriori informazioni su come procedere con la revisione, vedere [Esaminare i dati e collaborare alle richieste](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

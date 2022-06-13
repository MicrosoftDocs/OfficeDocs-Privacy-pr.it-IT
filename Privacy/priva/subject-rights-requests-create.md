---
title: Creare una richiesta e definire le impostazioni di ricerca in Richieste di diritti soggetto
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
description: Informazioni su come creare una nuova richiesta di diritti per l'oggetto e definire le impostazioni di ricerca in Richieste di diritti degli interessati Microsoft Priva.
ms.openlocfilehash: 7314fefa370b24bcb215a99b67b74c13b8b27613
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046640"
---
# <a name="create-a-request-and-define-search-settings"></a>Creare una richiesta e definire le impostazioni di ricerca

**Questo articolo** illustra come creare una richiesta in Priva per iniziare a soddisfare una richiesta di diritti dell'oggetto. Informazioni sulle impostazioni di ricerca per il recupero dei dati e su come perfezionare la ricerca.

Gli utenti che detengono un ruolo nel gruppo di ruoli Subject Rights Request Administrators diverso da quello di sola visualizzazione ([vedere autorizzazioni Priva](priva-permissions.md)) possono creare una richiesta in Richieste di diritti dell'oggetto. Un processo guidato illustra le impostazioni per la ricerca di dati personali su un interessato e l'avvio del processo di esecuzione della richiesta.

## <a name="request-types"></a>Tipi di richiesta

Richieste di diritti degli interessati Priva supporta tre diversi tipi di richieste:

1. **Accesso**: fornisce un riepilogo delle informazioni personali dell'interessato contenute nell'organizzazione in Microsoft 365.

2. **Esportazione**: fornisce un riepilogo e un file esportato di elementi di contenuto che contengono le informazioni personali dell'interessato. Questi sono gli elementi esaminati e contrassegnati come **Inclusi** durante la revisione dei dati raccolti dalle impostazioni di ricerca.

3. **Elenco con tag per il completamento**: genera un riepilogo di tutti i file contrassegnati durante la revisione dei dati che potrebbero richiedere un'azione aggiuntiva al di fuori di Priva. Ad esempio, potrebbe essere necessario facilitare l'eliminazione delle informazioni personali dell'interessato in base alla richiesta. È possibile visualizzare i tag inclusi e configurare tag personalizzati per l'organizzazione nelle [impostazioni Priva](priva-settings.md).

## <a name="getting-started-with-your-first-request"></a>Introduzione alla prima richiesta

Quando si avvia una versione di valutazione o una sottoscrizione di Richieste di diritti dell'oggetto, viene offerta una configurazione semplice e predefinita per la prima richiesta che usa le impostazioni predefinite. Questa configurazione consente di esplorare il flusso di lavoro della richiesta di diritti dell'oggetto e acquisire familiarità con le relative funzionalità.

La prima volta che si arriva alla pagina Richieste di diritti dell'oggetto, verrà visualizzato un banner nella parte superiore con un pulsante **di Attività iniziali**. Quando un utente seleziona questo pulsante, viene visualizzato un riquadro a comparsa con le informazioni dell'utente prepopolato nei campi nome e posta elettronica e vengono visualizzate tutte le impostazioni predefinite.

**Esplorazione della funzionalità di richiesta con le informazioni**: provare una richiesta di diritti dell'oggetto in base alle proprie informazioni può aiutare a acquisire familiarità e comfort nello spostamento in ogni fase del processo. Vedrai cosa produce una ricerca predefinita e puoi esercitarti a perfezionare i risultati modificando le impostazioni di ricerca. Nella scheda **Dati raccolti** è possibile esaminare gli elementi nell'area di anteprima a destra e praticare la redazione di testo, l'applicazione di tag, l'immissione di note e l'contrassegno di elementi da includere o escludere per il report finale.Trovare i dettagli in [Rivedi i dati per una richiesta di diritti dell'interessato](subject-rights-requests-data-review.md).

- Non è necessario usare le informazioni per creare la prima richiesta. Se si è pronti per avviare una richiesta per un interessato, sostituire il nome e l'indirizzo di posta elettronica con le informazioni dell'interessato.

Per accettare tutte le impostazioni e creare la richiesta, selezionare **Crea**. Il riquadro verrà chiuso e la nuova richiesta verrà visualizzata nella pagina **Richieste di diritti dell'oggetto** . Per modificare una delle impostazioni predefinite prima di creare la richiesta, selezionare **Modifica dettagli richiesta**, che consente di accedere alla [creazione guidata della richiesta con diritti dell'oggetto](#create-a-request).

> [!NOTE]
> Qualsiasi richiesta creata verrà conteggiata per l'assegnazione della sottoscrizione di valutazione o a pagamento, indipendentemente dalle informazioni dell'interessato usate per la richiesta. Il periodo di conservazione dei dati standard di 30 giorni si applica dopo la chiusura della richiesta. Informazioni su come modificare i [periodi di conservazione per le richieste di diritti dell'oggetto](subject-rights-requests-reports.md#retention-periods-for-reports-and-data).

## <a name="create-a-request"></a>Creare una richiesta

Seguire la procedura seguente per iniziare a soddisfare una richiesta di diritti dell'oggetto:

1. Nel [portale di conformità di Microsoft Purview](https://compliance.microsoft.com/) selezionare **Richieste di diritti degli interessati Priva** nel riquadro di spostamento a sinistra.

2. Nell'angolo in alto a destra della schermata selezionare **Crea una richiesta**.

3. Nella pagina **Informazioni sull'interessato** immettere il nome, il cognome e l'indirizzo di posta elettronica dell'interessato. Selezionare **Aggiungi residenza** per scegliere il paese di residenza dell'interessato. Selezionare l'opzione che identifica il modo in cui l'interessato è correlato all'organizzazione (ad esempio, cliente o dipendente corrente) e selezionare **Avanti** per passare al passaggio successivo.

4. Nella pagina **Località** decidere dove cercare le informazioni dell'interessato. Scegliere una o entrambe le posizioni seguenti spostando l'interruttore di stato accanto a ogni opzione nella posizione **Sì** :

   - **Exchange**: cercare i dati nelle cassette postali Exchange e nelle chat Teams individuali o di gruppo. È possibile scegliere di cercare tutti gli account Exchange nell'organizzazione oppure selezionare **Scegli account** per selezionare singoli utenti nel riquadro a comparsa **Exchange cassette postali**.

   - **SharePoint**: cercare i dati in siti SharePoint, siti OneDrive for Business e canali di Teams. È possibile scegliere di eseguire ricerche in tutti i siti SharePoint dell'organizzazione oppure selezionare **Scegli siti** per selezionare singoli utenti nel riquadro a comparsa **SharePoint siti**.

> [!TIP]
> Per informazioni sull'identificazione dei termini di ricerca appropriati, vedere gli argomenti seguenti:
> - SharePoint siti e URL: [Gestire i siti nell'interfaccia di amministrazione SharePoint](/sharepoint/manage-sites-in-new-admin-center) fornisce indicazioni su come ordinare e filtrare i siti e su come cercare un sito SharePoint. Usare questa opzione per trovare gli URL da immettere nel campo di ricerca nel riquadro a comparsa **SharePoint siti**.
> - Teams chat e canali: [Get-Team](/powershell/module/teams/get-team) mostra come trovare i team in Microsoft Teams fornendo proprietà o informazioni specifiche.
> - OneDrive siti e URL: [Informazioni sugli URL OneDrive](/onedrive/list-onedrive-urls#about-onedrive-urls) fornisce informazioni sul formato e sulle proprietà appropriate per l'URL OneDrive di un utente. Usare questa opzione per identificare OneDrive siti nella ricerca.

5. Nella pagina **Definisci impostazioni di ricerca** è possibile scegliere di apportare modifiche alla ricerca predefinita scegliendo tra le varie opzioni di ricerca avanzate. Qui è anche possibile scegliere di ottenere una stima prima che i dati siano restituiti automaticamente. Se si sceglie una di queste opzioni, quando si seleziona **Avanti** si procederà a schermate aggiuntive. Per informazioni dettagliate, vedere [Definire le impostazioni di ricerca](#defining-search-settings) riportate di seguito. Se non si vuole modificare la ricerca, lasciare vuote tutte le opzioni e selezionare **Avanti** per passare alla fase successiva.

6. Nella pagina **Selezionare il tipo di richiesta** scegliere il tipo di richiesta: **Accesso**, **Esportazione** o **Elenco tag per il completamento** ([vedere le descrizioni precedenti](#request-types)). Indicare se la richiesta riguarda un regolamento sulla privacy dei dati. Esaminare o apportare modifiche alla scadenza di completamento, che per impostazione predefinita è due settimane dopo la data di creazione della richiesta. Quindi, scegliere **Avanti**.

7. Nella pagina **Conferma o modifica il nome di questa richiesta** è possibile mantenere o modificare il nome descrittivo specificato per la richiesta e immettere una descrizione facoltativa. Quindi, scegliere **Avanti**.

8. Nella pagina **Revisione e fine** esaminare il riepilogo degli elementi immessi durante i passaggi precedenti. Qualsiasi campo può essere modificato selezionando il **collegamento Modifica** in ogni sezione. Al termine, selezionare **Crea richiesta**.

Una volta creata la richiesta, verrà visualizzata una schermata di conferma. Selezionare **Done (Fatto)** per tornare alla schermata principale Subject Rights Requests .Select Done to return to the subject rights requests screen. La nuova richiesta verrà elencata nella parte superiore dell'elenco di richieste. Selezionarlo dall'elenco per iniziare a esaminare e a lavorare sulle fasi di avanzamento.

#### <a name="what-happens-after-your-request-is-created"></a>Cosa accade dopo la creazione della richiesta

Si calcolerà immediatamente una stima della quantità di dati che si prevede di trovare in base ai parametri di ricerca. Visitare la pagina dei dettagli della richiesta tra pochi minuti e un'ora per visualizzare i risultati della stima e verificare se la richiesta è stata spostata nella fase successiva. La richiesta procederà automaticamente dalla **stima dei dati** al **recupero dei dati** , ad eccezione delle circostanze seguenti:

 - Se si è scelto di ricevere prima un'esimtae di dati nel passaggio 5, **Definire le impostazioni di ricerca**, sarà possibile visualizzare i dettagli della ricerca e apportare modifiche alla ricerca prima che tutti i dati vengano recuperati. È necessario passare manualmente alla fase successiva di **recupero dei dati** se si è sospeso in **Data estimate**.
 
 - Se non si è scelto di interrompere la stima dei dati, ma si prevede che la ricerca produrrà un volume elevato di dati, verrà visualizzata una barra dei messaggi nella parte superiore della richiesta con un collegamento per modificare la ricerca prima di procedere al **recupero dei dati**.

Per altre informazioni su queste fasi, vedere [Stima e recupero dei dati](subject-rights-requests-data-retrieval.md).

## <a name="defining-search-settings"></a>Definizione delle impostazioni di ricerca

Quando si crea una richiesta di diritti dell'oggetto, verrà eseguita una ricerca predefinita in base alle selezioni nella pagina **Percorsi** della creazione guidata. Se si vuole eseguire una ricerca più mirata o se si vuole ottenere una stima dei dati prima del recupero degli elementi di contenuto, è possibile effettuare tali selezioni nella pagina **Impostazioni di ricerca** della creazione guidata richiesta.

### <a name="advanced-search-options"></a>Opzioni di ricerca avanzate

- **Perfezionare la ricerca**: questa opzione consente di specificare proprietà aggiuntive per identificare l'interessato tra i dati dell'organizzazione. Dopo aver scelto questa opzione, verrà richiesto di aggiungere altri parametri di ricerca, illustrati di seguito in [Affinamento della ricerca](#refining-your-search).
- **Includi contenuto creato dall'interessato**: questa opzione cercherà il contenuto creato dall'interessato. Gli esempi includono i file creati dall'interessato o caricati in SharePoint dall'interessato. La selezione di questa opzione può aumentare significativamente la quantità di dati restituiti.
- **Includi tutte le versioni degli elementi**: se è stato selezionato SharePoint come percorso di ricerca, la query di ricerca predefinita restituirà solo la versione corrente degli elementi SharePoint. Se si seleziona questa casella, verranno restituite le versioni correnti e tutte le versioni precedenti degli elementi SharePoint, generando una quantità di dati significativamente maggiore da esaminare.

> [!TIP]
> È possibile scegliere di caricare materiale aggiuntivo per consentire a Priva di identificare gli interessati in base a valori di dati esatti. Per altre informazioni, vedere [Corrispondenza dei dati per le richieste di diritti dell'interessato](subject-rights-requests-data-match.md).

### <a name="data-estimate"></a>Stima dei dati

L'opzione **Ottieni una prima stima** presenterà una stima della quantità di dati che si prevede di trovare prima che i dati vengano recuperati automaticamente. Quando la stima viene visualizzata nella pagina dei dettagli della richiesta, è possibile scegliere di visualizzare i risultati della ricerca e visualizzare in anteprima un campionamento degli elementi individuati. Se gli elementi rappresentano i risultati previsti, è necessario selezionare **Recupera dati** per procedere con il recupero effettivo degli elementi di contenuto. Ottenere altri dettagli sulla [fase di stima dei dati](subject-rights-requests-data-retrieval.md).

## <a name="refining-your-search"></a>Affinamento della ricerca

Se si sceglie **Affina la ricerca** nella pagina **Impostazioni di ricerca** o se è stata sospesa la fase **di stima dei dati** e si sceglie di modificare la query di ricerca, verrà richiesto di specificare i dettagli per gli attributi e le condizioni personali per indirizzare ulteriormente i risultati della ricerca. È possibile aggiungere aggiunte in una o in entrambe le categorie. Al termine delle selezioni in questa sezione, il recupero dei dati per la richiesta si baserà sulle impostazioni di ricerca.

I dettagli illustrati di seguito sono anche quelli che verranno richiesti se si è sospesi nella fase **di stima dei dati** e si sceglie di modificare la query di ricerca. 

#### <a name="add-personal-attributes"></a>Aggiungere attributi personali

Immettere i valori nei campi di testo per i nomi, i nomi alternativi, gli indirizzi di posta elettronica e l'indirizzo dell'interessato. È possibile aggiungere altri identificatori, ad esempio la data di nascita o il numero di telefono, e i campi di testo supportano più voci separate da un punto e virgola. Al termine, selezionare **Avanti** per continuare con la pagina **Condizioni** .

#### <a name="conditions"></a>Condizioni

Selezionare il pulsante **Aggiungi condizione** per scegliere tra un intervallo di condizioni per indirizzare ulteriormente la ricerca, tra cui il nome dell'elemento, i nomi del mittente e del destinatario, il tipo di dati personali e se l'elemento è stato condiviso esternamente all'esterno dell'organizzazione. I campi di testo supportano più voci separate da un punto e virgola. Al termine, selezionare **Avanti** per salvare le impostazioni di ricerca e passare all'impostazione del tipo di richiesta.

## <a name="next-steps"></a>Passaggi successivi

Dopo aver creato la richiesta, verrà visualizzata nella pagina relativa alla richiesta di diritti dell'oggetto. Per altre informazioni su come procedere con la revisione, vedere [Esaminare i dati e collaborare alle richieste](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Legali

[Microsoft Priva dichiarazione di non responsabilità legale](priva-disclaimer.md)

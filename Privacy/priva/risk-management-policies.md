---
title: Criteri di gestione dei rischi per la privacy
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
description: Informazioni su come creare e gestire i criteri in Microsoft Priva Privacy Risk Management per la gestione dei dati personali dell'organizzazione in Microsoft 365.
ms.openlocfilehash: 87671cedc8c6cba75d5ad207b52831cdd2467187
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014496"
---
# <a name="privacy-risk-management-policies"></a>Criteri di gestione dei rischi per la privacy

I criteri di gestione dei rischi per la privacy consentono di gestire gli scenari di rischio importanti per l'organizzazione. I modelli di criteri sono incentrati sulla promozione di procedure di gestione dei dati valide.  Gli avvisi comunicano agli amministratori quando vengono rilevate corrispondenze ai criteri e potrebbero essere necessarie ulteriori indagini. Notifiche tramite posta elettronica e suggerimenti in Microsoft Teams aiutare gli utenti a comprendere quali attività comportano rischi per la privacy, consentono agli utenti di risolvere immediatamente i problemi e li indirizzano alla formazione sulla privacy.

Per una guida introduttiva, usare un modello con le impostazioni predefinite per creare nuovi criteri per la sovraesposizione dei dati, i trasferimenti di dati e la riduzione dei dati e gli scenari. È anche possibile personalizzare le impostazioni dei modelli per creare criteri adatti alle esigenze dell'organizzazione.

## <a name="policy-template-types"></a>Tipi di modello di criteri

Gestione dei rischi per la privacy ha tre modelli di criteri progettati per aiutarti ad affrontare le principali aree di preoccupazione per la protezione dei dati personali. Ogni modello ha impostazioni predefinite che è possibile accettare nel processo di configurazione rapida o personalizzare usando un processo guidato. Quando si crea un nuovo criterio, la prima attività consiste nel scegliere uno dei tre modelli elencati di seguito:

- **Sovraesposizione dei dati**: questo criterio identifica gli elementi di contenuto contenenti dati personali che potrebbero essere troppo accessibili da altre persone. Quando vengono trovate corrispondenze, è possibile configurare notifiche che richiedono ai proprietari del contenuto di applicare rapidamente la protezione.

- **Trasferimenti di dati**: questo criterio consente di rilevare i trasferimenti di dati personali attraverso i limiti che si determinano, che potrebbero comportare trasferimenti all'esterno dell'organizzazione o trasferimenti interni tra reparti o aree geografiche. Quando vengono trovate corrispondenze, è possibile configurare notifiche che incoraggiano i mittenti a revocare l'accesso al contenuto.

- **Minimizzazione dei dati**: questo criterio identifica gli elementi di contenuto contenenti dati personali che non sono stati toccati per lunghi periodi di tempo. Quando vengono trovate corrispondenze, è possibile inviare notifiche ai proprietari del contenuto che richiedono loro di intraprendere azioni rapide per mantenere o eliminare l'elemento.

## <a name="quick-setup-using-a-template-with-default-settings"></a>Configurazione rapida: uso di un modello con le impostazioni predefinite

Quando si creano criteri direttamente da un modello, la maggior parte delle impostazioni verrà scelta automaticamente per semplificare l'esecuzione. Seguire questa procedura per creare un criterio con le impostazioni predefinite usando uno dei modelli seguenti:

1. Nel [Centro conformità Microsoft Purview](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento a sinistra e selezionare **Criteri**.

2. Selezionare **Crea un criterio** nell'angolo in alto a destra della schermata, in cui viene visualizzato un riquadro a comparsa che elenca tutte le opzioni di creazione dei criteri.

3. Trovare il tipo di criterio da creare e nella relativa scheda selezionare **Crea**.

4. Un riquadro a comparsa contiene i dettagli dei criteri. Selezionando **Visualizza impostazioni** verranno visualizzate le impostazioni predefinite. È possibile modificare le impostazioni da qui, che consente di accedere al processo guidato descritto di seguito. Per continuare a creare i criteri usando le impostazioni predefinite, immettere semplicemente un nome descrittivo e quindi selezionare **Crea criterio**.

I criteri verranno creati e saranno elencati nella pagina **Criteri** .

Il criterio inizierà l'esecuzione in modalità test, ovvero non verranno generati avvisi o notifiche ed è possibile monitorarne le prestazioni. Quando si è pronti per attivare i criteri, selezionare il criterio e modificarlo per attivarlo.

## <a name="custom-setup-guided-process-to-choose-all-settings"></a>Configurazione personalizzata: processo guidato per scegliere tutte le impostazioni

L'opzione dei criteri personalizzati è un processo guidato per la creazione di un criterio. Si inizierà scegliendo un modello e quindi si esaminerà ogni impostazione per personalizzare i criteri. Le istruzioni seguenti forniscono informazioni dettagliate sulle impostazioni di base applicabili a ognuno dei tre tipi di criteri. Se le impostazioni sono diverse in base al tipo di criterio, verrà creato un collegamento a istruzioni specifiche.

Seguire la procedura seguente per creare un criterio:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento sinistro. Dal menu a discesa selezionare **Criteri**.

2. Selezionare **Crea un criterio**.

3. Scegliere l'opzione **Personalizzata** per creare i criteri usando la creazione guidata dei criteri in Gestione dei rischi per la privacy.

4. Scegliere il tipo di criterio: **sovraesposizione dei dati,** **trasferimenti di dati** o **minimizzazione dei dati**.

5. Assegnare un nome descrittivo ai criteri per identificarli nell'elenco dei criteri. Specificare una descrizione facoltativa, quindi selezionare **Avanti**.

6. I passaggi successivi consentono di definire tutte le impostazioni dei criteri. Per altri dettagli, è possibile passare alle descrizioni all'interno di questo articolo. Le opzioni disponibili sono:
    - [**Dati da monitorare**](#choose-data-to-monitor): selezionare il tipo di dati personali che i criteri monitoreranno.
    - [**Utenti e gruppi**](#choose-users-and-groups): applicare i criteri a tutti gli utenti o agli utenti selezionati.
    - [**Località**](#choose-locations): applicare i criteri alle aree selezionate in Microsoft 365.
    - [**Condizioni**](#set-conditions): impostare le condizioni per i criteri. Queste opzioni variano a seconda del tipo di criterio.
    - [**Risultati**](#define-outcomes-user-email-notifications-and-tips): definire i risultati quando viene trovata una corrispondenza dei criteri, ad esempio le notifiche tramite posta elettronica dell'utente.
    - [**Avvisi**](#set-alerts): decidere la frequenza degli avvisi per gli amministratori quando viene trovata una corrispondenza dei criteri.
    - [**Modalità**](#testing-a-policy): scegliere se eseguire o meno i criteri prima in modalità test.
7. Al termine di tutte le impostazioni, esaminare le scelte, apportare le modifiche desiderate e quindi selezionare **Invia** per creare il criterio.

Dopo alcuni secondi, verrà visualizzata una conferma della creazione del criterio. Selezionare **Fine** nella pagina di conferma, che consente di passare alla pagina **Criteri** in cui verranno visualizzati i nuovi criteri nella parte superiore della tabella.

Le sezioni immediatamente seguenti forniscono ulteriori dettagli su ogni impostazione di criterio.

## <a name="choose-data-to-monitor"></a>Scegliere i dati da monitorare

Quando si crea o si modifica un criterio, viene chiesto di selezionare i tipi di dati da monitorare. Esistono due opzioni:

- **Gruppi di classificazione**: elenco ricercabile di raggruppamenti di tipi di informazioni riservate; Ad esempio, un gruppo basato sull'Australia Health Records Act o un gruppo basato su informazioni personali degli Stati Uniti, ad esempio un numero di passaporto degli Stati Uniti.

- **Singoli tipi di informazioni sensibili**: elenco ricercabile di tipi di informazioni riservate; ad esempio i numeri di previdenza sociale o i numeri di patente di guida.

Se si seleziona tra i gruppi di classificazione esistenti, non è anche possibile selezionare singoli tipi o creare gruppi personalizzati. Per la massima flessibilità, scegli i singoli tipi di informazioni sensibili. Per utilizzare gli standard più comuni, scegliere tra i gruppi di classificazione. Altre informazioni su ogni tipo di dati sono disponibili di seguito.

### <a name="classification-groups"></a>Gruppi di classificazione

I gruppi di classificazione sono raggruppamenti di [tipi di informazioni sensibili](/microsoft-365/compliance/sensitive-information-type-entity-definitions) usati per rilevare il contenuto correlato ai dati personali o a normative specifiche.

Quando si seleziona questa opzione nella pagina **Dati da monitorare** , è necessario selezionare **+Aggiungi gruppi di classificazione** e scegliere uno o più gruppi dall'elenco visualizzato in un riquadro a comparsa.

### <a name="individual-sensitive-information-types"></a>Singoli tipi di informazioni sensibili

Scegliendo [tipi di informazioni sensibili](/microsoft-365/compliance/sensitive-information-type-entity-definitions) specifici, ad esempio i numeri di previdenza sociale o le informazioni sulla patente di guida, è possibile personalizzare il proprio gruppo o gruppi di dati da cercare. È possibile selezionare dall'elenco completo dei tipi di informazioni sensibili in Gestione dei rischi per la privacy. Ogni tipo di informazioni ha le proprie proprietà.

Quando si seleziona questa opzione nella pagina **Dati da monitorare** , viene visualizzato un selettore con **Default** elencato come nome per il gruppo di tipi di informazioni sensibili che verranno selezionati. Mantenere o modificare il nome del gruppo, quindi selezionare **Aggiungi** per selezionare uno o più tipi di informazioni sensibili dall'elenco completo in Gestione dei rischi per la privacy. Ogni tipo di informazioni ha le proprie proprietà e le impostazioni consigliate, che è possibile individuare selezionando l'icona delle informazioni a destra del menu a discesa con attendibilità dopo aver aggiunto il tipo di informazioni. È anche possibile modificare il numero di istanze per ogni tipo di informazioni riservate. Questa impostazione definisce il numero di istanze univoche di ogni tipo di informazioni riservate che si vuole rilevare nei criteri.

Se si creano più gruppi, la procedura guidata consente di selezionare il modo in cui i gruppi devono essere correlati (una relazione "e" o "o") e di definire l'ordine delle operazioni.

## <a name="choose-users-and-groups"></a>Scegliere utenti e gruppi

Sono disponibili due opzioni per decidere quali utenti verranno trattati da un criterio: tutti gli utenti e i gruppi oppure utenti e gruppi specifici.

- **Tutti gli utenti e i gruppi**: questa opzione applica i criteri a tutti gli utenti e ai gruppi Office 365 nell'organizzazione.

- **Utenti o gruppi specifici**: questa opzione consente di selezionare singoli utenti, singoli gruppi Office 365 o una combinazione di entrambi.
  - **Per scegliere gli utenti**: selezionare **Scegli utenti** e nel riquadro a comparsa cercare un utente immettendo un indirizzo di posta elettronica nella casella di ricerca. In alternativa, trovare l'utente dall'elenco e selezionare la casella di controllo a sinistra del nome. È possibile selezionare fino a 100 utenti. Al termine, selezionare **Aggiungi.**
  - **Per scegliere i gruppi**: selezionare **Scegli gruppi** e nel riquadro a comparsa selezionare la casella di controllo a sinistra di ogni nome di gruppo. È possibile selezionare fino a dieci gruppi. Al termine, selezionare **Aggiungi**.

Dopo aver progettato utenti e gruppi, selezionare **Avanti** per passare al passaggio successivo.

## <a name="choose-locations"></a>Scegliere le posizioni

In questo passaggio si designerà dove nell'ambiente di Microsoft 365 si vuole che i criteri cerchino corrispondenze di dati personali. Le opzioni relative alla posizione dipendono dal tipo di criterio ed è possibile selezionarne più di una. Ognuna delle posizioni è illustrata di seguito.

- **Exchange**: i criteri identificheranno le corrispondenze negli account Exchange degli utenti, che includono contenuto nel corpo dei messaggi di posta elettronica e negli allegati inviati o ricevuti dalle cassette postali Exchange.

- **OneDrive**: i criteri identificheranno le corrispondenze nei file archiviati nell'account OneDrive for Business degli utenti.

- **Teams**: i criteri identificheranno le corrispondenze nei messaggi degli utenti nei canali e nelle chat Teams.

- **SharePoint**: i criteri identificheranno le corrispondenze nei file archiviati nei siti SharePoint degli utenti. Quando si seleziona questa opzione, si sceglierà tra le opzioni seguenti:
    - **Tutti i siti SharePoint**: questa selezione coprirà tutti i siti per tutti gli utenti dell'organizzazione.

    - **Siti SharePoint specifici**: questa selezione richiede di designare siti specifici a cui applicare i criteri. È possibile immettere l'URL di un sito specifico direttamente nella casella URL e quindi selezionare il **+** segno per aggiungerlo all'elenco di siti. È anche possibile selezionare **Scegli siti** e nel riquadro a comparsa cercare e selezionare dall'elenco dei siti a cui si ha accesso. Selezionare la casella visualizzata quando si passa il puntatore del mouse sul sito da selezionare. Dopo aver effettuato le selezioni, selezionare **Aggiungi**.  Tutti i siti scelti verranno elencati nella parte inferiore della pagina **Posizioni** .
    
    > [!TIP]
    > Per informazioni sull'identificazione dei siti SharePoint nell'organizzazione, visitare [Gestire i siti nell'interfaccia di amministrazione SharePoint](/sharepoint/manage-sites-in-new-admin-center).

Al termine della designazione delle posizioni, selezionare **Avanti**.

## <a name="set-conditions"></a>Impostare le condizioni

Le condizioni per il rilevamento delle corrispondenze dei criteri differiscono in base al modello di criteri.

- **Sovraesposizione dei dati**: fare riferimento al passaggio relativo alle condizioni nelle [istruzioni di configurazione personalizzate](risk-management-policy-data-overexposure.md#custom-setup-guided-policy-creation-process) dei criteri di esposizione dei dati.
- **Trasferimenti di dati**: vedere il passaggio relativo alle condizioni nelle [istruzioni di configurazione personalizzate dei criteri di trasferimento dei dati](risk-management-policy-data-transfer.md#custom-setup-guided-policy-creation-process).
- **Minimizzazione dei dati**: vedere il passaggio relativo alle condizioni nelle [istruzioni di configurazione personalizzate dei criteri di minimizzazione dei dati](risk-management-policy-data-minimization.md#custom-setup-guided-policy-creation-process).

## <a name="define-outcomes-user-email-notifications-and-tips"></a>Definire i risultati: notifiche e suggerimenti tramite posta elettronica dell'utente

Le impostazioni dei risultati vengono gestite nella pagina **Risultati** della creazione guidata dei criteri. In questa pagina è possibile scegliere di inviare una notifica tramite posta elettronica agli utenti quando eseguono un'azione corrispondente alle condizioni di un criterio.

I criteri di trasferimento dei dati hanno un'opzione aggiuntiva per mostrare suggerimenti agli utenti in Teams quando le azioni generano una corrispondenza dei criteri. Questi suggerimenti includeranno collegamenti alla formazione sulla privacy, forniti dall'utente, e includeranno meccanismi per correggere i potenziali rischi.

Queste notifiche possono essere opportunità utili per evitare l'escalation dei problemi e per creare competenze e fiducia degli utenti nell'adozione di procedure di gestione dei dati sicure.

Per altre informazioni [sull'uso delle notifiche degli utenti, vedere Notifiche degli utenti in Gestione dei rischi](risk-management-notifications.md) per la privacy.

## <a name="set-alerts"></a>Impostare gli avvisi

Gli avvisi consentono agli amministratori di sapere quando un evento utente corrisponde alle condizioni di un criterio. La configurazione degli avvisi è facoltativa e si controlla la frequenza di generazione degli avvisi, la soglia che deve essere raggiunta prima della generazione di un avviso e la gravità dell'avviso. Gli avvisi vengono visualizzati nella scheda **Avvisi** nella pagina **Criteri** . Altre informazioni sulla [visualizzazione, l'analisi e la correzione degli avvisi](risk-management-alerts.md).

#### <a name="turn-on-alerts"></a>Attivare gli avvisi

È possibile attivare gli avvisi quando si crea un criterio per la prima volta o modificarli in un secondo momento per attivarli. Nella pagina **Avvisi** della creazione guidata criteri impostare l'interruttore **Crea avvisi** sulla posizione **Attiva** .

#### <a name="alert-frequency-and-thresholds"></a>Frequenza e soglie degli avvisi
Dopo aver attivato gli avvisi, decidere la frequenza con cui verranno generati.

- **Avviso ogni volta che si verifica una corrispondenza dei criteri**: la selezione di questa opzione potrebbe generare un numero elevato di avvisi.
- **Avviso quando viene raggiunta una soglia specifica**: verranno impostate soglie in base al numero e alla frequenza degli eventi utente rilevati.

#### <a name="alert-severity-level"></a>Livello di gravità dell'avviso
Selezionare un livello di gravità basso, medio o alto. È consigliabile che l'organizzazione definisca ciò che ogni livello rappresenta per l'utente.

## <a name="testing-a-policy"></a>Test di un criterio

Quando si crea un criterio, l'impostazione predefinita consiste nell'avviarlo in modalità test. Ciò significa che una volta creato il criterio:

- Non verranno generati avvisi. Tuttavia, verranno visualizzate informazioni dettagliate sulla pagina dei dettagli dei criteri quando vengono rilevate corrispondenze, inclusi i tipi di dati rilevati e le relative posizioni.

- Quando vengono rilevate corrispondenze ai criteri, non verranno inviate notifiche di posta elettronica dell'utente. Verranno tuttavia visualizzate informazioni dettagliate nella pagina dei dettagli dei criteri che mostrano quali utenti sono associati alle corrispondenze dei criteri.

La modalità di test consente di cercare corrispondenze degli ultimi 30 giorni di attività dell'utente. Usando queste informazioni dettagliate, è possibile misurare il comportamento dei criteri ed esaminare i tipi di avvisi che possono essere generati quando il criterio è attivato.

È consigliabile testare i criteri per almeno cinque giorni per comprendere il tipo e il volume delle corrispondenze che genererà. È possibile [modificare il criterio](#edit-a-policy) mentre è in modalità test in modo da poter monitorare il modo in cui le modifiche influiscono sulle prestazioni prima di attivarlo. Ad esempio, è possibile che il criterio sia troppo ampio e che le relative condizioni debbano essere adattate. In alternativa, è possibile che in base all'attività rilevi che gli avvisi non verranno generati in un intervallo di tempo utile per l'utente.

La pagina dei dettagli del criterio indica il numero di giorni di esecuzione del test. Si noterà il numero di corrispondenze trovate in base alla posizione, il numero di eventi utente corrispondenti alle condizioni dei criteri e i tipi di dati personali rilevati dalle corrispondenze dei criteri.

> [!NOTE]
> Se si attiva l'interruttore **Esegui in modalità test** sulla posizione **Disattivata** , *i criteri verranno attivati* al termine della creazione. Ciò significa che eventuali avvisi o notifiche utente configurati inizieranno a generare quando vengono rilevate corrispondenze.

Quando si è soddisfatti delle impostazioni dei criteri e si è pronti per attivarlo, selezionare il pulsante blu **Attiva criterio** . I criteri saranno ora attivi e genereranno eventuali avvisi e notifiche utente configurati.

## <a name="turn-on-a-policy"></a>Attivare un criterio

È possibile impostare un criterio per l'attivazione non appena viene creato. Questa operazione non è consigliata perché è consigliabile monitorare le prestazioni e le impostazioni mettendo i criteri in modalità di test prima di attivarli (vedere [Test di un criterio](#testing-a-policy)).

Se i criteri sono stati creati in modalità test, è possibile attivarli rapidamente seguendo questa procedura:

1. Nella pagina **Criteri** individuare i criteri e selezionarne il nome per aprire la pagina dei dettagli.
2. Nella scheda **Stato criteri** selezionare **Attiva criterio**.

I criteri saranno ora attivi e genereranno eventuali avvisi e notifiche utente configurati.

## <a name="turn-off-a-policy"></a>Disattivare un criterio

È possibile disattivare un criterio in qualsiasi momento selezionando **Disattiva criterio** nell'angolo superiore destro della pagina dei dettagli di un criterio. Quando un criterio è disattivato, non rileva corrispondenze o genera avvisi o notifiche tramite posta elettronica. La disattivazione di un criterio non comporta l'eliminazione di un criterio. È possibile riattivare un criterio selezionando **Attiva criterio** nell'angolo superiore destro della pagina dei dettagli dei criteri.

## <a name="view-details-and-activity-from-the-policy-details-page"></a>Visualizzare i dettagli e l'attività dalla pagina dei dettagli dei criteri

Ogni criterio ha una pagina dei dettagli che mostra le attività rilevate dai criteri e le informazioni dettagliate che consentono di affrontare i rischi.

Dopo aver creato i criteri, selezionarne il nome nella tabella nella pagina **Criteri** principale. La scheda **Panoramica** della pagina dei dettagli dei criteri indica lo stato dei criteri, fornisce informazioni dettagliate sui dati ed evidenzia le corrispondenze dei criteri. Qui è possibile visualizzare i dettagli sulle corrispondenze di criteri specifici e altre informazioni sui passaggi successivi. Se il criterio è in esecuzione in modalità test, verranno visualizzati i passaggi successivi consigliati in questa pagina e un pulsante per attivare il criterio.

Quando il criterio è attivato, è possibile continuare a esaminare la relativa pagina dei dettagli dei criteri per visualizzare informazioni dettagliate in corso sulle aree problematiche, la gravità e le tendenze degli avvisi e le azioni correttive eseguite.

### <a name="overview-tab"></a>Scheda Panoramica

Nella scheda **Panoramica** della pagina dei dettagli dei criteri sono disponibili informazioni dettagliate sul rilevamento dei criteri rispetto ai tipi e ai percorsi dei dati e dell'attività dell'utente. Le informazioni dettagliate nella pagina dei dettagli del criterio sono descritte di seguito. Dopo aver attivato un criterio, possono essere richieste fino a 48 ore prima che i dati vengano visualizzati.

#### <a name="policy-status"></a>Stato dei criteri

La scheda di stato dei criteri indicherà se il criterio si trova in uno dei tre stati seguenti: **Test**, **Attivato** o **Disattivato**.

**Test**: questa sezione mostra il numero di giorni in cui i criteri sono stati in modalità di test, il che significa che sta cercando corrispondenze di criteri in base alle condizioni impostate, ma non genera avvisi o notifiche utente. Verrà fornita una raccomandazione quando è opportuno attivare i criteri. È possibile attivarlo in qualsiasi momento selezionando il pulsante **Attiva criterio** in questa scheda.

**On**: quando i criteri sono attivati, la scheda stato visualizza le metriche che evidenziano quando si è verificata un'azione correttiva dopo che un criterio corrisponde alla generazione di avvisi e notifiche utente.

- **Azioni utente eseguite**: questa metrica mostra il numero di azioni correttive eseguite dagli utenti quando viene richiesto da un messaggio di posta elettronica di notifica di uscire dal numero totale di notifiche inviate. Ad esempio, 8/10 rappresenta che su 10 notifiche utente inviate, gli utenti hanno eseguito un'azione di correzione in 8 istanze.

- **Velocità di risoluzione utente**: questa metrica è la frequenza con cui gli utenti eseguono azioni correttive in base al numero di notifiche generate. Se la percentuale è bassa, è possibile [modificare il contenuto del messaggio di posta elettronica](risk-management-notifications.md#preview-and-customize-email-content) o esaminare attentamente le corrispondenze per determinare se i criteri rilevano l'attività prevista.

- **Azioni di amministratore eseguite**: questa metrica mostra il numero di azioni correttive eseguite dagli amministratori quando viene generato un avviso dai criteri. Altre informazioni su [come eseguire azioni sugli avvisi](risk-management-alerts.md#manage-alerts).

- **Velocità di risoluzione dell'amministratore**: questa metrica è la frequenza con cui gli amministratori eseguono azioni correttive in base al numero di avvisi.

#### <a name="matches-by-location"></a>Corrispondenze per località

La scheda **Corrisponde in base alla posizione** visualizza il numero di elementi di contenuto rilevati dai criteri in base alla posizione Microsoft 365.

#### <a name="user-notifications"></a>Notifiche inviate all'utente

La scheda **Notifiche utente** visualizza un grafico a barre che mostra il numero di messaggi di posta elettronica di notifica utente generati dai criteri se tali funzionalità sono attivate.

#### <a name="matches-by-user"></a>Corrispondenze per utente

La scheda **Corrisponde per utente** elenca gli utenti principali le cui azioni hanno attivato una corrispondenza dei criteri. Verrà visualizzato il numero di eventi rilevati dai criteri per ogni utente, insieme al numero di azioni di correzione eseguite dalle notifiche tramite posta elettronica. Selezionare **Visualizza tutti gli utenti** in questa scheda per esaminare l'elenco completo degli utenti rilevati dai criteri.

#### <a name="matches-by-data-type"></a>Corrispondenze per tipo di dati

Nella scheda **Corrisponde per tipo di dati** vengono visualizzati i tipi di dati personali rilevati dalle corrispondenze dei criteri e la quantità di ogni tipo. Il grafico a torta consente di dimostrare visivamente se un determinato tipo di dati personali, ad esempio numeri di previdenza sociale o numeri di carta di credito, è rappresentato prevalentemente negli scenari di rischio che si sta tentando di identificare.

> [!TIP]
> Quando si esaminano in modo olistico le posizioni, i tipi di dati e il numero di utenti coinvolti nelle corrispondenze dei criteri, è possibile avere un'idea migliore dei tipi di misure di training e protezione dei dati necessarie per aiutare l'organizzazione a proteggere i dati personali archiviati.

### <a name="matched-items-tab"></a>Scheda Elementi corrispondenti

Nella scheda **Elementi corrispondenti** viene visualizzato un elenco di tutti gli elementi di contenuto corrispondenti a una condizione impostata nei criteri. Da questa visualizzazione è possibile selezionare un elemento dalla relativa riga per visualizzarlo in anteprima nella finestra a destra dell'elenco di elementi.

Nella finestra di anteprima sono disponibili le schede seguenti che forniscono dettagli su ogni elemento:
- **Origine**: visualizza i dati personali che hanno attivato la corrispondenza.
- **Dettagli**: visualizza il proprietario del contenuto (utente dell'organizzazione) per l'elemento, la posizione Microsoft 365 dell'elemento, il numero di tipi di dati personali all'interno dell'elemento e i tipi di dati personali specifici.
- **Attività file**: visualizza qualsiasi etichetta o classificazione applicata all'elemento.
- **Cronologia delle correzioni**: visualizza informazioni sulle azioni di correzione eseguite da utenti o amministratori sull'elemento.

## <a name="edit-a-policy"></a>Modificare un criterio

È possibile modificare le impostazioni per un criterio in qualsiasi momento, in modalità di test o attivato. È possibile aggiornare la maggior parte delle impostazioni dei criteri, incluso il ripristino di un criterio in modalità di test dopo l'attivazione. Le uniche impostazioni che non è possibile modificare sono il modello di criterio e il nome del criterio.

Per modificare un criterio, seguire questa procedura:

1. Nel [Centro conformità Microsoft 365](https://compliance.microsoft.com/) individuare Priva Privacy Risk Management nel riquadro di spostamento sinistro. Dal menu a discesa selezionare **Criteri**.

2. Selezionare il criterio da modificare dalla relativa riga nella pagina **Criteri** , che visualizza la pagina dei dettagli del criterio.

3. Nella pagina dei dettagli dei criteri selezionare il comando **Modifica** nell'angolo superiore destro della pagina. Questa azione consentirà di accedere alla creazione di criteri in Gestione dei rischi per la privacy.

4. Procedere con i passaggi per accedere alle impostazioni che si desidera modificare. È possibile modificare tutte le impostazioni, ad eccezione del modello di criterio e del nome del criterio. Selezionare **Avanti** per passare a ogni passaggio successivo.

5. Nella pagina **Fine** esaminare le impostazioni e quindi selezionare **Invia** per salvare le modifiche apportate.

## <a name="delete-a-policy"></a>Eliminare un criterio

Se è necessario rimuovere un criterio di gestione dei rischi per la privacy esistente, trovarlo nell'elenco nella pagina **Criteri** , selezionare il menu azione (puntini di sospensione verticali) e scegliere l'azione **Elimina criteri** . È anche possibile aprire la pagina dei dettagli del criterio e selezionare **Elimina** nell'angolo in alto a destra.

Verrà richiesto di confermare la scelta prima che l'eliminazione sia definitiva e i criteri vengano rimossi definitivamente. L'eliminazione di un criterio non influirà sui file valutati in precedenza dai criteri e i problemi e gli avvisi generati dal criterio verranno comunque elencati nelle pagine **Avvisi** e **problemi** .

## <a name="next-steps"></a>Passaggi successivi

Dopo l'attivazione dei criteri e l'avvio della generazione di avvisi, è consigliabile iniziare a comprendere i rischi che possono presentare all'organizzazione. Informazioni su come gestire gli avvisi, analizzare gli eventi ed eseguire azioni correttive in Gestione dei rischi per la privacy visitando [Analisi e correzione degli avvisi](risk-management-alerts.md).

## <a name="legal-disclaimer"></a>Legali

[Dichiarazione di non responsabilità legale di Microsoft Priva](priva-disclaimer.md)

---
title: Impostare le aziende per sincronizzare i dati master
description: Scopri come impostare una o più società per sincronizzare i dati master.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# <a name="get-ready-to-synchronize-master-data"></a>Preparati a sincronizzare i dati master

Quando due o più società utilizzano alcuni degli stessi dati anagrafici, è possibile sincronizzare i dati anziché aggiungerli manualmente in ciascuna società. Ad esempio, la sincronizzazione dei dati è particolarmente utile quando si impostano nuove società filiali.

I dati master includono impostazioni e informazioni non transazionali su entità aziendali. Ad esempio, clienti, fornitori, articoli e dipendenti. I dati forniscono il contesto per le transazioni commerciali. Di seguito sono riportati alcuni esempi di dati master per un cliente:

* Name
* Numero di identificazione
* Indirizzo
* Condizioni pagamento
* Limite credito

Imposti la sincronizzazione delle società filiali. Utilizzando un modello pull, le filiali estraggono i dati dalla società di origine di cui hanno bisogno per fare affari con loro. Dopo aver impostato la sincronizzazione e sincronizzato i dati per la prima volta, è tutto pronto. I movimenti coda processi aggiornano i record accoppiati nelle filiali quando qualcuno cambia i dati nella società di origine.

## <a name="uni-directional-synchronization-only"></a>Sincronizzazione solo unidirezionale

È possibile sincronizzare i dati solo dalla società di origine alle società filiali in modalità pull. Le filiali non possono inviare i dati alla società di origine.

> [!NOTE]
> Sebbene sia possibile, non è consigliabile configurare la sincronizzazione bidirezionale. Ovvero, sincronizzare i dati dalla società di origine alle filiali e dalle filiali alla società di origine. La sincronizzazione dei dati in entrambe le direzioni può causare conflitti o sovrascritture indesiderate.

## <a name="before-you-start"></a>Operazioni preliminari

Di seguito sono riportati i requisiti per impostare la sincronizzazione.

* Tutte le aziende devono trovarsi nello stesso ambiente.
* L'utente che configura la filiale deve avere una licenza **Essential**, **Premium** o **ISV di base**.

> [!NOTE]
> Le licenze Membro del team e Amministratore interno consentono di accedere ma non di modificare i record, quindi non possono essere utilizzate per configurare la sincronizzazione. La licenza Amministratore delegato non ti consente di pianificare attività in background, quindi non sarai in grado di completare la configurazione.

## <a name="specify-the-source-company"></a>Specificare la società di origine

I primi passaggi sono specificare la società che sarà l'origine dati e abilitare la sincronizzazione. Le società filiali estraggono i dati dalla società di origine.

> [!NOTE]
> Quando abiliti la sincronizzazione, [!INCLUDE [prod_short](includes/prod_short.md)] crea e pianifica le voci della coda processi che sincronizzano i dati. Potrebbe sembrare che le voci sincronizzino immediatamente i dati, ma non è così. Le voci della coda di lavoro create sincronizzano solo i record accoppiati e a questo punto non l'hai ancora impostato. La sincronizzazione inizia dopo che hai eseguito [Abilitare o disabilitare tabelle e campi](#enable-or-disable-tables-and-fields) e [Sincronizzare per la prima volta](#synchronize-for-the-first-time).

1. Nella filiale, scegli l'icona ![Lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup gestione dati master**, quindi scegli il collegamento correlato.
1. Nel campo **Società di origine** , specifica la società da cui estrarre le modifiche.
1. Attiva il pulsante di attivazione/disattivazione **Abilita sincronizzazione**.
1. Nella finestra di dialogo di conferma scegli **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] troverà le tabelle e i campi disponibili presso l'azienda di origine.

Il passaggio successivo consiste nell'abilitare tabelle e campi per la sincronizzazione.

## <a name="enable-or-disable-tables-and-fields"></a>Abilitare o disabilitare tabelle e campi

Per risparmiare tempo, [!INCLUDE [prod_short](includes/prod_short.md)] fornisce un elenco di tabelle che le aziende spesso sincronizzano. Per impostazione predefinita, queste tabelle sono abilitate per la sincronizzazione. Puoi modificarli, disabilitarli o eliminarli come meglio credi. Come ulteriore risparmio di tempo, alcuni campi delle tabelle sono già disabilitati perché probabilmente non rilevanti per la filiale.

> [!NOTE]
> Se nella società di origine sono installate una o più estensioni, quando una filiale imposta la sincronizzazione la pagina **Tabelle di sincronizzazione** include le tabelle delle estensioni e puoi accedere ai loro campi. Tuttavia, se la società di origine aggiunge un'estensione dopo l'impostazione della sincronizzazione, ogni filiale deve aggiungere manualmente le tabelle. Per ulteriori informazioni sull'aggiunta di tabelle, vai ad [Aggiungere o eliminare tabelle dall'elenco delle tabelle di sincronizzazione](#add-or-delete-tables-from-the-synchronization-tables-list). Per ulteriori informazioni sull'estensione [!INCLUDE [prod_short](includes/prod_short.md)], vai a [Sviluppo di estensioni in Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup gestione dati master**, quindi scegli il collegamento correlato.
1. Scegli l'azione **Tabelle di sincronizzazione**.
1. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Il campo **Filtro tabella** è utile per controllare cosa sincronizzare per una tabella. È possibile impostare i filtri per la sincronizzazione solo quando vengono soddisfatte determinate condizioni. Ad esempio, puoi aggiungere filtri che specificano di sincronizzare solo i fornitori in una determinata regione. Oppure, i clienti che utilizzano una determinata valuta.
>
> Se la filiale dispone già di dati nelle proprie tabelle, un altro buon modo per impostare i criteri per la sincronizzazione consiste nell'impostare l'accoppiamento basato sulle corrispondenze. Per saperne di più sulla corrispondenza, vai a [Utilizzare l'accoppiamento basato sulla corrispondenza](#use-match-based-coupling).

1. Per abilitare i campi per una tabella, scegli la tabella, quindi scegli l'azione **Campi**.
1. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Un modo rapido per abilitare o disabilitare più campi contemporaneamente è selezionarli nell'elenco, quindi utilizzare le azioni **Abilita** o **Disabilita**.

### <a name="use-match-based-coupling"></a>Usare l'associazione basata su corrispondenza

È possibile specificare i dati da sincronizzare per una tabella abbinando i record in base a criteri. Sulla pagina **Setup gestione dati master** scegli l'azione **Accoppiamento basato sulla corrispondenza** per aprire la pagina **Seleziona criteri di accoppiamento**. Puoi definire i seguenti criteri per la corrispondenza:

* Se eseguire la sincronizzazione dopo aver accoppiato i record.
* Se creare un nuovo record nella società filiale nel caso in cui non sia possibile trovare una corrispondenza unica non accoppiata utilizzando i criteri di corrispondenza. Per attivare questa capacità, attiva l'azione **Crea nuovo se non si trova accoppiamento** .
* I campi da utilizzare per la corrispondenza dei record e se la corrispondenza fa distinzione tra maiuscole e minuscole.
* Dai priorità all'ordine di ricerca dei record specificando una priorità di corrispondenza. [!INCLUDE [prod_short](includes/prod_short.md)] cercherà una corrispondenza in ordine crescente in base alla priorità corrispondenza. Un valore vuoto equivale alla priorità 0, che è la priorità più alta. I campi con priorità 0 vengono considerati per primi.

## <a name="synchronize-for-the-first-time"></a>Sincronizzare per la prima volta

Quando sei pronto, sulla pagina **Setup gestione dati master** scegli l'azione **Avvia sincronizzazione iniziale**. Sulla pagina **Sincronizzazione iniziale dati master** scegli il tipo di sincronizzazione che desideri utilizzare per ogni tabella.

* Se disponi già di record sia nella società di origine che nella filiale e desideri creare una corrispondenza con i record esistenti, scegli l'azione **Usa l'accoppiamento basato sulla corrispondenza**. [!INCLUDE [prod_short](includes/prod_short.md)] confronta i record nella società controllata con i record nella società di origine. Le corrispondenze si basano sui criteri di corrispondenza definiti dall'utente. Per diverse tabelle predefinite, [!INCLUDE [prod_short](includes/prod_short.md)] ha già abbinato i record esistenti utilizzando la loro chiave primaria, ma puoi modificarli se lo desideri. È inoltre possibile consentire alla sincronizzazione di creare nuovi record nella filiale per i record nella società di origine che la filiale non possiede. Per saperne di più sulla corrispondenza, vai a [Utilizzare l'accoppiamento basato sulla corrispondenza](#use-match-based-coupling).
* Se scegli **Esegui sincronizzazione completa**, la sincronizzazione crea nuovi record per tutti i record nella società di origine che non sono ancora stati accoppiati. Ad esempio, questa opzione è utile nei seguenti scenari:

    * La filiale non ha dati nella tabella.
    * Desideri aggiungere record dalla società di origine senza corrispondenze.  

Dopo aver scelto l'opzione da utilizzare, scegli l'azione **Avvia tutto** per avviare la sincronizzazione.

Mentre la sincronizzazione è in esecuzione, la colonna **Stato processo** nella pagina **Sincronizzazione completa iniziale dati master** mostra lo stato di ciascun movimenti coda processi. Premi **F5** sulla tastiera per aggiornare lo stato.

> [!TIP]
> Le tabelle si sincronizzano in un ordine predefinito. Se la sincronizzazione si blocca su una tabella, seleziona la tabella e poi scegli l'azione **Riavvia** per farla ripartire.

Per accedere ai dettagli, come il numero di record inseriti o modificati, scegli il valore nella colonna **Stato processo** per aprire la pagina **Visualizza - Processi di sincronizzazione integrazione**. Per i record che sono stati inseriti, puoi scegliere il numero nella colonna **Inseriti** per accedere a maggiori dettagli sui nuovi record.

## <a name="add-or-delete-tables-from-the-synchronization-tables-list"></a>Aggiungere o eliminare tabelle dall'elenco delle tabelle di sincronizzazione

### <a name="add-a-table"></a>Aggiungere una tabella

> [!IMPORTANT]
> Sebbene nell'elenco siano disponibili tabelle che contengono dati transazionali, ad esempio tabelle che contengono movimenti contabili, non è consigliabile sceglierle. La sincronizzazione funziona solo per le tabelle che contengono dati non transazionali.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Tabelle di sincronizzazione**, quindi scegli il collegamento correlato.
1. Scegli **Nuovo**, quindi scegli la tabella da aggiungere.
1. Compila i campi in base alle esigenze. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### <a name="delete-a-table"></a>Eliminare una tabella

> [!NOTE]
> Se elimini un record nella società di origine, non viene eliminato anche nella filiale. Questo aiuta a prevenire la perdita indesiderata di dati. La filiale può decidere di eliminare la tabella se lo desidera.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Tabelle di sincronizzazione**, quindi scegli il collegamento correlato.
1. Scegliere l'azione **Elimina**.

## <a name="use-export-and-import-to-share-a-synchronization-setup"></a>Usare l'esportazione e l'importazione per condividere una configurazione di sincronizzazione

Se stai configurando diverse filiali che utilizzano impostazioni di sincronizzazione uguali o simili, c'è un risparmio di tempo. Configura una società consociata e quindi esportane l'impostazione in un file .xml. Il file contiene l'intera configurazione, inclusi i mapping di tabelle e campi e i criteri di filtro. È quindi possibile importare il file nella filiale successiva. Per importare o esportare un'impostazione, nella pagina **Setup gestione dati master** utilizza l'azione **Importa** o **Esporta**.

## <a name="see-also"></a>Vedere anche

[Gestire la sincronizzazione dei dati master](admin-sync-master-data.md)

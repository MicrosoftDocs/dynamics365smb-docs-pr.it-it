---
title: Informazioni sull'impostazione dell'IVA | Documenti Microsoft
description: Assicurarsi di calcolare, registrare e creare report corretti per l'IVA di vendite e acquisti.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 733405000725ccfca2a1bdd1bb2a893e6f5f3536
ms.contentlocale: it-it
ms.lasthandoff: 11/10/2017

---

# <a name="setting-up-to-calculations-and-posting-methods-for-value-added-tax"></a>Impostazione dei calcoli e registrazione dei metodi per l'IVA
I consumatori e le imprese pagano l'imposta sul valore aggiunto (IVA) quando acquistano beni o servizi. L'importo dell'IVA da pagare può variare, a seconda di diversi fattori. In [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile impostare l'IVA per specificare l'aliquota da utilizzare per calcolare gli importi IVA in base a quanto segue: 

* Persone a cui si vende  
* Persone da cui si acquista  
* Merci vendute  
* Merci acquistate  
  
È possibile impostare manualmente i calcoli IVA, ma può essere complesso e richiedere molto tempo. Per rendere più semplice questa operazione, è disponibile un setup assistito **Setup IVA** con passaggi guidati. Si consiglia di utilizzare il setup assistito per impostare l'IVA.

> [!NOTE]  
>   Si può utilizzare questa procedura guidata solo se è stata creata una società La mia azienda e se non sono state registrate transazioni con IVA. In caso contrario, sarebbe molto facile utilizzare erroneamente diverse aliquote IVA e rendere inaccurati i report sull'IVA.  
  
Se si desidera impostare i calcoli IVA manualmente, o se si desidera conoscere ciascun passaggio, in questo argomento vengono fornite descrizioni per ogni fase.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Per utilizzare il setup IVA assistito per impostare l'IVA (consigliato)
Si consiglia di utilizzare il setup IVA assistito per impostare l'IVA in [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

Per avviare la Guida assistita al setup, attenersi a questa procedura:
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report") e immettere **Setup assistito**.  
2. Scegliere **Setup IVA**.

## <a name="to-set-up-vat-business-posting-groups"></a>Per impostare le categorie di registrazione business IVA
Le categorie di registrazione business IVA dovrebbero rappresentare i mercati in cui si intrattengono relazioni commerciali con clienti e fornitori e dovrebbero definire il modo in cui calcolare l'IVA in ogni mercato. Esempi di categoria di registrazione business IVA sono **Nazionale** e **Unione Europea (UE)**.  

Utilizzare codici semplici da ricordare e che descrivano la categoria di registrazione business, ad esempio **Nazionale**, **UE**, **Non UE**. Il codice deve essere unico. Non è possibile utilizzare lo stesso codice più volte in una tabella, sebbene sia possibile impostare un numero indefinito di codici.
  
Per impostare una categoria di registrazione business IVA, attenersi a questa procedura:

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

Le categorie di registrazione business IVA di default vengono impostate collegandole alle categorie di registrazione business. [!INCLUDE[d365fin](includes/d365fin_md.md)] assegna automaticamente la categoria di registrazione business IVA quando viene assegnata la categoria di registrazione business a un cliente, un fornitore o un conto di contabilità generale. 

## <a name="to-set-up-vat-product-posting-groups"></a>Per impostare le categorie di registrazione articoli/servizi IVA
Le categorie di registrazione articoli/servizi IVA rappresentano articoli e risorse acquistate o vendute e determinano la tipologia di calcolo e di registrazione dell'IVA in base al tipo di articolo o risorsa acquistato o venduto.  
Si consiglia di utilizzare codici semplici da ricordare e descrittivi. Ad esempio, **NO-IVA** o **Zero**, **IVA10** o **Ridotta** per IVA al 10% e **IVA25** o **Standard** per il 25%.

Per impostare una categoria di registrazione business IVA, attenersi a questa procedura:

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Per combinare le categorie di registrazione IVA nei setup registrazione IVA
[!INCLUDE[d365fin](includes/d365fin_md.md)] calcola gli importi IVA su vendite e acquisti in base alle impostazioni di registrazione IVA, che sono combinazioni di categorie di registrazione business e di categorie di registrazione articoli/servizi IVA. Per ogni combinazione, è possibile specificare la percentuale IVA, la tipologia di calcolo IVA e i numeri di conto C/G per la registrazione dell'IVA relativa a vendite e acquisti e dell'IVA intracomunitaria. È inoltre possibile specificare se l'IVA viene ricalcolata quando viene applicato o ricevuto uno sconto pagamento.  

È possibile impostare un numero illimitato di combinazioni. Se si desidera raggruppare combinazioni di setup di registrazioni IVA con attributi simili, è possibile definire un **codice IVA** per ogni categoria e assegnare il codice ai membri della categoria.

Per combinare setup di registrazioni IVA, attenersi a questa procedura:

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.
2. Compilare i campi come necessario.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Per assegnare le categorie di registrazione IVA per impostazione predefinita a più entità
Se si desidera applicare le stesse categorie di registrazione IVA a più entità, è possibile impostare [!INCLUDE[d365fin](includes/d365fin_md.md)] per effettuare questa operazione in modo predefinita. Esistono due metodi per farlo:

* È possibile assegnare le categorie di registrazione business IVA a categorie di registrazione business generali, o modelli cliente o fornitore 
* È possibile assegnare le categorie di registrazione articolo/categorie IVA in categorie di registrazione di articoli e servizi generali  

La categoria registrazione business o articoli/servizi IVA è assegnata quando si sceglie una categoria registrazione business o articoli/servizi per un cliente, un fornitore, un articolo o una risorsa.

## <a name="to-assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Per assegnare le categorie di registrazione IVA a singoli conti, clienti, fornitori, articoli e risorse
Nelle sezioni successive viene descritto come assegnare le categorie di registrazione IVA alle singole entità.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Per assegnare categorie di registrazione IVA a singoli conti di contabilità generale 
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Piano dei conti**, quindi scegliere il collegamento correlato.  
2. Aprire la scheda **Conto C/G** per il conto.  
3. Nella Scheda dettaglio **Registrazione**, nel campo **Tipo reg. gen.**, selezionare **Vendita** o **Acquisto**.  
5. Scegliere le categorie di registrazione IVA da utilizzare per il conto vendite o acquisti.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Per assegnare le categorie di registrazione business IVA a clienti e fornitori  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona  Cerca pagina o report") , immettere **Cliente** o **Fornitore** e scegliere il collegamento correlato.  
2. Nella scheda del **Cliente** o **Fornitore**, espandere la Scheda dettaglio **Fatturazione**.  
3. Scegliere la categoria di registrazione business IVA.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Per assegnare le categorie di registrazione articoli/servizi IVA a singoli articoli e risorse  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona  Cerca pagina o report") , immettere **Cliente** o **Fornitore** e scegliere il collegamento correlato.  
2. Effettuare una delle seguenti operazioni:  

* Nella scheda **Articolo** espandere la Scheda dettaglio **Prezzo e registrazione** quindi scegliere **Mostra di più** per visualizzare il campo **Cat. reg. art./serv. IVA**.  
* Nella scheda **Risorsa** espandere la Scheda dettaglio **Fatturazione**.  
3. Scegliere la categoria di registrazione articoli/servizi IVA.  

## <a name="to-set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Per impostare le categorie con cui descrivere l'utilizzo di aliquote IVA non standard
È possibile impostare una categoria IVA per descrivere informazioni sul tipo di IVA che viene applicata. Le informazioni possono essere obbligatorie per la normativa statale. Dopo aver impostato una categoria IVA e averla associata a un setup registrazioni IVA, la categoria IVA viene visualizzata su tutti i documenti di vendita stampati con tale categoria di setup registrazioni IVA. 

Se necessario, è anche possibile specificare come tradurre automaticamente le categorie IVA in altre lingue. Successivamente, quando si crea e si stampa un documento di vendita contenente un codice IVA, il documento includerà la categoria IVA nel testo tradotto. Il codice lingua specificato nella scheda cliente determina la lingua.

È possibile modificare o eliminare una categoria IVA. Le modifiche si rifletteranno in un report generato. Tuttavia, [!INCLUDE[d365fin](includes/d365fin_md.md)] non conserva una cronologia della modifica. Nel report, le descrizioni della categoria IVA vengono stampate e visualizzate per tutte le righe del report accanto all'importo IVA e all'imponibile IVA. Se una categoria IVA non è stata definita per alcune righe del documento di vendita, allora viene omessa l'intera sezione quando il report viene stampato.
  
### <a name="to-set-up-vat-clauses"></a>Impostare categorie IVA
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Categorie IVA** e scegliere il collegamento correlato.  
2. Nella pagina **Categorie IVA** creare una nuova riga.  
3. Nel campo **Codice** immettere un identificatore per la categoria. Il codice viene usato per assegnare la categoria ai categorie di registrazione IVA.  
4. Nel campo **Descrizione** immettere il testo che si desidera visualizzare nei documenti che possono includere l'IVA. Nel campo **Descrizione 2** immettere testo aggiuntivo, se necessario. Il testo viene visualizzato nelle nuove righe.  
5. Facoltativo: per assegnare direttamente la categoria IVA a un setup registrazioni IVA, scegliere **Setup** e quindi la categoria. Se si desidera attendere, è possibile assegnare la categoria in seguito nella pagina Setup registrazioni IVA.  
6. Facoltativo: per specificare come tradurre automaticamente la categoria IVA scegliere l'azione **Traduzioni**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Per assegnare una categoria IVA a un setup di registrazione
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
2. Nella colonna **Categoria IVA** selezionare la categoria e utilizzarla per ogni setup registrazione IVA a cui si applica.  

### <a name="to-specify-translations-for-vat-clauses"></a>Per specificare le traduzioni per le categorie IVA
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Categorie IVA** e scegliere il collegamento correlato.  
2. Scegliere l'azione **Traduzioni**.  
3. Nel campo **Codice lingua** selezionare la lingua verso cui tradurre.  
4. Nei campi **Descrizione** e **Descrizione 2** immettere il testo tradotto delle descrizioni. Questo testo viene visualizzato nei documenti di report IVA tradotti.  
  
## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Per creare un setup registrazioni IVA per gestire l'IVA sulle importazioni
La funzionalità relativa all'IVA sulle importazioni viene utilizzata quando è necessario registrare un documento in cui l'intero importo è IVA. Si userà questa funzionalità quando si riceve una fattura con IVA dalle autorità fiscali per merci importate.  
  
Per impostare i codici per l'IVA sull'importazione, attenersi a questa procedura:  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
2. Nella pagina Categorie reg. art./serv. IVA impostare una nuova categoria di registrazione articoli/servizi IVA per l'IVA da importazione.  
3. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
4. Nella pagina Setup registrazioni IVA creare una nuova riga o utilizzare una delle categorie di registrazione business IVA esistenti in combinazione con la nuova categoria di registrazione articoli/servizi IVA per l'IVA da importazione.  
5. Nel campo **Tipologia IVA** selezionare **Sola IVA**.  
6. Nel campo **Conto IVA Acquisti** immettere il conto C/G da utilizzare per registrare l'IVA da importazione. Tutti gli altri conti sono facoltativi.  
  
## <a name="to-verify-vat-registration-numbers"></a>Per verificare la partita IVA
È importante che la partita IVA per clienti, fornitori e contatti sia valida. Ad esempio, le aziende cambiano talvolta lo stato di passività fiscale e in alcuni paesi le autorità fiscali potrebbero chiedere di fornire report, come il report IVA dell'elenco vendite UE, che elenca i numeri di partita IVA utilizzati per l'attività. 
  
La Commissione Europea offre un servizio di convalida dei numeri di partita IVA (VIES) tramite il proprio sito Web, che è pubblico e libero. [!INCLUDE[d365fin](includes/d365fin_md.md)] consente di risparmiare tale passaggio e di utilizzare il servizio VIES per convalidare e tracciare i numeri IVA per i clienti, i fornitori e i contatti direttamente dalle schede cliente, venditore e di contatto. Il servizio in [!INCLUDE[d365fin](includes/d365fin_md.md)] è denominato **servizio di convalida partita IVA comunitaria**. Il servizio è disponibile nella pagina **Connessioni servizio** e sarà possibile iniziare a utilizzarlo da subito. La connessione del servizio è gratuita e la registrazione non è necessaria.

> [!Note]
> Per abilitare il servizio di convalida partita IVA comunitaria, è necessario disporre di autorizzazioni di amministratore.

Quando si utilizza la connessione del servizio, viene registrata una cronologia dei numeri di partita IVA e delle verifiche per ogni cliente, fornitore o contatto, nel **Log partita IVA**, in modo da poterli facilmente tracciare. Il log è specifico per ogni cliente. Ad esempio, il log è utile per dimostrare di aver verificato che il numero di partita IVA corrente è corretto. Quando si verifica un numero di partita IVA, la colonna **Identificatore di richiesta** nel log indicherà che l'azione è stata eseguita. 

È possibile visualizzare il log di registrazione IVA nella scheda cliente, fornitore o di contatto, nella Scheda dettaglio **Fatturazione**, scegliendo il pulsante di ricerca nel campo **Partita IVA**.  

Il servizio consente anche di risparmiare tempo quando si crea un cliente o un fornitore. Se si conosce il numero di partita IVA del cliente, è possibile immetterlo nel campo **Partita IVA** nelle schede Cliente o Fornitore e la ragione sociale del cliente verrà compilato automaticamente. Alcuni paesi forniscono anche indirizzi aziendali in un formato strutturato. In questi paesi, l'indirizzo verrà compilato automaticamente.  

> [!NOTE]  
> Ci sono un paio di cose da notare sul servizio di convalida dei numeri di partita IVA VIES:

* Il servizio Web utilizza il protocollo HTTP, il che significa che i dati trasferiti tramite il servizio non sono crittografati.  
* È possibile che si verifichi un tempo di inattività per questo servizio per cui Microsoft non è responsabile. Il servizio fa parte di un'ampia rete europea di registri IVA nazionali.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Utilizzo dell'IVA intracomunitaria per il commercio tra i paesi della UE
Per il commercio tre due società nell'Unione Europea, per alcune società è necessario utilizzare l'IVA intracomunitaria. Ad esempio, la regola si applica agli acquisti e alle vendite nei paesi UE.  
  
> [!NOTE]  
> Questa regola è valida per il commercio con società registrate come soggette a IVA in un altro paese UE. Se si hanno relazioni commerciali dirette con clienti in altri paesi UE, è necessario contattare le autorità fiscali per informazioni sulle regole IVA applicabili.  
  
> [!TIP]  
> È possibile verificare che la società sia registrata come soggetto IVA in un altro paese UE utilizzando il servizio di convalida partita IVA UE. Il servizio è disponibile gratuitamente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere la sezione relativa _Verifica partita IVA_ in questo argomento.

### <a name="sales-to-eu-countries-or-regions"></a>Vendite ai paesi UE
Sulle vendite a società soggette a IVA in altri paesi UE l'IVA non viene calcolata. È necessario indicare il valore di tali vendite ai paesi UE separatamente nella dichiarazione IVA.  

Per calcolare correttamente l'IVA sulle vendite nei paesi UE, è necessario effettuare le seguenti operazioni:  
  
* Impostare una riga per le vendite con le stesse informazioni degli acquisti. Se sono già state impostate righe nella pagina Setup registrazioni IVA per gli acquisti dai paesi UE, è possibile quindi utilizzare tali righe anche per le vendite.  
* Assegnare categorie di registrazione business IVA nel campo **Cat. reg. business IVA** nella Scheda dettaglio **Fatturazione** della scheda cliente di ciascun cliente dell'UE. È inoltre necessario immettere la partita IVA del cliente nel campo **Partita IVA** della Scheda dettaglio **Commercio estero**.  

Quando si registra una vendita a un cliente in un altro paese UE, viene calcolato l'importo IVA e viene creato un movimento IVA con le informazioni sull'IVA intracomunitaria e sull'imponibile IVA, ovvero l'importo utilizzato per calcolare l'importo IVA. Non vengono registrati movimenti nei conti IVA nella contabilità generale.

## <a name="understanding-vat-rounding-for-documents"></a>Informazioni sull'arrotondamento IVA per i documenti
Gli importi nei documenti che non sono ancora stati registrati vengono arrotondati e visualizzati in modo da corrispondere all'arrotondamento finale degli importi effettivamente registrati. L'IVA viene calcolata per un documento completo, cioè l'IVA che viene calcolata è basata sulla somma di tutte le righe con lo stesso identificatore IVA nel documento.

## <a name="understanding-the-vat-rate-conversion-process"></a>Informazioni sul processo di conversione dell'aliquota IVA  
Lo strumento di modifica dell'aliquota IVA effettua le conversioni di aliquota IVA per dati master, registrazioni e ordini in modalità diverse. Le registrazioni e i dati master selezionati verranno aggiornati in base alla nuova categoria di registrazione articoli/servizi o a quella relativa agli articoli/servizi IVA. Se un ordine è stato spedito completamente o in parte, gli articoli spediti conserveranno la categoria di registrazione articoli/servizi o quella di articoli/servizi IVA corrente. Per gli articoli non spediti verrà creata una nuova riga ordine che verrà aggiornata in modo da corrispondere alle categorie di registrazione articoli/servizi o a quelle di articoli/servizi IVA correnti e nuove. Inoltre, verranno aggiornati di conseguenza gli impegni, le assegnazioni di addebito articoli e le informazioni sulla tracciabilità degli articoli.  
  
Esistono, tuttavia, alcuni elementi che lo strumento non converte:

* Ordini e fatture di vendita o di acquisto, in caso di registrazione delle spedizioni. Questi documenti vengono registrati utilizzando l'aliquota IVA corrente.  
* Documenti con fatture pagamento anticipato registrate. Ad esempio, se sono stati effettuati o ricevuti pagamenti anticipati relativi a fatture che non sono state completate prima dell'utilizzo dello strumento di modifica dell'aliquota IVA. In questo caso, vi sarà una differenza tra l'IVA dovuta e quella pagata nei pagamenti anticipati quando la fattura viene completata. Con lo strumento di modifica dell'aliquota IVA sarà possibile ignorare questi documenti che dovranno però essere aggiornati manualmente.  
* Spedizioni dirette o ordini speciali.  
* Ordini di vendita o di acquisto con l'integrazione warehouse qualora siano parzialmente spediti o ricevuti.  
* Contratti di assistenza.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Per preparare conversioni di modifica dell'aliquota IVA  
Prima di impostare lo strumento di modifica dell'aliquota IVA, è necessario effettuare le preparazioni riportate di seguito.

* Se si effettuano transazioni in cui si utilizzano aliquote differenti, esse devono essere separate in gruppi differenti creando nuovi conti di contabilità generale per ogni aliquota o utilizzando filtri di dati per raggruppare le transazioni in base all'aliquota.  
* Se si creano nuovi conti di contabilità generale, è necessario creare nuove categorie di registrazioni generali.  
* Per ridurre il numero di documenti che vengono convertiti, registrare il maggior numero di documenti possibile e ridurre al minimo quelli non registrati.  
* Eseguire il backup dei dati.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Per impostare lo strumento di modifica dell'aliquota IVA  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup modifiche aliquota IVA** e scegliere il collegamento correlato.  
2. Nelle Schede dettaglio **Dati master**, **Registrazioni** e **Documenti** scegliere un valore della categoria registrazione dall'elenco di opzioni per i campi necessari.  
  
### <a name="to-set-up-product-posting-group-conversion"></a>Per impostare la conversione delle categorie di registrazione prodotti  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup modifiche aliquota IVA** e scegliere il collegamento correlato.  
2. Nella pagina **Setup modifiche aliquota IVA**, nella scheda **Pagina iniziale**, nel gruppo **Processo** scegliere **Conv. cat. reg. art./serv. IVA** o **Conv. cat. reg. articolo/servizio**.  
3. Nel campo **Da codice** immettere la categoria di registrazione corrente.  
4. Nel campo **A codice** immettere la nuova categoria di registrazione.  

### <a name="to-perform-vat-rate-change-conversion"></a>Per eseguire la conversione della modifica dell'aliquota IVA  
È possibile utilizzare lo strumento di modifica aliquota IVA per gestire le modifiche nell'aliquota IVA standard. Vengono eseguite le conversioni della categoria di registrazione generale e dell'IVA per modificare le aliquote IVA e gestire il reporting IVA accurato. In base all'impostazione vengono apportate le modifiche seguenti:  
  
* Le categorie registrazione generale e IVA vengono convertite.  
* Le modifiche vengono apportate nei conti di contabilità generale, nei clienti, nei fornitori, nei documenti aperti, nelle righe di registrazione e anche in altri documenti.  
  
> [!IMPORTANT]  
>  Prima di eseguire la conversione modifica aliquota IVA, è possibile eseguire i test della conversione. A tale scopo, eseguire la procedura riportata di seguito, ma assicurarsi di deselezionare le caselle di controllo **Esegui conversione** e **Strumento di modifica aliquota IVA completato**. Durante la conversione di test, il campo **Convertito** nella tabella **Movimento log modifiche aliquota IVA** è stato rimosso e il campo **Data convertita** nella tabella **Movimento log modifiche aliquota IVA** è vuoto. Al termine della conversione, scegliere **Voci log modifiche aliquota IVA** per visualizzare i risultati del test di conversione. Verificare ciascun movimento prima di eseguire la conversione. In particolare, verificare le transazioni che usano un'aliquota IVA precedente.     

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Modifica aliquota IVA** e quindi scegliere il collegamento **Setup modifiche aliquota IVA**.  
2. Verificare che sia già stata impostata la conversione della categoria di registrazione articoli/servizi IVA o quella relativa agli articoli/servizi.  
3. Selezionare la casella di controllo **Esegui conversione**.  
  
> [!IMPORTANT]  
    >  Deselezionare la casella controllo **Strumento di modifica aliquota IVA completato**. La casella di controllo viene selezionata automaticamente al termine della conversione della modifica dell'aliquota IVA.  
  
4. Scegliere l'azione **Converti**.  
5. Al termine della conversione, nel gruppo **Processo** della scheda **Pagina iniziale** selezionare **Voci log modifiche aliquota IVA** per visualizzare i risultati della conversione.  
  
> [!IMPORTANT]  
>  Dopo la conversione, il campo **Convertito** nella tabella **Movimento log modifiche aliquota IVA** è selezionato e il campo **Data convertita** nella tabella **Movimento log modifiche aliquota IVA** visualizza la data di conversione.  
  
## <a name="see-also"></a>Vedi anche  
[Setup dell'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)  
[Procedura: Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Procedura: Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  

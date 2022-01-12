---
title: Impostare l'IVA (imposta sul valore aggiunto)
description: Assicurarsi di calcolare, registrare e creare report corretti per l'IVA di vendite e acquisti. Si consiglia di utilizzare il setup assistito per impostare l'IVA.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 12/28/2021
ms.author: bholtorf
ms.openlocfilehash: b4d9c6985000497f5a63f21ea06a9246d6a8ca19
ms.sourcegitcommit: 3a2d61f7d655e9753c1477d21149c83ea6b7fe7a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/28/2021
ms.locfileid: "7947014"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Setup dei calcoli e registrazione dei metodi per l'IVA

I consumatori e le imprese pagano l'imposta sul valore aggiunto (IVA) quando acquistano beni o servizi. L'importo dell'IVA da pagare può variare, a seconda di diversi fattori. In [!INCLUDE[prod_short](includes/prod_short.md)], puoi impostare l'IVA per specificare l'aliquota da utilizzare per calcolare gli importi IVA in base ai seguenti parametri:

* Persone a cui si vende  
* Persone da cui si acquista  
* Merci vendute  
* Merci acquistate  

È possibile impostare manualmente i calcoli IVA, ma può essere complesso e richiedere molto tempo. Per rendere più semplice questa operazione, è disponibile un setup assistito **Setup IVA** con passaggi guidati. Si consiglia di utilizzare il setup assistito per impostare l'IVA.

> [!NOTE]  
> Si può utilizzare questa procedura guidata solo se è stata creata una società La mia azienda e se non sono state registrate transazioni con IVA. In caso contrario, sarebbe molto facile utilizzare erroneamente diverse aliquote IVA e rendere inaccurati i report sull'IVA.  

Se si desidera impostare i calcoli IVA manualmente, o se si desidera conoscere ciascun passaggio, in questo argomento vengono fornite descrizioni per ogni fase.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Utilizzare il setup IVA assistito per impostare l'IVA (consigliato)

Si consiglia di utilizzare il setup IVA assistito per impostare l'IVA in [!INCLUDE[prod_short](includes/prod_short.md)].

Per avviare la Guida assistita al setup, attenersi a questa procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup assistito**.  
2. Scegliere **Imposta l'IVA** e completare i passaggi.
3. Dopo aver completato il setup assistito, visita la pagina **Setup registrazioni IVA** e verifica se è necessario compilare campi aggiuntivi in base ai requisiti della versione di [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Funzionalità locale in Business Central](about-localization.md)  

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Impostare i numeri di partita IVA per il paese o l'area geografica

Per garantire che le persone inseriscano numeri di partita IVA validi, è possibile definire i formati per i numeri di partita IVA utilizzati nei paesi in cui si opera. [!INCLUDE[prod_short](includes/prod_short.md)] visualizzerà un messaggio di errore quando qualcuno commette un errore o utilizza un formato non corretto per il paese.

Per impostare i numeri di partita VAT, attenersi a questa procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Paesi/Aree geografiche**.
2. Specificare il paese e quindi scegliere l'azione **Formati Nr. P. IVA**.
3. Nel campo **Formati**, specificare il formato immettendo uno o più dei seguenti caratteri:  

* **#** Richiede un numero a una cifra.  
* **@** Richiede una lettera. Il formato non rispetta la distinzione tra maiuscole e minuscole.  
* **?** Consente qualsiasi carattere.  

    > [!Tip]
    > È possibile utilizzare altri caratteri purché siano sempre presenti nel formato del paese. Ad esempio, se è necessario includere un punto o un trattino tra i set di numeri, è possibile definire il formato come ##.####.### o @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Impostare le categorie di registrazione business IVA

Le categorie di registrazione business IVA dovrebbero rappresentare i mercati in cui si intrattengono relazioni commerciali con clienti e fornitori e dovrebbero definire il modo in cui calcolare l'IVA in ogni mercato. Esempi di categoria di registrazione business IVA sono **Nazionale** e **Unione Europea (UE)**.  

Utilizzare codici semplici da ricordare e che descrivano la categoria di registrazione business, ad esempio **Nazionale**, **UE**, **Non UE**. Il codice deve essere unico. Non è possibile utilizzare lo stesso codice più volte in una tabella, sebbene sia possibile impostare un numero indefinito di codici.

Per impostare una categoria di registrazione business IVA, attenersi a questa procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cat. reg. business IVA**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

Le categorie di registrazione business IVA di default vengono impostate collegandole alle categorie di registrazione business. [!INCLUDE[prod_short](includes/prod_short.md)] assegna automaticamente la categoria di registrazione business IVA quando viene assegnata la categoria di registrazione business a un cliente, un fornitore o un conto di contabilità generale.

## <a name="set-up-vat-product-posting-groups"></a>Impostare le categorie di registrazione articoli/servizi IVA

Le categorie di registrazione articoli/servizi IVA rappresentano articoli e risorse acquistate o vendute e determinano la tipologia di calcolo e di registrazione dell'IVA in base al tipo di articolo o risorsa acquistato o venduto.  
Si consiglia di utilizzare codici semplici da ricordare e descrittivi. Ad esempio, **NO-IVA** o **Zero**, **IVA10** o **Ridotta** per IVA al 10% e **IVA25** o **Standard** per il 25%.

Per impostare una categoria di registrazione business IVA, attenersi a questa procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazioni articoli/servizi IVA**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Combinare le categorie di registrazione IVA nei setup registrazione IVA

[!INCLUDE[prod_short](includes/prod_short.md)] calcola gli importi IVA su vendite e acquisti in base alle impostazioni di registrazione IVA, che sono combinazioni di categorie di registrazione business e di categorie di registrazione articoli/servizi IVA. Per ogni combinazione, è possibile specificare la percentuale IVA, la tipologia di calcolo IVA e i numeri di conto C/G per la registrazione dell'IVA relativa a vendite e acquisti e dell'IVA intracomunitaria. È inoltre possibile specificare se l'IVA viene ricalcolata quando viene applicato o ricevuto uno sconto pagamento.  

È possibile impostare un numero illimitato di combinazioni. Se si desidera raggruppare combinazioni di setup di registrazioni IVA con attributi simili, è possibile definire un **codice IVA** per ogni categoria e assegnare il codice ai membri della categoria.

Per combinare setup di registrazioni IVA, attenersi a questa procedura:

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Assegnare le categorie di registrazione IVA per impostazione predefinita a più entità

Se si desidera applicare le stesse categorie di registrazione IVA a più entità, è possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] per effettuare questa operazione in modo predefinita. Esistono due metodi per farlo:

* È possibile assegnare le categorie di registrazione business IVA a categorie di registrazione business generali, o modelli cliente o fornitore
* È possibile assegnare le categorie di registrazione articolo/categorie IVA in categorie di registrazione di articoli e servizi generali  

La categoria registrazione business o articoli/servizi IVA è assegnata quando si sceglie una categoria registrazione business o articoli/servizi per un cliente, un fornitore, un articolo o una risorsa.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Assegnare le categorie di registrazione IVA a conti, clienti, fornitori, articoli e risorse

Nelle sezioni successive viene descritto come assegnare le categorie di registrazione IVA alle singole entità.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Per assegnare categorie di registrazione IVA a singoli conti di contabilità generale

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
2. Aprire la scheda **Conto C/G** per il conto.  
3. Nella Scheda dettaglio **Registrazione**, nel campo **Tipo reg. gen.**, selezionare **Vendita** o **Acquisto**.  
4. Scegliere le categorie di registrazione IVA da utilizzare per il conto vendite o acquisti.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Per assegnare le categorie di registrazione business IVA a clienti e fornitori

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cliente** o **Fornitore**, quindi scegli il collegamento correlato.  
2. Nella scheda del **Cliente** o **Fornitore**, espandere la Scheda dettaglio **Fatturazione**.  
3. Scegliere la categoria di registrazione business IVA.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Per assegnare le categorie di registrazione articoli/servizi IVA a singoli articoli e risorse

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articolo** o **Risorsa**, quindi scegli il collegamento correlato.  
2. Effettuare una delle seguenti operazioni:  

    * Nella scheda **Articolo** espandere la Scheda dettaglio **Prezzo e registrazione** quindi scegliere **Mostra di più** per visualizzare il campo **Cat. reg. art./serv. IVA**.  
    * Nella scheda **Risorsa** espandere la Scheda dettaglio **Fatturazione**.  
3. Scegliere la categoria di registrazione articoli/servizi IVA.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Impostare le categorie per spiegare l'esenzione IVA o le aliquote IVA non standard

È possibile impostare una categoria IVA per descrivere informazioni sul tipo di IVA che viene applicata. Le informazioni possono essere obbligatorie per la normativa statale. Dopo aver impostato una categoria IVA e averla associata a un setup registrazioni IVA, la categoria IVA viene visualizzata su tutti i documenti di vendita stampati con tale categoria di setup registrazioni IVA.

Se necessario, è anche possibile specificare come tradurre automaticamente le categorie IVA in altre lingue. Successivamente, quando si crea e si stampa un documento di vendita contenente un codice IVA, il documento includerà la categoria IVA nel testo tradotto. Il codice lingua specificato nella scheda cliente determina la lingua.

Quando vengono utilizzate aliquote IVA non standard in diversi tipi di documenti, come fatture o note di credito, le società sono generalmente tenute a includere un testo di esenzione (categoria IVA) indicante il motivo per cui è stata calcolata un'IVA ridotta o un'aliquota IVA zero. È possibile definire diverse categorie IVA da includere nei documenti commerciali per tipo di documento, come fattura o nota di credito. È possibile eseguire questa operazione nella pagina **Categorie IVA per tipo di documento**.

È possibile modificare o eliminare una categoria IVA. Le modifiche si rifletteranno in un report generato. Tuttavia, [!INCLUDE[prod_short](includes/prod_short.md)] non conserva una cronologia della modifica. Nel report, le descrizioni della categoria IVA vengono stampate e visualizzate per tutte le righe del report accanto all'importo IVA e all'imponibile IVA. Se una categoria IVA non è stata definita per alcune righe del documento di vendita, allora viene omessa l'intera sezione quando il report viene stampato.

### <a name="to-set-up-vat-clauses"></a>Impostare categorie IVA

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie IVA**, quindi scegli il collegamento correlato.  
2. Nella pagina **Categorie IVA** creare una nuova riga.  
3. Nel campo **Codice** immettere un identificatore per la categoria. Il codice viene usato per assegnare la categoria ai categorie di registrazione IVA.  
4. Nel campo **Descrizione** immettere il testo per l'esenzione IVA che si desidera visualizzare nei documenti che possono includere l'IVA. Nel campo **Descrizione 2** immetti testo aggiuntivo, se necessario. Il testo verrà visualizzato sulle nuove righe dei documenti.
5. Scegliere l'azione **Descrizione per tipo di documento**.
6. Nella pagina **Categorie IVA per tipo di documento**, compilare i campi per impostare il testo per l'esenzione IVA da visualizzare tipi di documento specifici.  
7. Facoltativo: per assegnare direttamente la categoria IVA a un setup registrazioni IVA, scegliere **Setup** e quindi la categoria. Se si desidera attendere, è possibile assegnare la categoria in seguito nella pagina **Setup registrazioni IVA**.  
8. Facoltativo: per specificare come tradurre automaticamente la categoria IVA scegliere l'azione **Traduzioni**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Per assegnare una categoria IVA a un setup di registrazione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.  
2. Nella colonna **Categoria IVA** selezionare la categoria e utilizzarla per ogni setup registrazione IVA a cui si applica.  

### <a name="to-specify-translations-for-vat-clauses"></a>Per specificare le traduzioni per le categorie IVA

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie IVA**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Traduzioni**.  
3. Nel campo **Codice lingua** selezionare la lingua verso cui tradurre.  
4. Nei campi **Descrizione** e **Descrizione 2** immettere il testo tradotto delle descrizioni. Questo testo viene visualizzato nei documenti di report IVA tradotti.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Creare un setup registrazioni IVA per gestire l'IVA sulle importazioni

La funzionalità relativa all'*IIVA sulle importazioni* viene utilizzata quando è necessario registrare un documento in cui l'intero importo è IVA. Si userà questa funzionalità quando si riceve una fattura con IVA dalle autorità fiscali per merci importate.  

Per impostare i codici per l'IVA sull'importazione, attenersi a questa procedura:  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazioni articoli/servizi IVA**, quindi scegli il collegamento correlato.  
2. Nella pagina Categorie reg. art./serv. IVA impostare una nuova categoria di registrazione articoli/servizi IVA per l'IVA da importazione.  
3. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.  
4. Nella pagina Setup registrazioni IVA creare una nuova riga o utilizzare una delle categorie di registrazione business IVA esistenti in combinazione con la nuova categoria di registrazione articoli/servizi IVA per l'IVA da importazione.  
5. Nel campo **Tipologia IVA** selezionare **Sola IVA**.  
6. Nel campo **Conto IVA Acquisti** immettere il conto C/G da utilizzare per registrare l'IVA da importazione. Tutti gli altri conti sono facoltativi.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Usare l'IVA intracomunitaria per il commercio tra i paesi della UE

Per il commercio tre due società nell'Unione Europea, per alcune società è necessario utilizzare l'IVA intracomunitaria. Ad esempio, la regola si applica agli acquisti e alle vendite nei paesi UE.  

> [!NOTE]  
> Questa regola è valida per il commercio con società registrate come soggette a IVA in un altro paese UE. Se si hanno relazioni commerciali dirette con clienti in altri paesi UE, è necessario contattare le autorità fiscali per informazioni sulle regole IVA applicabili.  

> [!TIP]  
> È possibile verificare che la società sia registrata come soggetto IVA in un altro paese UE utilizzando il servizio di convalida partita IVA UE. Il servizio è disponibile gratuitamente in [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Verificare i numeri di partita IVA](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Vendite ai paesi UE

Sulle vendite a società soggette a IVA in altri paesi UE l'IVA non viene calcolata. È necessario indicare il valore di tali vendite ai paesi UE separatamente nella dichiarazione IVA.  

Per calcolare correttamente l'IVA sulle vendite nei paesi UE, è necessario effettuare le seguenti operazioni:  

* Impostare una riga per le vendite con le stesse informazioni degli acquisti. Se sono già state impostate righe nella pagina Setup registrazioni IVA per gli acquisti dai paesi UE, è possibile quindi utilizzare tali righe anche per le vendite.  
* Assegnare categorie di registrazione business IVA nel campo **Cat. reg. business IVA** nella Scheda dettaglio **Fatturazione** della scheda cliente di ciascun cliente dell'UE. È inoltre necessario immettere la partita IVA del cliente nel campo **Partita IVA** della Scheda dettaglio **Commercio estero**.  

Quando si registra una vendita a un cliente in un altro paese UE, viene calcolato l'importo IVA e viene creato un movimento IVA con le informazioni sull'IVA intracomunitaria e sull'imponibile IVA, ovvero l'importo utilizzato per calcolare l'importo IVA. Non vengono registrati movimenti nei conti IVA nella contabilità generale.

## <a name="vat-rounding-for-documents"></a>Arrotondamento IVA per i documenti

Gli importi nei documenti che non sono ancora stati registrati vengono arrotondati e visualizzati in modo da corrispondere all'arrotondamento finale degli importi effettivamente registrati. L'IVA viene calcolata per un documento completo, cioè l'IVA che viene calcolata è basata sulla somma di tutte le righe con lo stesso identificatore IVA nel documento.

## <a name="see-also"></a>Vedere anche

[Impostazione di definizioni di dichiarazione IVA e di nomi delle dichiarazioni IVA](finance-how-setup-vat-statement.md)  
[Setup dell'IVA ad esigibilità differita](finance-setup-unrealized-vat.md)  
[Dichiarare l'IVA a un'autorità fiscale](finance-how-report-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Utilizzare lo strumento di modifica dell'aliquota IVA](finance-how-use-vat-rate-change-tool.md)  
[Verificare i numeri di partita IVA](finance-how-validate-vat-registration-number.md)  
[Funzionalità locale in Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]

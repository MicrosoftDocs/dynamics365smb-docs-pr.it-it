---
title: Impostare prezzi e sconti
description: Descrive come definire accordi su prezzi e sconti standard e speciali per vendite e acquisti.
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'price, pricing, discount, discounting, rebate, sale, purchase, invoice'
ms.search.form: '459, 460, 7001, 7011, 7015, 7016, 7017, 7018'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-prices-and-discounts"></a><a name="set-up-prices-and-discounts"></a><a name="set-up-prices-and-discounts"></a>Impostare prezzi e sconti

> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 abbiamo rilasciato processi semplificati per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti che utilizzano questa versione, trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** nella pagina **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Le strategie di prezzo e sconto per l'acquisto e la vendita di articoli e servizi sono strumenti fondamentali per le imprese di successo. Dopo aver impostato gli articoli e i servizi acquistati e venduti dalla società, è possibile definire quali pagare o addebitare e tali importi verranno automaticamente aggiunti ai documenti di vendita e acquisto. 

## <a name="setting-up-prices-and-discounts"></a><a name="setting-up-prices-and-discounts"></a><a name="setting-up-prices-and-discounts"></a>Impostazione di prezzi e sconti

Prima di creare listini prezzi, è necessario definire le strategie di prezzo e sconto sul file **Setup contabilità clienti** e **Setup contabilità fornitori e acquisti**.

È possibile impostare e utilizzare due tipi di sconto:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto riga** |Un importo di sconto fornito per le righe nei documenti di vendita e acquisto. In genere, gli sconti riga si basano su una combinazione di cliente, articolo, quantità minima, unità di misura o periodo di tempo definita per le vendite e gli acquisti nelle pagine **Setup contabilità clienti** e **Setup contabilità fornitori e acquisti**.|
| **Sconto fattura** |Una percentuale di sconto che viene sottratta dal totale nei documenti di vendita e di acquisto se la somma di tutte le righe di un documento supera un determinato valore minimo. |

Poiché i prezzi di vendita e gli sconti riga di vendita si basano su una combinazione di articolo e cliente, è altresì possibile eseguire questa configurazione dalla pagina dell'articolo, dove si applicano regole e valori.

> [!TIP]  
> Se un articolo non dovrà mai essere venduto a un prezzo scontato, lasciare vuoti i campi relativi allo sconto nella pagina dell'articolo e non includere l'articolo in alcuna impostazione di sconto riga.

## <a name="about-price-lists"></a><a name="about-price-lists"></a><a name="about-price-lists"></a>Informazioni sui listini prezzi

I listini prezzi sono flessibili e consentono di specificare il business partner o l'attività a cui si applicano. Ad esempio, è possibile configurare un listino prezzi applicabile a tutti i fornitori e clienti oppure offrire prezzi o sconti speciali per ogni business partner, ad esempio in base a una quantità minima sugli ordini di acquisto o di vendita o in base a una combinazione specifica di cliente, articolo, quantità minima, unità di misura o periodo di tempo. I prezzi e gli sconti definiti vengono applicati automaticamente ai documenti di acquisto e di vendita. 

## <a name="set-up-prices"></a><a name="set-up-prices"></a><a name="set-up-prices"></a>Impostare i prezzi

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### [Esperienza corrente](#tab/current-experience)  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Prezzi**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà un prezzo di vendita speciale al cliente.

#### [Nuova esperienza](#tab/new-experience)  

È possibile aggiungere articoli e servizi manualmente per ogni riga oppure utilizzare l'azione **Suggerisci righe** per creare nuovi prezzi per articoli, gruppi sconto articolo, risorse e altri tipi di prodotto selezionati. Se scegli **Suggerisci righe** nella pagina **Righe prezzo - Crea nuovo** è possibile utilizzare i filtri per selezionare gli articoli o i servizi da includere nel listino prezzi. È inoltre possibile specificare se considerare una quantità minima durante il calcolo dei prezzi, il fattore di rettifica da applicare per le nuove righe del listino prezzi e il metodo di arrotondamento da applicare per i prezzi. 

Per default, lo stato dei nuovi listini prezzi è **Bozza**. Quando si è pronti per iniziare a utilizzare il listino, modificare lo stato in **Attivo**.

Per rivedere i listini prezzi e i prezzi che si applicano a clienti o fornitori specifici, nella pagina **Cliente** o **Venditore** scegliere l'azione **Listini prezzi di vendita** o **Listini prezzi di acquisto**. Per articoli e risorse, è possibile visualizzare le righe del listino prezzi scegliendo **Prezzi di vendita** o **Prezzi di acquisto** nelle pagine **Articolo** e **Risorsa**.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Listini prezzi di vendita**. 
3. Scegliere **Nuovo** per creare un nuovo listino prezzi di vendita.
4. Nelle Schede dettaglio **Generale** e **Imposta** compilare i campi appropriati. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Per aggiungere articoli all'elenco, effettuare una delle seguenti operazioni:
   * Per aggiungere molti articoli, scegliere **Suggerisci righe** e quindi immettere i criteri di filtro per specificare i tipi di articolo da aggiungere. Facoltativamente, è anche possibile immettere alcune impostazioni aggiuntive per gli articoli specifici del listino prezzi. Se necessario, è possibile apportare le modifiche in un secondo momento.
   * Per copiare articoli da un altro listino prezzi, scegliere **Copia righe**, quindi scegliere il listino prezzi da copiare.
   * Per aggiungere articoli manualmente, nel campo **Tipo prodotto** selezionare il tipo di prodotto a cui si riferisce il listino prezzi. In base alla selezione, compilare i restanti campi in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Per iniziare a utilizzare il listino prezzi, nel campo **Stato** scegliere **Attivo**.  

---

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a><a name="to-set-up-a-sales-line-discount-for-a-customer"></a><a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Per impostare uno sconto riga vendita per un cliente

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### [Esperienza corrente](#tab/current-experience/)  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Apri la scheda cliente interessata e scegli l'azione **Sconti riga**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà uno sconto riga vendita al cliente.

> [!Note]
> Quando si aprono le pagine **Prezzi vendita** e **Sconti riga vendita** di un cliente specifico, i campi **Filtro tipo vendita** e **Filtro codice vendita** sono impostati per il cliente e non possono essere modificati né rimossi.
>
> Per impostare i prezzi o gli sconti riga per tutti i clienti, un gruppo di prezzi dei clienti o una campagna, è necessario aprire le pagine da una scheda articolo. In alternativa, per i prezzi di vendita, utilizzare la pagina **Prospetto Prezzi Vendita**. Per ulteriori informazioni, vedere [Per aggiornare in blocco i prezzi degli articoli](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Nuova esperienza](#tab/new-experience/)  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Listini prezzi di vendita**.
3. Aprire il listino prezzi per il quale specificare lo sconto riga.
4. Attivare **Consenti sconto riga**.
5. Creare una nuova riga o scegliere una riga esistente, quindi compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Nel campo **Definisce** scegliere **Prezzo e sconto** o solo **Sconto**. 
7. Nel campo **% sconto riga** specificare la percentuale di sconto.

   > [!TIP]
   > Se si modifica una riga esistente, è possibile filtrare le righe scegliendo l'opzione appropriata nel campo **Visualizza colonne per**.

---

## <a name="work-with-invoice-discounts-and-service-charges"></a><a name="work-with-invoice-discounts-and-service-charges"></a><a name="work-with-invoice-discounts-and-service-charges"></a>Utilizzare Sconti fattura e Addebito assistenza

Quando si utilizzano gli sconti fattura, lo sconto applicato dipende dall'importo della fattura. Nella pagina **Sconti fattura** è inoltre possibile aggiungere un addebito di assistenza a fatture che superano un certo importo.  <!--The Invoice Discounts page is hard to find.-->

Prima di utilizzare gli sconti fattura con le vendite è necessario immettere una serie di informazioni. È necessario decidere a quali clienti verrà concesso questo tipo di sconto e quali percentuali di sconto verranno applicate.  

Se lo si desidera, è possibile impostare il calcolo automatico degli sconti fattura nella pagina **Setup contabilità clienti e vendite**.  

Per ciascun cliente è possibile specificare se verranno concessi sconti fattura a condizione che determinati requisiti vengano soddisfatti, cioè quando l'importo della fattura raggiunge una certa somma. Si possono definire le condizioni per gli sconti fattura in valuta locale per i clienti nazionali e in valuta estera per i clienti esteri.  

Collegare le percentuali di sconto a importi fattura specifici nella pagina **Sconti fattura**. È possibile immettere il numero di percentuali necessario. A ogni cliente è possibile associare una propria pagina oppure è possibile collegare più clienti alla stessa pagina.  

Oltre a (oppure invece di) una percentuale di sconto, è possibile collegare l'importo di un addebito di assistenza a un importo della fattura specifico.  

> [!TIP]  
> Prima di iniziare a immettere queste informazioni, è consigliabile preparare in anticipo la struttura di sconto, in modo che sia più facile visualizzare i clienti che possono essere collegati alla stessa pagina di sconto fattura. Per ulteriori informazioni sugli sconti per le vendite, vedi [Impostare gli sconti per i clienti](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="to-set-up-an-invoice-discount-for-a-customer"></a><a name="to-set-up-an-invoice-discount-for-a-customer"></a><a name="to-set-up-an-invoice-discount-for-a-customer"></a>Per impostare uno sconto fattura per un cliente

Dopo avere stabilito a quali clienti si devono applicare gli sconti fattura, è necessario immettere i codici di sconto fattura nelle schede clienti e impostare le condizioni relative ai singoli codici.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Apri la pagina relativa al cliente al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il cliente. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> I codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni.

Continuare a impostare le nuove condizioni dello sconto fattura di vendita.

1. Nella pagina **Clienti** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura clienti**.
2. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
3. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
4. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
5. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

Lo sconto fattura è ora impostato e assegnato al cliente in questione. Quando si seleziona il codice cliente nel campo **Cod. sconto fatt.** nelle altre schede cliente, lo stesso sconto fattura viene assegnato a quei clienti.

## <a name="to-copy-sales-prices"></a><a name="to-copy-sales-prices"></a><a name="to-copy-sales-prices"></a>Per copiare prezzi di vendita

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### [Esperienza corrente](#tab/current-experience/)  

Se si desidera copiare prezzi di vendita, ad esempio i prezzi di vendita di un singolo cliente per poterli utilizzare per un gruppo prezzi cliente, eseguire il processo batch **Suggerisci prezzo vendita in prosp.** nella pagina **Prospetto Prezzi Vendita**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto prezzi vendita**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo vendita in prosp.** .  
3. Nella Scheda dettaglio **Prezzi vendita** immettere i prezzi di vendita originali che si desidera copiare nei campi **Tipo vendita** e **Codice vendita**.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.  
5. Per creare nuovi prezzi mediante il processo batch, selezionare la casella di controllo **Crea nuovi prezzi**.  
6. Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per il tipo vendita selezionato.  

   > [!NOTE]  
   > Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella pagina **Prezzo vendita**, scegliere l'azione **Implementare variazione prezzi** nella pagina **Prospetto prezzi vendita**.

#### [Nuova esperienza](#tab/new-experience/)  

Lo stato del listino prezzi deve essere **Bozza**. 

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Listini prezzi di vendita**, quindi seleziona il collegamento correlato. 
2. Scegliere il listino prezzi da copiare e quindi scegliere **Copia righe**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  
  
---

## <a name="to-bulk-update-item-prices"></a><a name="to-bulk-update-item-prices"></a><a name="to-bulk-update-item-prices"></a>Per aggiornare in blocco i prezzi degli articoli

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### [Esperienza corrente](#tab/current-experience/)

Eseguire il processo batch **Suggerisci prezzo articolo in prosp.** per aggiornare in blocco i prezzi degli articoli, come aumentare tutti i prezzi di una determinata percentuale. Il collegamento al processo batch è disponibile nella pagina **Prospetto Prezzi Vendita**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto prezzi vendita**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo articolo in prosp.** .  
3. Nella Scheda dettaglio **Articolo**, riempire il campo **Nr.** o **Categoria registrazione magazzino** o altri campi con i prezzi degli articoli originali che si desidera aggiornare.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.
5. Se si desidera che il processo batch rettifichi automaticamente i prezzi degli articoli suggeriti, immettere la rettifica nel campo **Fattore Rettifica**. Ad esempio, immettere 1.15 in **Fattore Rettifica** per aumentare del 15% il prezzo dell'articolo.  
6. Per creare nuovi prezzi mediante il processo batch, selezionare il campo **Crea nuovi prezzi**.  
7. Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per l'**articolo** selezionato.  

> [!NOTE]
> Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella tabella **Prezzo vendita**, utilizzare il processo batch **Implementare variazione prezzi**, che è possibile richiamare facendo clic sulla scheda **Azioni**, del gruppo **Funzioni** nella pagina **Prospetto prezzi vendita**.

#### [Nuova esperienza](#tab/new-experience/)

Per aggiornare i prezzi per più articoli, è necessario creare un nuovo listino prezzi e quindi copiare le righe da un listino prezzi esistente. Quando si copiano le righe, è anche possibile utilizzare i filtri per specificare cosa copiare, nonché specificare un numero intero o decimale nel campo **Fattore rettifica** per aumentare o ridurre i prezzi. Il listino prezzi deve essere nello stato **Bozza**. Se necessario, è possibile quindi disattivare il vecchio listino prezzi.

> [!NOTE]
> Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  

---

## <a name="calculating-the-best-price"></a><a name="calculating-the-best-price"></a><a name="calculating-the-best-price"></a>Calcolo del prezzo migliore

Dopo aver registrato prezzi speciali e sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino. Per ulteriori informazioni, vedi [Calcolo del prezzo migliore](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/customer-discounts-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

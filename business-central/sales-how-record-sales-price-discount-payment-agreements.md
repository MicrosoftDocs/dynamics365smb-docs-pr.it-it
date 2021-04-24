---
title: Impostare prezzi di vendita e sconti speciali per i clienti | Microsoft Docs
description: Descrive le modalità di definizione di prezzi e accordi di sconto alternativi che si desidera collegare a documenti di vendita per clienti diversi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6c5b7f3d4ac36bb2d4a3213217a521e5286f74bb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778674"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrare i prezzi di vendita e gli sconti speciali
> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 abbiamo rilasciato processi semplificati per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti che utilizzano questa versione, trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

È necessario definire gli accordi di prezzo e di sconto applicati alle transazioni di vendita ai clienti affinché vengano applicati le regole e i valori concordati ai documenti di vendita.

Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[prod_short](includes/prod_short.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino. Per ulteriori informazioni, vedere [Calcolo del prezzo migliore](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Per quanto riguarda i prezzi, è possibile fare in modo che venga inserito un prezzo di vendita speciale nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine. Per ulteriori informazioni, vedere le sezioni [Per impostare un prezzo di vendita per un cliente](#to-set-up-a-sales-price-for-a-customer) e [Calcolo del prezzo migliore](#best-price-calculation).  

Nel caso degli sconti, è possibile impostare e utilizzare due tipi di sconti su vendita:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto Riga Vendita** |È possibile fare in modo che venga inserito uno sconto sull'importo nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine. Il principio è lo stesso dei prezzi di vendita. |
| **Sconto fattura** |Una percentuale di sconto che viene sottratta dal totale nei documenti di vendita se la somma di tutte le righe di un documento supera un determinato valore minimo. |

Poiché i prezzi di vendita e gli sconti riga di vendita si basano su una combinazione di articolo e cliente, è altresì possibile eseguire questa configurazione dalla pagina dell'articolo, dove si applicano regole e valori.

> [!TIP]  
> Se un articolo non dovrà mai essere venduto a un prezzo scontato, lasciare vuoti i campi relativi allo sconto nella pagina dell'articolo e non includere l'articolo in alcuna impostazione di sconto riga.

I campi **Collega a - Tipo** e **Collega a - Nr.** consentono di scegliere a cosa collegare il listino prezzi, ad esempio al cliente o al gruppo prezzi cliente. Utilizzando **Visualizza colonne per**, puoi mostrare o nascondere le colonne rilevanti per impostare prezzi e sconti oppure prezzi o sconti.

È possibile impostare righe del listino prezzi manualmente oppure utilizzare ad esempio l'azione **Suggerisci righe** per creare nuovi prezzi per articoli, gruppi sconto articolo, risorse e altri tipi di prodotto selezionati. Se si sceglie Suggerisci righe, la pagina Righe prezzo - Crea nuovo consente di impostare filtri per selezionare i prodotti per i quali si desidera creare nuove righe di listino prezzi. È inoltre possibile specificare se considerare una quantità minima durante il calcolo dei prezzi, il fattore di rettifica da applicare per le nuove righe del listino prezzi e il metodo di arrotondamento da applicare per i prezzi. L'azione **Copia righe** consente di copiare le righe del listino prezzi esistenti tra i listini prezzi.

Per default, lo stato dei nuovi listini prezzi è Bozza. Quando hai finito di aggiungere righe e desideri che vengano aggiunte dal motore di calcolo del prezzo, puoi modificare lo stato in Attivo.

Per rivedere i listini prezzi e i prezzi che si applicano a clienti o fornitori specifici, nella pagina **Cliente** scegliere **Listini prezzi di vendita** o nella pagina **Fornitore** scegliere **Listini prezzi di acquisto**. È possibile visualizzare le righe del listino prezzi in vari listini prezzo scegliendo **Prezzi di vendita** o **Prezzi di acquisto** nelle pagine **Articolo** e **Risorsa**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Per impostare un prezzo di vendita per un cliente

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**.  

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Scegliere il cliente, quindi l'azione **Prezzi**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà un prezzo di vendita speciale al cliente.

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Scegliere il cliente, quindi l'azione **Listini prezzi di vendita**. 
3. Scegliere **Nuovo** per creare un nuovo listino prezzi di vendita.
4. Nelle Schede dettaglio **Generale** e **Imposta** compilare i campi appropriati. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Per aggiungere articoli all'elenco, effettuare una delle seguenti operazioni:
   * Per aggiungere molti articoli, scegliere **Suggerisci righe** e quindi immettere i criteri di filtro per specificare i tipi di articolo da aggiungere. Facoltativamente, è anche possibile immettere alcune impostazioni aggiuntive per gli articoli specifici del listino prezzi. Se necessario, è possibile apportare le modifiche in un secondo momento.
   * Per copiare articoli da un altro listino prezzi, scegliere **Copia righe**, quindi scegliere il listino prezzi da copiare.
   * Per aggiungere articoli manualmente, nella griglia, nel campo **Tipo prodotto** selezionare il tipo di prodotto a cui si riferisce il listino prezzi. In base alla selezione, compilare i restanti campi in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Per iniziare a utilizzare il listino prezzi, nel campo **Stato** scegliere **Attivo**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Sconti fattura di vendita e Addebito assistenza
Quando si utilizzano gli sconti fattura, l'importo totale in fattura determina lo sconto applicato. Nella pagina **Sconti fattura clienti** è inoltre possibile aggiungere un addebito di assistenza a fatture che superano un certo importo.  

Prima di utilizzare gli sconti fattura con le vendite si devono specificare varie informazioni. È necessario decidere quanto segue:  

- A quali clienti verrà concesso questo tipo di sconto  
- Quali percentuali di sconto verranno applicate  

Se si desidera calcolare automaticamente gli sconti fattura, è possibile specificarlo nella pagina **Setup contabilità clienti**.  

Per ciascun cliente è possibile specificare se verranno concessi sconti fattura a condizione che determinati requisiti vengano soddisfatti, cioè quando l'importo della fattura raggiunge una certa somma. Si possono definire le condizioni per gli sconti fattura in valuta locale per i clienti nazionali e in valuta estera per i clienti esteri.  

Per collegare le percentuali di sconto a importi di fatturazione specifici, utilizzare la pagina **Sconti fattura clienti** di ogni cliente. È possibile immettere un numero qualsiasi di percentuali. A ogni cliente è possibile associare una propria pagina oppure è possibile collegare più clienti alla stessa pagina.  

Oltre a (oppure invece di) una percentuale di sconto, è possibile collegare l'importo di un addebito di assistenza a un importo della fattura specifico.  

> [!TIP]  
> Prima di immettere le informazioni, è opportuno preparare uno schema della struttura di sconto che si desidera utilizzare. Questo consente di visualizzare più facilmente i clienti che possono essere collegati alla stessa pagina di sconto fattura. Minore è il numero delle pagine da impostare, più veloce risulta l'inserimento delle informazioni principali.

Per informazioni sugli sconti per le vendite, vedere [Impostare gli sconti per i clienti](/learn/modules/customer-discounts-dynamics-365-business-central/index) in Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcolo degli sconti fattura per le vendite

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Per impostare uno sconto riga vendita per un cliente
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Sconti riga**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà uno sconto riga vendita al cliente.

> [!Note]
> Quando si aprono le pagine **Prezzi vendita** e **Sconti riga vendita** di un cliente specifico, i campi **Filtro tipo vendita** e **Filtro codice vendita** sono impostati per il cliente e non possono essere modificati né rimossi.
>
> Per impostare i prezzi o gli sconti riga per tutti i clienti, un gruppo di prezzi dei clienti o una campagna, è necessario aprire le pagine da una scheda articolo. In alternativa, per i prezzi di vendita, utilizzare la pagina **Prospetto Prezzi Vendita**. Per ulteriori informazioni, vedere [Per aggiornare in blocco i prezzi degli articoli](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Scegliere il cliente, quindi l'azione **Listini prezzi di vendita**.
3. Aprire il listino prezzi per il quale specificare lo sconto riga.
4. Attivare **Consenti sconto riga**.
5. Creare una nuova riga o scegliere una riga esistente, quindi compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Nel campo **Definisce** scegliere **Prezzo e sconto** o solo **Sconto**. 
7. Nel campo **% sconto riga** specificare la percentuale di sconto.

    > [!TIP]
    > Se si modifica una riga esistente, è possibile filtrare le righe scegliendo l'opzione appropriata nel campo **Visualizza colonne per**.

    > [!NOTE]  
    > I codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni. Per impostare le condizioni di sconto fattura specifiche del cliente, impostare il campo **Codice sconto fattura** sul codice cliente del cliente, quindi procedere al passaggio successivo.

8. Nella pagina **Scheda cliente** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura clienti**.
9. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
10. Facoltativamente, nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
11. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
12. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

Lo sconto fattura è ora impostato e assegnato al cliente. Quando si seleziona il codice cliente nel campo **Cod. sconto fatt.** nelle altre schede cliente, lo stesso sconto fattura viene assegnato a quei clienti.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Per impostare uno sconto su fattura per un cliente
Dopo avere stabilito a quali clienti si debbano applicare gli sconti fattura, è necessario immettere i codici di sconto fattura nelle schede clienti e impostare le condizioni relative ai singoli codici.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la pagina relativa al cliente al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il cliente. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> I codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni.

Continuare a impostare le nuove condizioni dello sconto fattura di vendita.

1. Nella pagina **Clienti** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura clienti**.
2. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
3. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
4. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
5. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

## <a name="to-copy-sales-prices"></a>Per copiare prezzi di vendita
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)  

Se si desidera copiare prezzi di vendita, ad esempio i prezzi di vendita di un singolo cliente per poterli utilizzare per un gruppo prezzi cliente, eseguire il processo batch **Suggerisci prezzo vendita in prosp.** nella pagina **Prospetto Prezzi Vendita**.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prezzi vendita** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo vendita in prosp.** .  
3. Nella Scheda dettaglio **Prezzi vendita** immettere i prezzi di vendita originali che si desidera copiare nei campi **Tipo vendita** e **Codice vendita**.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.  
5. Per creare nuovi prezzi mediante il processo batch, selezionare la casella di controllo **Crea nuovi prezzi**.  
6. Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per il tipo vendita selezionato.  

   > [!NOTE]  
   > Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella pagina **Prezzo vendita**, scegliere l'azione **Implementare variazione prezzi** nella pagina **Prospetto prezzi vendita**.

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)  

Lo stato del listino prezzi deve essere **Bozza**. 

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Listini prezzi di vendita** e quindi scegliere il collegamento correlato. 
2. Scegliere il listino prezzi da copiare e quindi scegliere **Copia righe**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  
  
---

## <a name="to-bulk-update-item-prices"></a>Per aggiornare in blocco i prezzi degli articoli
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. 

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)

Eseguire il processo batch **Suggerisci prezzo articolo in prosp.** per aggiornare in blocco i prezzi degli articoli, come aumentare tutti i prezzi di una determinata percentuale. Il collegamento al processo batch è disponibile nella pagina **Prospetto Prezzi Vendita**.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prezzi vendita** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo articolo in prosp.** .  
3. Nella Scheda dettaglio **Articolo**, riempire il campo **Nr.** o **Categoria registrazione magazzino** o altri campi con i prezzi degli articoli originali che si desidera aggiornare.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.
5. Se si desidera che il processo batch rettifichi automaticamente i prezzi degli articoli suggeriti, immettere la rettifica nel campo **Fattore Rettifica**. Ad esempio, immettere 1.15 in **Fattore Rettifica** per aumentare del 15% il prezzo dell'articolo.  
6. Per creare nuovi prezzi mediante il processo batch, selezionare il campo **Crea nuovi prezzi**.  
7. Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per l'**articolo** selezionato.  

> [!NOTE]
> Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella tabella **Prezzo vendita**, utilizzare il processo batch **Implementare variazione prezzi**, che è possibile richiamare facendo clic sulla scheda **Azioni**, del gruppo **Funzioni** nella pagina **Prospetto prezzi vendita**.

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)

Per aggiornare i prezzi per più articoli, è necessario creare un nuovo listino prezzi e quindi copiare le righe da un listino prezzi esistente. Quando si copiano le righe, è anche possibile utilizzare i filtri per specificare cosa copiare, nonché specificare un numero intero o decimale nel campo **Fattore rettifica** per aumentare o ridurre i prezzi. Il listino prezzi deve essere nello stato **Bozza**. Se necessario, è possibile quindi disattivare il vecchio listino prezzi.

> [!NOTE]
> Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  

---

## <a name="best-price-calculation"></a>Calcolo del prezzo migliore
Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino.

Con il termine "miglior prezzo" si intende il prezzo più basso ammissibile che gode dello sconto riga più alto possibile praticabile in una specifica data. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente questo prezzo quando inserisce il prezzo unitario e la percentuale di sconto riga per gli articoli in nuove righe di documenti e di registrazione.

> [!NOTE]  
> Di seguito viene descritto come viene calcolato il prezzo migliore per le vendite. Il calcolo è lo stesso per gli acquisti.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla la combinazione del cliente di fatturazione e dell'articolo e quindi calcola il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    - Il cliente usufruisce di uno speciale accordo relativo a prezzi o sconti o appartiene a un gruppo che ne usufruisce?
    - L'articolo o il gruppo sconto articolo specificato nella riga è incluso in uno di tali accordi prezzi o sconti?
    - La data dell'ordine, o la data di registrazione per le fatture e le note di credito, è compresa nell'intervallo di validità dell'accordo prezzi o sconti?
    - È stato specificato un codice unità di misura? In caso affermativo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno controllati i prezzi o gli sconti aventi lo stesso codice di unità di misura, altrimenti verranno verificati prezzi o gli sconti a cui non è associato alcun codice di unità di misura.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se si applicano accordi di prezzo/sconto alle informazioni sul documento o sulla riga di registrazione, quindi inserisce il prezzo unitario e la percentuale di sconto riga utilizzando i seguenti criteri:

    - C'è un requisito di quantità minima nell'accordo di prezzo/sconto che è soddisfatto?
    - C'è un requisito di valuta nell'accordo di prezzo/sconto che è soddisfatto? In caso affermativo, il prezzo più basso e lo sconto riga più alto per tale valuta vengono immessi, anche se la valuta locale fornirebbe un prezzo migliore. Se non esistono accordi prezzi o sconti riga per il codice di valuta specificato, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente selezionati il prezzo più basso e lo sconto riga più alto per la valuta locale.

Se non è possibile calcolare alcun prezzo speciale per l'articolo specificato nella riga, viene recuperato l'ultimo costo diretto o il prezzo unitario dalla scheda articolo immesso.

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
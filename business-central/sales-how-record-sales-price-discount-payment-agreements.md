---
title: Impostare prezzi di vendita e sconti speciali per i clienti | Microsoft Docs
description: "Descrive le modalità di definizione di prezzi e accordi di sconto alternativi che si desidera collegare a documenti di vendita per clienti diversi."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 11/28/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: b0af8e6d6dd477ebabbfc1fa05e8d57378eee226
ms.contentlocale: it-it
ms.lasthandoff: 11/29/2018

---
# <a name="record-special-sales-prices-and-discounts"></a>Registrare i prezzi di vendita e gli sconti speciali
È necessario definire i diversi criteri di prezzo e di sconto applicati alle transazioni di vendita ai diversi clienti affinché vengano applicati le regole e i valori concordati ai documenti di vendita creati per i clienti.

Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino. Per ulteriori informazioni, vedere la sezione "Calcolo del prezzo migliore".

Per quanto riguarda i prezzi, è possibile fare in modo che venga inserito un prezzo di vendita speciale nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine.

Nel caso degli sconti, è possibile impostare e utilizzare due tipi di sconti su vendita:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto Riga Vendita** |È possibile fare in modo che venga inserito uno sconto sull'importo nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine. Il principio è lo stesso dei prezzi di vendita. |
| **Sconto fattura** |Uno sconto in percentuale che viene sottratto dal totale del documento se l'importo del valore di tutte le righe di un documento di vendita supera un determinato valore minimo. |

Poiché i prezzi di vendita e gli sconti riga di vendita si basano su una combinazione di articolo e cliente, è altresì possibile eseguire questa configurazione dalla scheda articolo dello specifico articolo, dove si applicano regole e valori.

> [!NOTE]  
> Se non si desidera vendere mai un articolo a un prezzo scontato, lasciare semplicemente vuoti i campi relativi allo sconto nella scheda articolo vuota e non includere l'articolo in alcuna impostazione di sconto riga.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Per impostare un prezzo di vendita per un cliente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Prezzi**.

    Il campo **Tipo vendita** viene precompilato con **Cliente** e il campo **Codice vendita** viene precompilato con il numero del cliente.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà un prezzo di vendita speciale al cliente.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Per impostare uno sconto riga vendita per un cliente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Sconti riga**.

    Il campo **Tipo vendita** viene precompilato con **Cliente** e il campo **Codice vendita** viene precompilato con il numero del cliente.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà uno sconto riga vendita al cliente.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Per impostare uno sconto su fattura per un cliente
Dopo avere stabilito a quali clienti si debbano applicare gli sconti fattura, è necessario immettere i codici di sconto fattura nelle schede clienti e impostare le condizioni relative ai singoli codici.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente relativa al cliente al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il cliente.

> [!NOTE]  
>   I codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni.

Continuare a impostare le nuove condizioni dello sconto fattura di vendita.

1. Nella pagina **Scheda cliente** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura clienti**.
2. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
3. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
4. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
5. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

Lo sconto fattura è ora impostato e assegnato al cliente in questione. Quando si seleziona il codice cliente nel campo **Cod. sconto fatt.** nelle altre schede cliente, lo stesso sconto fattura viene assegnato a quei clienti.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Per utilizzare gli sconti su fatture di vendita e addebiti di assistenza
Quando si utilizzano gli sconti fattura, lo sconto applicato dipende dall'importo della fattura.  

Nella pagina **Sconti fattura clienti** è inoltre possibile aggiungere un addebito di assistenza a fatture che superano un certo importo.  

Prima di utilizzare gli sconti fattura con le vendite è necessario immettere una serie di informazioni. È necessario decidere:  

- a quali clienti verrà concesso questo tipo di sconto.  
- quali percentuali di sconto verranno applicate.  

Se lo si desidera, è possibile impostare il calcolo automatico degli sconti fattura nella pagina **Setup contabilità clienti e vendite**.  

Per ciascun cliente è possibile specificare se verranno concessi sconti fattura a condizione che determinati requisiti vengano soddisfatti, cioè quando l'importo della fattura raggiunge una certa somma. Si possono definire le condizioni per gli sconti fattura in valuta locale per i clienti nazionali e in valuta estera per i clienti esteri.  

Per collegare le percentuali di sconto a importi di fatturazione specifici, utilizzare le pagine **Sconti fattura clienti**. È possibile immettere un numero qualsiasi di percentuali in ogni pagina. A ogni cliente è possibile associare una propria pagina oppure è possibile collegare più clienti alla stessa pagina.  

Oltre a (oppure invece di) una percentuale di sconto, è possibile collegare l'importo di un addebito di assistenza a un importo della fattura specifico.  

> [!TIP]  
>  Prima di immettere le informazioni, è opportuno preparare uno schema della struttura di sconto che si desidera utilizzare. Questo consente di visualizzare più facilmente i clienti che possono essere collegati alla stessa pagina di sconto fattura. Minore è il numero delle pagine da impostare, più veloce risulta l'inserimento delle informazioni principali.  

## <a name="best-price-calculation"></a>Calcolo del prezzo migliore
Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino.

Con il termine "miglior prezzo" si intende il prezzo più basso ammissibile che gode dello sconto riga più alto possibile praticabile in una specifica data. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente questo prezzo quando inserisce il prezzo unitario e la percentuale di sconto riga per gli articoli in nuove righe di documenti e di registrazione.

> [!NOTE]  
>   Di seguito viene descritto come viene calcolato il prezzo migliore per le vendite. Il calcolo è lo stesso per gli acquisti.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla la combinazione del cliente di fatturazione e dell'articolo e quindi calcola il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    - Il cliente usufruisce di uno speciale accordo relativo a prezzi o sconti o appartiene a un gruppo che ne usufruisce?
    - L'articolo o il gruppo sconto articolo specificato nella riga è incluso in uno di tali accordi prezzi o sconti?
    - La data dell'ordine, o la data di registrazione per le fatture e le note di credito, è compresa nell'intervallo di validità dell'accordo prezzi o sconti?
    - È stato specificato un codice unità di misura? In caso affermativo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno controllati i prezzi o gli sconti aventi lo stesso codice di unità di misura, altrimenti verranno verificati prezzi o gli sconti a cui non è associato alcun codice di unità di misura.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se si applicano accordi di prezzo/sconto alle informazioni sul documento o sulla riga di registrazione, quindi inserisce il prezzo unitario e percentuale di sconto della riga, utilizzando i seguenti criteri:

    - C'è un requisito di quantità minima nell'accordo di prezzo/sconto che è soddisfatto?
    - C'è un requisito di valuta nell'accordo di prezzo/sconto che è soddisfatto? In caso affermativo, il prezzo più basso e lo sconto riga più alto per tale valuta vengono immessi, anche se la valuta locale fornirebbe un prezzo migliore. Se non esistono accordi prezzi o sconti riga per il codice di valuta specificato, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente selezionati il prezzo più basso e lo sconto riga più alto per la valuta locale.

Se non è possibile calcolare alcun prezzo speciale per l'articolo specificato nella riga, viene recuperato l'ultimo costo diretto o il prezzo unitario dalla scheda articolo immesso.

## <a name="to-copy-sales-prices"></a>Per copiare prezzi di vendita  
Eseguire il processo batch **Suggerisci prezzo vendita in prosp.** se si desidera copiare prezzi di vendita, ad esempio i prezzi di vendita di un singolo cliente per poterli utilizzare in un gruppo di prezzi cliente. L'azione per il processo batch è disponibile nella pagina **Prospetto Prezzi Vendita**.    

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prezzi vendita** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Suggerisci prezzo vendita in prosp.** .  
3.  Nella Scheda dettaglio **Prezzi vendita** immettere i prezzi di vendita originali che si desidera copiare nei campi **Tipo vendita** e **Codice vendita**.  
4.  Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.  
5.  Per creare nuovi prezzi mediante il processo batch, selezionare la casella di controllo **Crea nuovi prezzi**.  
6.  Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per il tipo vendita selezionato.  

> [!NOTE]  
>  Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella pagina **Prezzo vendita**, scegliere l'azione **Implementare variazione prezzi** nella pagina **Prospetto prezzi vendita**.

## <a name="to-bulk-update-item-prices"></a>Per aggiornare in blocco i prezzi degli articoli   
Eseguire il processo batch **Suggerisci prezzo articolo in prosp.** per aggiornare in blocco i prezzi degli articoli, come aumentare tutti i prezzi di una determinata percentuale. Il collegamento al processo batch è disponibile nella pagina **Prospetto Prezzi Vendita**.     

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prezzi vendita** e quindi scegliere il collegamento correlato.   
2.  Scegliere l'azione **Suggerisci prezzo articolo in prosp.** .   
3.  Nella Scheda dettaglio **Articolo**, riempire il campo **Nr.** o **Categoria registrazione magazzino** o altri campi con i prezzi degli articoli originali che si desidera aggiornare.   
4.  Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.
5.  Se si desidera che il processo batch rettifichi automaticamente i prezzi degli articoli suggeriti, immettere la rettifica nel campo **Fattore Rettifica**. Ad esempio, immettere 1.15 in **Fattore Rettifica** per aumentare del 15% il prezzo dell'articolo.  
6.  Per creare nuovi prezzi mediante il processo batch, selezionare il campo **Crea nuovi prezzi**.   
7.  Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per l'**articolo** selezionato.   

> [!NOTE]   
>  Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella tabella **Prezzo vendita**, utilizzare il processo batch **Implementare variazione prezzi**, che è possibile richiamare facendo clic sulla scheda **Azioni**, del gruppo **Funzioni** nella pagina **Prospetto prezzi vendita**.

## <a name="see-also"></a>Vedi anche
[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


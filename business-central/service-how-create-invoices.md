---
title: Creare fatture o note di credito per servizi | Microsoft Docs
description: Informazioni su come creare fatture per poter essere pagati per il servizio di assistenza fornito.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 61890301542ea7225039341eb30fbf4e3dd035d0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778274"
---
# <a name="create-service-invoices-or-credit-memos"></a>Creare fatture o note di credito di assistenza
La facilità di fatturazione degli ordini di assistenza è una caratteristica chiave di [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo che un tecnico dell'assistenza possa creare una fattura di assistenza non collegata ad alcun contratto o ordine esistente. In alternativa, impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo da fatturare periodicamente i contratti di assistenza. Il periodo di fatturazione di ogni contratto definisce con quale frequenza avviene la fatturazione.

## <a name="to-invoice-several-service-contracts"></a>Per fatturare più contratti di assistenza

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Crea fatture contratto assistenza** e quindi scegliere il collegamento correlato.  
2. Impostare i filtri che si desidera applicare.  
3. Nel campo **Data di registrazione** inserire la data che si intende utilizzare come data di registrazione nelle fatture di assistenza.  
4. Nel campo **Fattura Alla Data** immettere la data fino a cui si intendono fatturare contratti. Il processo batch includerà i contratti con le date di fatturazione successive fino a tale data.  
5. Nel campo **Azione** scegliere **Crea fatture**.  
6. Scegliere **OK** per creare le fatture di assistenza.  
  
È anche possibile fatturare un contratto di assistenza direttamente dalla pagina **Contratto di Assistenza** se la data della prossima fatturazione nel contratto risulta precedente alla data di lavoro.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Per fatturare un contratto di assistenza dalla pagina Contratto assistenza   
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contratti assistenza** e quindi scegliere il collegamento correlato.  
2. Scegliere il contratto di assistenza da fatturare e aprire la scheda contratto.  
3. Scegliere l'azione **Crea fattura assistenza**. 
4. Scegliere **Sì** per creare le fatture di assistenza.  
  
  > [!NOTE]  
  > Non è possibile creare fatture di assistenza per il contratto di assistenza quando il valore del campo **Modifica stato** è impostato su **Aperto**.  

## <a name="to-post-an-invoice-from-a-service-order"></a>Per registrare una fattura da un ordine di assistenza  
La procedura seguente indica le modalità di definizione della parte dei servizi di assistenza da addebitare al cliente.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini assistenza** e quindi scegliere il collegamento correlato.  
2. Scegliere l'ordine di assistenza da fatturare e aprire la scheda ordine.  
3. Scegliere l'azione **Righe assistenza**.  
4. Individuare i movimenti necessari, quindi specificare le quantità da addebitare al cliente nel campo **Qtà da fatturare**.  
  
   > [!NOTE]  
   > È possibile emettere una fattura relativa all'assistenza registrata totale o parziale. Se la fattura è totale, il valore del campo **Qtà da fatturare** deve corrispondere a quello del campo **Quantità**. È possibile registrare una fattura totale con una spedizione completa ed è possibile registrare una fattura totale per una spedizione completa già registrata non fatturata né consumata in precedenza.  
   >  
   > Quando si registra una fattura parziale, è possibile specificare la quantità da fatturare in due modi diversi. Se l'assistenza viene registrata mediante l'opzione **Spedisci e fattura**, il valore del campo **Qtà da fatturare** deve corrispondere a quello del campo **Qtà da spedire**. Se si desidera fatturare una spedizione già registrata, la quantità da fatturare non deve superare il valore specificato nel campo **Quantità spedita**.  
  
5. Scegliere **Registra**, quindi **Fattura** o **Spedisci e fattura**. Per ulteriori informazioni su queste opzioni, vedere [Registrazione in Gestione assistenza](service-service-posting.md).  
  
 La riga di assistenza selezionata viene registrata. Per registrare diverse righe di assistenza contemporaneamente selezionarle tutte e scegliere **Registra**. Se si esegue questa operazione, verificare di avere immesso tutte le informazioni necessarie nelle righe da registrare.  
  
 Se si registra l'ordine mediante l'opzione **Fattura**, verrà creata una fattura di assistenza registrata con i movimenti contabili corrispondenti e verranno aggiornati i campi relativi nelle righe di assistenza dell'ordine. Verranno inoltre aggiornati i documenti di spedizione registrati in precedenza con le quantità fatturate. Se si seleziona l'opzione di registrazione **Spedisci e fattura**, verrà creata una spedizione registrata.

## <a name="to-create-a-service-invoice-manually"></a>Per creare una fattura di assistenza manualmente  
In genere, dopo la registrazione di un ordine di assistenza mediante l'opzione **Fattura** o **Spedisci e fattura**, verrà registrata automaticamente una fattura di assistenza. Può essere tuttavia necessario emettere una fattura che non sia collegata a un contratto di assistenza oppure a un ordine di assistenza. Di seguito vengono descritte le modalità di emissione di una fattura nel momento in cui il cliente riceve l'assistenza.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture assistenza** e quindi scegliere il collegamento correlato.  
2. Creare una nuova fattura di assistenza.  
3. Compilare debitamente i campi **Nr.**    
  
    > [!NOTE]  
    >  Se è stata impostata una numerazione per le fatture di assistenza nella pagina **Setup gest. assist.**, per selezionare il numero successivo di fattura di assistenza disponibile, premere INVIO.  
  
4. Nel campo **Nr. cliente** immettere il numero di un cliente. Selezionare il cliente appropriato dalla lista.  
  
    I campi del cliente vengono compilati con le informazioni della scheda **Cliente**.  
  
5. Immettere una data nel campo **Data di registrazione**. Tale data verrà visualizzata sui movimenti registrati. Il campo viene compilato con la data di lavoro corrente, ma è possibile modificarla manualmente.  
6. Immettere una data nel campo **Data documento**. Tale data verrà visualizzata nella fattura stampata e verrà utilizzata per calcolare la data di scadenza.  
7. Compilare le righe di assistenza della fattura. Compilare i campi **Tipo**, **Nr.** e **Quantità** per registrare articoli, risorse e costi utilizzati durante le operazioni di assistenza. 

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders"></a>Per creare una fattura che combina le righe di spedizione registrate da uno o più ordini di assistenza 
Può essere necessario creare una fattura relativa a un'assistenza che è già stata spedita da uno o più ordini, ma non ancora fatturata o consumata. È possibile compilare automaticamente le righe della fattura con le righe di spedizione registrate e selezionate relative a un cliente specifico.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Fatture assistenza** e quindi scegliere il collegamento correlato.  
2. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Creare righe di fattura per servizi di assistenza spediti, ma non fatturati. In alternativa, è possibile utilizzare l'azione **Prendi righe di spedizione** per aggiungere righe di spedizione registrate alla fattura.  
4. Registrare la fattura di assistenza.  
  
 Verranno creati la fattura di assistenza registrata e i movimenti contabili corrispondenti. Verranno aggiornati i documenti di spedizione registrati in precedenza, nonché le quantità fatturate e quelle relative alle righe di assistenza degli ordini di origine.  

## <a name="to-create-a-service-credit-memo"></a>Per creare una nota di credito di assistenza  
Una nota di credito di assistenza viene in genere utilizzata quando un cliente restituisce un articolo, ma può essere creata anche per risarcire un cliente o per correggere una fattura non corretta.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note credito assistenza** e quindi scegliere il collegamento correlato.  
2. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nei campi **Data di registrazione** e **Data documento** viene visualizzata la data di lavoro. Se necessario, è possibile modificarla.    
4. Nelle righe della nota di credito immettere le informazioni relative agli articoli resi o rimossi oppure al risarcimento concesso al cliente.  

## <a name="see-also"></a>Vedi anche
[Registrare le fatture di assistenza](service-how-to-post-service-orders.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  
[Registrazione di assistenza](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
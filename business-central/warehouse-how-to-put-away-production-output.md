---
title: "Procedura: Stoccare l'output di produzione | Documenti Microsoft"
description: La modalità di stoccaggio dell'output di produzione dipende dalla modalità di impostazione della warehouse come ubicazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5d2a8e53d26ea6a6f0ab591b9695acb39024348b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881680"
---
# <a name="put-away-production-or-assembly-output"></a>Stoccare l'output produzione o l'output assemblaggio
La modalità di stoccaggio dell'output di produzione dipende dalla modalità di impostazione della warehouse come ubicazione. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).  

Nelle configurazioni di warehouse di base in cui l'ubicazione richiede l'elaborazione degli stoccaggi ma non l'elaborazione dei carichi, è possibile utilizzare il documento **Stoccaggio magazzino** per organizzare e registrare lo stoccaggio dell'output.  

Nelle configurazioni di warehouse avanzate in cui l'ubicazione richiede sia l'elaborazione degli stoccaggi che dei carichi, è possibile creare un documento di stoccaggio interno oppure un documento di movimento per stoccare l'output.  

La prima fase del processo di creazione dello stoccaggio dell'output prevede la creazione della richiesta warehouse in entrata. Questa richiesta comunica alla warehouse che l'output dell'ordine di produzione o assemblaggio è pronto per lo stoccaggio.

## <a name="to-create-the-inbound-warehouse-request"></a>Per creare la richiesta warehouse in entrata  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordine produzione rilasciato** e quindi scegliere il collegamento correlato.  
2.  Nell'ordine di produzione pronto per lo stoccaggio, scegliere l'azione **Crea richiesta whse. in entrata**.  

> [!NOTE]  
>  È inoltre possibile creare la richiesta warehouse in entrata selezionando la casella di controllo **Crea richiesta in entrata** quando si aggiorna l'ordine di produzione. Per ulteriori informazioni, vedere [Ripianificare o aggiornare gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Per eseguire lo stoccaggio dell'output con uno stoccaggio di magazzino  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stoccaggio in magazzino** e quindi scegliere il collegamento correlato.  
2.  Creare un nuovo stoccaggio di magazzino. Per ulteriori informazioni, vedere [Stoccare articoli con gli stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Per accedere all'output dell'ordine di produzione, scegliere l'azione **Prendi documenti origine** e selezionare l'ordine di produzione rilasciato.  
4.  Compilare debitamente le righe di stoccaggio.
5.  Quando le righe sono pronte per la registrazione, scegliere l'azione **Registra**. Verranno creati i movimenti di warehouse necessari e verrà registrato l'output degli articoli.  

È inoltre possibile creare uno **Stoccaggio magazzino** direttamente dall'ordine produzione rilasciato. Per ulteriori informazioni, vedere [Stoccare articoli con gli stoccaggi magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Quando si registra uno stoccaggio magazzino, si presume che tutte le operazioni siano registrate in base al ciclo standard, ovvero la quantità di output viene registrata in base all'ultima operazione. È possibile utilizzare le registrazioni output per registrare variazioni nella quantità di output e tempi di lavorazione e setup. Se è necessario eseguire una registrazione parziale dopo lo stoccaggio magazzino, è possibile farlo nel setup di tempi e quantità per tutte le operazioni, eccetto l'ultima. In questo caso, l'ultima operazione è controllata dallo stoccaggio magazzino.  

Se è necessario registrare il tempo di setup o di esecuzione sull'ultima operazione, impostare la quantità di output dell'ultima operazione su 0. In alternativa, è possibile scegliere di non registrare affatto l'ultima riga semplicemente eliminandola  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Per eseguire lo stoccaggio dell'output tramite uno stoccaggio interno della warehouse
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stocc. int. whse.** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Nella testata di un nuovo stoccaggio interno compilare almeno il campo **Cod. ubicazione**.  
4. Compilare una riga per ciascun articolo che si desidera trasferire nella warehouse. È sufficiente compilare i campi **Nr. articolo** e **Quantità**.  

    > [!NOTE]  
    >  Quando si seleziona il campo **Nr. articolo**, viene visualizzata la finestra **Lista contenuto collocazione** anziché la finestra **Lista Articoli**. Questo si verifica perché si sta eseguendo lo stoccaggio di un articolo contenuto in una particolare collocazione, ovvero un contenuto collocazione e non semplicemente un articolo, e si conosce già la collocazione da cui l'articolo deve essere prelevato.  

4.  Per immettere nelle righe del prospetto l'intero contenuto della collocazione o il contenuto di collocazioni specifiche nell'ubicazione, scegliere l'azione **Ottieni contenuto collocazione**.  
5.  Scegliere l'azione **Crea stoccaggio** e gli articoli che si desidera trasferire dall'area di produzione verranno inclusi nelle istruzioni di stoccaggio, in attesa di essere immagazzinati.  

> [!NOTE]  
>  Quando l'ubicazione della warehouse prevede l'utilizzo di stoccaggi e prelievi guidati, la warehouse è collegata alla funzione di manufacturing tramite le collocazioni di produzione di default, ovvero le collocazioni di produzione in entrata e in uscita e la collocazione del reparto produttivo aperto, che vengono definite nella Scheda dettaglio **Collocazioni** della scheda ubicazione. Quando si registra l'output di un ordine di produzione, l'output viene inserito nella **collocazione di produzione in uscita**. La procedura descritta in precedenza consente di eseguire lo stoccaggio dell'output di produzione ma, anziché utilizzare la collocazione di default dell'articolo, si procederà a spostare o stoccare gli articoli dalla **collocazione di produzione in uscita** alla collocazione di default dell'articolo.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Per specificare manualmente una collocazione in cui immagazzinare gli articoli dell'output di produzione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto movimentazioni** e quindi scegliere il collegamento correlato.  
2.  Compilare la testata e creare una riga per ciascun articolo che si desidera trasferire nella warehouse.  
3.  Compilare entrambi i campi **Dal codice collocazione** e **A codice collocazione**, quindi immettere la quantità nel campo **Quantità**.  
4.  Per immettere nelle righe del prospetto l'intero contenuto della collocazione o il contenuto di collocazioni specifiche nell'ubicazione, scegliere l'azione **Ottieni contenuto collocazione**.  
5. Selezionare l'azione **Crea movimento**. Verranno create istruzioni di movimentazione della warehouse con le righe di azione Prendere e Mettere indirizzate agli impiegati della warehouse.  

> [!NOTE]  
>  Entrambe le procedure non prevedono l'immissione del numero del documento di origine, ad esempio il numero dell'ordine di produzione, nei documenti per operazioni di stoccaggio interno, stoccaggio o movimentazione.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

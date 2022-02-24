---
title: 'Procedura: Stoccare articoli con gli stoccaggi magazzino | Documenti Microsoft'
description: Quando l'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi ma non l'elaborazione dei carichi, utilizzare il documento **Stoccaggio Magazzino** per registrare e contabilizzare le informazioni riguardanti lo stoccaggio e il carico per i documenti di origine. Il documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di produzione il cui output è pronto per lo stoccaggio.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 439072c09555c7781632c5933ab563caf432c270
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192845"
---
# <a name="put-items-away-with-inventory-put-aways"></a>Eseguire lo stoccaggio con Stoccaggi Magazzino
Quando l'ubicazione è impostata in modo da richiedere l'elaborazione degli stoccaggi ma non l'elaborazione dei carichi, utilizzare il documento **Stoccaggio magazzino** per registrare e contabilizzare le informazioni riguardanti lo stoccaggio e il carico per i documenti di origine. Il documento di origine in entrata può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di asseblaggio o produzione il cui output è pronto per lo stoccaggio.  

È possibile creare uno stoccaggio in magazzino in tre modi:  

- Creare lo stoccaggio in due passaggi redigendo prima una Richiesta Warehouse dal documento di origine, per segnalare alla warehouse che il documento di origine è pronto per lo stoccaggio. Lo stoccaggio in magazzino può quindi essere creato utilizzando la pagina **Stoccaggio Magazzino** in base al documento origine.  
- Creare lo stoccaggio in magazzino direttamente dal documento di origine.  
- Creare stoccaggi in magazzino per più documenti di origine contemporaneamente utilizzando un processo batch.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Per richiedere uno stoccaggio magazzino emettendo il documento di origine
Per gli ordini di acquisto, gli ordini di reso vendita, gli ordini di trasferimento in entrata e gli ordini di assemblaggio, creare la richiesta warehouse emettendo l'ordine. Di seguito viene descritto come eseguire l'operazione da un ordine di acquisto.  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.
2. Selezionare l'ordine di acquisto che si intende rilasciare, quindi scegliere l'azione **Rilascio**.  

    Per gli ordini di produzione, la richiesta warehouse viene creata redigendo una richiesta in entrata dall'ordine di produzione rilasciato.  
3.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di produzione rilasciati** e quindi scegliere il collegamento correlato.  
4. Scegliere l'azione **Crea richiesta whse. in entrata**.  

> [!NOTE]  
>  È inoltre possibile creare la richiesta warehouse in entrata selezionando la casella di controllo **Crea richiesta in entrata** quando si aggiorna l'ordine di produzione. Per ulteriori informazioni, vedere [Ripianificare o aggiornare gli ordini di produzione](production-how-to-replan-refresh-production-orders.md).  

In seguito alla creazione della richiesta warehouse, un dipendente della warehouse addetto allo stoccaggio degli articoli vedrà che il documento di origine è pronto e potrà creare un documento di stoccaggio magazzino.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Per creare uno stoccaggio in magazzino in base al documento origine
Ora che la richiesta è stata creata, l'impiegato della warehouse può creare un nuovo stoccaggio in magazzino basato sul documento di origine rilasciato.   
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Stoccaggio in magazzino** e quindi selezionare il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Nel campo **Documento origine**, selezionare il tipo di documento di origine per cui si esegue lo stoccaggio.  
4. Nel campo **Nr. origine** selezionare il documento di origine.  
5. In alternativa, scegliere l'azione **Prendi documento origine** per selezionare il documento da una lista di documenti di origine in entrata pronti per lo stoccaggio presso l'ubicazione.  
6. Selezionare il pulsante **OK** per compilare le righe di stoccaggio in base al documento di origine selezionato.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Per creare uno stoccaggio magazzino dal documento origine  
1.  Nel documento di origine, che può essere un ordine di acquisto, un ordine di reso da vendita, un ordine di trasferimento in entrata o un ordine di produzione, scegliere l'azione **Crea stoccaggio / prelievo mag.**.  
2. Selezionare la casella di controllo **Crea stoccaggio mag.**.
3. Scegliere il pulsante **OK**. Verrà creato un nuovo stoccaggio di magazzino.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Per creare più stoccaggi in magazzino utilizzando un processo batch  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Crea stoccaggio/Prelievo mag.** e quindi scegliere il collegamento correlato.  
2.  Nella Scheda dettaglio **Richiesta warehouse** della pagina di richiesta, utilizzare i campi **documento origine** e **Nr. documento** per filtrare determinati tipi di documenti oppure intervalli di numeri di documenti.  
3.  Nella Scheda dettaglio **Opzioni** selezionare la casella di controllo **Crea stoccaggio mag.**.
4.  Scegliere il pulsante **OK**. Verranno creati gli stoccaggi magazzino specificati.

## <a name="to-record-the-inventory-put-away"></a>Per registrare lo stoccaggio magazzino  
1. Aprire un documento di stoccaggio creato in precedenza selezionandone uno dalla pagina **Stoccaggi magazzino**.  
2. Nel campo **Codice collocazione** nelle righe di stoccaggio, la collocazione in cui gli articoli devono essere stoccati suggerisce la collocazione di default dell'articolo. È possibile modificare la collocazione in questa pagina, se necessario.  
3. Eseguire lo stoccaggio e immettere le informazioni riguardanti la quantità effettiva stoccata nel campo **Qtà da Gestire**.

    Se è necessario ubicare gli articoli relativi a una riga in più collocazioni, ad esempio perché la collocazione designata è piena, utilizzare la funzione **Dividi riga** della Scheda dettaglio **Righe**. Per ulteriori informazioni sulla divisione delle righe, vedere [Suddividere le righe attività warehouse](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Dopo avere eseguito lo stoccaggio, scegliere l'azione **Registra**.  

Il processo di registrazione contabilizzerà il carico, o nel caso di ordini di produzione, l'output delle righe del documento origine per le quali è stato eseguito lo stoccaggio e, se l'ubicazione prevede l'utilizzo di collocazioni, verranno anche creati i movimenti warehouse per la registrazione delle modifiche delle quantità nelle collocazioni.

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

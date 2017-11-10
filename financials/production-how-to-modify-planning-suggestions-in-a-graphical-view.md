---
title: Come modificare i suggerimenti di pianificazione in una visualizzazione grafica | Microsoft Docs
description: "Un'attività tipica di pianificazione consiste nel modificare o aggiungere le righe del prospetto di pianificazione per modificare gli ordini di approvvigionamento suggeriti prima del commit eseguendo la funzione **Esegui messaggi di azione**. Un'alternativa a questa operazione nel prospetto di pianificazione è utilizzare una visualizzazione grafica."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6cdd86fb96e89e99ea2378221d2991bd640f887e
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-modify-planning-suggestions-in-a-graphical-view"></a>Procedura: Modificare i suggerimenti di pianificazione in una visualizzazione grafica
Un'attività tipica di pianificazione consiste nel modificare o aggiungere le righe del prospetto di pianificazione per modificare gli ordini di approvvigionamento suggeriti prima del commit eseguendo la funzione **Esegui messaggi di azione** . Un'alternativa a questa operazione nel prospetto di pianificazione è utilizzare una visualizzazione grafica.

Nella finestra **Disponibilità articolo per sequenza temporale** è possibile modificare gli ordini e i suggerimenti di approvvigionamento trascinando gli elementi lungo l'asse x per modificare la quantità o lungo l'asse y per modificare la data di scadenza.  

 Nella finestra **Disponibilità articolo per sequenza temporale** e nella finestra **Prospetto pianific.** è possibile effettuare le seguenti modifiche:  

-   Modificare un ordine di approvvigionamento suggerito che esiste solo come riga di pianificazione.  
-   Modificare un ordine di approvvigionamento esistente che il sistema di pianificazione suggerisce di modificare.  
-   Creare un nuovo ordine di approvvigionamento suggerito e modificarlo.  

Per ulteriori informazioni sui tipi di riga di pianificazione visualizzati, vedere il campo Descrizione nella Scheda dettaglio **Modifiche evento**.  

Scegliendo **Salva modifiche** nella finestra **Disponibilità articolo per sequenza temporale**, le modifiche effettuate in corrispondenza vengono copiate nel prospetto di pianificazione o nella richiesta di approvvigionamento. È ora possibile implementarli utilizzando la funzione **Pianificaz. - Esegui mess. azione**.  

La seguente procedura illustra come modificare i suggerimenti di approvvigionamento mediante il trascinamento della selezione. In alternativa, è possibile modificare i campi **Data sc.** e **Quantità** nella Scheda dettaglio **Modifiche evento** e immediatamente visualizzare graficamente le modifiche nella Scheda dettaglio **Sequenza temporale** della finestra **Prospetto pianific.**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Per modificare gli ordini di approvvigionamento suggeriti nella visualizzazione grafica  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Disponibilità articolo per sequenza temporale**, quindi scegliere il collegamento correlato.  

    La finestra **Disponibilità articolo per sequenza temporale** verrà visualizzata con il numero di articolo, l'ubicazione e la variante dell'articolo nella riga di pianificazione selezionata precompilata della Scheda dettaglio **Opzioni**. La Scheda dettaglio **Sequenza temporale** mostra una rappresentazione grafica del magazzino previsto dell'articolo, inclusi i suggerimenti di pianificazione.  

2.  Assicurarsi che il campo **Includi suggerimenti pianificazione** sia selezionato.  
3.  Individuare l'ordine di approvvigionamento suggerito che si desidera modificare. È possibile identificare gli articoli modificabili dal cerchio verde e l'icona a forma di disco. Per ulteriori informazioni sui differenti simboli, vedere la sezione "Simboli e icone nella Scheda dettaglio Sequenza temporale".  
4.  Selezionare il puntatore sul cerchio verde finché non si ingrandisce e il puntatore assume la forma Sposta (quattro frecce).  
5.  Tenere premuto il pulsante del mouse mentre si trascina il puntatore verso l'alto o verso il basso per modificare la quantità. Tenere premuto il pulsante del mouse mentre si trascina il puntatore a sinistra o a destra per modificare la data di scadenza.  
6.  Oltre che spostando gli elementi con il trascinamento, è possibile modificare i suggerimenti di pianificazione usando una serie di funzioni del menu a discesa. Accedere al menu a discesa facendo clic con il pulsante destro del mouse sul cerchio verde di un elemento di approvvigionamento suggerito e selezionare una delle seguenti funzioni  

    |Funzione|Description|  
    |--------------|---------------------------------------|  
    |**Crea nuovo approvvigionamento**|Crea un nuovo elemento nel punto in cui si accede al menu a discesa. Tale elemento rappresenta un nuovo ordine di approvvigionamento suggerito. Diventa una nuova riga del prospetto di pianificazione quando si sceglie **Salva modifiche**.<br /><br /> **NOTA:** se i campi **Filtro ubicazione** o **Filtro variante** nella Scheda dettaglio **Opzioni** sono vuoti o hanno più di un valore di filtro, il nuovo approvvigionamento viene creato e successivamente viene salvato nel prospetto di pianificazione o nella richiesta di approvvigionamento con i seguenti codici:<br /><br /> *Se il campo del filtro è vuoto, il nuovo approvvigionamento viene creato senza un'ubicazione o un codice variante.<br /><br /> *Se più di un valore di filtro è definito, il nuovo approvvigionamento viene creato per il primo valore del filtro in base al metodo di ordinamento.<br /><br /> Se si desidera un altro codice variante o ubicazione, è necessario modificarlo manualmente nella nuova riga di pianificazione.|  
    |**Regola automaticamente approvvigionamento**|Ottimizza un nuovo approvvigionamento creato nel grafico assicurando che risulti come magazzino zero prima dell'approvvigionamento successivo.|  
    |**Elimina approvvigionamento**|Elimina l'elemento nella Scheda dettaglio **Sequenza temporale** ed elimina la riga di pianificazione quando si sceglie **Salva modifiche**. L'icona assume la forma di un disco con una croce rossa quando l'approvvigionamento è stato eliminato.<br /><br /> **NOTA:** è possibile eliminare solo un approvvigionamento del tipo di messaggio di azione **Nuovo**. Dopo aver scelto **Salva modifiche**, è necessario eliminare manualmente la riga di pianificazione in questione nel prospetto di pianificazione o nella richiesta di approvvigionamento.|  

7.  Scegliere l'azione **Ricarica** se si desidera ripristinare tutte le eventuali modifiche apportate dopo l'ultima apertura della finestra **Disponibilità articolo per sequenza temporale** o dopo che si è selezionato **Ricarica**.  
8. Quando gli elementi si trovano nel punto desiderato nel diagramma, selezionare **Salva modifiche** per copiare la quantità modificata e le modifiche alle date nelle righe di richiesta di approvvigionamento o di pianificazione che rappresentano gli elementi grafici.  

Per implementare le modifiche del piano di approvvigionamento, è necessario seguire i messaggi di azione risultanti dal prospetto di pianificazione oppure dalla richiesta di approvvigionamento. Per ulteriori informazioni, vedere Pianificaz - Esegui mess. azione.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Simboli e icone nella Scheda dettaglio Sequenza temporale
 |Simbolo/Icona|Description|  
 |------------------|---------------------------------------|  
 |Croce nera|Ordini (sia domanda che approvvigionamento).<br /><br /> - Non modificabile.<br />-   Visibile quando il campo **Mostra magazzino previsto** è selezionato (grafico arancione).|  
 |Cerchio rosso|Ordini di approvvigionamento esistenti che non sono nei suggerimenti di pianificazione.<br /><br /> - Non modificabile.<br />-   Visibile quando il campo **Mostra magazzino previsto** è selezionato (grafico arancione).|  
 |Stella gialla|Previsione della domanda.<br /><br /> -   Non modificabile.<br />- Visibile quando il campo **Nome previsione** contiene un valore.<br /><br /> Quando i campi **Mostra magazzino previsto** e **Includi suggerimenti pianificazione** sono entrambi selezionati, ciascuna stella gialla ha una controparte collegata nel grafico opposto. Ciò illustra come un approvvigionamento suggerito soddisfa la domanda prevista.|  
 |Cerchio verde con icona a forma di disco con una croce rossa|Ordine di approvvigionamento suggerito con messaggio di azione *Annulla*.<br /><br /> - Non modificabile.<br />-   Visibile quando il campo **Includi suggerimenti pianificazione** è selezionato (grafico verde).|  
 |Cerchio verde con icona a forma di disco con una stella|Ordini di approvvigionamento suggeriti con messaggio di azione *Nuovo*.<br /><br /> - Modificabile.<br />-   Visibile quando il campo **Includi suggerimenti pianificazione** è selezionato (grafico verde).|  
 |Cerchio verde con icona a forma di disco con una o due frecce|Ordini di approvvigionamento suggeriti con messaggio di azione *Riprogramma*, *Modifica Qtà*, o *Riprogr. e mod. qtà*<br /><br /> - Modificabile.<br />-   Visibile quando il campo **Includi suggerimenti pianificazione** è selezionato (grafico verde).<br /><br /> Le frecce riflettono la direzione del suggerimento di pianificazione. Ad esempio, una freccia sinistra con un freccia rivolta verso l'alto corrisponde a un messaggio di azione *Riprogr. e mod. qtà* composto da una riprogrammazione all'indietro e un aumento della quantità.|  

Quando si accede al menu a discesa per la Scheda dettaglio **Sequenza temporale**, in base alla scelta eseguita vengono visualizzate le seguenti funzioni  

 |Funzione|Description|  
 |--------------|---------------------------------------|  
 |**Crea nuovo approvvigionamento**|Crea un nuovo elemento nel punto in cui si accede al menu a discesa. Tale elemento rappresenta un nuovo ordine di approvvigionamento suggerito. Diventa una nuova riga del prospetto di pianificazione quando si sceglie **Salva modifiche** nella scheda **Processo**.<br /><br /> Tutti i valori dei filtri definiti nei campi **Filtro ubicazione** o **Filtro variante** nella Scheda dettaglio **Opzioni** verranno applicati al nuovo ordine di approvvigionamento. **Nota:**  Se i campi filtro sono vuoti o hanno più di un valore, il nuovo ordine di approvvigionamento viene creato utilizzando i seguenti codici: <ul><li>Se il campo del filtro è vuoto, il nuovo approvvigionamento viene creato senza un'ubicazione o un codice variante.</li><li>Se più di un valore di filtro è definito, il nuovo approvvigionamento viene creato utilizzando il primo valore del filtro in base all'ordinamento.</li></ul> Se si desidera un altro codice variante o ubicazione nel nuovo ordine di approvvigionamento, è necessario modificarlo manualmente nella nuova riga di pianificazione.|  
 |**Regola automaticamente approvvigionamento**|Ottimizza un nuovo approvvigionamento creato nel grafico assicurando che risulti come magazzino zero prima dell'approvvigionamento successivo.|  
 |**Elimina approvvigionamento**|Elimina l'elemento nella Scheda dettaglio **Sequenza temporale** e la riga di pianificazione quando si sceglie **Salva modifiche** nella scheda **Processo**. L'icona diventa un disco con una croce rossa quando l'approvvigionamento è stato eliminato. **Nota:** è possibile eliminare solo un approvvigionamento del tipo di messaggio di azione *Nuovo*. Dopo aver scelto **Salva modifiche** nella scheda **Processo**, è necessario eliminare manualmente la riga di pianificazione in questione nel prospetto di pianificazione o nella richiesta di approvvigionamento.|  
 |**Mostra documento**|Apre l'ordine, la riga di pianificazione o la previsione che l'elemento rappresenta.|  
 |**Zoom indietro (CTRL++)**|Ingrandisce la scala dell'asse x, in modo che vengano visualizzati meno giorni. **Nota:**  È possibile ottenere lo stesso risultato tenendo premuto CTRL mentre si ruota la rotellina del mouse.|  
 |**Zoom avanti (CTRL+-)**|Riduce la scala dell'asse x, in modo che vengano visualizzati più giorni. **Nota:**  È possibile ottenere lo stesso risultato tenendo premuto CTRL mentre si ruota la rotellina del mouse.|  
 |**Reimposta zoom (CTRL+0)**|Ripristina la scala originale dell'asse x.|  

Oltre alle azioni da tastiera descritte in precedenza, è possibile utilizzare le seguenti azioni da tastiera nella Scheda dettaglio **Sequenza temporale**.  

 |Azione da tastiera|Description|  
 |---------------------|---------------------------------------|  
 |CTRL + rotellina di scorrimento del mouse|Modifica la scala dell'asse x.|  
 |Selezionare un elemento, quindi premere MAIUSC+FRECCIA|Sposta l'elemento nella direzione della freccia utilizzata.|  
 |TAB|Passa all'elemento successivo.|  
 |MAIUSC+TAB|Passa all'elemento precedente.|  
 |Mentre si sposta un elemento, premere Esc.|Annulla lo spostamento. **Nota:**Non funziona se è stato rilasciato il pulsante del mouse.|

## <a name="see-also"></a>Vedi anche  
[Pianif.](production-planning.md)   
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


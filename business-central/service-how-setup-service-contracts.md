---
title: Impostare i contratti di assistenza
description: 'Scopri come impostare contratti di assistenza con i prerequisiti richiesti, inclusi gruppi di contratti di assistenza, modelli di contratto e modelli di clienti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="set-up-service-contracts"></a>Impostare i contratti di assistenza
Prima di poter utilizzare i contratti, è necessario impostare quanto segue: 

* **Gruppi contratti assistenza**: raggruppano i contratti di assistenza in qualche modo correlati tra di loro.
* **Gruppi conto del contratto di assistenza**: raggruppano i conti dei contratti di assistenza per le fatture di assistenza create per i contratti di assistenza. È possibile assegnare tali gruppi ai contratti di assistenza.  
* **Modelli di contratto**: definiscono i layout dei contratti che includono i dettagli dei contratti di assistenza utilizzati più comunemente. È possibile creare le offerte di contratto di assistenza utilizzando i modelli. Quando si crea un'offerta di contratto, i campi vengono automaticamente riempiti con il contenuto dei campi del modello.
* **Modelli clienti**: consentono di creare delle offerte per i contatti o i potenziali clienti che non sono registrati come clienti in [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Per impostare un gruppo di contratti di assistenza
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi contratto assistenza**, quindi scegli il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Scegliere la casella di controllo **Sc. solo su ordini contr.** se si desidera che gli sconti contratto o assistenza siano validi solo per gli ordini di assistenza contratto, ad esempio la manutenzione.  

## <a name="to-set-up-a-service-contract-account-group"></a>Per impostare un gruppo conto dei contratti di assistenza
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi conto contratto assist.**, quindi scegli il collegamento correlato.  
2. Creare un nuovo gruppo di conto dei contratti dei assistenza.   
3. Compilare i campi **Codice** e **Descrizione**. Questi campi forniscono una descrizione del gruppo conto contratti di assistenza.  
4. Compilare il campo **Conto contratto non prepagato**, quindi scegliere il numero di conto di contabilità generale per il conto non prepagato.  
5. Nel campo **Conto contratto prepagato** scegliere il numero di conto di contabilità generale per il conto prepagato.  

## <a name="to-set-up-a-contract-template"></a>Per impostare un modello di contratto
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Modelli contratto assistenza**, quindi scegli il collegamento correlato.  
2. Creare un nuovo modello di contratto di assistenza.  
3. Nel campo **Nr.** immettere un numero per il modello di contratto.  
  
     In alternativa, se hai impostato una numerazione per i modelli di contratti nella pagina **Setup gest. assist.**, puoi selezionare <kbd>INVIO</kbd> per inserire il successivo numero di modello di contratto disponibile. Compilare gli altri campi, se pertinenti.  
  
4. Nella Scheda dettaglio **Fattura** compilare i campi **Codice gr. conto contratto assist.**, **Periodo di fatturazione** e così via. Compilare gli altri campi, se pertinenti.  
5. Scegliere l'azione **Sconti assistenza** per aggiungere sconti contrattuali.  

## <a name="to-set-up-a-customer-template"></a>Per impostare un modello di cliente
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Modelli cliente**, quindi scegli il collegamento correlato.  
2. Creare una nuova scheda modello cliente.  
3. Nella Scheda dettaglio **Generale** immettere un codice e una descrizione per il modello cliente rispettivamente nei campi **Codice** e **Descrizione**. 
4. Per definire i criteri di ricerca, compilare gli altri campi, ad esempio **Cod. paese**, **Cod. regione** e **Cod. lingua**.  
5. Compilare i campi **Cat. Reg. Business** e **Cat. Reg. Cliente**.  

## <a name="see-also"></a>Vedere anche
[Impostazione della gestione assistenza](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

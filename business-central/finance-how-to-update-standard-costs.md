---
title: Aggiornare i costi standard
description: Periodicamente è necessario aggiornare i costi standard dei componenti ed eseguire il rollup dei nuovi costi nell'articolo padre.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Aggiornare i costi standard
Periodicamente è necessario aggiornare i costi standard dei componenti ed eseguire il rollup dei nuovi costi nell'articolo padre. Il processo in genere è costituito dai quattro passaggi seguenti:  

1.  Aggiornare i costi ai livelli di capacità e componente. Per ulteriori informazioni, vedere il processo batch **Suggerisci costo std. articolo**.  
2.  Consolidamento e roll up dei costi dei componenti e della capacità per calcolare il costo totale di produzione o di assemblaggio degli articoli.  
3.  Implementare i costi standard che vengono registrati quando si eseguono i processi batch precedenti. I costi standard non saranno effettivi finché non verranno implementati. Usa il processo batch **Implementa modifiche costo std.** che consente di aggiornare il costo standard degli elementi riportati nella tabella Prospetto costo standard.  
4.  Implementare le modifiche per aggiornare il campo **Costo unitario** nella scheda articolo ed eseguire la rivalutazione di magazzino. Per ulteriori informazioni, vedere [Rivalutare il magazzino](inventory-how-revalue-inventory.md).  

Per ulteriori informazioni, vedere [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md).
  
## Per aggiornare i costi standard

1.  Eseguire il processo batch **Rettifica costo - Movimenti articoli**. Per avviare il processo batch, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Rettifica costo - Mov. art.**, quindi scegli il collegamento correlato. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] - Esamina i risultati e apporta le modifiche necessarie.  
2.  Eseguire il processo batch **Registra costo magazzino in C/G**. Per avviare il processo batch, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registra costo magazzino in C/G**, quindi scegli il collegamento correlato. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] - Esamina i risultati e apporta le modifiche necessarie.  
3.  Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti un valore in **Prospetto costo standard** e utilizza una o più delle seguenti azioni:

    1.  Eseguire il processo batch **Suggerisci costo std. articolo**.  
    2.  Analizzare i risultati e apportare le modifiche necessarie.  
    3.  Eseguire il processo batch **Suggerisci costo standard capacità**.  
    4.  Analizzare i risultati e apportare le modifiche necessarie.
    5. Eseguire il processo batch **Roll up del costo standard**.
    6.  Analizzare i risultati e apportare le modifiche necessarie.
    7.  Eseguire il processo batch **Implementa modifiche costo std.**  
4.  Analizzare e contabilizzare la pagina **Registrazioni rivalutazioni**, in cui sono stati inseriti i dati ricavati tramite i passaggi precedenti del processo.  

## Vedi anche

 [Informazioni sul calcolo del costo standard](finance-about-calculating-standard-cost.md)   
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)   
 [Dati finanziari](finance.md)  
 [Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
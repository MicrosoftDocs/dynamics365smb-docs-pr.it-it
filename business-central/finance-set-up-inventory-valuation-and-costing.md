---
title: Impostare la valutazione magazzino e i costi | Microsoft Docs
description: Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Impostazione della valutazione magazzino e i costi
Per assicurarsi che i costi di magazzino vengano registrati correttamente, è necessario impostare vari campi e finestre prima di iniziare a effettuare transazioni di articoli.

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|Impostare un metodo di costing per ogni articolo in modo da definire come verrà utilizzato il relativo costo in entrata per valutare il valore di magazzino e il delle merci vendute.|[Registrare nuovi articoli](inventory-how-register-new-items.md)|  
|Assicurarsi che il costo venga registrato automaticamente nella contabilità generale ogni volta che viene contabilizzata una transazione di magazzino.|campo **Reg. automatica costi** nella finestra **Setup magazzino**|  
|Assicurarsi che i costi previsti siano registrati nella contabilità generale per visualizzare, dai conti C/G provvisori, una stima degli importi residui e il costo degli articoli trattati, prima dell'effettiva fatturazione.|Campo **Reg. costi previsti in C/G** nella finestra **Setup magazzino**|  
|Impostare il sistema affinché venga effettuata la rettifica automatica delle eventuali modifiche dei costi ogni volta che si registrano transazioni di magazzino.|[Rettifica costi articolo](inventory-how-adjust-item-costs.md)|  
|Definire se il costo medio deve essere calcolato solo per articolo o per articolo per ogni unità di stockkeeping e per ogni variante dell'articolo.|Campo **Tipo calcolo costo medio** nella finestra **Setup magazzino**|  
|Selezionare il periodo di tempo che si desidera venga utilizzato dal programma per calcolare il costo medio ponderato degli articoli per i quali è utilizzato il metodo di costing Medio.|Campo **Costo medio periodo** nella finestra **Setup magazzino**|  
|Definire i periodi di magazzino per controllare il valore di magazzino nel tempo, disabilitando la registrazione delle transazioni nei periodi di magazzino chiusi.|[Utilizzare periodi di magazzino](finance-how-to-work-with-inventory-periods.md)|  
|Assicurarsi che i resi di vendita vengano applicati alla transazione in uscita originale per mantenere il valore di magazzino.|Campo **Storno esatto costo obblig.** nella finestra **Contabilità clienti**|  
|Assicurarsi che i resi di acquisto vengano applicati alla transazione in entrata originale per mantenere il valore di magazzino.|Campo **Storno esatto costo obblig.** nella finestra **Contabilità fornitori**|
|Impostare le regole di arrotondamento da applicare quando i prezzi degli articoli e i costi standard vengono rettificati o suggeriti.|Finestra **Metodo di arrotondamento**|  

## <a name="see-also"></a>Vedi anche  
[Gestione dei costi di magazzino](finance-manage-inventory-costs.md)  
[Utilizzo di Business Central](ui-work-product.md)  
[Finanze](finance.md)  


---
title: Impostazione delle condizioni di pagamento
description: "Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/27/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 05e768e6c8c244571d6056551beda635994ec6aa
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-payment-terms"></a>Impostazione delle condizioni di pagamento
Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.  

Se una condizione di pagamento deve prevedere un unico pagamento, è necessario specificare come verrà calcolata la data di scadenza.  

## <a name="to-set-up-payment-terms"></a>Per impostare le condizioni di pagamento  
1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Condizioni pagamento**, quindi scegliere il collegamento correlato.    
2.  Compilare i campi della finestra **Condizioni pagamento**. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]  
3.  Scegliere l'azione **Calcola**.  
4.  Nella finestra **Righe condizioni pagamento**, compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**% pagamento**|Specificare la percentuale del pagamento totale a cui si riferisce il pagamento rateale.<br /><br /> Ad esempio, se il pagamento deve essere effettuato in una rata, immettere **100**.|  
    |**Calcolo Data di Scadenza**|Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato.<br /><br /> Ad esempio, se il pagamento deve essere effettuato in una rata dopo due settimane, immettere **14D**. Per ulteriori informazioni, vedere la sezione "Utilizzo di formule per le date" in [Immissione di dati](../../ui-enter-data.md).|  
    |**Calcolo Sconto per Data**|Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato per ottenere uno sconto.|  
    |**Sconto %**|Specificare la percentuale di sconto che viene applicata per il pagamento anticipato di un importo fattura.|  

5.  Scegliere il pulsante **OK**.  

Il campo **Nr. di pagamenti** nella finestra **Condizioni pagamento** viene aggiornato. Le condizioni di pagamento impostate qui saranno un riferimento per il calcolo automatico della data di scadenza dei documenti registrati per clienti e fornitori.  

## <a name="see-also"></a>Vedi anche  
 [Procedura: Impostare i pagamenti automatici e gli effetti automatici](how-to-set-up-automatic-payments-and-automatic-bills.md)   
 [Funzionalità locale per l'Italia](italy-local-functionality.md)   


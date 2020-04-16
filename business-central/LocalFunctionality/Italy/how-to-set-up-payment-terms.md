---
title: Impostazione delle condizioni di pagamento
description: Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9a66c66770b30ac64604cb36fcf26cd1a1919f25
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181122"
---
# <a name="set-up-payment-terms"></a>Impostazione delle condizioni di pagamento
Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.  

Se una condizione di pagamento deve prevedere un unico pagamento, è necessario specificare come verrà calcolata la data di scadenza.  

## <a name="to-set-up-payment-terms"></a>Per impostare le condizioni di pagamento  
1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Condizioni pagamento** e quindi scegliere il collegamento correlato.    
2.  Compilare i campi nella pagina **Condizioni pagamento**. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]  
3.  Scegliere l'azione **Calcola**.  
4.  Nella pagina **Righe condizioni pagamento**, compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**% pagamento**|Specificare la percentuale del pagamento totale a cui si riferisce il pagamento rateale.<br /><br /> Ad esempio, se il pagamento deve essere effettuato in una rata, immettere **100**.|  
    |**Calcolo Data di Scadenza**|Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato.<br /><br /> Ad esempio, se il pagamento deve essere effettuato in una rata dopo due settimane, immettere **14D**. Per ulteriori informazioni, vedere [Utilizzo di formule per le date](../../ui-enter-date-ranges.md#using-date-formulas).|  
    |**Calcolo Sconto per Data**|Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato per ottenere uno sconto.|  
    |**Sconto %**|Specificare la percentuale di sconto che viene applicata per il pagamento anticipato di un importo fattura.|  

5.  Scegliere il pulsante **OK**.  

Il campo **Nr. di pagamenti** nella pagina **Condizioni pagamento** viene aggiornato. Le condizioni di pagamento impostate qui saranno un riferimento per il calcolo automatico della data di scadenza dei documenti registrati per clienti e fornitori.  

## <a name="see-also"></a>Vedi anche  
 [Impostare i pagamenti automatici e gli effetti automatici](how-to-set-up-automatic-payments-and-automatic-bills.md)   
 [Funzionalità locale per l'Italia](italy-local-functionality.md)   

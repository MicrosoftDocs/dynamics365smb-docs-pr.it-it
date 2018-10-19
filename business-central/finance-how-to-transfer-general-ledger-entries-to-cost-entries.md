---
title: Come trasferire movimenti C/G ai movimenti di costi | Microsoft Docs
description: I movimenti C/G possono essere trasferiti ai movimenti di costi.
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
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Trasferire movimenti C/G a movimenti di costi
I movimenti C/G possono essere trasferiti ai movimenti di costi.  

Prima di eseguire il processo per il trasferimento dei movimenti C/G ai movimenti di costi, è necessario preparare il trasferimento per evitare la registrazione manuale della correzione.  

## <a name="to-prepare-the-transfer"></a>Per preparare il trasferimento  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità industriale** e quindi scegliere il collegamento correlato.  
2.  Nella finestra **Setup contabilità industriale** controllare che il campo **Data inizio per trasferimento C/G** sia impostato sul valore corretto.  
3.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei tipi di costo** e quindi scegliere il collegamento correlato.  
4.  Nella finestra **Scheda tipo costo** verificare che il campo **Intervallo conti C/G** sia collegato correttamente per ogni tipo di costo per prelevare i movimenti dalla contabilità generale.  
5.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.  
6.  Per ogni conto di contabilità generale pertinente, nella finestra **Scheda conto C/G** verificare che il campo **Nr. tipo di costo** sia collegato correttamente a un tipo di costo. Per ulteriori informazioni, vedere [Definizione della relazione tra i tipi di costo e i conti di contabilità generale](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Verificare che a tutti i relativi movimenti C/G siano associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Per trasferire movimenti C/G a movimenti di costi  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Trasferisci movimenti C/G a CA** e quindi scegliere il collegamento correlato.  
2.  Scegliere **Sì** per avviare il trasferimento. Con il processo vengono trasferiti tutti i movimenti C/G che non sono già stati trasferiti.  

    Durante il trasferimento, con il processo vengono creati collegamenti nei movimenti nella tabella **Movimento di costo** e nella tabella **Registro costi**. In questo modo è possibile analizzare l'origine dei movimenti di costi.  

## <a name="see-also"></a>Vedi anche  
 [Criteri per trasferire movimenti C/G ai movimenti di costi](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Trasferimento automatico e movimenti combinati](finance-automatic-transfer-combined-entries.md)   
 [Risultati del trasferimento](finance-results-of-the-transfer.md)   
 [Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)   
 [Definizione della relazione tra i tipi di costo e i conti di contabilità generale](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   


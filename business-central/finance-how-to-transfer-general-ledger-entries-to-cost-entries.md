---
title: Come trasferire movimenti C/G ai movimenti di costi | Microsoft Docs
description: I movimenti C/G possono essere trasferiti ai movimenti di costi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: a33fb434cc239de951d18783911c879587a3ace0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242603"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Trasferire movimenti C/G a movimenti di costi
I movimenti C/G possono essere trasferiti ai movimenti di costi.  

Prima di eseguire il processo per il trasferimento dei movimenti C/G ai movimenti di costi, è necessario preparare il trasferimento per evitare la registrazione manuale della correzione.  

## <a name="to-prepare-the-transfer"></a>Per preparare il trasferimento  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità industriale** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Setup contabilità industriale** controllare che il campo **Data inizio per trasferimento C/G** sia impostato sul valore corretto.  
3.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei tipi di costo** e quindi scegliere il collegamento correlato.  
4.  Nella pagina **Scheda tipo costo** verificare che il campo **Intervallo conti C/G** sia collegato correttamente per ogni tipo di costo per prelevare i movimenti dalla contabilità generale.  
5.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.  
6.  Per ogni conto di contabilità generale pertinente, nella pagina **Scheda conto C/G** verificare che il campo **Nr. tipo di costo** sia collegato correttamente a un tipo di costo. Per ulteriori informazioni, vedere [Impostazione della contabilità industriale](finance-set-up-cost-accounting.md).  
7.  Verificare che a tutti i relativi movimenti C/G siano associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Per trasferire movimenti C/G a movimenti di costi  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Trasferisci movimenti C/G a CA** e quindi scegliere il collegamento correlato.  
2.  Scegliere **Sì** per avviare il trasferimento. Con il processo vengono trasferiti tutti i movimenti C/G che non sono già stati trasferiti.  

    Durante il trasferimento, con il processo vengono creati collegamenti nei movimenti nella tabella **Movimento di costo** e nella tabella **Registro costi**. In questo modo è possibile analizzare l'origine dei movimenti di costi.  

## <a name="see-also"></a>Vedi anche  
[Trasferimento e registrazione di movimenti di costi](finance-transfer-and-post-cost-entries.md)   
[Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)   

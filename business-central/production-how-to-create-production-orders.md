---
title: Come creare le testate degli ordini di produzione | Microsoft Docs
description: Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 683631572b7898ede3b7f1418f68a7ce95743ff8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380901"
---
# <a name="create-production-order-headers"></a>Creare le testate degli ordini di produzione
Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.

Gli ordini di produzione vengono in genere creati automaticamente da una funzione di pianificazione per soddisfare una domanda conosciuta. Per ulteriori informazioni, vedere [Pianificazione](production-planning.md).   

Nella seguente procedura viene creato un ordine produzione confermato. È anche possibile creare ordini di produzione con uno stato differente.  

## <a name="to-create-a-production-order-header"></a>Per creare una testata degli ordini di produzione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ord. produzione confermati** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Nel campo **Nr.** inserire il numero di serie successivo.  
4.  Selezionare nel campo **Tipo Origine** l'origine dell'ordine di produzione.

    Qui è possibile selezionare la famiglia di articoli. Per ulteriori informazioni, vedere [Utilizzare famiglie di prodotti](production-how-work-family.md).
5.  Nel campo **Nr. origine** selezionare il numero dell'articolo, della famiglia o della testata di vendita per il quale deve essere generato l'ordine di produzione.  
6.  Compilare i campi **Quantità** e **Data Scadenza** con i dati desiderati.  

Quando i requisiti di produzione cambiano, ad esempio componenti o operazioni, è possibile ripianificare rapidamente l'ordine di produzione. Per ulteriori informazioni, vedere [Ripianificare o aggiornare direttamente gli ordini di produzione](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Vedi anche  
[Manufacturing](production-manage-manufacturing.md)    
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)      
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Come creare le testate degli ordini di produzione | Microsoft Docs
description: "Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a>Procedura: Creare le testate degli ordini di produzione
Gli ordini di produzione possono essere creati manualmente. Prima di tutto è necessario creare la testata ordine di produzione.

Gli ordini di produzione vengono in genere creati automaticamente da una funzione di pianificazione per soddisfare una domanda conosciuta. Per ulteriori informazioni, vedere [Pianificazione](production-planning.md).   

Nella seguente procedura viene creato un ordine produzione confermato. È anche possibile creare ordini di produzione con uno stato differente.  

## <a name="to-create-a-production-order-header"></a>Per creare una testata degli ordini di produzione  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ord. produzione confermato**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Nel campo **Nr.** inserire il numero di serie successivo.  
4.  Selezionare nel campo **Tipo Origine** l'origine dell'ordine di produzione.

    Qui è possibile selezionare la famiglia di articoli. Per ulteriori informazioni, vedere [Procedura: Utilizzare famiglie di prodotti](production-how-work-family.md).
5.  Nel campo **Nr. origine** selezionare il numero dell'articolo, della famiglia o della testata di vendita per il quale deve essere generato l'ordine di produzione.  
6.  Compilare i campi **Quantità** e **Data Scadenza** con i dati desiderati.  

Quando i requisiti di produzione cambiano, ad esempio componenti o operazioni, è possibile ripianificare rapidamente l'ordine di produzione. Per ulteriori informazioni, vedere [Procedura: Ripianificare o aggiornare direttamente gli ordini di produzione](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Vedi anche  
[Manufacturing](production-manage-manufacturing.md)    
[Impostazione della produzione](production-configure-production-processes.md)  
[Pianif.](production-planning.md)      
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
title: 'Procedura: Creazione di più schede cespite'
description: Durante la registrazione delle fatture di acquisto è possibile creare automaticamente più schede cespite.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d3f7edde01c763b02453e094efac8a541b3ea9d9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919995"
---
# <a name="create-multiple-fixed-asset-cards"></a>Creazione di più schede cespite
Durante la registrazione delle fatture di acquisto è possibile creare automaticamente più schede cespite. Se ad esempio la società acquista 200 computer dello stesso tipo dallo stesso fornitore, non è necessario creare manualmente una scheda cespite per ogni computer, ma tali schede possono essere create automaticamente.  

## <a name="to-create-multiple-fixed-asset-cards"></a>Per creare più schede cespite  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Liste**, quindi l'azione **Cespiti**.  
3.  Nella pagina **Lista cespiti**, scegliere l'azione **Nuovo**.  
4.  Compilare i campi della pagina **Scheda cespite**.  

    Verrà utilizzato il valore del campo **Nr.** quando successivamente si generano i cespiti residui.  

5.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e quindi scegliere il collegamento correlato.  
6.  Creare un nuovo ordine di acquisto o aprire l'ordine di acquisto esistente.  
7.  Espandere la Scheda dettaglio **Righe**.  
8.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo**|Selezionare **Cespite**.|  
    |**Nr.**|Specificare il numero del cespite.<br /><br /> **NOTA:** deve corrispondere al numero di cespite immesso nell'elenco **Cespite**.|  
    |**Nr. di schede cespite**|Specificare il numero di duplicati corrispondente per il cespite.<br /><br /> **NOTA:** durante la registrazione della fattura vengono automaticamente generate schede cespite duplicate, che vengono aggiunte all'elenco di cespiti. L'unica differenza tra le varie schede cespite duplicate è il numero assegnato a ciascun cespite.|  

9. Scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedere anche  
 [Cespiti](../../fa-manage.md)  
 [Cespiti italiani](italian-fixed-assets.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 60078a4a4ec1d86bd48b8af41a0fce351528d3d9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241764"
---
# <a name="create-multiple-fixed-asset-cards"></a>Creazione di più schede cespite
Durante la registrazione delle fatture di acquisto è possibile creare automaticamente più schede cespite. Se ad esempio la società acquista 200 computer dello stesso tipo dallo stesso fornitore, non è necessario creare manualmente una scheda cespite per ogni computer, ma tali schede possono essere create automaticamente.  

## <a name="to-create-multiple-fixed-asset-cards"></a>Per creare più schede cespite  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cespiti**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Liste**, quindi l'azione **Cespiti**.  
3.  Nella pagina **Lista cespiti**, scegliere l'azione **Nuovo**.  
4.  Compilare i campi della pagina **Scheda cespite**.  

    Verrà utilizzato il valore del campo **Nr.** quando successivamente si generano i cespiti residui.  

5.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ordini acquisto**, quindi scegliere il collegamento correlato.  
6.  Creare un nuovo ordine di acquisto o aprire l'ordine di acquisto esistente.  
7.  Espandere la Scheda dettaglio **Righe**.  
8.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo**|Selezionare **Cespite**.|  
    |**Nr.**|Specificare il numero del cespite.<br /><br /> **NOTA:** deve corrispondere al numero di cespite immesso nell'elenco **Cespite**.|  
    |**Nr. di schede cespite**|Specificare il numero di duplicati corrispondente per il cespite.<br /><br /> **NOTA:** durante la registrazione della fattura vengono automaticamente generate schede cespite duplicate, che vengono aggiunte all'elenco di cespiti. L'unica differenza tra le varie schede cespite duplicate è il numero assegnato a ciascun cespite.|  

9. Scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedi anche  
 [Cespiti](../../fa-manage.md)  
 [Cespiti italiani](italian-fixed-assets.md)
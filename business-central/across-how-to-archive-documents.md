---
title: Come archiviare documenti di acquisto e vendita | Documenti Microsoft
description: "È possibile archiviare ordini di acquisto e vendita, offerte, ordini di reso e ordini programmati e utilizzare il documento archiviato per ricreare il documento da cui è stato archiviato."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4827e25d97127faf691b96df9868320bb47dee39
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="archive-documents"></a>Archiviare documenti
È possibile archiviare ordini di acquisto e vendita, offerte, ordini di reso e ordini programmati e utilizzare il documento archiviato per ricreare il documento da cui è stato archiviato.

## <a name="to-set-up-automatic-document-archiving"></a>Per impostare l'archiviazione automatica dei documenti  
È possibile impostare l'archiviazione automatica di documenti di vendita e di acquisto, offerte, ordini programmati e ordini di reso, prima di eliminarli.

La procedura seguente illustra come configurare l'archiviazione automatica di documenti di vendita. I passaggi sono simili per i documenti di acquisto.
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità clienti e vendite** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup contabilità clienti e vendite** compilare i campi come descritto di seguito.

|Campo|Description|
|-----|-----------|
|**Archiviazione Offerte Vendita**|**Mai** per non archiviare mai offerte di vendita quando vengono eliminate. **Domanda** per chiedere all'utente di scegliere se archiviare le offerte di vendita quando vengono eliminate. **Sempre** per non archiviare automaticamente le offerte di vendita quando vengono eliminate.|
|**Archiviazione ordini di vendita programmati**|Selezionare questa opzione per archiviare automaticamente gli ordini di vendita programmati ogni volta che vengono eliminati.|
|**Ordini archiviati e ordini di reso**|Selezionare questa opzione per archiviare automaticamente gli ordini di vendita ogni volta che vengono eliminati.|

## <a name="to-archive-a-sales-order"></a>Per archiviare un ordine di vendita
Di seguito viene descritto come archiviare un ordine di vendita. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini di vendita** e quindi scegliere il collegamento correlato.  
2.  Aprire un ordine di vendita da archiviare.  
3.  Scegliere l'azione **Archivia documento**.

L'ordine di vendita è archiviato. È possibile visualizzarlo nella pagina **Ordine vendite archiviato**. Da qui, è anche possibile utilizzarlo per ricreare l'ordine di vendita da cui è stato archiviato.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Per ricreare un ordine di vendita dall'archivio
Di seguito viene descritto come ricreare un ordine di vendita. I passaggi sono simili per tutti gli ordini, gli ordini programmati, gli ordini di reso e le offerte.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita archiviati** e quindi scegliere il collegamento correlato.
2.  Selezionare l'ordine di vendita archiviato da ricreare, quindi scegliere l'azione **Ripristina**.  

L'ordine di vendita viene creato e aggiunto alla pagina **Ordini vendita**.

## <a name="to-delete-archived-sales-orders"></a>Per eliminare ordini di vendita archiviati
Di seguito viene descritto come eliminare ordini di vendita archiviati. I passaggi sono simili per altri altri documenti di acquisto e vendita archiviati.

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elimina versioni ordine vendita archiviate** e quindi scegliere il collegamento correlato.  
2.  Nella pagina **Elimina versioni ordine vendita archiviate**, selezionare i filtri appropriati.  
3.  Scegliere il pulsante **OK**.

## <a name="see-also"></a>Vedi anche
[Tenere traccia delle righe dei documenti](across-how-to-track-document-lines.md)  
[Vendite](sales-manage-sales.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


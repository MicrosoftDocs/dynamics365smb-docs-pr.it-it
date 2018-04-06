---
title: Impostare una scheda ubicazione e definire i percorsi di trasferimento | Documenti Microsoft
description: "È possibile creare una scheda ubicazione per ogni area in cui vengono immagazzinati gli articoli in magazzino, ad esempio warehouse o centro di distribuzione, per impostare percorsi per il trasferimento degli articoli tra le ubicazioni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57e16fe7d7dd3edd832fb29773fc2a9c13cba153
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-locations"></a>Impostare le ubicazioni
Se si acquista, immagazzina o si vendono articoli in più aree o warehouse, è necessario impostare ogni ubicazione con una scheda ubicazione e definire i percorsi di trasferimento.

È quindi possibile creare le righe del documento per una specifica ubicazione, visualizzare la disponibilità per ubicazione e trasferire il magazzino tra le ubicazioni. Per ulteriori informazioni, vedere [Gestire il magazzino](inventory-manage-inventory.md).

## <a name="to-create-a-location-card"></a>Per creare una nuova scheda Ubicazione
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Ubicazioni**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella finestra **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ripetere i passaggi 2 e 3 per ogni ubicazione in cui si desidera mantenere il magazzino.

> [!NOTE]  
> Molti campi della scheda ubicazione fanno riferimento alla gestione degli articoli nei processi della warehouse in entrata e in uscita. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Per creare i percorsi di trasferimento
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Percorsi di trasferimento**, quindi scegliere il collegamento correlato.
2. In alternativa, da una qualsiasi finestra **Scheda Ubicazione** scegliere l'azione **Percorsi trasferimento**.
3. Scegliere l'azione **Nuovo**.
4. Nella finestra **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

A questo punto è possibile trasferire agli articoli di magazzino tra due ubicazioni. Per ulteriori informazioni, vedere [Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Vedi anche
[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizzazione dell'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


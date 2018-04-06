---
title: Impostare codici per servizi standard | Documenti Microsoft
description: "Informazioni su come impostare i codici per le attività di assistenza eseguite di frequente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bca816da5473ea3f5f8eab892125e32a045ffec3
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-standard-service-codes"></a>Impostare codici di servizio standard
Quando si presta un tipo di assistenza standard, è spesso necessario creare documenti di assistenza le cui righe contengono informazioni simili. Per facilitare la creazione di queste righe, è possibile impostare dei codici di servizio standard aventi un insieme predefinito di righe di assistenza. Quando si sceglie il codice in un documento di assistenza, le righe vengono immesse automaticamente. È possibile impostare un qualsiasi numero di codici di servizio standard e a ogni codice può essere collegato un numero illimitato di righe di assistenza di tipo diverso, tra cui articolo, risorsa, costo o testo standard. Vengono create righe di assistenza per ciascun codice di servizio standard nella scheda **Codice servizio standard**. A questo punto è possibile assegnare codici di servizio standard a gruppi di articoli in assistenza nella pagina **Cod. gr. art. ass. standard**. Successivamente, quando si crea un documento di assistenza, è possibile utilizzare l'azione **Ottieni codici servizio std.** per aggiungere righe di assistenza.  
  
> [!Tip]
>  È possibile utilizzare la stessa procedura per creare righe nei documenti di vendita e acquisto. Per altre informazioni, vedere [Creare righe di vendite e acquisti ricorrenti](sales-how-work-standard-lines.md).    
  
## <a name="to-set-up-a-standard-service-code"></a>Per impostare un codice di servizio standard    
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Codici servizio standard**, quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Compilare le righe di assistenza collegate al codice specifico.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Per assegnare un codice di servizio standard a un gruppo di articoli in assistenza
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Gruppi articoli in assistenza**, quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Compilare le righe di assistenza collegate al codice specifico.  

## <a name="see-also"></a>Vedi anche
[Gestione assistenza](service-service.md)

---
title: Associare e sincronizzare i record manualmente | Microsoft Docs
description: La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record in una tabella in Business Central e nell'entità Dynamics 365 for Sales che sono associati.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6d1248ac77208e382c5594af57335df6ff824630
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726769"
---
# <a name="couple-and-synchronize-records-manually"></a>Associare e sincronizzare i record manualmente
In questo argomento viene descritto come associare uno o più record in [!INCLUDE[d365fin](includes/d365fin_md.md)] a record in [!INCLUDE[crm_md](includes/crm_md.md)]. L'associazione di record consente di visualizzare le infomazioni di [!INCLUDE[crm_md](includes/crm_md.md)] da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa. L'associazione consente inoltre di sincronizzare dati tra i record. È possibile associare i record esistenti, oppure creare e associare nuovi record.

> [!Note]
> L'associazione e la sincronizzazione con [!INCLUDE[crm_md](includes/crm_md.md)] sono disponibili solo se l'amministratore di sistema ha creato una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)]. Un modo rapido di verificare è di aprire la scheda **Cliente** e di cercare l'azione **Imposta associazione**. Se l'azione è disponibile, le app sono collegate.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Per associare un record  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  

    È inoltre possibile aprire la pagina elenco e selezionare il record che si desidera associare.  

2.  Scegliere l'azione **Imposta associazione**.  
3.  Compilare i campi e scegliere **OK**.  

## <a name="to-synchronize-a-single-record"></a>Per sincronizzare un singolo record  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  
2.  Scegliere l'azione **Sincronizza adesso**.  
3.  Se un record può essere sincronizzato da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.  

## <a name="to-synchronize-multiple-records"></a>Per sincronizzare più record  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la pagina elenco per il record, ad esempio le pagine elenco Clienti o Contatti.  
2.  Selezionare i record che si intende sincronizzare, quindi scegliere **Sincronizza adesso**.  
3.  Se i record possono essere sincronizzati da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.  

## <a name="see-also"></a>Vedere anche  
[Utilizzo di Dynamics 365 for Sales da Business Central](marketing-integrate-dynamicscrm.md)

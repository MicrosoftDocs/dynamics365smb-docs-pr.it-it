---
title: Associare e sincronizzare i record manualmente | Microsoft Docs
description: La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record in una tabella in Business Central e nell'entità Dynamics 365 Sales che sono associati.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196665"
---
# <a name="couple-and-synchronize-records-manually"></a>Associare e sincronizzare i record manualmente
In questo argomento viene descritto come associare uno o più record in [!INCLUDE[d365fin](includes/d365fin_md.md)] a record in Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)]. L'associazione di record consente di visualizzare le infomazioni di Common Data Service da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa. L'associazione consente inoltre di sincronizzare dati tra i record. È possibile associare i record esistenti, oppure creare e associare nuovi record.

> [!Note]
> L'associazione e la sincronizzazione dei dati è disponibile solo se l'amministratore di sistema ha creato una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)]. Un modo rapido di verificare è di aprire la scheda **Cliente** e di cercare l'azione **Imposta associazione**. Se l'azione è disponibile, le app sono collegate.   

## <a name="video-example"></a>Esempio di video

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Per associare un record  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  

    È inoltre possibile aprire la pagina elenco e selezionare il record che si desidera associare.  

2.  Scegliere l'azione **Imposta associazione**.  
3.  Compilare i campi e scegliere **OK**.  

## <a name="to-synchronize-a-single-record"></a>Per sincronizzare un singolo record  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  
2.  Scegliere l'azione **Sincronizza adesso**.  
3.  Se un record può essere sincronizzato in una direzione, selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Per sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  In [!INCLUDE[crm_md](includes/crm_md.md)], aprire il modulo del record da associare. Ad esempio, la scheda Account o il modulo scheda Contatto.  
2.  Scegli l'azione **[!INCLUDE[d365fin](includes/d365fin_md.md)]** nella barra multifunzione per aprire e associare automaticamente il record.

> [!Note]
> È possibile sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)] automaticamente solo quando **Sinc. solo record associati** è disabilitata e la direzione di sincronizzazione è impostata su Bidirezionale o Da tabella di integrazione nella pagina **Integration Table Mapping** per il record. Per ulteriori informazioni, vedere [Mappatura delle tabelle e dei campi da sincronizzare](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Per sincronizzare più record  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)], aprire la pagina elenco per il record, ad esempio le pagine elenco Clienti o Contatti.  
2.  Selezionare i record che si intende sincronizzare, quindi scegliere **Sincronizza adesso**.  
3.  Se i record possono essere sincronizzati in una direzione, selezionare l'opzione che specifica la direzione e scegliere **OK**.  

## <a name="see-also"></a>Vedere anche  
[Utilizzo di Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md)

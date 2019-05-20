---
title: Visualizzare e modificare in Excel da Business Central | Microsoft Docs
description: Informazioni su come aprire le pagine in Microsoft Excel da Business Central per una migliore analisi dei dati.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 68139f258595bcca2658e394a4251e30dfbe6510
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240213"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visualizzare e modificare in Excel da Business Central 

Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel. A questo proposito, sono disponibili due opzioni. È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina. Di seguito sono descritte le differenze tra le due azioni:  

## <a name="open-in-excel"></a>Apri in Excel

-    Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati. Ciò significa che la cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prodshort](includes/prodshort.md)].

-    In Excel è possibile apportare modifiche ai record, ma non ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)]. È possibile salvare le modifiche solo in un file Excel nel computer. 

-    Questa azione è compatibile con Windows e macOS. 

>[!NOTE]
>Per [!INCLUDE[prodshort](includes/prodshort.md)] locale, l'azione **Apri in Excel** non è disponibile se è già presente l'azione **Modifica in Excel**.

## <a name="edit-in-excel"></a>Modifica in Excel

-    Con questa azione, la cartella di lavoro Excel non rispetta i filtri nella pagina che limitano i record visualizzati. Ciò significa che la cartella di lavoro Excel conterrà tutti i record e le colonne disponibili, indipendentemente da ciò che è visualizzato nella pagina. 

-    Il vantaggio dell'azione **Modifica in Excel** è che consente di apportare modifiche ai record in Excel e quindi di ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].

-    È compatibile con Windows ma non con macOS.

>[!NOTE]
>Per [!INCLUDE[prodshort](includes/prodshort.md)] locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato installato dall'amministratore. Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Vedere le differenze tra le opzioni 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Vedere anche
[Utilizzo di Business Central](ui-work-product.md)  

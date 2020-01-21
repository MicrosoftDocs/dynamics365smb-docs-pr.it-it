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
ms.date: 01/13/2020
ms.author: jswymer
ms.openlocfilehash: 9fd5c6c242932d75addcfa5c1811bdd1aff99a94
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953050"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visualizzare e modificare in Excel da Business Central

Con le pagine che visualizzano un elenco di record in righe e colonne, come un elenco di clienti, ordini di vendita o fatture, è anche possibile visualizzare i record utilizzando Microsoft Excel. A questo proposito, sono disponibili due opzioni. È possibile selezionare l'azione **Apri in Excel** o l'azione **Modifica in Excel** nella pagina. Di seguito sono descritte le differenze tra le due azioni:  

## <a name="open-in-excel"></a>Apri in Excel

- Con questa azione, Excel rispetta tutti i filtri nella pagina che limitano i record visualizzati. Ciò significa che la cartella di lavoro Excel conterrà le stesse righe e colonne presenti nella pagina in [!INCLUDE[prodshort](includes/prodshort.md)].

- In Excel è possibile apportare modifiche ai record, ma non ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)]. È possibile salvare le modifiche solo in un file Excel nel computer.

- Questa azione è compatibile con Windows e macOS.

> [!NOTE]
> Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale l'azione **Apri in Excel** è disponibile per impostazione predefinita. Tuttavia, se [!INCLUDE [prodshort](includes/prodshort.md)] in locale è configurato per la modifica dei dati in Excel, l'azione **Apri in Excel** è sostituita dall'azione **Modifica in Excel**.

## <a name="edit-in-excel"></a>Modifica in Excel

- Con questa azione, Excel rispetta la maggior parte dei filtri nella pagina che limitano i record visualizzati. Ciò significa che la cartella di lavoro Excel conterrà quasi gli stessi record e le stesse colonne.

- Il vantaggio dell'azione **Modifica in Excel** è che consente di apportare modifiche ai record in Excel e quindi di ripubblicare le modifiche in [!INCLUDE[prodshort](includes/prodshort.md)].

- È compatibile con Windows ma non con macOS.

Ciò è stato migliorato nella seconda ondata di rilascio del 2019. Per ulteriori informazioni, vedere [Miglioramenti all'integrazione di Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale, l'azione **Modifica in Excel** è disponibile solo se il componente aggiuntivo di Excel è stato configurato dall'amministratore. Gli amministratori che desiderano installare il componente aggiuntivo di Excel possono consultare [Installazione del componente aggiuntivo di Excel per la modifica dei dati di Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Per [!INCLUDE[prodshort](includes/prodshort.md)] in locale, questa funzione è disponibile solo per il client Web.

### <a name="see-the-differences-between-the-options"></a>Vedere le differenze tra le opzioni
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Utilizzo di Business Central](ui-work-product.md)  

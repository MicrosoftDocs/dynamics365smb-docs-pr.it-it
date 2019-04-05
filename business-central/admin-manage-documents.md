---
title: Gestire, eliminare o comprimere documenti | Microsoft Docs
description: Conservare i dati storici o eliminarli.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 5cc49d8b17a56c8f19926cf33e63467005d4788c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802254"
---
# <a name="manage-documents"></a>Gestione dei documenti
Un ruolo centrale, ad esempio l'amministratore dell'applicazione, deve occuparsi regolarmente dell'accumularsi dei documenti storici, eliminandoli o comprimendoli.  

## <a name="delete-documents"></a>Eliminare documenti
In certe situazioni, si ha la necessità di eliminare degli ordini di acquisto fatturati. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica che gli ordini di acquisto eliminati siano stati completamente fatturati. Non è possibile eliminare ordini che non siano stati completamente fatturati e ricevuti.  

Gli ordini di reso sono in genere eliminati dopo la fatturazione. Quando si registra una fattura, viene trasferita nella pagina **Note credito acq. registrate** . Se si seleziona la casella di controllo **Spediz. resi in nota credito** nella pagina **Setup contabilità fornitori**, la fattura viene trasferita nella pagina **spedizione reso registrata**. È possibile eliminare i documenti mediante il processo batch **Rimuovi ordini resi acq. fatt.** . Prima di eliminarli, il processo batch verifica se gli ordini di reso acquisto sono completamente spediti e fatturati.  

Gli ordini di acquisto programmati non vengono eliminati dopo aver elaborato e fatturato tutti gli ordini di acquisto correlati. È possibile eliminare ordini programmati tramite il processo batch **Elimina ordini acq. progr. fatturati**.  

Gli ordini di assistenza fatturati vengono in genere eliminati automaticamente dopo che sono stati completamente fatturati. Quando si registra una fattura, viene creato un movimento corrispondente nella pagina **Fatture assistenza registrate**. Il documento registrato può essere visualizzato nella pagina **Fattura assistenza registrata**.  

Gli ordini di assistenza non vengono, tuttavia, eliminati automaticamente se la quantità totale indicata nell'ordine è stata registrata non dall'ordine stesso, ma dalla pagina **Fattura assistenza**. In questo caso può essere necessario eliminare ordini fatturati che non sono stati eliminati. Per eseguire questa operazione, utilizzare il processo batch **Elimina ordini assistenza fatturati**.  

## <a name="see-also"></a>Vedi anche  
[Amministrazione](admin-setup-and-administration.md)  

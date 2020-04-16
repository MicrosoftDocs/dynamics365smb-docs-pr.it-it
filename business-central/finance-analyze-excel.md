---
title: Utilizzare le sintesi finanziarie in Excel | Microsoft Docs
description: Informazioni su come aprire i rendiconti finanziari in Microsoft Excel da Business Central per una migliore analisi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d20dc2ba62a5b13042fe864963f1d483c383563f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183982"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analisi dei rendiconti finanziari in Microsoft Excel
In [!INCLUDE[d365fin](includes/d365fin_md.md)] è possibile vedere i KPI e ottenere le sintesi dello stato finanziario della società. È inoltre possibile aprire elenchi in Excel e analizzarvi i dati. È inoltre possibile esportare rendiconti finanziari complessi, ad esempio il conto patrimoniale o il conto economico in Excel, analizzare i dati e stampare i report.  

In Gestione ruolo utente Contabile e Manager aziendali è possibile scegliere quali rendiconti finanziari visualizzare in Excel dal menu a discesa nella sezione Report nella barra multifunzione. Quando si sceglie un rendiconto, questo viene aperto in Excel o Excel Online. Un componente aggiuntivo connette i dati a [!INCLUDE[d365fin](includes/d365fin_md.md)]. È tuttavia necessario connettersi con lo stesso account che si utilizza con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Visualizzazione di una panoramica e dei dettagli in Excel
Nella barra multifunzione, scegliere il report di Excel interessato e attendere che venga aperto automaticamente per visualizzare la panoramica che si desidera. In questa versione di [!INCLUDE[d365fin](includes/d365fin_md.md)] sono disponibili i report di Excel seguenti:

- Conto patrimoniale  
- Conto economico  
- Rendiconto flusso di cassa  
- Rendiconto degli utili non distribuiti  
- Scadenziario fornitori  
- Scadenziario clienti  

Si supponga di voler analizzare meglio il flusso di cassa. Nella Gestione ruolo utente Contabile o Manager aziendale, è possibile aprire il report Rendiconto flusso di cassa in Excel, ma ciò che avviene realmente è che vengono esportati i dati pertinenti e viene creata una cartella di lavoro di Excel in base a un modello predefinito. A seconda del browser, potrebbe essere chiesto di salvare o aprire la cartella di lavoro.  

In Excel è disponibile una scheda in cui i dati sono disposti automaticamente nel primo foglio di lavoro. Tutti i dati che sono stati esportati sono inoltre presenti in altri fogli di lavoro in caso di necessità. È possibile stampare il report immediatamente o modificarlo fino a ottenere la sintesi e i dettagli desiderati. Utilizzare il componente aggiuntivo per Excel [!INCLUDE[d365fin](includes/d365fin_md.md)] per filtrare e analizzare ulteriormente i dati.  

## <a name="the-d365fin-excel-add-in"></a>Componente aggiuntivo per Excel [!INCLUDE[d365fin](includes/d365fin_md.md)]
L'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)] include un componente aggiuntivo per Excel. A seconda della sottoscrizione, si viene connessi automaticamente oppure è necessario specificare gli stessi dettagli di accesso che si utilizzano per [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Tramite il componente aggiuntivo è possibile ottenere dati aggiornati da [!INCLUDE[d365fin](includes/d365fin_md.md)], e importare nuovamente le modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tuttavia, la funzionalità che consente di importare nuovamente i dati nel database è disattivata per i report finanziari di Excel nell'elenco precedente.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di Business Central](ui-work-product.md)  

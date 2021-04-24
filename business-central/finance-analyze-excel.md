---
title: Utilizzare le sintesi finanziarie in Excel
description: Informazioni su come aprire i rendiconti finanziari in Microsoft Excel da Business Central per una migliore analisi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 69aaeb21bec95d41aab338caa3013a0947de9ef9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780884"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analisi dei rendiconti finanziari in Microsoft Excel

In [!INCLUDE [prod_short](includes/prod_short.md)] è possibile vedere i KPI e ottenere le sintesi dello stato finanziario della società. È inoltre possibile aprire elenchi in Excel e analizzarvi i dati. È inoltre possibile esportare rendiconti finanziari complessi, ad esempio il conto patrimoniale o il conto economico in Excel, analizzare i dati e stampare i report.  

In Gestione ruolo utente Contabile e Manager aziendali è possibile scegliere quali rendiconti finanziari visualizzare in Excel dal menu a discesa nella sezione Report nella barra multifunzione. Quando si sceglie un rendiconto, questo viene aperto in Excel o Excel Online. Un componente aggiuntivo connette i dati a [!INCLUDE [prod_short](includes/prod_short.md)]. È tuttavia necessario connettersi con lo stesso account che si utilizza con [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Visualizzazione di una panoramica e dei dettagli in Excel

Nella barra multifunzione, scegliere il report di Excel interessato e attendere che venga aperto automaticamente per visualizzare la panoramica che si desidera. In questa versione di [!INCLUDE [prod_short](includes/prod_short.md)] sono disponibili i report di Excel seguenti:

- Conto patrimoniale  
- Conto economico  
- Rendiconto flusso di cassa  
- Rendiconto degli utili non distribuiti  
- Scadenziario fornitori  
- Scadenziario clienti  

Si supponga di voler analizzare meglio il flusso di cassa. Nella Gestione ruolo utente Contabile o Manager aziendale, è possibile aprire il report **Rendiconto flusso di cassa** in Excel, ma ciò che avviene realmente è che vengono esportati i dati pertinenti e viene creata una cartella di lavoro di Excel in base a un modello predefinito. A seconda del browser, potrebbe essere chiesto di salvare o aprire la cartella di lavoro.  

In Excel è disponibile una scheda in cui i dati sono disposti automaticamente nel primo foglio di lavoro. Tutti i dati che sono stati esportati sono inoltre presenti in altri fogli di lavoro in caso di necessità. È possibile stampare il report immediatamente o modificarlo fino a ottenere la sintesi e i dettagli desiderati. Utilizzare il componente aggiuntivo per Excel [!INCLUDE [prod_short](includes/prod_short.md)] per filtrare e analizzare ulteriormente i dati.  

### <a name="understanding-the-excel-templates"></a>Comprendere i modelli di Excel

I report di Excel predefiniti si basano sui dati dell'azienda attuale. Ad esempio, la società di dimostrazione ha impostato il piano dei conti per elencare tre conti di cassa sotto *Cespiti correnti* : 10100 **Conto assegni**, 10200 **Conto di risparmio** e 10300 **Piccola cassa**. I conti hanno il campo **Sottocategoria conto** impostato su *Cassa* e l'importo combinato che viene visualizzato come *Cassa* nel report di Excel **Conto patrimoniale**.  

Fogli aggiuntivi nella cartella di lavoro di Excel mostrano i dati utilizzati per il report. Tuttavia per scoprire cosa si nasconde dietro i raggruppamenti nei report di Excel, potrebbe essere necessario tornare a [!INCLUDE [prod_short](includes/prod_short.md)] e ad esempio applicare i filtri agli elenchi.  

## <a name="the-prod_short-excel-add-in"></a>Componente aggiuntivo per Excel [!INCLUDE [prod_short](includes/prod_short.md)]

L'esperienza [!INCLUDE [prod_short](includes/prod_short.md)] include un componente aggiuntivo per Excel. A seconda della sottoscrizione, si viene connessi automaticamente oppure è necessario specificare gli stessi dettagli di accesso che si utilizzano per [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Visualizzare e modificare in Excel da Business Central](across-work-with-excel.md).  

Tramite il componente aggiuntivo è possibile ottenere dati aggiornati da [!INCLUDE [prod_short](includes/prod_short.md)], e importare nuovamente le modifiche in [!INCLUDE [prod_short](includes/prod_short.md)]. Tuttavia, la funzionalità che consente di importare nuovamente i dati nel database è disattivata per i report finanziari di Excel nell'elenco precedente.  

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Visualizzare e modificare in Excel da Business Central](across-work-with-excel.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Utilizzo di Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
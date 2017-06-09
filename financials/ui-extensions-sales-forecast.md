---
title: Previsione vendite e magazzino | Documenti Microsoft
description: Fornisce informazioni sull&quot;estensione Sales and Inventory Forecast.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ebaea8b98264e981f9ad2e0abda592e2e4a72427
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a>Previsione vendite e magazzino per Dynamics 365 for Financials
La Gestione del magazzino è un trade-off tra l'assistenza clienti e la gestione dei costi. Da un lato, un magazzino basso richiede meno capitale di lavoro, ma dall'altro un magazzino in esaurimento potenzialmente porta a vendite mancate. L'estensione Previsione vendite e magazzino prevede le vendite potenziali utilizzando i dati storici e fornisce una chiara panoramica delle scorte esaurite previste. A seconda della previsione, l'estensione consente di creare le richieste di approvvigionamento per i fornitori e quindi di risparmiare tempo.  

## <a name="setting-up-forecasting"></a>Impostazione delle previsioni
In [!INCLUDE[d365fin](includes/d365fin_md.md)] la connessione a [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) è già impostata. Tuttavia è possibile configurare la previsione per utilizzare un tipo diverso del periodo per il report, ad esempio cambiare dalle previsioni in base al mese alle previsioni in base al trimestre. È inoltre possibile scegliere il numero di periodi per calcolare la previsione, a seconda dei dettagli si desidera includere nella previsione. Si suggerisce di effettuare una previsione in base al mese e con un orizzonte di 12 mesi.  

## <a name="using-the-forecasts"></a>Uso delle previsioni
L'estensione utilizza Cortana Intelligence per stimare le vendite future in base allo storico delle vendite allo scopo di evitare l'insufficienza di scorte. Ad esempio, quando si sceglie un articolo nella finestra **Articoli**, nel grafico **Previsione articolo** vengono visualizzate le vendite stimate dell'articolo nel periodo futuro. In questo modo è possibile vedere se si stanno per esaurire le scorte dell'articolo.  

È inoltre possibile utilizzare l'estensione per suggerire quando rifornire il magazzino. Ad esempio, se si crea un ordine di acquisto per Fabrikam perché si desidera acquistare la loro nuova sedia da scrittorio, l'estensione Previsione vendite e magazzino suggerisce anche di rifornirsi della poltrona girevole LONDRA che in genere viene acquistata da questo fornitore. Ciò avviene in quanto l'estensione prevede che le scorte della poltrona girevole LONDRA si esauriranno nel prossimo bimestre e pertanto è possibile che si desideri ordinare già da ora altre sedie.  

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  


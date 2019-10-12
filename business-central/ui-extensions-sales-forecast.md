---
title: Utilizzo delle previsioni di vendita e magazzino per gestire magazzino | Documenti Microsoft
description: Questa estensione consente di effettuare previsioni relative alle vendite, offre una chiara panoramica del magazzino in esaurimento e consente di creare richieste di approvvigionamento per i fornitori.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 9b5cf95eb076a365dfefa318f990b944a4c458d2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315393"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>Estensione Previsione vendite e magazzino
La Gestione del magazzino è un trade-off tra l'assistenza clienti e la gestione dei costi. Da un lato, un magazzino basso richiede meno capitale di lavoro, ma dall'altro un magazzino in esaurimento potenzialmente porta a vendite mancate. L'estensione Previsione vendite e magazzino prevede le vendite potenziali utilizzando i dati storici e fornisce una chiara panoramica delle scorte esaurite previste. A seconda della previsione, l'estensione consente di creare le richieste di approvvigionamento per i fornitori e quindi di risparmiare tempo.  

## <a name="setting-up-forecasting"></a>Impostazione delle previsioni
In [!INCLUDE[d365fin](includes/d365fin_md.md)], la connessione a [Azure AI](https://azure.microsoft.com/en-us/overview/ai-platform/) è già impostata. Tuttavia è possibile configurare la previsione per utilizzare un tipo diverso del periodo per il report, ad esempio cambiare dalle previsioni in base al mese alle previsioni in base al trimestre. È inoltre possibile scegliere il numero di periodi per calcolare la previsione, a seconda dei dettagli si desidera includere nella previsione. Si suggerisce di effettuare una previsione in base al mese e con un orizzonte di 12 mesi.  

## <a name="using-the-forecasts"></a>Uso delle previsioni
L'estensione utilizza Azure AI per stimare le vendite future in base allo storico delle vendite allo scopo di evitare l'insufficienza di scorte. Ad esempio, quando si sceglie un articolo nella pagina **Articoli**, nel grafico **Previsione articolo** vengono visualizzate le vendite stimate dell'articolo nel periodo futuro. In questo modo è possibile vedere se si stanno per esaurire le scorte dell'articolo.  

È inoltre possibile utilizzare l'estensione per suggerire quando rifornire il magazzino. Ad esempio, se si crea un ordine di acquisto per Fabrikam perché si desidera acquistare la loro nuova sedia da scrittorio, l'estensione Previsione vendite e magazzino suggerisce anche di rifornirsi della poltrona girevole LONDRA che in genere viene acquistata da questo fornitore. Ciò avviene in quanto l'estensione prevede che le scorte della poltrona girevole LONDRA si esauriranno nel prossimo bimestre e pertanto è possibile che si desideri ordinare già da ora altre sedie.  

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Magazzino](inventory-manage-inventory.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  

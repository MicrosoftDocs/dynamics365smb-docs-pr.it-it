---
title: Impostare la manutenzione cespiti| Documenti Microsoft
description: Per gestire la riparazione e l'assistenza del cespite, specificare le informazioni di manutenzione generali, i codici per il tipo di lavoro e un conto registrazione per i costi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7fa3763f50549d418b0189604c170448b70c01b9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "800953"
---
# <a name="set-up-fixed-asset-maintenance"></a>Per impostare la manutenzione cespiti
Per gestire la manutenzione dei cespiti, è prima necessario impostare alcune informazioni generali di manutenzione, un conto analitico per i costi di manutenzione e i codici di manutenzione per i tipi di lavoro, ad esempio assistenza di routine o riparazione.

## <a name="to-set-up-general-maintenance-information"></a>Per impostare le informazioni generali di manutenzione
Se vengono impostati campi per la manutenzione è possibile registrare le spese di manutenzione dalla registrazione cespiti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.
2. Selezionare il cespite per cui si desidera definire la copertura assicurativa, quindi scegliere l'azione **Modifica**.
3. Compilare i campi appropriati nella Scheda dettaglio **Manutenzione**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Per impostare i codici di manutenzione
Quando si registrano dei costi di manutenzione dalle registrazioni COGE, si compila il campo **Cod. manutenzione** per registrare il tipo di manutenzione eseguita, ad esempio assistenza di routine o riparazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Manutenzione** e quindi scegliere il collegamento correlato.
2. Nella pagina **Manutenzione**, impostare i codici per i diversi tipi di lavoro di manutenzione.

## <a name="to-set-up-maintenance-expense-accounts"></a>Per impostare i conti spesa manutenzione
Per registrare i costi di manutenzione occorre prima immettere un numero di conto nella pagina **Cat. Reg. Cespite**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie registrazione cespiti** e quindi scegliere il collegamento correlato.
2. Compilare il campo **Conto Spesa Manutenzione** per ogni categoria di registrazione.

> [!NOTE]  
>   Per definire che i costi di manutenzione vengano allocati ai reparti o ai progetti, impostare le chiavi di allocazione. Per ulteriori informazioni, vedere [Impostare le funzionalità generali per i cespiti](fa-how-setup-general.md).

## <a name="see-also"></a>Vedi anche
[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Finanze](finance.md)  
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

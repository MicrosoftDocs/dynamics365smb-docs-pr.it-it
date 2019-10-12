---
title: "Procedura: Impostazione dell'ammortamento compresso dei cespiti"
description: È possibile comprimere l'ammortamento dei cespiti in sottoclassi e decidere di visualizzare solo la somma totale per sottoclasse.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 62c585e443bb66e477b8295a9e2b2105a196a7d3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301297"
---
# <a name="set-up-compressed-depreciation-of-fixed-assets"></a>Impostazione dell'ammortamento compresso dei cespiti
È possibile comprimere l'ammortamento dei cespiti in sottoclassi e decidere di visualizzare solo la somma totale per sottoclasse. È possibile decidere di registrare solo i totali di ammortamento raggruppati per categoria. Questo è particolarmente importante per le società che dispongono di più cespiti suddivisi in molti articoli singoli.  

Durante il calcolo dell'ammortamento, viene generata una riga per ogni cespite. Ad esempio, se si registrano gli ammortamenti per 100 cespiti, vengono generate 100 righe che vengono registrate sia nella contabilità generale che nei movimenti contabili cespiti.  

## <a name="to-set-up-compressed-depreciation-of-fixed-assets"></a>Per impostare l'ammortamento compresso dei cespiti  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registri beni ammortizz.**, quindi scegliere il collegamento correlato.  
2.  Nella pagina **Lista reg. reni ammortizz.**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Modifica**.  
3.  Per registrare solo i totali dell'ammortamento delle risorse raggruppate per categoria, nella pagina **Scheda registro beni ammortizz.**, nella Scheda dettaglio **Generale**, selezionare la casella di controllo **Raggruppa scritture amm.**.  

    > [!NOTE]  
    >  Verranno compresse più righe di ammortamento nella contabilità generale e visualizzate in un unico movimento suddiviso per categorie di cespiti.  

4.  Scegliere il pulsante **OK**.  

## <a name="see-also"></a>Vedi anche  
 [Impostare l'ammortamento dei cespiti](../../fa-how-setup-depreciation.md)   
 [Cespiti italiani](italian-fixed-assets.md)   
 [Impostare metodi di ammortamento alternativi](how-to-set-up-alternate-depreciation-methods.md)   
 [Creare più schede cespite](how-to-create-multiple-fixed-asset-cards.md)   
 [Stampare report dei registri dei beni ammortizzabili](how-to-print-depreciation-book-reports.md)

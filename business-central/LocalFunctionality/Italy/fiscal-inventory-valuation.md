---
title: Valutazione magazzino fiscale
description: È necessario inviare un report annuale che indichi il valore monetario degli articoli di magazzino per l'anno fiscale.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e170cae333f569cde5775dc4b3a0adef9b965354
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747497"
---
# <a name="fiscal-inventory-valuation"></a>Valutazione magazzino fiscale
È necessario inviare un report annuale che indichi il valore monetario degli articoli di magazzino per l'anno fiscale. A seconda dei requisiti italiani per la valutazione del magazzino fiscale, è necessario calcolare i seguenti tipi di costi:  

- Costo medio annuale  
- Costo medio ponderato  
- Costo FIFO (First-In-First-Out)  
- Costo LIFO (Last-In-First-Out)  
- Costo LIFO discreto  

## <a name="fiscal-inventory-valuation-in-prod_short"></a>Valutazione magazzino fiscale in [!INCLUDE[prod_short](../../includes/prod_short.md)]  
Inizialmente, è necessario impostare la valutazione magazzino fiscale per tutti i tipi di costo nella pagina **Setup costing articolo** e nella pagina **Scheda articolo**. Per ulteriori informazioni, vedere [Impostare la valutazione magazzino fiscale](how-to-set-up-fiscal-inventory-valuation.md).  

Quando si imposta [!INCLUDE[prod_short](../../includes/prod_short.md)], è necessario immettere i movimenti contabili del magazzino per il primo anno per calcolare la valutazione dell'articolo. È possibile effettuare questa operazione nella pagina Costo articolo prima dell'inizio.  

Per calcolare il costo LIFO discreto, è necessario impostare le informazioni nella pagina **Scheda articolo** e nella pagina **Prezzi Conto Lavoro**.

> [!NOTE]  
>  Il costo LIFO discreto può essere calcolato solo per gli articoli per i quali il campo **Valutazione magazzino** è impostato su **LIFO discreto** nella pagina **Scheda articolo**.

Dopo aver impostato il calcolo del costo LIFO discreto, è possibile registrare le transazioni di vendita e acquisto basate sui costi di fine anno.  

## <a name="end-of-year"></a>Fine anno  
 Alla fine dell'anno fiscale, è possibile eseguire il processo batch Calcola costi fine anno per calcolare il valore del magazzino fiscale di ogni articolo di magazzino in base ai metodi di valutazione richiesti. I risultati sono visualizzati nella pagina Lista storico costo articolo. Quindi, è possibile eseguire il report **Valutazione fiscale magazzino** e il report **Valutazione LIFO** per visualizzare la valutazione del magazzino.  

 Per le operazioni di fine anno, come il calcolo di profitti e delle perdite in un anno fiscale, esiste un periodo definitivo e un periodo non definitivo. Se il campo **Anno di competenza** della pagina **Lista storico costo articolo** è uguale alla data di fine dell'anno fiscale, è un periodo definitivo e non è possibile ricalcolare i dati per un periodo definitivo. Se i dati definitivi differiscono dalla data di fine dell'anno fiscale, si tratta di un periodo non definitivo. Per eseguire calcoli o calcoli parziali è necessario disporre dei dati relativi ad almeno un periodo non definitivo.

## <a name="see-also"></a>Vedi anche  
 [Funzionalità locale per l'Italia](italy-local-functionality.md)   
 [Impostare la valutazione magazzino fiscale](how-to-set-up-fiscal-inventory-valuation.md)   
 [Impostare i costi iniziali per gli articoli](how-to-set-up-initial-item-costs.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
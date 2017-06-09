---
title: 'Procedura: Registrare i prezzi di acquisto e gli sconti speciali | Documenti Microsoft'
description: 'Procedura: Registrare i prezzi di acquisto e gli sconti'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Procedura: Registrare i prezzi di acquisto e gli sconti speciali
I differenti accordi relativi a prezzi e sconti applicati quando si effettuano acquisti da fornitori diversi devono essere definiti in modo che le regole e i valori concordati vengano applicati ai documenti di acquisto creati per il fornitore.

Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino. Per ulteriori informazioni, vedere [Avanzate: Calcolo del prezzo migliore](advanced-best-price-calculation.md).

Per quanto riguarda i prezzi, è possibile fare in modo che venga inserito un prezzo di acquisto speciale nelle righe di acquisto quando si verifica una determinata combinazione di fornitore, articolo, quantità minima, unità di misura o data di inizio o di fine.

Nel caso degli sconti, è possibile impostare e utilizzare due tipi di sconti:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto riga acquisto** |È possibile fare in modo che venga inserito uno sconto sull'importo nelle righe di acquisto quando si verifica una determinata combinazione di fornitore, articolo, quantità minima, unità di misura o data di inizio o di fine. Il principio è lo stesso dei prezzi di acquisto. |
| **Sconto fattura** |Uno sconto in percentuale che viene sottratto dal totale del documento se l'importo del valore di tutte le righe di un documento di acquisto supera un determinato valore minimo. |

Poiché gli sconti riga acquisto e i prezzi di acquisto sono basati su una combinazione di articolo e fornitore, è anche possibile immettere questa configurazione dalla scheda articolo, in cui sono definiti le regole e i valori. Per ulteriori informazioni, vedere [Procedura: Registrare nuovi articoli](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Per impostare un prezzo di acquisto speciale per un fornitore
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Fornitori**, quindi scegliere il collegamento correlato.
2. Aprire la scheda fornitore interessata e scegliere l'azione **Prezzi**.

    Il campo **Tipo di acquisto** è già impostato su **Fornitore** e il campo **Codice acquisto** è impostato sul numero del fornitore.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Compilare una riga per ogni combinazione per la quale il fornitore concede uno sconto riga acquisto.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Per impostare uno sconto riga per un fornitore
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Fornitori**, quindi scegliere il collegamento correlato.
2. Aprire la scheda fornitore interessata e scegliere l'azione **Sconti riga**.

    Il campo **Tipo di acquisto** è già impostato su **Fornitore** e il campo **Codice acquisto** è impostato sul numero del fornitore.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Compilare una riga per ogni combinazione per la quale il fornitore concede uno sconto riga acquisto.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Per impostare uno sconto su fattura per un fornitore
Una volta informati degli sconti su fattura concessi dai fornitori, immettere il codice sconto fattura nelle schede fornitore e impostare le condizioni per ciascun codice.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Fornitori**, quindi scegliere il collegamento correlato.
2. Aprire la scheda fornitore relativa al fornitore al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il fornitore.

    **Nota**: i codici sconto fattura sono rappresentati da schede fornitore esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai fornitori perché basterà selezionare il nome di un altro fornitore che avrà le stesse condizioni.

    Continuare a impostare le nuove condizioni dello sconto fattura di acquisto.
4. Nella finestra **Scheda fornitore** scegliere l'azione **Sconti fattura**. Verrà visualizzata la finestra **Sconti fattura fornitori**.
5. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
6. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
7. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
8. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il fornitore riceverà uno sconto fattura diverso.

Lo sconto fattura è ora impostato e assegnato al fornitore in questione. Quando si seleziona il codice fornitore nel campo **Cod. sconto fatt.** nelle altre schede fornitore, lo stesso sconto fattura viene assegnato a quei fornitori.

## <a name="see-also"></a>Vedi anche
[Avanzate: Calcolo del prezzo migliore](advanced-best-price-calculation.md)  
[Impostazioni acquisti](purchasing-setup-purchasing.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


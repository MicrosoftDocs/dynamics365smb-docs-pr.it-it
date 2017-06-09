---
title: 'Procedura: Registrare i prezzi di vendita e gli sconti speciali | Documenti Microsoft'
description: 'Procedura: Registrare i prezzi di vendita e gli sconti speciali'
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
ms.openlocfilehash: 5ceddded2f95e15a6a7449bf2776b7776ce8a55c
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Procedura: Registrare i prezzi di vendita e gli sconti speciali
È necessario definire i diversi criteri di prezzo e di sconto applicati alle transazioni di vendita ai diversi clienti affinché vengano applicati le regole e i valori concordati ai documenti di vendita creati per i clienti.

Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino. Per ulteriori informazioni, vedere [Avanzate: Calcolo del prezzo migliore](advanced-best-price-calculation.md).

Per quanto riguarda i prezzi, è possibile fare in modo che venga inserito un prezzo di vendita speciale nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine.

Nel caso degli sconti, è possibile impostare e utilizzare due tipi di sconti su vendita:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto Riga Vendita** |È possibile fare in modo che venga inserito uno sconto sull'importo nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine. Il principio è lo stesso dei prezzi di vendita. |
| **Sconto fattura** |Uno sconto in percentuale che viene sottratto dal totale del documento se l'importo del valore di tutte le righe di un documento di vendita supera un determinato valore minimo. |

Poiché i prezzi di vendita e gli sconti riga di vendita si basano su una combinazione di articolo e cliente, è altresì possibile eseguire questa configurazione dalla scheda articolo dello specifico articolo, dove si applicano regole e valori.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Per impostare un prezzo di vendita per un cliente
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Clienti**, quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Prezzi**.

    Il campo **Tipo vendita** viene precompilato con **Cliente** e il campo **Codice vendita** viene precompilato con il numero del cliente.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà un prezzo di vendita speciale al cliente.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Per impostare uno sconto riga vendita per un cliente
1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Clienti**, quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Sconti riga**.

    Il campo **Tipo vendita** viene precompilato con **Cliente** e il campo **Codice vendita** viene precompilato con il numero del cliente.
3. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà uno sconto riga vendita al cliente.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Per impostare uno sconto su fattura per un cliente
Dopo avere stabilito a quali clienti si debbano applicare gli sconti fattura, è necessario immettere i codici di sconto fattura nelle schede clienti e impostare le condizioni relative ai singoli codici.

1. Nell'angolo superiore destro scegliere l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), inserire **Clienti**, quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente relativa al cliente al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il cliente.

    **Nota**: i codici sconto fattura sono rappresentati da schede clienti esistenti. Questo consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni.

    Continuare a impostare le nuove condizioni dello sconto fattura di vendita.
4. Nella finestra **Scheda cliente** scegliere l'azione **Sconti fattura**. Viene aperta la finestra **Sconti fattura clienti**.
5. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
6. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
7. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
8. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

Lo sconto fattura è ora impostato e assegnato al cliente in questione. Quando si seleziona il codice cliente nel campo **Cod. sconto fatt.** nelle altre schede cliente, lo stesso sconto fattura viene assegnato a quei clienti.

## <a name="see-also"></a>Vedi anche
[Avanzate: Calcolo del prezzo migliore](advanced-best-price-calculation.md)  
[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


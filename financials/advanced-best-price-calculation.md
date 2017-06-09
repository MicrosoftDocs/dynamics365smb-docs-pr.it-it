---
title: 'Avanzate: Calcolo del prezzo migliore | Documenti Microsoft'
description: Descrive come l&quot;uso di prezzi speciali e sconti riga assicura che il profitto sia sempre ottimale.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: pricing, sales price
ms.date: 02/08/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e4dbe800abef3fa4afe3eabec3450b6ee0f20080
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="advanced-best-price-calculation"></a>Avanzate: Calcolo del prezzo migliore
Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino.

Con il termine "miglior prezzo" si intende il prezzo più basso ammissibile che gode dello sconto riga più alto possibile praticabile in una specifica data. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente questo prezzo quando inserisce il prezzo unitario e la percentuale di sconto riga per gli articoli in nuove righe di documenti e di registrazione.

**Nota**: di seguito viene descritto come viene calcolato il prezzo migliore per le vendite. Il calcolo è lo stesso per gli acquisti.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla la combinazione del cliente di fatturazione e dell'articolo e quindi calcola il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    - Il cliente usufruisce di uno speciale accordo relativo a prezzi o sconti o appartiene a un gruppo che ne usufruisce?
    - L'articolo o il gruppo sconto articolo specificato nella riga è incluso in uno di tali accordi prezzi o sconti?
    - La data dell'ordine, o la data di registrazione per le fatture e le note di credito, è compresa nell'intervallo di validità dell'accordo prezzi o sconti?
    - È stato specificato un codice unità di misura? In caso affermativo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno controllati i prezzi o gli sconti aventi lo stesso codice di unità di misura, altrimenti verranno verificati prezzi o gli sconti a cui non è associato alcun codice di unità di misura.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se si applicano accordi di prezzo/sconto alle informazioni sul documento o sulla riga di registrazione, quindi inserisce il prezzo unitario e percentuale di sconto della riga, utilizzando i seguenti criteri:

    - C'è un requisito di quantità minima nell'accordo di prezzo/sconto che è soddisfatto?
    - C'è un requisito di valuta nell'accordo di prezzo/sconto che è soddisfatto? In caso affermativo, il prezzo più basso e lo sconto riga più alto per tale valuta vengono immessi, anche se VL fornirebbe un prezzo migliore. Se non esistono accordi prezzi o sconti riga per il codice di valuta specificato, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente selezionati il prezzo più basso e lo sconto riga più alto per la valuta locale.

Se non è possibile calcolare alcun prezzo speciale per l'articolo specificato nella riga, viene recuperato l'ultimo costo diretto o il prezzo unitario dalla scheda articolo immesso.

## <a name="see-also"></a>Vedi anche
[Procedura: Registrare i prezzi di vendita e gli sconti speciali](sales-how-record-sales-price-discount-payment-agreements.md)  
[Procedura: Registrare i prezzi di acquisto e gli sconti speciali](purchasing-how-record-purchase-price-discount-payment-agreements.md)  
[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


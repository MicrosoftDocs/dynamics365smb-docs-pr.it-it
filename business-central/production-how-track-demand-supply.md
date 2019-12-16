---
title: Come tenere traccia delle relazioni tra domanda e approvvigionamento | Microsoft Docs
description: A partire da qualsiasi documento dell'approvvigionamento o della domanda, è possibile tenere traccia della richiesta dell'ordine (quantità tracciata), della previsione, dell'ordine di vendita programmato o del parametro di pianificazione (quantità non tracciata) che ha generato la riga di pianificazione in questione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3d387ebaf9b7c5e20d50f22b0400d3089e973f8b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877713"
---
# <a name="track-relations-between-demand-and-supply"></a>Tenere traccia delle relazioni tra domanda e approvvigionamento
A partire da qualsiasi documento dell'approvvigionamento o della domanda, è possibile tenere traccia della richiesta dell'ordine (quantità tracciata), della previsione, dell'ordine di vendita programmato o del parametro di pianificazione (quantità non tracciata) che ha generato la riga di pianificazione in questione.

I prospetti di pianificazione offrono anche informazioni di supporto alla pianificazione relative a entità non di ordine per consentire al responsabile della pianificazione di ottenere un piano di approvvigionamento ottimale. Per ulteriori informazioni, vedere [Elementi di pianificazione non tracciati](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Per tracciare articoli collegati
Tramite i sistemi di impegno e pianificazione, la funzione di tracciabilità degli ordini consente di conoscere la relazione tra ordini di vendita, di produzione e di acquisto e l'ordine di manufacturing.

Di seguito viene descritto come tenere traccia degli articoli collegati in un ordine di produzione pianificato. I passaggi sono simili per tutti gli altri tipi di ordini e per le righe del prospetto di pianificazione.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordine produzione confermato** e quindi scegliere il collegamento correlato.
2. Aprire l'ordine di produzione confermato appropriato dall'elenco.
3. Nella Scheda dettaglio **Righe** scegliere l'azione **Funzioni**, quindi l'azione **Tracciabilità ordine**.

Nelle righe in **Tracciabilità ordine** vengono visualizzati i documenti collegati alla riga dell'ordine di produzione corrente.

## <a name="untracked-planning-elements"></a>Elementi di pianificazione non tracciati
Quando si sceglie il campo **Qtà non tracciata** nella pagina **Pianificazione ordini**, viene visualizzata la pagina **Elementi di pianificazione non tracciati**. Questa finestra è utilizzate per due scopi:

1. Contenere informazioni sulle quantità non tracciate che vengono visualizzate quando l'utente effettua una ricerca dalla pagina Tracciabilità ordine.
2. Contenere i messaggi di errore visualizzati quando si sceglie un'icona **Avviso** nella pagina **Prospetto pianificazione**.

In questa pagina sono contenuti movimenti che rappresentano una quantità di surplus non tracciata nella rete di tracciabilità dell'ordine. Questi movimenti vengono generati durante l'esecuzione della pianificazione e indicano la provenienza di tale quantità presente nelle righe di tracciabilità dell'ordine. Il surplus non tracciato può derivare dai seguenti elementi:

- Previsione di produzione
- Ordini programmati
- Scorta di sicurezza
- Punto di riordino
- Giacenza massima
- Quantità di riordino
- Quantità massima dell'ordine
- Quantità minima dell'ordine
- Molteplicità dell'ordine
- Smorzamento (percentuale di dimensione del lotto)

## <a name="see-also"></a>Vedi anche  
[Pianif.](production-planning.md)   
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Impegno, tracciabilità e messaggistica di azioni](design-details-reservation-order-tracking-and-action-messaging.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

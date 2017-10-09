---
title: 'Procedura: Abilitare il prelievo in base al metodo FEFO | Documenti Microsoft'
description: "FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 34d6e46146f3072da49cd28e4b4bf1b0f00d1369
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-picking-items-by-fefo"></a>Procedura: Abilitare il prelievo di articoli tramite il metodo FEFO
FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.  

 La funzionalità può essere utilizzata solo quando vengono soddisfatti i seguenti criteri:  

-   L'articolo deve avere un numero seriale o di lotto.  
-   Nel setup del codice di tracciabilità dell'articolo è necessario selezionare il campo **Tracciab. NS in warehouse** o **Tracciab. lotto in warehouse**.  
-   L'articolo deve essere registrato in magazzino con una data di scadenza.  
-   Nella scheda Ubicazione, la casella di controllo **Richiesto prelievo** deve essere selezionata.  
-   Nella scheda ubicazione è necessario selezionare la casella di controllo **Prelievo in base a FEFO**.  
-   Nella scheda Ubicazione, la casella di controllo **Collocazione obbligatoria** deve essere selezionata.  

 Una volta soddisfatti tutti i criteri, gli articoli con numeri seriali/di lotto da prelevare verranno ordinati con i più vecchi per primi in tutti gli prelievi e tutte le movimentazioni, ad eccezione degli articoli che utilizzano la tracciabilità NS specifico o lotto specifico.  

> [!NOTE]  
>  Se alcuni articoli con numeri seriali/di lotto utilizzano la tracciabilità specifica, questi vengono rispettati per primi e quindi vengono elencati i rimanenti numeri seriali/di lotto in base al metodo FEFO.  

 Se due articoli con numeri seriali o di lotto hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore. Se i numeri di lotto o seriali sono identici, viene selezionato automaticamente l'articolo registrato per primo.  

> [!NOTE]  
>  -   Quando si prelevano articoli con numeri di serie o di lotto in ubicazioni impostate per stoccaggi e prelievi guidati, solo le quantità nelle collocazioni di tipo *Prelievo* vengono prelevate in base al metodo FEFO.  
> -   Per abilitare le movimentazioni in base al metodo FEFO, nella finestra **Movimento di magazzino** o **Prospetto movimentazioni**, è necessario lasciare vuoto il campo **Dal codice collocazione**.  
> -   Se il campo **Registrazione scadenza vincolante** è selezionato, solo gli articoli che non sono scaduti verranno inclusi nel prelievo. Ciò si applica anche se non viene utilizzata l'opzione Prelievo in base a FEFO.  

## <a name="see-also"></a>Vedi anche  
[Prelievo di articoli](warehouse-pick-items.md)   
[Procedura: Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Procedura: prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


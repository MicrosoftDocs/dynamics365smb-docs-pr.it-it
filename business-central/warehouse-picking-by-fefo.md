---
title: 'Procedura: Abilitare il prelievo in base al metodo FEFO | Documenti Microsoft'
description: FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 466736905815efb0b013a66fd05854769da24be5
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324008"
---
# <a name="enable-picking-items-by-fefo"></a>Abilitare il prelievo di articoli tramite il metodo FEFO
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
> Se alcuni articoli con numeri seriali/di lotto utilizzano la tracciabilità specifica, questi vengono rispettati per primi e quindi vengono elencati i rimanenti numeri seriali/di lotto in base al metodo FEFO.
<br /><br />
Se due articoli con numeri seriali o di lotto hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore.
<br /><br />
Quando si prelevano articoli con numeri di serie o di lotto in ubicazioni impostate per stoccaggi e prelievi guidati, solo le quantità nelle collocazioni di tipo *Prelievo* vengono prelevate in base al metodo FEFO.  
<br /><br />
Per abilitare le movimentazioni in base al metodo FEFO, nella pagina **Movimento di magazzino** o **Prospetto movimentazioni**, è necessario lasciare vuoto il campo **Dal codice collocazione**.  
<br /><br />
Se il campo **Registrazione scadenza vincolante** è selezionato, solo gli articoli che non sono scaduti verranno inclusi nel prelievo. Ciò si applica anche se non viene utilizzata l'opzione Prelievo in base a FEFO.

## <a name="see-also"></a>Vedi anche  
[Prelievo di articoli](warehouse-pick-items.md)   
[Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

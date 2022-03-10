---
title: 'Procedura: Abilitare il prelievo in base al metodo FEFO | Documenti Microsoft'
description: FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1855391f5bf2c0807ac4ffcd8d42e0ea8122fd87
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141859"
---
# <a name="enable-picking-items-by-fefo"></a>Abilitare il prelievo di articoli tramite il metodo FEFO
FEFO (First-Expired-First-Out) è un metodo di ordinamento che assicura che vengano prelevati per primi gli articoli meno recenti, ovvero quelli con le date di scadenza più prossime.  

 La funzionalità può essere utilizzata solo quando vengono soddisfatti i seguenti criteri:  

-   L'articolo deve avere un numero seriale o di lotto.  
-   Nel setup del codice di tracciabilità dell'articolo è necessario selezionare il campo **Tracciab. NS in warehouse** o **Tracciab. lotto in warehouse**.  
-   L'articolo deve essere registrato in magazzino con una data di scadenza.  
-   Sul posto, i toggle **Richiesto prelievo**, **Prelievo in base a FEFO** e **Collocazione obbligatoria** devono essere attivate.  

 Una volta soddisfatti tutti i criteri, gli articoli con numeri seriali/di lotto da prelevare verranno ordinati con i più vecchi per primi in tutti gli prelievi e tutte le movimentazioni, ad eccezione degli articoli che utilizzano la tracciabilità NS specifico o lotto specifico.  

> [!NOTE]  
> Se alcuni articoli con numeri seriali o di lotto utilizzano la tracciabilità specifica, questi vengono rispettati per primi e quindi vengono elencati i rimanenti numeri seriali/di lotto in base al metodo FEFO.
<br /><br />
Se due articoli con numeri seriali o di lotto hanno la stessa data di scadenza, viene selezionato automaticamente quello con il numero di lotto o seriale inferiore.
<br /><br />
Quando si prelevano articoli con numeri di serie o di lotto in ubicazioni impostate per stoccaggi e prelievi guidati, solo le quantità nelle collocazioni di tipo *Prelievo* vengono prelevate in base al metodo FEFO.  
<br /><br />
Per abilitare le movimentazioni in base al metodo FEFO, lasciare il campo **Dal codice collocazione** vuoto nella pagina **Movimento di magazzino** o nelle pagine **Movimento worksheet**.  
<br /><br />
Se il campo **Registrazione scadenza vincolante** è selezionato in **Scheda cod. tracciab. articolo**, nel prelievo verranno inclusi solo gli articoli non scaduti e le righe verranno ordinate secondo il principio FEFO.

## <a name="see-also"></a>Vedere anche  
[Prelievo di articoli](warehouse-pick-items.md)   
[Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Prelevare articoli con prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Magazzino](inventory-manage-inventory.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
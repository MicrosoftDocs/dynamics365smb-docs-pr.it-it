---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470289"
---
Una volta immessi tutti gli articoli nelle righe vendita, sarà possibile calcolare lo sconto fattura per l'intero documento scegliendo l'azione **Calcola sconto fattura**.

Lo sconto viene calcolato in base a tutte le righe nel documento di vendita per gli articoli per cui il campo **Consenti sconto fattura** della riga dell'ordine di vendita contenga il valore **Sì**. Questa è l'impostazione di default per gli articoli. Le righe con addebiti articolo non vengono ad esempio incluse nel calcolo dello sconto fattura. Se si desidera applicare uno sconto a tali righe, è necessario impostare il campo **% sconto riga** nelle righe pertinenti.  

> [!TIP]
> Se il campo **Calcola sconto fatt.** è selezionato nella pagina **Setup contabilità clienti**, lo sconto fattura viene calcolato automaticamente quando su un documento di vendita si effettua una delle seguenti operazioni:
>
> * Visualizzare statistiche
> * Visualizzare un report di test
> * Stampa
> * Spedizioni postali

Le condizioni di sconto fattura per un cliente vengono definite nella pagina **Sconti fattura clienti** per il cliente. Il codice valuta nel documento di vendita viene utilizzato per identificate le condizioni dello sconto in fattura nella valuta corrispondente.

Se gli sconti fattura non sono stati definiti in valuta estera, per calcolarli vengono usate automaticamente le condizioni di sconto fattura in valuta locale definite nella pagina **Sconti fattura clienti** e il tasso di cambio alla data di registrazione del documento di vendita.

---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035789"
---
Una volta immessi tutti gli articoli nelle righe ordine di vendita, sarà possibile calcolare lo sconto sulla fattura per l'intero documento di vendita scegliendo l'azione **Calcola sconto fattura**.

Se il campo **Calcola sconto fatt.** viene selezionato nella finestra **Setup contabilità clienti**, lo sconto fattura viene calcolato automaticamente quando sul documento di vendita si esegue una delle seguenti operazioni:

* Visualizzare statistiche
* Visualizzare un report di test
* Stampa
* Spedizioni postali

Nei documenti di acquisto di articoli e risorse lo sconto viene distribuito su tutte le righe nel cui campo **Sconto Fattura** sia stato immesso **Sì**. Questa è l'impostazione di default per gli articoli.

Per calcolare lo sconto fattura, si definiscono le condizioni di sconto fattura definite nella pagina **Sconti fattura clienti**. Il codice valuta nel documento di vendita viene utilizzato per identificate le condizioni dello sconto in fattura nella valuta corrispondente.

Se gli sconti fattura non sono stati definiti in valuta estera, per calcolarli vengono usate automaticamente le condizioni di sconto fattura in valuta locale definite nella pagina **Sconti fattura clienti** e il tasso di cambio alla data di registrazione del documento di vendita.

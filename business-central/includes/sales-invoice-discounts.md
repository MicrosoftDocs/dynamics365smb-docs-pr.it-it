---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
---
Una volta aggiunti tutti gli articoli nelle righe, sarà possibile calcolare lo sconto fattura per l'intero documento di vendita scegliendo l'azione **Calcola sconto fattura**.

Lo sconto viene calcolato in base a tutte le righe del documento di vendita in cui viene selezionata la casella di controllo **Sconto fattura**. Per impostazione predefinita, sono consentiti sconti fattura. Tuttavia, le righe con addebiti articolo non vengono ad esempio incluse nel calcolo dello sconto fattura. Per applicare uno sconto a tali righe, immetti un valore nel campo **Importo Sconto Riga** nelle righe.  

> [!NOTE]
> Per impostazione predefinita, i campi **Sconto Fattura** e **Importo Sconto Riga** sono nascosti sulle righe. Se i campi non sono disponibili, puoi aggiungerli personalizzando la pagina. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

> [!TIP]
> Se il campo **Calcola sconto fatt.** nella pagina **Setup contabilità clienti** è selezionato, lo sconto sulla fattura viene calcolato automaticamente. Il momento in cui avviene il calcolo varia a seconda del tipo di documento di vendita che stai utilizzando.
>
> Se stai utilizzando un ordine cliente, lo sconto viene calcolato quando aggiungi una riga. Per tutti gli altri documenti di vendita, come le fatture di vendita, lo sconto viene calcolato quando si esegue una delle seguenti azioni:
>
> * Visualizzare statistiche
> * Visualizzare un report di test
> * Stampa
> * Spedizioni postali

Definisci le condizioni di sconto fattura per un cliente nella pagina **Sconti fattura clienti**. Il codice valuta nel documento di vendita viene utilizzato per identificate le condizioni dello sconto in fattura nella valuta corrispondente.

Se non sono stati definiti sconti fattura per valute estere, le condizioni di sconto nella pagina **Sconti fattura clienti** vengono utilizzate per calcolare lo sconto. Il calcolo utilizza la tua valuta locale e il tasso di cambio valido alla data di registrazione del documento.

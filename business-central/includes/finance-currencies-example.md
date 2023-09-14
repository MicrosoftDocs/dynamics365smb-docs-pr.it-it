---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
---
Quando ricevi una fattura da un'azienda in valuta estera, è abbastanza facile calcolare il valore in valuta locale (VL) della fattura in base al tasso di cambio corrente. Tuttavia, la fattura spesso viene fornita con termini di pagamento in modo da poter ritardare il pagamento a una data successiva, il che implica un tasso di cambio potenzialmente diverso. Questo problema, in combinazione con il fatto che i tassi di valuta bancaria differiscono sempre dai tassi di valuta ufficiali, rende impossibile anticipare l'importo esatto in valuta locale (VL) richiesto per coprire la fattura. Se la data di scadenza della fattura si estende al mese successivo, potrebbe essere necessario rivalutare l'importo in valuta locale (VL) alla fine del mese. La rettifica della valuta è necessaria perché il nuovo valore VL richiesto per coprire l'importo della fattura potrebbe essere diverso e il debito della società nei confronti del fornitore è potenzialmente cambiato. Il nuovo importo VL potrebbe essere superiore o inferiore all'importo precedente e rappresenta quindi un guadagno o una perdita. Tuttavia, poiché la fattura non è stata ancora pagata, si considera l'utile o la perdita come *non realizzati*. Successivamente, la fattura viene pagata e la banca restituisce il tasso di cambio effettivo per il pagamento. Fino ad allora l'utile o la perdita *realizzati* non vengono calcolati. L'utile o la perdita non realizzati vengono quindi stornati e al loro posto vengono registrati l'utile o la perdita realizzati.

Nell'esempio seguente, il 1° gennaio viene ricevuta una fattura con l'importo in valuta di 1000. Al momento il tasso di cambio è 1,123.

|Date|Azione|Importo valuta|Aliquota documento|Importo LCY nel documento|Tasso di cambio|Importo utili non realizzati|Aliquota Pagamento|Importo perdite realizzate|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fattura**|1000|1,123|1123|||||
|1/31|**Rettifica**|1000||1125|1,125|2|||
|2/15|**Rettifica Storno al pagamento**|1000||||-2|||
|2/15|**Pagamento**|1000||1120|||1,120|-3|

Alla fine del mese viene eseguito un aggiustamento valutario in cui il tasso di valuta aggiustamento è stato impostato a 1,125, che attiva un guadagno non realizzato di 2.

Al momento del pagamento, il tasso di cambio effettivo registrato sulla transazione bancaria mostra un tasso di valuta di 1,120.

Qui c'è una transazione non realizzata, e quindi verrà stornata insieme al pagamento.

Infine, il pagamento viene registrato e la perdita effettiva viene registrata nel conto delle perdite realizzate.

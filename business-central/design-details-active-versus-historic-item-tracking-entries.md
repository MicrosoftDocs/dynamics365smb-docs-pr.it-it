---
title: Dettagli di progettazione - Movimenti di tracciabilità articolo storici e attivi
description: 'Quando vengono registrate parti di una quantità di una riga documento, solo quella quantità viene trasferita ai movimenti contabili articoli e ai relativi numeri di tracciabilità articolo.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Dettagli di progettazione: Movimenti di tracciabilità articolo storici e attivi
Quando vengono registrate parti di una quantità di una riga documento, solo quella quantità in questione viene trasferita ai movimenti contabili articoli e ai relativi numeri di tracciabilità articolo. Tuttavia, è opportuno accedere a tutte le informazioni rilevanti di tracciabilità articoli direttamente dalla riga del documento attivo. Ovvero non solo si desidererà vedere i movimenti che sono correlati alla quantità residua, ma si vorranno anche informazioni sulle unità che sono state registrate. Quando si visualizza o si modifica la pagina **Righe tracciabilità articolo**, i contenuti collettivi delle tabelle **Specifica tracciabilità** (T336) e **Movimenti impegni** (T337) vengono presentati in una versione temporanea di T336. In questo modo si garantisce l'accesso unico ai dati di tracciabilità articolo attivi e storici.  

 Nella seguente tabella viene mostrato come T336 e T337 vengono utilizzati in uno scenario di acquisto. Le cifre in grassetto rappresentano i valori che l'utente immette manualmente nella pagina **Righe tracciabilità articolo**.  

 Passaggio 1: Creare una riga di ordine di acquisto di sette pezzi con numeri di tracciabilità articolo.  

||**Quantità (base)**|**Qtà da gestire**|**Qtà da fatturare (base)**|**Quantità gestita (base)**|**Quantità fatturata (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Passaggio 2: Ricevere quattro pezzi.  

||**Quantità (base)**|**Qtà da gestire**|**Qtà da fatturare (base)**|**Quantità gestita (base)**|**Quantità fatturata (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Pagina **Righe tracciabilità articolo**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Passaggio 3: Ricevere due pezzi e fatturare due pezzi.  

||**Quantità (base)**|**Qtà da gestire**|**Qtà da fatturare (base)**|**Quantità gestita (base)**|**Quantità fatturata (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Pagina **Righe tracciabilità articolo**|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Passaggio 4: Ricevere un pezzo.  

||**Quantità (base)**|**Qtà da gestire**|**Qtà da fatturare (base)**|**Quantità gestita (base)**|**Quantità fatturata (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Pagina **Righe tracciabilità articolo**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fatturare 5 pezzi.  

||**Quantità (base)**|**Qtà da gestire**|**Qtà da fatturare (base)**|**Quantità gestita (base)**|**Quantità fatturata (base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Pagina **Righe tracciabilità articolo**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Vedi anche
 [Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)   
 [Dettagli di progettazione: Pagina righe tracciabilità articolo](design-details-item-tracking-lines-window.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

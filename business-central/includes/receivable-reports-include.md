---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e75327e1c87af593d8e3f7e4f95e74349fb3a63c
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104154"
---
La tabella seguente descrive alcuni dei report di contabilità clienti.

| Report | ID oggetto | Descrizione |
|--|--|--|
| **Scadenzari clienti** | 120 | Mostra l'importo in sospeso dei clienti, suddiviso in intervalli di tempo per il tempo scaduto. Il report visualizza anche la parte del saldo dei clienti che non è dovuta e può essere visualizzata con o senza i dettagli del documento per ciascun cliente. Questo report è il report principale per la riconciliazione della contabilità clienti con la contabilità generale. Supponendo che non sia stata consentita la registrazione diretta nei conti utilizzati nel conto crediti delle categorie di registrazione clienti, questo report è una specifica degli importi presenti nella contabilità generale. |
| **Rendiconto cliente** | 1316 | Genera un rendiconto cliente per un intervallo di tempo specificato. Di solito viene inviato ai clienti per fornire loro una panoramica degli importi in sospeso e anche come promemoria per il pagamento di eventuali importi scaduti. Puoi scegliere di mostrare gli importi scaduti in una sezione separata. È possibile includere un periodo scadenzario simile a quello utilizzato nel report **Scadenzari clienti**. Per il periodo scadenzario, di solito si imposta *30G*, che significa intervalli di 30 giorni come 30, 60, 90 e 90+ giorni di ritardo, dalla data di fine, o *1M+CM*, che sarà il corrente mese in un intervallo separato e gli intervalli mensili per i mesi precedenti. **Nota**: nella lista clienti, questo report ha anche un'azione separata, **Rendiconti programmati**. Questa opzione non si applica al cliente selezionato. È lo stesso report ma utilizzato quando vuoi inviare un estratto conto a tutti o più clienti. |
| **Cliente - Saldo alla data** | 121 | Mostra i movimenti contabili clienti aperti fino alla data di fine. Questo report mostra un contenuto simile all'estratto conto del cliente, ma non indica se il movimento è scaduto. **Nota**: il filtro data verrà applicato ai movimenti contabili dettagliati dei clienti. Pertanto se hai pagamenti successivi alla data di fine che sono stati applicati alle fatture entro l'intervallo di date, le fatture verranno visualizzate nel report in quanto non sono state chiuse entro la data di fine. |
| **Clienti - Bilancio di verifica** | 129 | Mostra i saldi periodi per i clienti per il periodo specificato nel filtro data, nonché il saldo periodo da inizio anno per l'anno fiscale corrispondente al periodo selezionato. Il report è raggruppato per categorie di registrazione clienti e fornirà una vista diversa della contabilità clienti rispetto al report **Scadenziario clienti**. **Nota**: Se non è stato impostato alcun periodo contabile, il sistema non saprà quale anno fiscale utilizzare e mostrerà l'anno in corso dall'ultimo anno fiscale definito o selezionerà semplicemente il periodo, che può essere o meno dall'inizio di un anno.|
| **Cliente - Dett. bilancio di verifica** | 104 | Mostra tutti i movimenti contabili clienti all'interno del filtro data specificato. Questo report viene generalmente utilizzato per verificare che tutti i movimenti per un cliente specifico siano contabilizzati o per altri controlli interni sui libri contabili dei clienti. |
| **Clienti - Ricevuta di pagamento** | 211 | Crea una ricevuta di pagamento per ogni movimento contabile cliente di tipo **Pagamento**. Se il pagamento è stato applicato alle fatture, verranno specificate le fatture; in caso contrario, indicherà semplicemente l'importo del pagamento come non applicato. Questo report viene utilizzato per inviare ai clienti che desiderano la documentazione della ricevuta di pagamento.|
| **Riconcilia conti clienti e fornitori** | 33 |Mostra i movimenti C/G risultanti dalla registrazione dei movimenti clienti e fornitori suddivisi per conto C/G e categorie di registrazione. Questo report viene utilizzato per riconciliare i saldi dei libri contabili dei clienti e dei fornitori con i saldi della contabilità generale. |
| **Clienti - Scadenzario riepilogativo semplice**| 109 |Si tratta di una versione legacy di un report scadenzario clienti. Ti consigliamo di utilizzare il report **Scadenziario clienti**. |
| **Statistiche vendite** |112  |[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)]<br>Questo report può essere utilizzato anche nella contabilità clienti poiché è più semplice eseguire una rapida ricerca di pagamenti registrati, sconti e vendite per un determinato cliente.|
|**Lista clienti**|101| Visualizza varie informazioni di base sui clienti, quali categorie di registrazione cliente, categoria di sconto, addebiti interessi e informazioni sui pagamenti, venditori, valuta predefinita e limite di credito del cliente in valuta locale (VL) e il saldo corrente del cliente in VL. Il report può essere utilizzato ad esempio per mantenere le informazioni nella tabella Cliente.|

---
title: Dettagli di progettazione - Disponibilità tracciabilità articolo
description: Nelle pagine Righe tracciabilità articolo e Riepilogo tracciabilità articolo sono presenti informazioni dinamiche sulla disponibilità relative ai numeri seriali o di lotto che aumentano la trasparenza per gli utenti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 4fd66e1b6e5aff71ee10b0e24d9f25b81eb85887
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138624"
---
# <a name="design-details-item-tracking-availability"></a>Dettagli di progettazione: Disponibilità tracciabilità articolo
Nelle pagine **Righe tracciabilità articolo** e **Riepilogo tracciabilità articolo** sono presenti informazioni dinamiche sulla disponibilità relative ai numeri seriali o di lotto. Lo scopo di questo è di aumentare la trasparenza per gli utenti nei documenti in uscita, come gli ordini di vendita, mostrando loro quali numeri seriali o quante unità di un numero di lotto sono attualmente assegnati in altri documenti aperti. Ciò riduce l'incertezza che è causata dalla doppia allocazione e infonde fiducia nei gestori ordini che i numeri di tracciabilità articolo e le date che promettono negli ordini di vendita non registrati possano essere rispettati. Per ulteriori informazioni, vedere [Dettagli di progettazione: Pagina righe tracciabilità articolo](design-details-item-tracking-lines-window.md).  

 Quando si apre la pagina **Righe tracciabilità articolo**, i dati sulla disponibilità vengono recuperati dalla tabella **Mov. contabile articoli** e dalla tabella **Movimenti impegni**, senza filtro sulla data. Quando si sceglie il campo **Nr. seriale** o il campo **Nr. lotto**, viene visualizzata la pagina **Riepilogo tracciabilità articolo** e viene mostrato un riepilogo delle informazioni sulla tracciabilità articoli nella tabella **Movimenti impegni**. Il riepilogo contiene le seguenti informazioni relative a ogni numero seriale o di lotto nella riga di tracciabilità articolo:  

|Campo|Descrizione|  
|---------------------------------|---------------------------------------|  
|**Quantità totale**|La quantità totale del numero seriale o di lotto al momento nel magazzino.|  
|**Qtà totale richiesta**|La quantità totale del numero seriale o di lotto attualmente richiesta in tutti i documenti.|  
|**Quantità corrente in sospeso**|Quantità che viene immessa nell'istanza corrente della pagina **Righe tracciabilità articolo** ma non ancora caricata nel database.|  
|**Quantità totale disponibile**|La quantità del numero seriale o di lotto disponibile per l'utente da richiedere.<br /><br /> Questa quantità viene calcolata da altri campi nella pagina nel modo seguente:<br /><br /> quantità totale – (quantità richiesta totale + quantità corrente in sospeso).|  

> [!NOTE]  
>  È inoltre possibile vedere le informazioni nella tabella precedente utilizzando la funzione **Seleziona movimenti** nella pagina **Righe tracciabilità articolo**.  

 Per mantenere le prestazioni del database, i dati di disponibilità vengono recuperati solo una volta dal database quando si apre la pagina **Righe tracciabilità articolo** e quando si utilizza la funzione **Aggiorna disponibilità** nella pagina.  

## <a name="calculation-formula"></a>Formula di calcolo  
 Come descritto nella tabella precedente, la disponibilità di un numero seriale o di lotto specificato viene calcolata nel modo seguente.  

 quantità totale disponibile = quantità in magazzino – (tutte le domande + quantità non ancora sottoposta a commit nel database)  

> [!IMPORTANT]  
>  La formula implica che il calcolo della disponibilità del numero seriale o di lotto prenda in considerazione solo il magazzino e ignori i carichi previsti. Di conseguenza, l'approvvigionamento non ancora registrato in magazzino non influisce sulla disponibilità di tracciabilità articolo, a differenza della disponibilità articolo normale in cui sono inclusi i carichi previsti.  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
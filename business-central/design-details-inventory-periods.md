---
title: 'Dettagli di progettazione: Periodi di magazzino | Microsoft Docs'
description: Le transazioni retrodatate o le rettifiche dei costi spesso influenzano i saldi e le valutazioni di magazzino per i periodi contabili che possono essere considerati chiusi. Ciò può avere effetti negativi sulla precisione dei report, in particolare all'interno delle società globali. La funzionalità Periodi di magazzino può essere utilizzata per evitare tali problemi aprendo o chiudendo i periodi di magazzino per limitare la registrazione in un determinato periodo di tempo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2f7ef91c2d7ecc01f38deeda371c409e80eafd27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913740"
---
# <a name="design-details-inventory-periods"></a>Dettagli di progettazione: Periodi di magazzino
Le transazioni retrodatate o le rettifiche dei costi spesso influenzano i saldi e le valutazioni di magazzino per i periodi contabili che possono essere considerati chiusi. Ciò può avere effetti negativi sulla precisione dei report, in particolare all'interno delle società globali. La funzionalità Periodi di magazzino può essere utilizzata per evitare tali problemi aprendo o chiudendo i periodi di magazzino per limitare la registrazione in un determinato periodo di tempo.  

 Un periodo di magazzino è un periodo di tempo, definito da una data di fine, in cui si registrano transazioni di magazzino. Quando si chiude un periodo di magazzino, non è possibile registrare alcuna modifica dei valori nel periodo chiuso. Sono incluse le registrazioni di nuovi valori, le registrazioni previste o fatturate, le modifiche a valori esistenti e le rettifiche dei costi. Tuttavia, è ancora possibile collegare a un movimento contabile aperto che ricade nel periodo chiuso. Per ulteriori informazioni, vedere [Dettagli di progettazione: Collegamento articoli](design-details-item-application.md).  

 Per assicurarsi che tutti movimenti di transazione in un periodo chiuso siano finali, le seguenti condizioni devono essere soddisfatte prima della chiusura di un periodo di magazzino:  

-   Tutti i movimenti contabili articoli in uscita nel periodo devono essere chiusi (nessuna giacenza negativa).  
-   Tutti i costi articolo nel periodo devono essere rettificati.  
-   Gli ordini di produzione rilasciati e completati nel periodo devono essere rettificati.  

 Quando si chiude un periodo di magazzino, viene creato un movimento periodo di magazzino utilizzando il numero dell'ultimo registro magazzino che ricade nel periodo di magazzino. Inoltre, l'ora, la data e il codice dell'utente che chiude il periodo vengono registrati nel movimento periodo di magazzino. Utilizzando queste informazioni con l'ultimo registro magazzino per il periodo precedente, è possibile visualizzare quali transazioni di magazzino sono registrate nel periodo di magazzino. È possibile riaprire i periodi di magazzino se occorre registrare in un periodo chiuso. Quando si riapre un periodo di magazzino, viene creato un movimento periodo di magazzino.  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md) [Gestione dei costi di magazzino](finance-manage-inventory-costs.md) [Contabilità](finance.md)  
 [Utilizzo di Business Central](ui-work-product.md)

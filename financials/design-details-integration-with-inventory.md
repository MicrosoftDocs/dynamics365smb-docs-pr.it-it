---
title: 'Dettagli di progettazione: Integrazione con il magazzino | Microsoft Docs'
description: L'area di applicazione Gestione warehouse e l'area di applicazione Magazzino interagiscono tra loro nell'inventario fisico e nella rettifica della warehouse o di magazzino.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-integration-with-inventory"></a>Dettagli di progettazione: Integrazione con il magazzino
L'area di applicazione Gestione warehouse e l'area di applicazione Magazzino interagiscono tra loro nell'inventario fisico e nella rettifica della warehouse o di magazzino.  
  
## <a name="physical-inventory"></a>Physical Inventory  
 La finestra **Registrazioni Inventario Whse.** viene utilizzata con la finestra **Registrazioni inventario fis.** per tutte le ubicazioni warehouse avanzate. Il magazzino a livello di collocazione viene calcolato e viene stampato un elenco per l'impiegato warehouse. L'elenco indica quali elementi devono essere conteggiati in quali collocazioni.  
  
 Un impiegato warehouse immette la quantità conteggiata nella finestra **Registrazioni Inventario Whse.**, quindi effettua le registrazioni.  
  
 Se la quantità conteggiata è maggiore della quantità nella riga delle registrazioni, verrà registrato un movimento per questa differenza dalla collocazione rettifica predefinita alla collocazione conteggiata. In questo modo viene aumentata la quantità nella collocazione conteggiata e viene diminuita la quantità nella collocazione rettifica predefinita.  
  
 Se la quantità conteggiata è minore della quantità nella riga delle registrazioni, verrà registrato un movimento per questa differenza dalla collocazione conteggiata alla collocazione rettifica predefinita. In questo modo la quantità nella collocazione conteggiata diminuisce e la quantità nella collocazione rettifica predefinita aumenta.  
  
 Nelle configurazioni avanzate della warehouse, il valore nel campo **Quantità (calcolata)** viene recuperato dai movimenti contabili articoli e il valore nel campo **Qtà (inv. fisico)** viene recuperato dai movimenti warehouse, escluso il contenuto della collocazione rettifica. Il campo **Quantità** specifica la differenza tra i primi due campi, che devono essere uguali al contenuto della collocazione di rettifica.  
  
 Quando si effettuano le registrazioni di inventario, vengono aggiornati il magazzino e la collocazione rettifica predefinita.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Rettifiche di warehouse nel movimento contabile articolo  
 La finestra **Registrazioni magazzino** e la funzione **Calcola rettifica whse** consentono di rettificare il magazzino nei movimenti magazzino conformemente a una rettifica che è stata eseguita sulla quantità di articoli in una collocazione warehouse. Per creare un collegamento tra il magazzino e la warehouse, è necessario definire una collocazione di rettifica predefinita per ubicazione.  
  
 La collocazione rettifica predefinita registra gli articoli nella warehouse quando si registra un aumento del magazzino. Tuttavia, se si registra una riduzione, anche la quantità nella collocazione predefinita viene diminuita. In entrambi i casi, vengono creati movimenti contabili articoli e movimenti warehouse.  
  
> [!NOTE]  
>  La collocazione rettifica non è inclusa nel calcolo della disponibilità.  
  
 Se si desidera rettificare il contenuto collocazione, è possibile utilizzare le registrazioni articoli warehouse, da cui è possibile immettere il numero di articolo, il codice zona, il codice collocazione e la quantità da rettificare.  
  
 Se si immette una quantità positiva e si registra la riga, il magazzino archiviato nella collocazione aumenta e la quantità della collocazione di rettifica predefinita diminuisce di conseguenza.  
  
## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)   
 [Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md)

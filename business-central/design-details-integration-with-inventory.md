---
title: Dettagli di progettazione - Integrazione con il magazzino
description: La Gestione warehouse e l'area di applicazione Magazzino interagiscono tra loro nell'inventario fisico e nella rettifica della warehouse o di magazzino.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="design-details-integration-with-inventory"></a>Dettagli di progettazione: Integrazione con il magazzino

Le funzionalità Gestione warehouse e Magazzino interagiscono tra loro nell'inventario fisico e nella rettifica della warehouse o di magazzino.  

## <a name="physical-inventory"></a>Inventario fisico

La pagina **Registrazioni Inventario Whse.** viene utilizzata con la pagina **Registrazioni inventario fis.** per tutte le ubicazioni warehouse avanzate. Il magazzino a livello di collocazione viene calcolato e viene stampato un elenco per l'impiegato warehouse. L'elenco indica quali elementi devono essere conteggiati in quali collocazioni.  
  
Un impiegato warehouse immette la quantità conteggiata nella pagina **Registrazioni Inventario Whse.**, quindi effettua le registrazioni.  
  
Se la quantità conteggiata è maggiore della quantità nella riga delle registrazioni, verrà registrato un movimento per questa differenza dalla collocazione rettifica predefinita alla collocazione conteggiata. In questo modo viene aumentata la quantità nella collocazione conteggiata e viene diminuita la quantità nella collocazione rettifica predefinita.  
  
Se la quantità conteggiata è minore della quantità nella riga delle registrazioni, verrà registrato un movimento per questa differenza dalla collocazione conteggiata alla collocazione rettifica predefinita. In questo modo la quantità nella collocazione conteggiata diminuisce e la quantità nella collocazione rettifica predefinita aumenta.  
  
Nelle configurazioni avanzate della warehouse, il valore nel campo **Quantità (calcolata)** viene recuperato dai movimenti contabili articoli e il valore nel campo **Qtà (inv. fisico)** viene recuperato dai movimenti warehouse, escluso il contenuto della collocazione rettifica. Il campo **Quantità** specifica la differenza tra i primi due campi, che devono essere uguali al contenuto della collocazione di rettifica.  
  
Quando si effettuano le registrazioni di inventario, vengono aggiornati il magazzino e la collocazione rettifica predefinita.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## <a name="warehouse-adjustments-to-the-item-ledger"></a>Rettifiche di warehouse nel movimento contabile articolo

La pagina **Registrazioni magazzino** e la funzione **Calcola rettifica whse** consentono di rettificare il magazzino nei movimenti magazzino conformemente a una rettifica che è stata eseguita sulla quantità di articoli in una collocazione warehouse. Per creare un collegamento tra il magazzino e la warehouse, è necessario definire una collocazione di rettifica predefinita per ubicazione.  
  
La collocazione rettifica predefinita registra gli articoli nella warehouse quando si registra un aumento del magazzino. Tuttavia, se si registra una riduzione, anche la quantità nella collocazione predefinita viene diminuita. In entrambi i casi, vengono creati movimenti contabili articoli e movimenti warehouse.  
  
> [!NOTE]  
> I calcoli dell'inventario non includono la collocazione di rettifica.  
  
Per rettificare il contenuto collocazione, utilizza le registrazioni articoli warehouse, dove è possibile immettere il numero di articolo, il codice zona, il codice collocazione e la quantità da rettificare.  
  
Se si immette una quantità positiva e si registra la riga, il magazzino archiviato nella collocazione aumenta e la quantità della collocazione di rettifica predefinita diminuisce di conseguenza.  
  
## <a name="see-also"></a>Vedere anche

[Panoramica gestione del magazzino](design-details-warehouse-management.md)  
[Dettagli di progettazione: Disponibilità nella warehouse](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

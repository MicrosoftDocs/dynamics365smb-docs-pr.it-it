---
title: 'Dettagli di progettazione: Ricerca delle combinazioni di dimensione | Microsoft Docs'
description: 'Quando si chiude la pagina dopo avere modificato un set di dimensioni, in Business Central viene valutato se il set di dimensioni modificato esiste. Se il set non esiste, viene creato un nuovo set e viene restituito l''ID combinazione delle dimensioni.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-searching-for-dimension-combinations"></a>Dettagli di progettazione: Ricerca delle combinazioni di dimensione
Quando si chiude la pagina dopo avere modificato un set di dimensioni, in [!INCLUDE[prod_short](includes/prod_short.md)] viene valutato se il set di dimensioni modificato esiste. Se il set non esiste, viene creato un nuovo set e viene restituito l'ID combinazione delle dimensioni.  

## <a name="building-search-tree"></a>Creazione albero di ricerca
 La tabella 481 **Nodo albero set di dimensioni** viene utilizzata quando [!INCLUDE[prod_short](includes/prod_short.md)] valuta se un set di dimensioni esiste già nella tabella 480 **Voce set di dimensioni**. La valutazione viene eseguita in modo ricorsivo lungo l'albero di ricerca a partire dal livello massimo con numero 0. Il livello massimo 0 rappresenta un set di dimensioni senza movimenti di set di dimensioni. I figli di questo set di dimensioni rappresentano i set di dimensioni con un solo movimento set di dimensioni. I figli di questi set di dimensioni rappresentano i set di dimensioni con due elementi figlio e così via.  

### <a name="example-1"></a>Esempio 1
 Nel seguente diagramma viene rappresentato un albero di ricerca con sei set di dimensioni. Solo il movimento set di dimensioni distintivo viene visualizzato nel grafico.  

 ![Esempio di struttura ad albero dimensioni.](media/nav2013_dimension_tree.png "Esempio di struttura ad albero dimensioni")  

 Nella tabella seguente viene descritto un elenco di movimenti set di dimensioni che costituiscono ogni set di dimensioni.  

|Set di dimensioni|Movimenti set di dimensioni|  
|--------------------|---------------------------|  
|Set 0|Nessuno|  
|Set 1|AREA 30|  
|Set 2|AREA 30, REPARTO ADM|  
|Set 3|AREA 30, REPARTO PROD|  
|Set 4|AREA 30, REPARTO ADM, PROJ VW|  
|Set 5|AREA 40|  
|Set 6|AREA 40, PROJ VW|  

### <a name="example-2"></a>Esempio 2
 In questo esempio viene mostrato in che modo [!INCLUDE[prod_short](includes/prod_short.md)] valuta se è presente un set di dimensioni costituito da movimenti di set di dimensioni AREA 40, DEPT PROD.  

 [!INCLUDE[prod_short](includes/prod_short.md)] aggiorna prima di tutto anche la tabella **Nodo albero set di dimensioni** per assicurarsi che l'albero di ricerca somigli al diagramma seguente. Pertanto il set di dimensioni 7 diventa un figlio del set di dimensioni 5.  

 ![Esempio di struttura ad albero dimensioni in NAV 2013.](media/nav2013_dimension_tree_example2.png "Esempio di struttura ad albero dimensioni in NAV 2013")  

### <a name="finding-dimension-set-id"></a>Ricerca ID set di dimensioni
 A livello concettuale, i valori **ID padre**, **Dimensione** e **Valore dimensioni**, nell'albero di ricerca vengono combinati e utilizzati come chiave primaria perché [!INCLUDE[prod_short](includes/prod_short.md)] attraversa la struttura ad albero nello stesso ordine dei movimenti con dimensione. La funzione Get (record) viene utilizzata per cercare l'ID set di dimensioni. Nell'esempio di codice riportato di seguito viene illustrato come trovare l'ID set di dimensioni quando sono presenti tre valori di dimensione.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

Tuttavia, per mantenere la capacità di [!INCLUDE[prod_short](includes/prod_short.md)] di rinominare una dimensione e un valore di dimensione, la tabella 349, **Valore dimensioni**, viene estesa con un campo di numero intero, **ID valore dimensioni**. Questa tabella converte la coppia di campi, **Dimensione** e **Valore dimensioni**, in un valore intero. Quando si rinominano la dimensione e il valore di dimensione, il valore intero non viene modificato.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Vedere anche
    
 [Dettagli di progettazione: Movimenti set di dimensioni](/dynamics365/business-central/design-details-dimension-set-entries-overview)   
 [Sintesi movimenti set di dimensioni](design-details-dimension-set-entries-overview.md)   
 [Dettagli di progettazione - Struttura della tabella](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]

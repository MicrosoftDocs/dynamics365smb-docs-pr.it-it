---
title: Utilizzo delle famiglie di prodotti in Manufacturing
description: 'L''operazione principale da eseguire per personalizzare un calendario di base per la propria società, o per uno dei partner commerciali, è la modifica dello stato dei giorni lavorativi e non lavorativi.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000790, 99000791, 99000792, 99000793'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-production-families"></a><a name="work-with-production-families"></a>Utilizzare famiglie di prodotti

Una famiglia di prodotti consiste in un gruppo di articoli individuali la cui relazione si basa sulla similarità dei rispettivi processi di lavorazione. Formando delle famiglie di produzione, è possibile che alcuni articoli siano lavorati due o più volte nel corso di una produzione; questa operazione ottimizzerà il consumo di materiale.

Nel campo **Quantità** della pagina **Famiglie di prodotti**, immettere la quantità che sarà prodotta quando l'intera famiglia sarà stata lavorata una volta.

## <a name="example"></a><a name="example"></a>Esempio

Nei processi di perforazione, è possibile che da una lamina vengano prodotti contemporaneamente quattro pezzi di un articolo e 10 pezzi di un altro articolo differente. La perforatrice perforerà tutti i 14 pezzi in un'unica fase.

La creazione di famiglie di produzione riduce le quantità di scarto perché ciò che generalmente costituisce gli scarti rimanenti dalla produzione di pezzi di grandi dimensioni viene utilizzato per produrre i pezzi di piccole dimensioni.

## <a name="to-set-up-a-production-family"></a><a name="to-set-up-a-production-family"></a>Per impostare una famiglia di prodotti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Famiglie**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><a name="to-produce-based-on-a-production-family"></a>Per produrre in base a una famiglia di prodotti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ord. produzione confermati**, quindi seleziona il collegamento correlato.
2. Creare un nuovo ordine di produzione. Per ulteriori informazioni, vedere [Creare ordini di produzione](production-how-to-create-production-orders.md).
3. Nel campo **Tipo origine**, selezionare **Famiglie di prodotti**.  
4. Nel campo **Nr. risorsa**, selezionare la famiglia di prodotti pertinente.

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)
[Pianificazione](production-planning.md)   
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

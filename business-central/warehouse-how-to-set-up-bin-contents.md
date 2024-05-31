---
title: Creare il contenuto delle collocazioni
description: Dopo aver impostato le collocazioni è possibile specificare gli articoli che si desidera stoccare e impostare le regole che controllano la frequenza di rifornimento dei contenitori.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 7374
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-bin-contents"></a>Creare il contenuto delle collocazioni

Dopo avere impostato le collocazioni, è possibile impostare il contenuto collocazione. Ciò significa che è possibile impostare gli articoli che si desidera inserire in una determinata collocazione e le regole che verranno seguite per l'inserimento di uno specifico articolo in una collocazione. Questa operazione può essere effettuata manualmente nella pagina **Contenuto collocazioni** o automaticamente tramite la pagina **Crea prospetto contenuto collocazione**.

## <a name="to-create-bin-content-manually"></a>Per creare manualmente il contenuto collocazione

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2. Selezionare l'ubicazione in cui si desidera impostare contenuti collocazione e scegliere l'azione **Collocazioni**.  
3. Selezionare la collocazione in cui si desidera impostare contenuti e scegliere l'azione **Contenuti**.  
4. Per ogni articolo che si desidera inserire nella collocazione, compilare i campi di una riga della pagina **Contenuto collocazioni** immettendo le informazioni appropriate. Alcuni campi sono già compilati con le informazioni relative alla collocazione.  
5. Compilare innanzitutto il campo **Nr. articolo**, quindi, se si utilizzano stoccaggi e prelievi guidati, compilare gli altri campi, quali **Cod. unità di misura**, **Qtà massima** e **Qtà minima**.  

Selezionare il campo **Fisso** se necessario. Se la collocazione deve essere utilizzata come collocazione di default per l'articolo, selezionare il campo **Collocazione di default**.  

Se si utilizzano stoccaggi e prelievi guidati e, nella scheda articolo, sono state specificate le informazioni di dimensione corrette relative alle unità di misura di ciascun articolo, la quantità massima immessa nella pagina **Contenuto collocazioni** viene confrontata con le capacità fisiche della collocazione. I valori di quantità massima e minima verranno utilizzati per il calcolo del rifornimento della collocazione e dei suggerimenti relativi allo stoccaggio.  

Se si seleziona il campo **Fisso**, si stabilisce che l'articolo debba essere associato principalmente a tale collocazione. Ciò significa che in [!INCLUDE[prod_short](includes/prod_short.md)] l'articolo verrà inserito nella collocazione se la quantità di spazio disponibile è sufficiente e il record indicante l'associazione fissa tra articolo e collocazione verrà conservato anche quando la quantità all'interno della collocazione è pari a 0. Il fatto che un determinato articolo venga associato in modo fisso a una specifica collocazione non preclude la possibilità di inserire altri articoli nella collocazione in questione.  

> [!NOTE]  
> È possibile impostare diversi contenuti collocazione contemporaneamente nella pagina **Prospetto creaz. cont. colloc.**  

## <a name="to-create-bin-content-with-a-worksheet"></a>Per creare il contenuto delle collocazioni con un prospetto

Dopo avere creato le collocazioni, è possibile specificare il contenuto desiderato per ciascuna collocazione nel prospetto creazione contenuto collocazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Prospetto creaz. cont. colloc.**, quindi seleziona il collegamento correlato.  
2. Nella testata del prospetto, dal campo **Nome** selezionare il prospetto dell'ubicazione in cui si desidera creare il contenuto delle collocazioni.  
3. Nel campo **Cod. collocazione** selezionare il codice della collocazione per la quale si desidera definire il contenuto.  

    Se si utilizzano stoccaggi e prelievi guidati, i campi relativi alla collocazione, quali **Tipo collocazione**, **Codice classe warehouse** e **Valutazione collocazione**, vengono compilati automaticamente. Queste informazioni sono necessarie per definire il contenuto della collocazione.  
4. Selezionare l'articolo che si desidera assegnare alla collocazione, quindi compilare i campi relativi al contenuto della collocazione. Se si utilizzano stoccaggi e prelievi guidati e si desidera utilizzare la funzione **Calcola rifornimento collocazione**, compilare i campi **Qtà massima** e **Qtà minima**.  

    Per impostare la collocazione come collocazione preferita per l'articolo anche se la quantità nella collocazione è pari a **0**, a parità di tutti gli altri criteri di stoccaggio, inserire un segno di spunta nel campo **Fisso**.  
5. Ripetere i passaggi da 3 e 4 per ogni articolo che si desidera assegnare a una collocazione.  
6. Scegliere l'azione **Stampa** per visualizzare in anteprima e stampare il contenuto delle collocazioni specificato nel prospetto. Esaminare il contenuto delle collocazioni e apportare le eventuali correzioni finché il risultato non è soddisfacente.  
7. Quando si è pronti scegliere l'azione **Crea contenuto collocazione**.  

Poiché questo prospetto consente di utilizzare più righe di contenuto collocazione per più collocazioni, è possibile ottenere una panoramica precisa di tutti gli articoli che si stanno inserendo nelle varie collocazioni presenti in una determinata zona, corsia o scaffalatura.  

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

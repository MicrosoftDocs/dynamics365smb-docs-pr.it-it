---
title: Impostare stoccaggi e prelievi guidati
description: Lo stoccaggio e il prelievo diretti ti offrono funzionalità per gestire la tua warehouse in modo efficiente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a><a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a><a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Impostare articoli e ubicazioni per gli stoccaggi e i prelievi guidati

L'impostazione dell'ubicazione di una warehouse per stoccaggi e prelievi guidati offre una nuova funzionalità che consente di gestire la warehouse nel modo più efficiente possibile. Per sfruttare al meglio tale funzionalità occorre fornire informazioni aggiuntive sugli articoli, le quali verranno utilizzate per effettuare i calcoli necessari e suggerire le modalità più efficaci ed efficienti per eseguire le attività di warehouse. 

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a><a name="to-set-up-an-item-for-directed-put-away-and-pick"></a><a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Per impostare un articolo per gli stoccaggi e i prelievi guidati

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Aprire la scheda per l'articolo da impostare per stoccaggio e prelievo guidati.
3. Nella Scheda dettaglio **Warehouse** della scheda articolo, compilare i campi appropriati per definire le modalità di gestione dell'articolo nella warehouse.  
4. Scegliere l'azione **Unità di misura**.
5. Nella pagina **Unità di misura articoli** definisci le unità di misura utilizzabili nelle transazioni riguardanti l'articolo specificando altezza, larghezza, lunghezza, cubatura e peso.
6. Scegliere l'azione **Contenuto collocazioni**.
7. Nella pagina **Contenuto collocazioni** definire l'ubicazione e la collocazione a cui deve essere associato l'articolo. Il campo **Default** non è disponibile quando l'ubicazione viene impostata per gli stoccaggi e i prelievi guidati.  

## <a name="to-start-using-directed-put-away-and-pick"></a><a name="to-start-using-directed-put-away-and-pick"></a><a name="to-start-using-directed-put-away-and-pick"></a>Per iniziare a utilizzare lo stoccaggio e il prelievo diretti

Gli stoccaggi e i prelievi guidati fanno parte delle funzioni di configurazione di warehouse avanzate che consentono di migliorare notevolmente l'efficienza e aumentare l'affidabilità dei dati. Per utilizzare queste funzionalità occorre innanzitutto impostare alcuni parametri nell'ubicazione della warehouse.  

Per utilizzare la funzionalità di stoccaggi e prelievi guidati, è necessario attivarla nella scheda ubicazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2. Selezionare l'ubicazione in cui si desidera utilizzare stoccaggi e prelievi guidati, quindi scegliere l'azione **Modifica**.  
3. Seleziona la casella di controllo **Stoccaggi e prelievi guidati** nella Scheda dettaglio **Warehouse**.  

È possibile compilare gli altri campi della scheda ubicazione nelle fasi successive del processo di setup.  

> [!NOTE]  
> Non è possibile impostare l'utilizzo di collocazioni per la warehouse se l'ubicazione presenta movimenti contabili articoli aperti.  

Il passo successivo consiste nel definire il tipo di collocazioni che si desidera utilizzare. Per ulteriori informazioni, vedere [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md). Il tipo di collocazioni determina la modalità di utilizzo di una determinata collocazione durante l'elaborazione del flusso degli articoli all'interno della warehouse. È possibile assegnare un tipo collocazione sia a una zona che a una collocazione.  

È inoltre possibile definire i codici di classe warehouse, qualora la warehouse contenga articoli che richiedono specifiche condizioni di immagazzinamento. I codici classe warehouse vengono utilizzati quando vengono forniti suggerimenti sulla posizione degli articoli nelle collocazioni. I codici classe warehouse vengono assegnati a gruppi di prodotti, che vengono quindi assegnati ad articoli e unità di stockkeeping oppure a zone e collocazioni in grado di soddisfare le condizioni di immagazzinamento richieste dai codici classe warehouse.  

Ora sei pronto per configurare le zone, se lo desideri. L'utilizzo delle zone riduce il numero dei campi che è necessario compilare durante l'impostazione delle collocazioni, in quanto le collocazioni create all'interno delle zone ne ereditano varie proprietà. Le zone consentono inoltre agli impiegati nuovi o temporanei di orientarsi più facilmente all'interno della warehouse. Si noti che il flusso è controllato dalle collocazioni, pertanto è possibile utilizzare più collocazioni e una sola zona.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a><a name="to-set-up-a-zone-in-your-warehouse"></a><a name="to-set-up-a-zone-in-your-warehouse"></a>Per impostare una zona nella warehouse

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2. Selezionare l'ubicazione in cui si desidera impostare la zona e aprire la scheda ubicazione, quindi scegliere l'azione **Zone**.  
3. Compilare i campi nella pagina **Zone** come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Quando si modifica un parametro di zona, tutte le collocazioni create successivamente in tale zona erediteranno le nuove caratteristiche, mentre le collocazioni originali resteranno invariate.  

> [!NOTE]  
> Se non si desidera utilizzare le zone, è comunque necessario almeno un codice di zona, che non verrà definito se non per quanto riguarda il codice.  

Il passaggio successivo consiste nella definizione delle collocazioni. Per ulteriori informazioni, vedi [Impostare ubicazioni per l'utilizzo di collocazioni](warehouse-how-to-set-up-locations-to-use-bins.md).  

Inoltre, è necessario creare modelli di stoccaggio e periodi di conteggio. Per ulteriori informazioni, vedi [Impostare i modelli di stoccaggio](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

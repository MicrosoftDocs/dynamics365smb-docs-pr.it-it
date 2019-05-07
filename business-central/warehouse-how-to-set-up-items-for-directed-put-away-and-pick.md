---
title: Impostare stoccaggi e prelievi guidati | Documenti Microsoft
description: L'impostazione dell'ubicazione di una warehouse per stoccaggi e prelievi guidati offre una nuova funzionalità che consente di gestire la warehouse nel modo più efficiente possibile.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2492ebf0d9987bd126fa963c6d7d940c6a114796
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "914812"
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Impostare articoli e ubicazioni per gli stoccaggi e i prelievi guidati
L'impostazione dell'ubicazione di una warehouse per stoccaggi e prelievi guidati offre una nuova funzionalità che consente di gestire la warehouse nel modo più efficiente possibile. Per sfruttare al meglio tale funzionalità occorre fornire informazioni aggiuntive sugli articoli, le quali verranno utilizzate per effettuare i calcoli necessari e suggerire le modalità più efficaci ed efficienti per eseguire le attività di warehouse. Per ulteriori informazioni, vedere [Dettagli di progettazione: Setup warehouse](design-details-warehouse-setup.md).

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Per impostare un articolo per gli stoccaggi e i prelievi guidati  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.  
2.  Aprire la scheda per l'articolo da impostare per stoccaggio e prelievo guidati.
3. Nella Scheda dettaglio **Warehouse** della scheda articolo, compilare i campi appropriati per definire le modalità di gestione dell'articolo nella warehouse.  
4.  Scegliere l'azione **Unità di misura**.
5. Nella pagina **Unità di misura articoli** compilare i campi per definire le diverse unità di misura utilizzabili nelle transazioni riguardanti l'articolo, incluse altezza, larghezza, lunghezza, cubatura e peso per l'unità di misura.
6. Scegliere l'azione **Contenuto collocazioni**.
7. Nella pagina **Contenuto collocazioni** definire l'ubicazione e la collocazione a cui deve essere associato l'articolo. Il campo **Default** non è disponibile quando l'ubicazione viene impostata per gli stoccaggi e i prelievi guidati.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>Per attivare la funzionalità di stoccaggi e prelievi guidati  
Gli stoccaggi e i prelievi guidati fanno parte delle funzioni di configurazione di warehouse avanzate che consentono di migliorare notevolmente l'efficienza e aumentare l'affidabilità dei dati. Per utilizzare queste funzionalità occorre innanzitutto impostare alcuni parametri nell'ubicazione della warehouse.  

Per utilizzare la funzionalità di stoccaggi e prelievi guidati, è necessario attivarla nella scheda ubicazione.    
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'ubicazione in cui si desidera utilizzare stoccaggi e prelievi guidati, quindi scegliere l'azione **Modifica**.  
3.  Selezionare la casella di controllo **Stoccaggi e prelievi guidati** nella Scheda dettaglio **Warehouse**.  

È possibile compilare gli altri campi della scheda ubicazione nelle fasi successive del processo di setup.  

> [!NOTE]  
>  Non è possibile impostare l'utilizzo di collocazioni per la warehouse se l'ubicazione presenta movimenti contabili articoli aperti.  

Il passo successivo consiste nel definire il tipo di collocazioni che si desidera utilizzare. Per ulteriori informazioni, vedere [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md). Il tipo di collocazioni determina la modalità di utilizzo di una determinata collocazione durante l'elaborazione del flusso degli articoli all'interno della warehouse. È possibile assegnare un tipo collocazione sia a una zona che a una collocazione.  

È inoltre possibile definire i codici di classe warehouse, qualora la warehouse contenga articoli che richiedono diverse condizioni di immagazzinamento. I codici classe warehouse vengono utilizzati quando vengono forniti suggerimenti sulla posizione degli articoli nelle collocazioni. I codici classe warehouse vengono assegnati a gruppi di prodotti, che vengono quindi assegnati ad articoli e unità di stockkeeping oppure a zone e collocazioni in grado di soddisfare le condizioni di immagazzinamento richieste dai codici classe warehouse.  

A questo punto, se si desidera utilizzare le zone nella warehouse, è possibile procedere all'impostazione. L'utilizzo delle zone riduce il numero dei campi che è necessario compilare durante l'impostazione delle collocazioni, in quanto le collocazioni create all'interno delle zone ne ereditano varie proprietà. Le zone consentono inoltre agli impiegati nuovi o temporanei di orientarsi più facilmente all'interno della warehouse. Si noti che il flusso è controllato dalle collocazioni, pertanto è possibile utilizzare più collocazioni e una sola zona.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>Per impostare una zona nella warehouse  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.  
2.  Selezionare l'ubicazione in cui si desidera impostare la zona e aprire la scheda ubicazione, quindi scegliere l'azione **Zone**.  
3.  Compilare i campi nella pagina **Zone** come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Quando si modifica un parametro di zona, tutte le collocazioni create successivamente in tale zona erediteranno le nuove caratteristiche, mentre le collocazioni originali resteranno invariate.  

> [!NOTE]  
>  Se non si desidera utilizzare le zone, è comunque necessario almeno un codice di zona, che non verrà definito se non per quanto riguarda il codice.  

Il passaggio successivo del processo di impostazione della warehouse consiste nella definizione delle collocazioni. Per ulteriori informazioni, vedere [Impostare ubicazioni per l'utilizzo di collocazioni](warehouse-how-to-set-up-locations-to-use-bins.md).  

Inoltre, è necessario creare modelli di stoccaggio e periodi di conteggio. Per ulteriori informazioni, vedere [Impostare i modelli di stoccaggio](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

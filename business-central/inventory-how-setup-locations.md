---
title: Impostare una scheda Ubicazione e definire i percorsi di trasferimento
description: È possibile creare una scheda ubicazione per ogni area in cui vengono immagazzinati gli articoli in magazzino, ad esempio warehouse o centro di distribuzione, per impostare percorsi per il trasferimento degli articoli tra le ubicazioni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184326"
---
# <a name="set-up-locations"></a>Impostare le ubicazioni

Se si acquista, immagazzina o si vendono articoli in più aree o warehouse, è necessario impostare ogni ubicazione con una scheda ubicazione e definire i percorsi di trasferimento. [!INCLUDE [prod_short](includes/prod_short.md)] utilizza le ubicazioni per tenere traccia dell'inventario sia nei casi più semplici che nei processi di magazzino più complessi.

È quindi possibile creare le righe del documento per una specifica ubicazione, visualizzare la disponibilità per ubicazione e trasferire il magazzino tra le ubicazioni. Per ulteriori informazioni, vedere [Gestire il magazzino](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Schede Ubicazione

La scheda Ubicazione specifica le informazioni su un'ubicazione, ad esempio un warehouse o un centro di distribuzione. A ogni ubicazione vengono assegnati un nome e un codice che la rappresenta. Quando si desidera registrare le transazioni per una determinata ubicazione, è possibile immettere il codice ubicazione in altre aree del programma.  

È possibile immettere informazioni sui criteri di logistica warehouse per ogni ubicazione. In base ai criteri di logistica warehouse selezionati, sarà possibile utilizzare le opzioni della Scheda dettaglio **Collocazioni** per definire le collocazioni di default che verranno utilizzate durante l'esecuzione delle transazioni. Se è previsto l'utilizzo di stoccaggi e prelievi guidati, utilizzare la maggior parte delle opzioni della Scheda dettaglio **Criteri per collocazione** per definire le modalità di utilizzo delle varie funzioni di logistica avanzate.  

Alcuni campi opzione sono visualizzati in grigio e disabilitati da altre impostazioni nella pagina **Scheda Ubicazione** per limitare le combinazioni di setup non supportate.  

Selezionare l'azione **Zone** o **Collocazioni** per visualizzare le informazioni relative a zone e collocazioni che possono essere definite per l'ubicazione.

### <a name="to-create-a-location-card"></a>Per creare una nuova scheda Ubicazione

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ripetere i passaggi 2 e 3 per ogni ubicazione in cui si desidera mantenere il magazzino.

> [!NOTE]  
> Molti campi della scheda ubicazione fanno riferimento alla gestione degli articoli nei processi della warehouse in entrata e in uscita. I campi non sono rilevanti per le aziende che non richiedono la funzionalità di magazzino più complessa. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

È possibile modificare la configurazione di un'ubicazione in un secondo momento, ma non è possibile modificare l'impostazione delle ubicazioni con movimenti contabili articoli.  

Successivamente, se disponi di più sedi, puoi definire percorsi di trasferimento tra le sedi.  

### <a name="to-create-a-transfer-route"></a>Per creare i percorsi di trasferimento

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Percorsi di trasferimento** e quindi scegliere il collegamento correlato.
2. In alternativa, da una qualsiasi pagina **Scheda Ubicazione** scegliere l'azione **Percorsi trasferimento**.
3. Scegliere l'azione **Nuovo**.
4. Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

A questo punto è possibile trasferire agli articoli di magazzino tra due ubicazioni. Per ulteriori informazioni, vedere [Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Collocazioni

Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli. Dopo avere creato le collocazioni desiderate, è possibile definire precisamente il contenuto che si desidera includere in ciascuna collocazione. In alternativa, è possibile utilizzare la collocazione come collocazione variabile, ovvero priva di contenuto specifico. Le collocazioni vengono utilizzate principalmente nelle operazioni di magazzino di base e anticipate. Se gestisci l'inventario in una configurazione più semplice, probabilmente non hai bisogno di collocazioni.

Per utilizzare la funzionalità di collocazione in una ubicazione, devi prima attivare la funzionalità sulla scheda **Ubicazione** selezionando il campo **Collocazione obbligatoria** sulla Scheda dettaglio **Warehouse**. Si progetterà quindi il flusso degli articoli nell'ubicazione specificando i codici di collocazione nei campi di setup che rappresentano i diversi flussi.

> [!NOTE]
> Prima di poter specificare i codici di collocazione nella scheda Ubicazione, è necessario creare i codici di collocazione.

Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zone

Se vuoi strutturare le tue collocazioni in zone, puoi farlo nella pagina **Zone**.

[!INCLUDE [prod_short](includes/prod_short.md)] copia i campi impostati per una determinata zona nelle collocazioni all'interno della zona in questione. In questo modo sarà quindi possibile assegnare una zona a una collocazione o a una definizione di collocazione (filtro per la creazione delle collocazioni), e diversi altri campi verranno compilati automaticamente.

Tuttavia, è possibile scegliere di impostare una singola zona e organizzare la warehouse solo in base alle collocazioni. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Vedere anche

[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)  
[Creare collocazioni](warehouse-how-to-create-individual-bins.md)  
[Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
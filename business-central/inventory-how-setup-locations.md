---
title: Impostare una scheda ubicazione e definire i percorsi di trasferimento (video)
description: Se acquisti, immagazzini o vendi articoli in più aree o warehouse, devi impostare ogni ubicazione con una scheda ubicazione e definire i percorsi di trasferimento.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 870effafbd38cdee0733097fa6fb0c0340fa77b8
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077269"
---
# <a name="set-up-locations"></a>Impostare le ubicazioni

Le ubicazioni sono luoghi come i magazzini in cui acquisti, stocchi o vendi articoli. [!INCLUDE [prod_short](includes/prod_short.md)] utilizza le ubicazioni per tenere traccia dell'inventario sia nei casi semplici che nei processi di magazzino complessi.

È quindi possibile creare le righe del documento per una specifica ubicazione, visualizzare la disponibilità per ubicazione e trasferire il magazzino tra le ubicazioni. Per ulteriori informazioni, vedere [Gestire il magazzino](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Schede Ubicazione

Specifica le informazioni su un'ubicazione, ad esempio un warehouse o un centro di distribuzione nella pagina **Scheda ubicazione**. A ogni ubicazione vengono assegnati un nome e un codice che la rappresenta. Quando si desidera registrare le transazioni per una determinata ubicazione, è possibile immettere il codice ubicazione in altre aree del programma.  

È possibile immettere informazioni sui criteri di logistica warehouse per ogni ubicazione. In base ai criteri di logistica warehouse selezionati, sarà possibile utilizzare le opzioni della Scheda dettaglio **Collocazioni** per definire le collocazioni di default che verranno utilizzate durante l'esecuzione delle transazioni. Se è previsto l'utilizzo di stoccaggi e prelievi guidati, utilizzare la maggior parte delle opzioni della Scheda dettaglio **Criteri per collocazione** per definire le modalità di utilizzo delle varie funzioni di logistica avanzate.  

Alcuni campi opzione dipendono da altre impostazioni nella pagina **Scheda Ubicazione** per limitare le combinazioni di setup non supportate.  

Seleziona l'azione **Zone** o **Collocazioni** per visualizzare le informazioni relative a zone e collocazioni che sono definite per l'ubicazione.

### <a name="to-set-up-a-location"></a>Per impostare un'ubicazione

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ripetere i passaggi 2 e 3 per ogni ubicazione in cui si desidera mantenere il magazzino.

> [!NOTE]  
> Molti campi della pagina Scheda ubicazione fanno riferimento alla gestione degli articoli nei processi della warehouse in entrata e in uscita. Questi campi non sono rilevanti per le aziende che non richiedono la funzionalità di magazzino complessa. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).

È possibile modificare la configurazione di un'ubicazione in un secondo momento, ma non è possibile modificare l'impostazione delle ubicazioni con movimenti contabili articoli.  

Se disponi di più ubicazioni, puoi definire percorsi di trasferimento tra le ubicazioni. Per ulteriori informazioni, vedi [Per creare i percorsi di trasferimento ](inventory-how-setup-locations.md#to-create-a-transfer-route). 

### <a name="to-create-a-transfer-route"></a>Per creare i percorsi di trasferimento

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Percorsi di trasferimento**, quindi scegli il collegamento correlato.
2. In alternativa, da una qualsiasi pagina **Scheda Ubicazione** scegliere l'azione **Percorsi trasferimento**.
3. Scegliere l'azione **Nuovo**.
4. Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

A questo punto è possibile trasferire agli articoli di magazzino tra due ubicazioni. Per ulteriori informazioni, vedere [Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Collocazioni

Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli. Dopo avere creato le collocazioni desiderate, puoi definire il contenuto o utilizzarle come collocazioni variabili, ovvero prive di contenuto specifico. Le collocazioni vengono utilizzate principalmente nelle operazioni di magazzino di base e anticipate. Se gestisci l'inventario in una configurazione più semplice, probabilmente non hai bisogno di collocazioni.

Per utilizzare la funzionalità di collocazione in una ubicazione, devi prima attivare la funzionalità sulla pagina **Scheda ubicazione** selezionando il campo **Collocazione obbligatoria** sulla Scheda dettaglio **Warehouse**. Si progetterà quindi il flusso degli articoli nell'ubicazione specificando i codici di collocazione nei campi di setup che rappresentano i diversi flussi.

> [!NOTE]
> Prima di poter specificare i codici di collocazione in una ubicazione, è necessario creare i codici di collocazione. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zone

Se vuoi strutturare le tue collocazioni in zone, puoi farlo nella pagina **Zone**.

[!INCLUDE [prod_short](includes/prod_short.md)] copia i campi impostati per una determinata zona nelle collocazioni all'interno della zona in questione. In questo modo sarà quindi possibile assegnare una zona a una collocazione o a una definizione di collocazione (filtro per la creazione delle collocazioni), e diversi altri campi verranno compilati automaticamente.

Tuttavia, è possibile scegliere di impostare una singola zona e organizzare la warehouse solo in base alle collocazioni. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Dimensioni predefinite per le ubicazioni

Si impostano le dimensioni predefinite per un'ubicazione nella pagina **Scheda ubicazione** scegliendo **ubicazione**, e poi **Dimensioni**. Le dimensioni predefinite dell'ubicazione vengono copiate nei giornali di registrazione e nei documenti quando si specifica l'ubicazione su una riga, ma è possibile eliminare o modificare la dimensione sulla riga, se necessario. Puoi richiedere che le persone specifichino le dimensioni per ubicazioni specifiche prima di poter registrare una voce. Puoi anche includere i valori delle dimensioni ubicazione in **Priorità dimensione predefinita** e **Combinazioni dimensioni** per combinazioni di priorità e regole di dimensioni.

## <a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche

[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)  
[Creare collocazioni](warehouse-how-to-create-individual-bins.md)  
[Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
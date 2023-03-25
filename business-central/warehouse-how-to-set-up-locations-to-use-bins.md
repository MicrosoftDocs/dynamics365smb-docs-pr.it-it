---
title: Come impostare ubicazioni per l'utilizzo di collocazioni
description: Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento e all'ubicazione degli articoli.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# Impostare ubicazioni per l'utilizzo di collocazioni

Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli. Dopo avere creato le collocazioni desiderate, è possibile definire in modo specifico il contenuto che si desidera includere in ciascuna collocazione. In alternativa, è possibile utilizzare la collocazione come collocazione variabile, ovvero priva di contenuto specifico.  

Per utilizzare la funzionalità relativa alle collocazioni in un'ubicazione, è necessario prima attivarla nella scheda **Ubicazione**. Si progetterà quindi il flusso degli articoli nell'ubicazione specificando i codici di collocazione nei campi di setup che rappresentano i diversi flussi.  

> [!NOTE]  
>  Prima di poter specificare i codici di collocazione nella scheda Ubicazione, è necessario creare i codici di collocazione. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md).  

## Per impostare un'ubicazione per l'utilizzo di collocazioni

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2.  Selezionare l'ubicazione in cui si desidera utilizzare le collocazioni.  
3.  Scegliere l'azione **Modifica**.  
4.  Nella Scheda Dettaglio **Warehouse** selezionare la casella di controllo **Collocazione obbligatoria**.  
5.  Se non si utilizzano stoccaggi e prelievi guidati per l'ubicazione, nel campo **Selezione Collocazioni di Default** specificare il metodo che il sistema deve utilizzare per assegnare una collocazione di default a un articolo.  
6.  Aprire la scheda per l'ubicazione per cui si desidera impostare le collocazioni.
7.  Nella Scheda dettaglio **Collocazioni**, selezionare le collocazioni da utilizzare come default per i carichi, le spedizioni e le collocazioni di produzione in entrata, in uscita e aperte.  
8.  I codici delle collocazioni immessi in questa scheda verranno visualizzati automaticamente nelle testate e nelle righe dei vari documenti di warehouse. Le collocazioni di default definiscono le posizioni iniziali e finali degli articoli nella warehouse.  
9.  Se si utilizzano stoccaggi e prelievi guidati, selezionare una collocazione per le rettifiche di warehouse. Il codice di collocazione nel campo **Codice collocazione rettifica** definisce la collocazione virtuale in cui registrare le eventuali discrepanze rilevate nelle giacenze quando si registrano le differenze riscontrate e registrate nelle registrazioni articoli warehouse o le differenze calcolate durante la registrazione di un inventario fisico della warehouse.  
10. Compilare i campi nella Scheda dettaglio **Criteri per collocazione** se appropriati per la warehouse. I campi più importanti sono **Criteri capacità collocazione**, **Permettere breakbulk** e **Codice modello stoccaggio**.  
11. Nella Scheda dettaglio **Warehouse** compilare i campi **Tempo gest. uscita da whse.**, **Tempo gest. entrata in whse.** e **Codice calendario base**. Per ulteriori informazioni, vedere [Impostare i calendari di base](across-how-to-assign-base-calendars.md).

## Rifornimento della collocazione di consumo

Questo diagramma di flusso illustra in che modo il campo **Cod. collocazione** nelle righe del componente dell'ordine di produzione viene compilato in base al setup dell'ubicazione.

![Diagramma di flusso collocazione.](media/binflow.png "BinFlow")  

## Vedi il relativo [training Microsoft](/training/modules/configure-bins-location/)

## Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

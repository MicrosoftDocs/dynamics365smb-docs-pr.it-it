---
title: "Procedura: Impostare le ubicazioni per l'utilizzo di collocazioni | Documenti Microsoft"
description: Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli. Dopo avere creato le collocazioni desiderate, è possibile definire in modo specifico il contenuto che si desidera includere in ciascuna collocazione. In alternativa, è possibile utilizzare la collocazione come collocazione variabile, ovvero priva di contenuto specifico.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f7123a5c59b94085d845f3f256c715ce5ad5a3cf
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196165"
---
# <a name="set-up-locations-to-use-bins"></a>Impostare ubicazioni per l'utilizzo di collocazioni
Le collocazioni rappresentano la struttura di warehouse di base e vengono utilizzate per creare suggerimenti relativi al posizionamento degli articoli. Dopo avere creato le collocazioni desiderate, è possibile definire in modo specifico il contenuto che si desidera includere in ciascuna collocazione. In alternativa, è possibile utilizzare la collocazione come collocazione variabile, ovvero priva di contenuto specifico.  

Per utilizzare la funzionalità relativa alle collocazioni in un'ubicazione, è necessario prima attivarla nella scheda **Ubicazione**. Si progetterà quindi il flusso degli articoli nell'ubicazione specificando i codici di collocazione nei campi di setup che rappresentano i diversi flussi.  

> [!NOTE]  
>  Prima di poter specificare i codici di collocazione nella scheda Ubicazione, è necessario creare i codici di collocazione. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Per impostare un'ubicazione per l'utilizzo di collocazioni  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazioni** e quindi scegliere il collegamento correlato.  
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

## <a name="filling-the-consumption-bin"></a>Rifornimento della collocazione di consumo
Questo diagramma di flusso illustra in che modo il campo **Cod. collocazione** nelle righe del componente dell'ordine di produzione viene compilato in base al setup dell'ubicazione.

![Diagramma di flusso collocazione](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Vedere anche
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

---
title: 'Procedura: Spostare articoli ad hoc nelle configurazioni della warehouse di base | Documenti Microsoft'
description: "Talvolta può essere necessario spostare gli articoli tra le collocazioni interne, non le collocazioni di ricezione o spedizione, senza una richiesta specifica da un documento di origine. È possibile eseguire queste movimentazioni ad hoc, ad esempio per riorganizzare la warehouse, per immettere gli articoli in un'area di ispezione o inserire o estrarre articoli aggiuntivi da un'area di produzione senza una relazione di sistema al documento di origine dell'ordine di produzione."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7b753f291ebc4fefee523430e1b10d091e86cd0e
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Spostare articoli ad hoc nelle configurazioni della warehouse di base
Talvolta può essere necessario spostare gli articoli tra le collocazioni interne, non le collocazioni di ricezione o spedizione, senza una richiesta specifica da un documento di origine. È possibile eseguire queste movimentazioni ad hoc, ad esempio per riorganizzare la warehouse, per immettere gli articoli in un'area di ispezione o inserire o estrarre articoli aggiuntivi da un'area di produzione senza una relazione di sistema al documento di origine dell'ordine di produzione.  

Nelle configurazioni di base della warehouse, ovvero ubicazioni che utilizzano il campo del setup **Collocazione obbligatoria** ed eventualmente i campi di setup **Richiesto prelievo** e **Richiesto stoccaggio**, è possibile registrare le movimentazioni ad hoc senza documenti di origine nei seguenti modi:  

- Con la pagina **Movimentazione interna**.  
- Con la pagina **Registrazioni riclassificazione articolo**.  

> [!NOTE]  
>  Nelle configurazione warehouse avanzate, ovvero ubicazioni che utilizzano il campo del setup **Stoccaggi e prelievi guidati**, si utilizza la pagina **Prospetto movimentazioni** oppure la pagina **Prelievo interno whse.** o **Stoccaggio interno whse.** per spostare articoli ad hoc tra le collocazioni.  

## <a name="to-move-items-as-an-internal-movement"></a>Per spostare gli articoli come movimentazione interna  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Movimentazione interna** e quindi scegliere il collegamento correlato.  
2.  Nella Scheda dettaglio **Generale** compilare il campo **Nr.** uscendo dal campo o scegliendo il pulsante **AssistEdit** per selezionare tra la numerazione.  
3.  Nel campo **Cod. ubicazione** immettere l'ubicazione in cui si verifica la movimentazione.  

    Se l'ubicazione è impostata come ubicazione di default come impiegato warehouse, il codice ubicazione viene inserito automaticamente.  
4.  Nel campo **A codice collocazione** immettere un codice per la collocazione in cui si desidera spostare l'articolo. Ai fini della produzione, questo potrebbe essere il codice collocazione produzione aperta, ad esempio, come definito nella scheda Ubicazione o nell'area di produzione.  
5.  Nel campo **Data scadenza** immettere la data a partire dalla quale la movimentazione deve essere completata.  
6.  Nella Scheda dettaglio **Righe** selezionare il campo **Nr. articolo** per aprire la pagina **Lista contenuto collocazione** e selezionare l'articolo da spostare in base alla disponibilità nelle collocazioni. In alternativa, selezionare l'azione **Prendi contenuto collocazione** per compilare le righe movimentazione interna in base ai filtri. Per ulteriori informazioni, vedere la descrizione comando per l'azione **Ottieni contenuto collocazione**.   

    Dopo avere selezionato l'articolo, il campo **Dal codice collocazione** viene compilato automaticamente in base al contenuto della collocazione selezionata, ma è possibile modificarlo con qualsiasi altra collocazione in cui l'articolo è disponibile.  

    > [!NOTE]  
    >  Poiché il campo **Nr. articolo** e il campo **Dal codice collocazione** sono connessi, i relativi valori possono variare in modo interdipendente quando si modifica uno dei campi.  

    Il campo **A codice collocazione** viene compilato con il valore immesso nella testata, ma è possibile modificarlo nella riga con qualsiasi altro codice collocazione che non risulti bloccato o dedicato a scopi particolari. Per ulteriori informazioni sulla creazione di collocazioni dedicate, vedereDedicata.  
7.  Dopo avere impostato le collocazioni nelle quale e dalle quali si desidera spostare l'articolo, immettere la quantità da spostare nel campo **Quantità**.  

    > [!NOTE]  
    >  La quantità deve essere disponibile in Dal codice collocazione.  

8.  Quando si è pronti per elaborare la movimentazione interna, selezionare l'azione **Crea movimento di magazzino**.  

    > [!NOTE]  
    >  Dopo avere creato il movimento di magazzino, le righe movimentazione interna vengono eliminate.  

    Il resto della movimentazione ad hoc si effettua nella pagina **Movimento di magazzino** con la stessa procedura utilizzata per una movimentazione basata su documenti di origine. Per ulteriori informazioni, vedere ad esempio [Spostare componenti in un'area di operazione nelle configurazioni di warehouse di base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Per spostare articoli con le registrazioni di riclassificazione articolo
Anziché utilizzare documenti di movimento di warehouse, è possibile registrare lo spostamento di articoli riclassificando i relativi codici di collocazione. Per ulteriori informazioni, vedere [Conteggio, rettifica e riclassificazione dell'inventario](inventory-how-count-adjust-reclassify.md).   
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni riclass. articolo** e quindi scegliere il collegamento correlato.  
2.  In ogni riga di registrazione, definire le collocazioni da cui e in cui si desidera spostare articoli compilando i campi **Cod. collocazione** e **Nuovo cod. collocazione**.  

    1.  Per spostare l'intero contenuto di una collocazione in un'altra collocazione, scegliere l'azione **Prendi contenuto collocazione**.  
    2.  Compilare i filtri per trovare la collocazione di cui si desidera spostare il contenuto, quindi scegliere **OK**. Le righe di registrazione vengono compilate con il contenuto della collocazione.  
3.  Compilare i restanti campi di ogni riga di registrazione.   
4.  Registrare le registrazioni di riclassificazione.  

    > [!NOTE]  
    >  A differenza dei documenti di movimentazione, un movimento contabilizzato nelle registrazioni di riclassificazione non crea una richiesta warehouse per eseguire il task fisico.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


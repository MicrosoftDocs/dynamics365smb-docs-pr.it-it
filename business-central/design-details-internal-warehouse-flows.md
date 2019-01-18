---
title: 'Dettagli di progettazione: Flussi warehouse interni | Microsoft Docs'
description: "Il flusso di articoli in una collocazione all'interno della società si concentra sul prelievo di componenti e sullo stoccaggio degli articoli finali per gli ordini di produzione o di assemblaggio e i movimenti ad hoc, ad esempio i rifornimenti delle collocazioni, senza una relazione con i documenti di origine."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: b728815592975091a683eb96f87b1a632da62567
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-internal-warehouse-flows"></a>Dettagli di progettazione: Flussi warehouse interni
Il flusso di articoli in una collocazione all'interno della società si concentra sul prelievo di componenti e sullo stoccaggio degli articoli finali per gli ordini di produzione o di assemblaggio e i movimenti ad hoc, ad esempio i rifornimenti delle collocazioni, senza una relazione con i documenti di origine. L'ambito e la natura delle attività implicate variano tra la gestione di base e avanzata della warehouse.  

 Alcuni flussi interni si sovrappongono con flussi in entrata o in uscita. Alcuni flussi sovrapposti sono mostrati rispettivamente come passaggi 4 e 5 nei diagrammi grafici per i flussi in entrata e in uscita avanzati. Per ulteriori informazioni, vedere [Dettagli di progettazione: Flusso warehouse in entrata](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Flussi interni nella gestione di base della warehouse  
 In una configurazione di base della warehouse, il flusso di articoli tra collocazioni all'interno della società si concentra sul prelievo di componenti e sullo stoccaggio degli articoli finali per gli ordini di produzione o di assemblaggio e i movimenti ad hoc, ad esempio i rifornimenti delle collocazioni, senza relazione con i documenti di origine.  

### <a name="flows-to-and-from-production"></a>Flussi verso e dalla produzione  
 La principale integrazione tra gli ordini di produzione e le attività di base della warehouse è rappresentata dalla possibilità di prelevare i componenti di produzione con la pagina **Prelievo magazzino** o la pagina **Movimento magazzino**.  

> [!NOTE]  
>  Nella pagina **Prelievi magazzino** il consumo di componenti viene registrato insieme alla registrazione del prelievo. Tramite la pagina **Movimento di magazzino** solo le rettifiche della collocazione vengono registrate, non si verificano altre registrazioni dei movimenti contabili magazzino.  

 Oltre alla gestione dei componenti, l'integrazione è rappresentata dalla capacità di stoccare gli articoli prodotti con la pagina **Stoccaggio magazzino**.  

 I campi **Cod. coll. art. per produzione**, **Cod. coll. art. da produzione** e **Codice coll. produzione aperta** nella scheda ubicazione o nelle schede centro di lavoro/area di produzione definiscono i flussi predefiniti da e verso le aree di produzione.  

 Per ulteriori informazioni su come il consumo del componente è consuntivato dalla collocazione articoli per produzione o produzione aperta, vedere la sezione "Componenti di produzione di flushing nel magazzino" in questo argomento.  

### <a name="flows-to-and-from-assembly"></a>Flussi verso e dall'assemblaggio  
 La principale integrazione tra gli ordini di assemblaggio e le attività di base della warehouse è rappresentata dalla possibilità di spostare i componenti di assemblaggio nell'area di assemblaggio.  

 Quando non sono disponibili funzionalità di warehouse specifiche per lo stoccaggio di articoli di assemblaggio, il codice collocazione nell'intestazione dell'ordine di assemblaggio può essere impostato su una collocazione di stoccaggio predefinita. La registrazione dell'ordine di assemblaggio funziona quindi come la registrazione di uno stoccaggio. L'attività di warehouse di spostare gli articoli di assemblaggio nella warehouse può essere gestita tramite la pagina **Movimentazione interna**, senza alcuna relazione all'ordine di assemblaggio.  

 Sono disponibili i seguenti flussi di assemblaggio.  

|Workflow|Descrizione|  
|----------|---------------------------------------|  
|Assemblaggio per magazzino|I componenti sono necessari in un ordine di assemblaggio in cui l'output è archiviato nella warehouse.<br /><br /> Questo flusso di warehouse viene gestito nella pagina **Movimento di magazzino**. Una riga Prendere specifica dove prendere i componenti. Una riga Mettere specifica dove posizionare i componenti.|  
|Assemblaggio su ordine|I componenti sono necessari in un ordine di assemblaggio che è collegato a un ordine di vendita che viene spedito quando l'articolo venduto è assemblato.|  

> [!NOTE]  
>  Se gli articoli vengono assemblati su ordine, il prelievo magazzino dell'ordine di vendita collegato avvia un movimento di magazzino per tutti i componenti di assemblaggio implicati, non solo per l'articolo venduto come quando si spediscono gli articoli di magazzino.  

 I campi **Cod. coll. art. per assembl.**, **Cod. coll. art. da assembl.** e **Cod. coll. sp. ass. su ordine** nella scheda ubicazione definiscono i flussi di default da e verso le aree di assemblaggio.  

> [!NOTE]  
>  Il campo **Cod. coll. sp. ass. su ordine** funge da collocazione da assemblaggio negli scenari di assemblaggio su ordine.  

### <a name="ad-hoc-movements"></a>Movimenti ad hoc  
 Nella gestione di base della warehouse, lo spostamento degli articoli tra collocazioni senza relazione con i documenti di origine viene eseguito nella pagina **Movimentazione interna**, che viene utilizzata insieme alla pagina **Movimento di magazzino**.  

 Un altro modo per spostare gli articoli ad hoc tra le collocazioni è di registrare i movimenti positivi nel campo **Nuovo cod. collocazione** della pagina **Reg. riclass. articoli**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Flussi interni nella gestione avanzata della warehouse  
 Nelle configurazioni della warehouse avanzate, il flusso di articoli tra le collocazioni all'interno della società si concentra sul prelievo dei componenti e sullo stoccaggio degli articoli finali per gli ordini di produzione e sul prelievo di componenti per gli ordini di assemblaggio. Inoltre, i flussi interni si verificano come movimenti ad hoc, ad esempio rifornimenti collocazione, senza alcuna relazione con i documenti di origine.  

### <a name="flows-to-and-from-production"></a>Flussi Verso e Dalla produzione  
 La principale integrazione tra gli ordini di produzione e le attività avanzate della warehouse è rappresentata dalla possibilità di prelevare i componenti di produzione, nelle pagine **Prelievo warehouse** e **Prospetto prelievi**, e dalla possibilità di stoccare gli articoli prodotti tramite la pagina **Stoccaggio interno whse.**.  

 Un altro punto di integrazione nella produzione viene fornito con la pagina **Movimentazione warehouse**, insieme alla pagina Movimento worksheet, che consente di inserire i componenti e prelevare gli articoli prodotti per gli ordini di produzione rilasciati.  

 I campi **Cod. coll. art. per produzione**, **Cod. coll. art. da produzione** e **Codice coll. produzione aperta** nella scheda ubicazione o nelle schede centro di lavoro/area di produzione definiscono i flussi predefiniti da e verso le aree di produzione.  

 Per ulteriori informazioni su come il consumo del componente è consuntivato dalla collocazione articoli per produzione o produzione aperta, vedere la sezione "Componenti di produzione di flushing nel magazzino" in questo argomento.  

### <a name="flows-to-and-from-assembly"></a>Flussi verso e dall'assemblaggio  
 La principale integrazione tra gli ordini di assemblaggio e le attività avanzate della warehouse è rappresentata dalla possibilità di prelevare componenti di assemblaggio, sia con la pagina **Prelievo warehouse** sia con la pagina **Prospetto prelievi**. Questa funzionalità funziona come quando si prelevano componenti per gli ordini di produzione.  

 Quando non sono disponibili funzionalità di warehouse specifiche per lo stoccaggio di articoli di assemblaggio, il codice collocazione nell'intestazione dell'ordine di assemblaggio può essere impostato su una collocazione di stoccaggio predefinita. La registrazione dell'ordine di assemblaggio funziona quindi come la registrazione di uno stoccaggio. L'attività di warehouse di spostare gli articoli di assemblaggio nella warehouse può essere gestita tramite la pagina **Movimento worksheet** o la pagina **Stoccaggio interno whse.**, senza alcuna relazione all'ordine di assemblaggio.  

> [!NOTE]  
>  Se gli articoli vengono assemblati su ordine, la spedizione warehouse dell'ordine di vendita collegato avvia un prelievo warehouse per tutti i componenti di assemblaggio implicati, non solo per l'articolo venduto come quando si spediscono gli articoli di magazzino.  

 I campi **Cod. coll. art. per assembl.** e **Cod. coll. art. da assembl.** nella scheda ubicazione definiscono i flussi predefiniti da e verso le aree di assemblaggio.  

### <a name="ad-hoc-movements"></a>Movimenti ad hoc  
 Nella gestione avanzata della warehouse, lo spostamento di articoli tra collocazioni senza relazione con i documenti di origine viene gestito nella pagina **Movimento worksheet** e viene registrato nella pagina Movimentazione warehouse.  

## <a name="flushing-production-components-in-the-warehouse"></a>Consuntivazione componenti di produzione nel magazzino  
 Se impostati in una scheda articolo, i componenti prelevati con prelievi warehouse vengono registrati come consumati dall'ordine di produzione durante la registrazione del prelievo warehouse. Utilizzando il metodo **Prelievo+Aut.Inizio** e il metodo di flushing **Prelievo+Aut.Fine** la registrazione del prelievo attiva la registrazione del consumo correlata quando inizia la prima operazione o quando termina l'ultima operazione, rispettivamente.  

 Considerare il seguente scenario in base all'ubicazione BIANCA del database di esempio di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Esiste un ordine di produzione per 15 PZ dell'articolo LS-100. Alcuni degli articoli nell'elenco dei componenti devono essere consuntivati manualmente in una registrazione di consumo, mentre altri articoli dell'elenco possono essere prelevati e consuntivati automaticamente utilizzando il metodo di consuntivazione **Prelievo+Aut.Fine**.  

> [!NOTE]  
>  **Prelievo + Aut.Inizio** funziona solo se la seconda operazione della riga del ciclo di produzione utilizza un codice di legame ciclo-distinta base. Il rilascio di un ordine di produzione pianificato avvia la consuntivazione in avanti di componenti impostati su **Prelievo+Aut.Inizio**. Tuttavia, consuntivazione non può essere eseguita fino a quando il prelievo dei componenti non viene registrato, operazione che a sua volta può essere eseguita solo quando l'ordine viene rilasciato.  

 I seguenti passaggi descrivono le azioni implicate da utenti differenti e la risposta correlata:  

1.  Il supervisore di produzione rilascia l'ordine di produzione. Gli articoli con il metodo di consuntivazione in **Avanti** e privi di un codice di legame ciclo-distinta base vengono dedotti dalla collocazione produzione aperta.  
2.  Il supervisore di produzione fa clic sul pulsante **Creare il prelievo warehouse** nell'ordine di produzione. Un documento di prelievo warehouse viene creato per il prelievo degli articoli con i metodi di flushing **Manuale**, **Prelievo + Indietro** e **Prelievo + Avanti**. Questi articoli si trovano nella collocazione articoli per produzione.  
3.  Il responsabile di warehouse assegna i prelievi a un lavoratore warehouse.  
4.  L'addetto warehouse seleziona gli articoli dalle collocazioni appropriate e li inserisce nella collocazione articoli per produzione o nella collocazione specificata nel prelievo warehouse, che può essere una collocazione centro di lavoro o area di produzione.  
5.  L'addetto warehouse registra il prelievo. La quantità viene sottratta dalle collocazioni di prelievo e aggiunta alla collocazione di consumo. Il campo **Qtà prelevata** nell'elenco dei componenti per tutti gli articoli selezionati viene aggiornato.  

    > [!NOTE]  
    >  Solo la quantità che è prelevata può essere utilizzata.  

6.  L'operatore di macchina informa il responsabile di produzione che gli articoli finali sono terminati.  
7.  Il supervisore di produzione utilizza le registrazioni di produzione o di consumo per registrare il consumo di articoli componenti che utilizzano il metodo di consuntivazione **Manuale** o i metodi di consuntivazione **Avanti** o **Prelievo+Aut.Inizio** insieme ai codici di legame del ciclo.  
8.  Il responsabile di produzione registra l'output dell'ordine di produzione e modifica lo stato in **Completato**. La quantità di articoli componenti che utilizzano il metodo di consuntivazione **Da fine ordine** viene dedotta dalla collocazione produzione aperta e la quantità di articoli componente che utilizzano il metodo di consuntivazione **Prelievo+Aut.Fine** viene dedotta dalla collocazione articoli per produzione.  

 Nell'illustrazione seguente viene mostrato quando il campo **Cod. collocazione** nell'elenco di componenti viene compilato in base all'ubicazione o all'impostazione area di produzione/centro di lavoro.  

 ![Panoramica del momento e della modalità con cui il campo Codice collocazione viene compilato](media/binflow.png "Panoramica del momento e della modalità con cui il campo Codice collocazione viene compilato")  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)


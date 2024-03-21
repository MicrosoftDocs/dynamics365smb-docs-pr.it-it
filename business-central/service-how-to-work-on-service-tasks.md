---
title: Come utilizzare i compiti di assistenza
description: Questo argomento tratta i diversi modi di lavorare con i compiti di assistenza. La pagina Compiti di assistenza fornisce una sintesi di tutti gli articoli in assistenza che richiedono attenzione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Utilizzare i compiti di assistenza
Dopo aver creato un ordine o un'offerta di assistenza, registrato righe di articoli in assistenza e assegnato risorse agli articoli in assistenza nell'ordine o nell'offerta, è possibile iniziare la riparazione e la manutenzione di tali articoli.  

[!INCLUDE[prod_short](includes/prod_short.md)] dispone di una pagina **Compiti di assistenza** che fornisce una sintesi di tutti gli articoli in assistenza che richiedono attenzione. È possibile considerarla una sorta di pannello di comando dell'assistenza, da dove poter visualizzare gli ordini in sospeso, cercare e registrare pezzi di ricambio e mantenere aggiornato il magazzino.  

Per tenere traccia delle modifiche e ottenere una vista grafica dell'andamento dell'attività di assistenza, si possono utilizzare gli strumenti statistici di [!INCLUDE[prod_short](includes/prod_short.md)] , che consentono di generare rapidamente e automaticamente grafici e analisi di vario tipo.  

## Per utilizzare un compito di assistenza  
1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"). immetti **Task assistenza**, quindi scegli il collegamento correlato.
2. Se vuoi una lista dei compiti di assistenza a cui sono assegnati una risorsa o un gruppo di risorse specifico, compila il campo **Filtro per risorsa** o **Filtro gruppo risorse** e premi <kbd>INVIO</kbd>.  
3. Se vuoi una lista di compiti di assistenza con una o più date di risposta specifiche che rientrano in un determinato intervallo di date, compila il campo **Filtro data di risposta**, quindi premi <kbd>INVIO</kbd>.  
4. Se vuoi una lista di compiti di assistenza con un determinato stato di assegnazione o riparazione, compila il campo **Filtro stato assegnazione** o **Filtro cod. stato riparaz.** e premi <kbd>INVIO</kbd>.  
5. Selezionare il compito di assistenza che si desidera utilizzare. Scegliere l'azione **Prospetto interv. articolo**. Verrà visualizzata la pagina **Prospetto articoli in assistenza**.  
6. Registrare i testi standard, i pezzi di ricambio, le ore e i costi relativi alle risorse utilizzando le opzioni corrispondenti nel campo **Tipo**: \<Blank\>, **Articolo**, **Risorsa** e **Costo**.  
7. Nel campo **Stato riparazione** selezionare lo stato appropriato.  

   > [!NOTE]  
   >  Compilare il campo **Stato riparazione** con lo stato **Completato** o **Parzialmente assistito** se l'articolo in assistenza è stato completamente assistito o se un'altra risorsa continuerà l'assistenza. Lo stato **Completato** o **Riassegnazione necessaria** viene specificato automaticamente per il movimento di assegnazione corrispondente all'articolo in assistenza.  

## Per registrare le operazioni di assistenza  
Quando si esegue un'operazione di assistenza relativa a un ordine specifico, è possibile registrarne i dettagli specificando gli articoli utilizzati, i costi sostenuti e il tempo impiegato. I dati specificati vengono archiviati nella pagina **Prospetto articoli in assistenza**. Se necessario, è possibile aggiornare i dati.

1. Scegli la ![lampadina che apre la funzione Dimmi 2](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"). immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di assistenza per registrare le operazioni di assistenza e scegliere la riga dell'articolo.  
3. Scegliere l'azione **Prospetto articoli in assistenza**.  
4. Nelle righe specificare gli articoli utilizzati, i costi sostenuti e il tempo impiegato per prestare assistenza.  

   > [!NOTE]  
   >  È possibile registrare le operazioni di assistenza direttamente sulle righe di assistenza collegate all'ordine di assistenza.  

## Per registrare i pezzi di ricambio  
Quando si elaborano gli articoli in assistenza negli ordini di assistenza, potrebbe essere necessario utilizzare i pezzi di ricambio per l'assistenza. La seguente procedura indica come registrare i pezzi di ricambio che si utilizzano nella pagina **Prospetto Art. in Assist.**  

1. Scegli la ![lampadina che apre la funzione Dimmi 3](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"). , entrare in **Attività di servizio**, e poi scegliere il link relativo.
2. Scegliere la riga che comprende l'articolo in assistenza appropriato, quindi scegliere l'azione **Prospetto interv. articolo**.  
3. Immettere una nuova riga di assistenza.  
4. Nel campo **Tipo** scegliere **Articolo**.  
5. Nel campo **Nr.** selezionare il pezzo di ricambio appropriato.  
6. Nel campo **Quantità** immettere la quantità di articoli da utilizzare.  

 È possibile utilizzare una procedura simile per registrare i pezzi di ricambio nella pagina **Righe assistenza**, che è possibile aprire dalla pagina **Ordine assistenza**.  

## Per registrare i pezzi di ricambio da un ordine di assistenza  
1. Scegli la ![lampadina che apre la funzione Dimmi 4.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Ordini di servizio**, e poi scegliere il link relativo.  
2. Aprire l'ordine di assistenza per cui si desidera registrare pezzi di ricambio.  
3. Scegliere la riga che include l'articolo in assistenza appropriato. Scegliere **Azioni**, quindi **Ordine** e infine **Righe assistenza**.  
4. Immettere una nuova riga di assistenza.  

## Per sostituire un articolo in assistenza o un componente dell'articolo in assistenza  
Quando si presta assistenza ad un articolo in assistenza composto da diverse parti, potrebbe essere necessario sostituire un componente guasto con uno nuovo. Ogni volta che si immette un pezzo di ricambio per un articolo in assistenza composto da varie parti, si ha la possibilità di sostituire un componente o di crearne uno nuovo. Il nuovo articolo non viene registrato come componente dell'articolo in assistenza prima della registrazione della riga o dell'ordine di assistenza.

1. Scegli la ![lampadina che apre la funzione Dimmi 5.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Attività di servizio**, e poi scegliere il link relativo.
2. Scegliere la riga che comprende l'articolo in assistenza, quindi scegliere l'azione **Prospetto art. in assist.**.  
3. Immettere una nuova riga di assistenza.  
4. Nel campo **Tipo** scegliere **Articolo**.  
5. Nel campo **Nr.** selezionare il componente da sostituire.  
6. Seleziona <kbd>INVIO</kbd>. Verrà visualizzata una finestra di dialogo con tre opzioni: **Sostituisci componente**, **Nuovo componente** e **Ignora**. Nella seguente tabella vengono illustrate le opzioni.  

    |Opzione | Description|  
    |----------------------------------|---------------------------------------|  
    |**Sostituisci componente**|Lo stato del componente in sostituzione diventa inattivo, mentre il componente viene visualizzato nella lista dei componenti sostituiti per l'articolo in assistenza.|  
    |**Nuovo componente**|Il nuovo componente viene immesso nella lista componenti dell'articolo in assistenza.|  
    |**Ignora**|La lista dei componenti dell'articolo in assistenza non viene modificata.|  

7. Scegliere **Sostituisci componente**.  
8. Scegliere il componente da sostituire quindi scegliere **OK**.  

## Per modificare il tempo di risposta per una riga di articolo in assistenza  
Quando si registra una riga di articolo in assistenza in un ordine o in un'offerta di assistenza, a seconda che l'articolo in assistenza sia incluso in un contratto di assistenza o meno, viene automaticamente immesso il tempo di risposta espresso in ore e vengono calcolate di conseguenza la data e l'ora della risposta. Se necessario, è possibile modificare il tempo di risposta in ore e la data e l'ora di risposta.  

1. Scegli la ![lampadina che apre la funzione Dimmi 6.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza** o **Offerte assistenza**, quindi seleziona il collegamento correlato.  
2. Scegliere l'ordine o l'offerta di assistenza per aprire la scheda.  
3. Nella riga dell'articolo in assistenza per cui si desidera modificare il tempo di risposta, immettere il nuovo tempo di risposta espresso in ore oppure la data e l'ora di risposta nel campo **Tempo risposta (ore)** o nei campi **Data risposta** e **Ora risposta**.  

## Per registrare i codici di guasto/risoluzione  
In seguito alla riparazione dell'articolo in assistenza, è possibile registrare il codice guasto e il codice risoluzione per l'articolo, selezionando una combinazione delle relazioni esistenti dei codici guasto/risoluzione. I codici guasto e risoluzione verranno visualizzati nei campi corrispondenti nella pagina **Prospetto articoli in assistenza**. È possibile inoltre registrare i codici direttamente in questa pagina.  

1. Scegli la ![lampadina che apre la funzione Dimmi 7.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , entrare in **Attività di servizio**, e poi scegliere il link relativo.
2. Scegliere la riga che comprende l'articolo in assistenza appropriato, quindi scegliere l'azione **Prospetto interv. articolo**.  
3. Nella pagina **Prospetto articoli in assistenza** scegliere **Relazioni codici guasto/risoluzione**. Viene aperta la pagina **Relazioni codici guasto/risoluzione**.  

  >  [!NOTE]
  >  I filtri vengono impostati nelle relazioni visualizzate nella pagina copiando il gruppo di articoli in assistenza e i codici guasto dalla pagina **Prospetto articoli in assistenza**.  

4. Compilare la riga. Scegliere la corretta combinazione di codici guasto e risoluzione, quindi scegliere **OK** per copiarla nell'articolo in assistenza. Se non si riesce a trovare una combinazione corretta è possibile creare una nuova combinazione nella pagina.  

## Vedi anche  
[Impostare il reporting dei guasti](service-how-setup-fault-reporting.md)
[Stato di assegnazione e stato di riparazione](service-allocation-status-and-repair-status.md)  
[Registrazione di assistenza](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
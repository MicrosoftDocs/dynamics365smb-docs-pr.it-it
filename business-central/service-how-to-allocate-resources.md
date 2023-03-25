---
title: 'Procedura: Assegnare risorse | Documenti Microsoft'
description: È possibile modificare l'importo annuo del contratto di assistenza o dell'offerta di contratto per correggere l'importo da fatturare annualmente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# Assegnare risorse
L'elemento chiave della gestione dell'assistenza sono le persone che forniscono i servizi di assistenza. È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo da assegnare le persone ai processi in modo appropriato. Le assegnazioni possono essere effettuate in base alle zone di assistenza in cui il personale è dislocato oppure a dove l'intervento di assistenza avrà luogo. Quando si risponde a richieste di assistenza è inoltre possibile raggruppare le risorse. Per ulteriori informazioni, vedere [Impostare l'assegnazione delle risorse](service-how-setup-resource-allocation.md).

È possibile assegnare le risorse, ad esempio i tecnici, utilizzando il **Quadro attività** o da un ordine di assistenza. È possibile utilizzare la disponibilità delle risorse per assegnare risorse che svolgano compiti di assistenza negli ordini o nelle offerte.

È possibile assegnare la stessa risorsa, ad esempio un tecnico, o un gruppo di risorse a tutti gli articoli in assistenza di un ordine di assistenza. Vengono creati movimenti di assegnazione per gli altri articoli in assistenza nell'ordine con lo stesso numero di risorsa e data di assegnazione della riga assegnata. Le ore assegnate sono le ore assegnate divise per il numero di articoli in assistenza nell'ordine. Il campo **Stato** viene automaticamente impostato su **Attivo** per tutti i movimenti creati.

## Per visualizzare una sintesi degli ordini e delle offerte di assistenza  
Spesso è necessario visualizzare la lista degli ordini di assistenza o delle offerte di assistenza che soddisfano determinati criteri per potere eseguire operazioni specifiche su un ordine o un'offerta alla volta. Ad esempio, è possibile che occorra assegnare delle risorse agli ordini di assistenza che appartengono a un cliente specifico.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Quadro attività**, quindi scegli il collegamento correlato.  
2. Nel campo **Filtro documento** scegliere il tipo di documenti che si desidera visualizzare.
3. Per ottenere una lista di documenti che contengono compiti di assistenza a cui sono assegnati una risorsa o un gruppo di risorse specifici, compila i campi **Filtro per risorsa** e **Filtro gruppo risorse**, quindi premi <kbd>Invio</kbd>.  
4. Per ottenere una lista di documenti con una o più date di risposta specifiche che rientrano in un determinato intervallo di date, compila il campo **Filtro data di risposta**, quindi premi <kbd>Invio</kbd>.  
5. Per ottenere una lista di documenti con uno stato di assegnazione o uno stato di documento specifico, compila il campo **Filtro assegnazione/Filtro stato**, quindi premi <kbd>Invio</kbd>.  
6. Per ottenere una lista di documenti che appartengono a un contratto, un cliente o una zona specifici, compila il campo **Filtro Contratto/Filtro Cliente/Filtro per Zona**, quindi premi <kbd>Invio</kbd>.  
7. Scegliere una riga corrispondente a un ordine di assistenza o a un'offerta di assistenza, quindi scegliere l'azione **Mostra documento**.  

    Viene aperta la pagina **Ordine assistenza** o **Offerta assistenza** in cui è possibile utilizzare il documento. Per tornare alla pagina **Quadro attività** scegliere **OK**.

## Per assegnare una risorsa usando la disponibilità della risorsa o del gruppo di risorse    
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Quadro attività**, quindi scegli il collegamento correlato.  
2. Scegliere l'ordine di assistenza, quindi scegliere l'azione **Assegnazioni risorse**.  
3. Scegliere il movimento con il compito di assistenza a cui si desidera assegnare una risorsa.  
4. Scegliere l'azione **Disponibilità risorse** o **Disponibilità cat. ris.**.  
5. Nella pagina **Disponibilità ris.(assistenza)** scegliere **Mostra matrice**.  
6. Scegliere una risorsa da assegnare. Alcuni criteri di selezione possono essere se la risorsa è competente per il compito, se si trova nella zona cliente e/o se è la preferita del cliente.  
7. Specificare una data in cui la risorsa abbia abbastanza ore disponibili per il compito e che sia vicina alla data di risposta dell'ordine di assistenza.  
8. Nel campo **Quantità da assegnare** immettere il numero di ore per cui si intende assegnare la risorsa al compito di assistenza.  
9. Scegliere l'azione **Assegna** per assegnare la risorsa selezionata alla data selezionata.  

     Il campo **Stato** viene impostato su **Attivo**.  

 Ripetere i passaggi indicati per ogni data in cui si intende assegnare la risorsa al compito di assistenza.  

> [!NOTE]  
>  Per un articolo in assistenza in un ordine di assistenza possono esistere soltanto movimenti di assegnazione con stato **Attivo** con una risorsa o un gruppo di risorse alla volta.  

## Per assegnare una risorsa tramite un ordine di assistenza  
Dopo avere creato e compilato un ordine di assistenza o un'offerta di assistenza, è possibile assegnare le risorse, ad esempio i tecnici. per eseguire i compiti di assistenza registrati come righe di articoli in assistenza nel documento.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Scegliere l'ordine di assistenza, quindi scegliere **Modifica**.  
3. Scegliere la riga dell'articolo in assistenza corrispondente al compito di assistenza a cui si desidera assegnare una risorsa.  
4. Scegliere **Assegnazioni risorse**.
5. Nella pagina **Assegnazioni risorse** scegliere un movimento di assegnazione non attivo con il compito di assistenza a cui si desidera assegnare la risorsa. Se il movimento di questo tipo non esiste, è possibile crearne uno scegliendo **Nuovo**.  
7. Specificare il compito di assistenza compilando il campo **Nr. articolo in assistenza** nella stessa riga.  
8. Nel campo **Nr. risorsa** scegliere la risorsa. Se la risorsa fa parte di un gruppo di risorse, il numero del gruppo di risorse verrà automaticamente immesso nel campo **Nr. gruppo risorse** .  
9. Compilare i campi **Data assegnazione** e **Ore assegnate**. Il campo **Stato** verrà impostato su **Attivo**. Ciò significa che la risorsa è assegnata al compito di assistenza.  
10. Facoltativamente, assegnare la risorsa a tutti gli articoli, scegliere **Assegna a tutti articoli assistenza**.

> [!NOTE]  
>  Per un articolo in assistenza in un ordine di assistenza possono esistere soltanto movimenti di assegnazione con stato Attivo con una risorsa o un gruppo di risorse alla volta.

## Per riassegnare le risorse su un ordine di assistenza  
È possibile riassegnare le risorse direttamente da un ordine di assistenza o da un'offerta di assistenza su cui si sta lavorando. Il movimento originale esisterà ancora, ma il relativo stato viene aggiornato come segue:  

* Se l'assistenza è iniziata quando l'assegnazione aveva stato **Attivo**, ovvero se lo stato di riparazione dell'articolo in assistenza nel movimento è diventato **In corso**, lo stato di assegnazione passerà da **Riassegnazione necessaria** a **Completato**.  
* Se l'assistenza non è iniziata quando l'assegnazione aveva stato **Attivo**, lo stato di assegnazione passerà da **Riassegnazione necessaria** ad **Annullato**.  
* Se si sta riassegnando un ordine di assistenza convertito da un offerta, lo stato dei movimenti di assegnazione registrati per l'offerta diventerà sempre **Completato** durante la riassegnazione degli articoli in assistenza nell'ordine di assistenza.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di assistenza desiderato.  
3. Selezionare la riga di un articolo in assistenza corrispondente al compito di assistenza a cui si desidera assegnare una risorsa e scegliere l'azione **Assegnazioni risorse**.  
4. Nella pagina **Assegnazioni risorse** selezionare un movimento di assegnazione con il compito di assistenza a cui si desidera riassegnare la risorsa. Nel campo **Nr. risorsa** selezionare la risorsa appropriata. Il numero della risorsa presente nel campo verrà sovrascritto.  
5. Seleziona <kbd>INVIO</kbd>. Verrà visualizzata una finestra di dialogo che chiederà se si intende riassegnare il movimento. Compilare il campo **Causale** se necessario e fare clic su **Sì** per confermare la riassegnazione.  
6. Compilare i campi **Data assegnazione** e **Ore assegnate**. Il movimento ora contiene la nuova risorsa e il relativo stato è **Attivo**.

## Per riassegnare una risorsa tramite la finestra Quadro attività  
Se la risorsa assegnata a un compito di assistenza non è in grado di svolgere il lavoro, il compito di assistenza dovrà essere riassegnato. Solitamente la riassegnazione delle risorse a un compito di assistenza viene effettuata mediante la finestra **Quadro attività**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Quadro attività**, quindi scegli il collegamento correlato.  
2. Nel campo **Filtro Assegnazione** selezionare **Riassegnazione Necessaria**. Nella pagina **Quadro Attività** verrà visualizzata la lista degli ordini di assistenza che includono compiti di assistenza da riassegnare.  
3. Selezionare l'ordine di assistenza appropriato, quindi scegliere l'azione **Assegnazioni risorse**. Verrà visualizzata la pagina **Assegnazioni risorse**.  
4. Selezionare il movimento di assegnazione con il compito di assistenza a cui si intende riassegnare una risorsa.  
5. Nel campo **Nr. risorsa** selezionare la risorsa appropriata. Il numero della risorsa presente nel campo verrà sovrascritto.  
6. Seleziona <kbd>INVIO</kbd>. Viene aperta la finestra di dialogo **Causali riassegnaz. movimenti** in cui viene chiesto se si desidera riassegnare il movimento. Compilare il campo **Causale** se necessario e fare clic su **Sì** per confermare la riassegnazione.  
7.  Compilare i campi **Data assegnazione** e **Ore assegnate**. Il movimento ora contiene la nuova risorsa e il relativo stato è **Attivo**.  

    > [!NOTE]  
    >  Il movimento precedente esiste ancora, ma il relativo stato viene aggiornato come segue.  
    >   
    >  * Se l'assistenza è iniziata quando l'assegnazione aveva stato **Attivo**, ovvero se lo stato di riparazione dell'articolo in assistenza nel movimento è diventato **In corso**, lo stato di assegnazione passerà da **Riassegnazione necessaria** a **Completato**.  
    > * Se l'assistenza non è iniziata quando l'assegnazione aveva stato **Attivo**, lo stato di assegnazione passerà da **Riassegnazione necessaria** ad **Annullato**.  
    > * Se si sta riassegnando un ordine di assistenza convertito da un offerta, lo stato dei movimenti di assegnazione registrati per l'offerta diventerà sempre **Completato** durante la riassegnazione degli articoli in assistenza nell'ordine di assistenza.  

## Per registrare le ore di risorse  
Durante l'elaborazione degli articoli in assistenza negli ordini di assistenza, occorre registrare le ore di risorse per l'assistenza. La seguente procedura indica come registrare le ore delle risorse nella pagina **Prospetto Art. in Assist.**  

È possibile utilizzare la stessa procedura per registrare le ore nella pagina **Righe assistenza**, che è possibile aprire dalla pagina Ordine assistenza. Aprire la scheda di assistenza appropriato, quindi scegliere l'azione **Righe assistenza**.  

Se si utilizza la stessa risorsa per tutti gli articoli in assistenza nell'ordine di assistenza, è possibile registrare le ore totali della risorsa per un articolo in assistenza soltanto e poi dividere la riga della risorsa in modo da assegnarne le ore agli altri articoli in assistenza.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Task assistenza**, quindi scegli il collegamento correlato.
2. Selezionare la riga che comprende l'articolo in assistenza appropriato, quindi scegliere l'azione **Prospetto interv. articolo**.  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Per assegnare una risorsa a tutti gli articoli in assistenza in un ordine
Se la stessa risorsa, ad esempio un tecnico, opera su tutti gli articoli in assistenza nell'ordine di assistenza, è possibile registrare le ore totali della risorsa per un solo articolo in assistenza e poi dividere la riga delle risorse per suddividere le ore delle risorse nelle righe delle risorse per gli altri articoli in assistenza.  

La seguente procedura mostra come dividere le righe della risorsa nella pagina **Righe Fattura Assistenza**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Aprire l'ordine di assistenza desiderato.  
3. Nella Scheda dettaglio **Righe** scegliere l'azione **Righe assistenza**. Viene visualizzata la pagina **Righe assistenza**.  
4. Selezionare la riga della risorsa che si intende suddividere. Il contenuto del campo **Quantità** viene suddiviso tra tutti gli articoli in assistenza nell'ordine.  
5. Scegliere l'azione **Dividi riga risorse**. Scegliere **Sì** per confermare.  

    Vengono create righe delle risorse per gli altri articoli in assistenza nell'ordine con lo stesso numero di risorsa della riga divisa. La quantità corrisponde alla quantità della riga suddivisa divisa per il numero di articoli in assistenza nell'ordine.  

## Per eliminare un assegnazione  
È possibile eliminare le assegnazioni risorse per i compiti di assistenza senza riassegnare i compiti.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Quadro attività**, quindi scegli il collegamento correlato.  
2. Scegliere l'ordine di assistenza, quindi scegliere l'azione **Assegnazioni risorse**.  
3. Scegliere il movimento di assegnazione con il compito di assistenza per cui si intende eliminare un'assegnazione.  
4. Scegliere l'azione **Elimina assegnazione**.  
5. Nel campo **Causale** selezionare la causale appropriata.  
6. Scegliere **Sì** per confermare l'eliminazione.  

    > [!NOTE]  
    > Nel campo **Stato** verrà automaticamente selezionata l'opzione **Riassegnazione necessaria**. Se lo stato di riparazione dell'articolo in assistenza nel movimento è **Iniziale**, verrà impostato su **Demandato**, che indica che l'assistenza non è iniziata. Se lo stato di riparazione è **In corso**, passerà a **Parzialmente assistito**, ovvero parte dell'assistenza è stata completata.

## Vedi anche
[Impostare l'assegnazione delle risorse](service-how-setup-resource-allocation.md)  
[Stato assegnazione e stato riparazione](service-allocation-status-and-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
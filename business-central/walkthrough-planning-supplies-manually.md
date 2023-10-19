---
title: Procedura dettagliata - Pianificazione manuale degli approvvigionamenti
description: 'Questa procedura dettagliata illustra il processo di pianificazione degli ordini di approvvigionamento per soddisfare la nuova domanda, inclusa la pianificazione di un ordine di acquisto, trasferimento e produzione.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# <a name="walkthrough-planning-supplies-manually"></a>Procedura dettagliata: Pianificazione manuale degli approvvigionamenti

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

La presente procedura dettagliata illustra il processo di pianificazione degli ordini di approvvigionamento per soddisfare una nuova domanda. È possibile avviare la pianificazione dell'approvvigionamento a intervalli fissi, ad esempio ogni mattina o ogni lunedì, oppure su notifica del personale di vendita o di produzione. Nella procedura dettagliata viene impiegata a tal fine la pagina **Pianificazione ordini**, un semplice strumento di pianificazione degli approvvigionamenti che prevede la decisione e l'intervento manuale dell'utente anziché utilizzare parametri predefiniti per la pianificazione automatica.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata
 In questa procedura dettagliata sono illustrati i task seguenti:  

-   Pianificazione di un ordine di acquisto per componenti di manufacturing  
-   Pianificazione di un ordine di trasferimento per soddisfare la domanda di vendita  
-   Pianificazione di un ordine di produzione di un articolo multilivello  

## <a name="roles"></a>Ruoli
 Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Responsabile pianificazione produzione  
-   Rivenditore  
-   Gestore degli ordini di vendita  

## <a name="prerequisites"></a>Prerequisiti
 Prima di iniziare questa procedura dettagliata, occorre installare [!INCLUDE[prod_short](includes/prod_short.md)]. Le seguenti modifiche devono essere apportate al database:  

-   Eliminare tutti gli ordini di biciclette esistenti  
-   Creare un ordine di vendita per 10 biciclette per l'ubicazione EST.  
-   Eliminare tutti gli ordini di produzione confermati e pianificati. Non eliminare gli ordini avviati con movimenti già registrati.  

 Come regola generale, si raccomanda di utilizzare i dati suggeriti nella procedura perché dispongono dei record necessari.  

## <a name="story"></a>Scenario
 Eduardo, l'addetto alla pianificazione della produzione di una piccola società , si sta apprestando a pianificare la produzione e gli ordini di acquisto per soddisfare una nuova domanda di vendita.  

 Poiché i prodotti hanno pochi livelli di distinta base e il flusso degli ordini è relativamente basso, Eduardo utilizza la pagina **Pianificazione ordini** per creare manualmente gli ordini di approvvigionamento — un livello di prodotto per volta.  

 In un ambiente produttivo più complesso, per pianificare gli approvvigionamenti viene utilizzato il prospetto pianificazione, che applica parametri specifici degli articoli come periodo di riprogrammazione, lead time di sicurezza, punto di riordino e calcoli batch della domanda consolidata per tutti i livelli di prodotto.  

## <a name="setting-up-the-sample-data"></a>Impostazione dei dati di esempio
 La società di esempio CRONUS standard ha attualmente elevati livelli di domanda non pianificata. Durante le differenti attività di pianificazione di questa procedura dettagliata, sarà necessario deviare dalla realtà del flusso aziendale ignorando le domande con data di scadenza prossima e dedicandosi invece a quelle con data di scadenza più lontana nel tempo.  

## <a name="use-the-order-planning-page"></a>Utilizzare la pagina Pianificazione ordini

È possibile accedere alla pagina **Pianificazione ordini** da diverse posizioni:  

-   Manufacturing, Pianificazione  
-   Vendite e marketing, Gestione ordini  
-   Acquisto, Pianificazione  
-   È inoltre possibile aprire questa pagina per un ordine di produzione specifico selezionando l'azione **Pianificazione**.

### <a name="to-use-the-order-planning-page"></a>Per utilizzare la pagina Pianificazione ordini

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Pianificazione ordini**, quindi scegli il collegamento correlato.  

     Alla prima apertura della pagina **Pianificazione ordini**, è necessario calcolare un piano per mostrare la nuova domanda dall'ultimo calcolo.  

2.  Scegliere l'azione **Calcola piano**.  

     Il sistema di pianificazione analizza tutte le nuove domande introdotte, come nuove vendite, modifiche alle vendite e ordini di produzione.  

     La quantità necessaria di ogni riga della domanda viene calcolata sulla base della disponibilità totale. Il calcolo viene eseguito ordine per ordine. Ciò significa che l'ordine che include la riga di domanda con la prima data di scadenza o di spedizione utile verrà calcolato per primo. Dopo questa operazione, le righe di domanda aggiuntive saranno calcolate nello stesso ordine, indipendentemente dalla data di scadenza o la data di spedizione.  

3.  Ingrandire la pagina **Pianificazione ordini** e ridimensionare i campi delle colonne in modo che tutti i nomi di campo predefiniti siano visibili.  

     Al termine del calcolo, nella pagina sono visualizzate tutte le domande non soddisfatte in righe di testata d'ordine compresse e ordinate in base alla data di richiesta più prossima.  

     Si noti che CRONUS ha diversi ordini con domanda non soddisfatta. Ogni riga di pianificazione in grassetto rappresenta un ordine - di vendita o di produzione - comprendente almeno una riga con disponibilità insufficiente.  

4.  Nel campo **Mostra domanda come** selezionare il filtro **Tutta la domanda**.  

     Il campo **Tipo domanda** consente di scegliere i tipi di ordini da visualizzare.  

     Gli ordini che non presentano problemi di disponibilità non sono visualizzati. Se non esistono ordini nel momento in cui il piano viene calcolato, verrà visualizzato un messaggio e non verrà riportata alcuna riga di pianificazione.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Pianificazione di un ordine di acquisto per soddisfare la domanda di componenti
 In questa procedura viene creato un ordine di acquisto per i componenti necessari per la produzione.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Per pianificare un ordine di acquisto per i componenti necessari per la produzione

1.  Espandere la prima riga (fare clic sul simbolo +).  
2.  Scegliere la prima riga di domanda, con l'articolo **LSU-15**, quindi scegliere l'azione **Mostra documento**.  
3.  Chiudere l'ordine di produzione aperto per tornare alla pagina **Pianificazione ordini**.  
4.  Nel campo **Sistema di rifornimento** selezionare **Acquisto**.  

     Il valore di default corrisponde alla scheda articolo (o scheda USK), ma è possibile modificarlo selezionando una delle opzioni seguenti:  

    -   **Acquisto**: per creare un ordine di acquisto  
    -   **Trasferimento**: per creare un ordine di trasferimento  
    -   **Ord. prod.**: per creare un ordine di produzione  

5.  Nel campo **Approvvigionamento da** selezionare una delle opzioni seguenti in base al sistema di rifornimento specificato:  

    -   **Fornitore** - Per acquisti  
    -   **Ubicazione** – Per i trasferimenti  

     Se il campo è lasciato vuoto, viene visualizzato un messaggio di errore quando si cerca di creare gli ordini di approvvigionamento.  

    > [!NOTE]  
    >  Se nelle schede articolo è impostato un fornitore predefinito per i componenti, le righe saranno precompilate.  

6.  Selezionare il campo **Approvvigionamento da** .  
7.  Nella pagina **Catalogo art. fornitori** scegliere l'azione **Nuovo** e selezionare il fornitore **30000**.  
8.  Fare clic su **OK** per tornare alla pagina **Pianificazione ordini**.  
9. Copiare il fornitore **30000** nelle altre righe del componente "altoparlante" nell'ordine di produzione.  

     È ora possibile creare un ordine di acquisto.  

10. Scegliere l'azione **Crea ordini**. Viene visualizzata la pagina **Crea ordini approvvigionamento**.  
11. Nella Scheda dettaglio **Pianificazione ordini**, nel campo **Crea ordini per**, selezionare l'opzione **Ordine attivo**.  
12. Nel campo **Crea ordini di acquisto** della Scheda dettaglio **Opzioni** scegliere l'opzione **Crea ordini acquisto**.  
13. Scegliere **OK** per creare ordini di acquisto per tutti i componenti dell'ordine.  

     Gli ordini di acquisto sono ora creati e sono salvati come ultimi nella lista degli ordini di acquisto.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Pianificazione di un ordine di trasferimento per soddisfare la domanda di vendita
 In questa procedura si pianificherà la domanda per un ordine di vendita. Le righe di domanda rappresentano righe di vendita e non righe di componenti, come nella domanda di produzione.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Per pianificare un ordine di trasferimento per soddisfare la domanda di vendita

1.  Spostare il puntatore nella riga di pianificazione dell'ordine **2008**.  
2.  Espandere la riga e spostare il puntatore sulla riga di domanda.  

     L'ordine di vendita numero **2008** è per dieci altoparlanti di tipo **LS-120**, ordinati da Rotadent ingranaggi S.r.l.  

     Vengono visualizzati il sistema di rifornimento e il venditore predefiniti dell'articolo.  

    > [!NOTE]  
    >  Nella parte inferiore della pagina sono presenti quattro campi informativi. Il campo **Prima data disponibile** indica che i dieci pezzi necessari saranno disponibili, in un ordine di approvvigionamento in entrata, nove giorni dopo la data di scadenza corrente. Il campo **Disponibile per trasferimento** indica che in un'altra ubicazione sono presenti 13 pezzi dello stesso articolo. Sarà opportuno pianificare l'utilizzo di questa scorta.  

3.  Selezionare il campo **Disponibile per trasferimento** per aprire la pagina **Ottieni approvvigionamento alternativo**.  
4.  Fare clic su **OK** per prenotare i dieci articoli disponibili.  

    > [!NOTE]  
    >  Nella riga di domanda, l'acquisto suggerito è stato sostituito con un trasferimento dall'ubicazione PRINCIPALE. La funzione **Crea ordini** genera un ordine di trasferimento dall'ubicazione PRINCIPALE all'ubicazione richiesta. Il campo **Esistono sostitutivi** funziona nello stesso modo.  

5.  Scegliere l'azione **Crea ordini**. Viene visualizzata la pagina **Crea ordini approvvigionamento**.  
6.  Nella Scheda dettaglio **Pianificazione ordini**, nel campo **Crea ordini per**, selezionare l'opzione **Ordine attivo**.  
7.  Nel campo **Crea ordine per trasferimenti** della Scheda dettaglio **Opzioni** selezionare l'opzione **Crea ordini di trasferimenti**.  
8.  Fare clic su **OK** per creare l'ordine di trasferimento per approvvigionare l'ordine di vendita.  

     L'ordine di trasferimento è ora creato ed è salvato come ultimo nella lista degli ordini di trasferimento aperti.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Pianificazione di un ordine di produzione multilivello per soddisfare la domanda di vendita
 In questa procedura si pianificherà di soddisfare la domanda di vendita di un articolo con più livelli di produzione, ciascuno dei quali crea una domanda di produzione dipendente.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Per pianificare un ordine di produzione multilivello per soddisfare la domanda di vendita

1.  Selezionare la riga di pianificazione con la domanda di vendita per l'ordine **1001**, creato in precedenza come prerequisito.  

     Questa domanda è una riga di vendita, ma il sistema di rifornimento previsto per l'articolo è **Ordine di produzione**. È necessario aggiungere un altro campanello ai componenti necessari per ciascuna bicicletta.  

2.  Scegliere l'azione **Componenti** per aprire la pagina **Componenti pianificazione**.  
3.  Nella riga con l'articolo Campanello, modificare il campo **Quantità per** da **1** a **2**.  
4.  Nella pagina **Pianificazione ordini**, considerare le opzioni di pianificazione. In questo caso non esistono metodi di approvvigionamento alternativi, trasferimento, prodotti sostitutivi o una consegna ritardata. È necessario quindi creare l'ordine di approvvigionamento suggerito, ovvero un ordine di produzione.  
5.  Selezionare l'azione **Crea ordini** per creare l'ordine di produzione.  

     Si noti che nella pagina **Pianificazione ordini** la riga di pianificazione per l'ordine di vendita **1001** non è più presente e che la domanda di vendita iniziale è stata coperta.  

6.  Chiudere la pagina **Pianificazione ordini**.  

     A questo punto, è possibile completare tutte le attività di pianificazione in questa finestra. Tuttavia, per questo esercizio, si assumerà il ruolo di addetto alla pianificazione della produzione e si aprirà a tal scopo l'ordine appena creato nella pagina **Pianificazione ordini**.  

 L'addetto alla pianificazione della produzione ha in questo caso il compito di pianificare un ordine di produzione specifico.  

### <a name="to-plan-a-specific-production-order"></a>Per pianificare un ordine di produzione specifico

1.  Aprire l'ordine di produzione **101001** (per dieci biciclette) appena creato utilizzando la funzione **Crea ordini**.  
2.  Aprire la pagina **Componenti ordine produzione** per controllare che il campanello in più sia riflesso nell'ordine di produzione.  
3.  Scegliere l'azione **Pianifica**.  

     La pagina **Pianificazione ordini** viene aperta in una visualizzazione che è sempre filtrata in modo da mostrare la domanda specifica di produzione. La domanda di vendita non è visualizzata. Per visualizzare la domanda aggiuntiva, occorre ricalcolare il piano.  

4.  Scegliere l'azione **Calcola piano**.  

     Si noti che sono presenti quattro nuovi ordini di produzione come domanda di produzione non pianificata derivante dall'ordine **101001**. Le nuove righe rappresentano la nuova domanda di produzione dei sottoassemblaggi che devono essere creati per produrre l'ordine.  

5.  Scegliere l'azione **Espandi tutto** per ottenere una panoramica di tutta la domanda di produzione derivante dagli ordini di produzione.  

     Per inserire informazioni ulteriori sulle righe della domanda, è possibile aggiungere i campi **Quantità domanda** e **Qtà domanda disponibile** alla visualizzazione.  

     È ora necessario procurare dieci pezzi di ciascun componente.  

     Si noti che quattro righe di domanda hanno il sistema di rifornimento Ord. prod. Questi quattro sottoassemblaggi rappresentano il secondo livello di prodotto della bicicletta.  

     Le impostazioni di rifornimento predefinite sono già inserite ed è possibile procedere alla creazione degli ordini.  

6.  Scegliere l'azione **Crea ordini**.  

     Prima di fare clic su **OK**, si noti il testo nella Scheda dettaglio **Pianificazione ordini**. Questo testo è importante perché evidenzia che la bicicletta ha diversi componenti prodotti, ovvero sottoassemblaggi, nella sua struttura di produzione, per i quali potrebbe esservi una domanda quando si crea l'ordine di produzione.  

7.  Nella pagina **Crea ordini approvvigionamento** , nel campo **Crea ordini per** , scegliere l'opzione **Tutte le righe** e fare clic sul pulsante **OK** per creare gli ordini di produzione per il secondo livello di prodotto dell'ordine.  

     Si noti che la domanda di produzione di livello superiore per l'ordine di produzione 101001 non è più presente. Ciò significa che la domanda di produzione iniziale di sottoassemblaggi è stata pianificata.  

     Ricalcolare il piano nella pagina **Pianificazione ordini** per pianificare la struttura della bicicletta.  

8.  Scegliere l'azione **Calcola piano** per ricalcolare il piano come suggerito nel testo della Guida incorporato.  

     Le due nuove righe rappresentano un'ulteriore domanda di produzione derivante dai sottoassemblaggi pianificati nelle fasi precedenti. Viene suggerito di creare due ordini di produzione per i mozzi delle ruote, uno per 10 mozzi anteriori e uno per 10 mozzi posteriori.  

9. Scegliere l'azione **Espandi tutto** per ottenere una panoramica di tutta la domanda di produzione derivante dai due ordini di produzione.  

     Il piano di approvvigionamento suggerito indica che siano creati quattro ordini di acquisto per i componenti. Si decide di creare gli ordini proposti.  

10. Scegliere l'azione **Crea ordini**.  
11. Nel campo **Crea ordini per** , selezionare l'opzione **Tutte le righe** e fare clic sul pulsante **OK** . Controllare se esiste un'ulteriore domanda di produzione dell'articolo principale, la bicicletta, venduta con l'ordine di vendita 1001.  
12. Scegliere l'azione **Calcola piano**.  

     Il messaggio indica che tutti gli articoli necessari sono ora approvvigionati. Verificare gli ordini di produzione confermati creati.  

13. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ord. produzione confermati**, quindi seleziona il collegamento correlato.  

     Nella pagina **Ord. produzione confermati** esaminare la pianificazione delle ore di inizio e di fine dei singoli ordini definita in base alla struttura del prodotto. I componenti di ultimo livello sono prodotti per primi. Di conseguenza, è necessario pianificare ordini multilivello come dimostrato nel flusso di lavoro di pianificazione.  

## <a name="see-also"></a>Vedere anche
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]

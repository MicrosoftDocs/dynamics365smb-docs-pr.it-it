---
title: 'Vendita, assemblaggio e spedizione di kit'
description: 'Per supportare un magazzino JIT (just-in-time), gli ordini di assemblaggio possono essere automaticamente creati e collegati non appena viene creata la riga ordine di vendita.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-selling-assembling-and-shipping-kits" />Procedura dettagliata: vendita, assemblaggio e spedizione di kit

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Per supportare un magazzino JIT (just-in-time) e la capacità di personalizzare i prodotti in base alle richieste del cliente, gli ordini di assemblaggio possono essere automaticamente creati e collegati non appena viene creata la riga ordine di vendita. Il collegamento tra la domanda di vendita e l'approvvigionamento di assemblaggio consente ai gestori dell'ordine di vendita di personalizzare l'articolo di assemblaggio al fine di comunicare le date di consegna in base alla disponibilità dei componenti. Inoltre, con la spedizione dell'ordine di vendita collegato vengono registrati automaticamente l'output e il consumo in fase di assemblaggio.  

Questa funzione speciale consente di gestire la spedizione delle quantità per l'assemblaggio su ordine, sia nella configurazione di base che in quella avanzata di warehouse. Quando i lavoratori completano l'assemblaggio delle parti o di tutta la quantità da assemblare su ordine, registrano il campo **Qtà da spedire** sulla riga spedizione warehouse, in configurazioni avanzate, quindi scelgono **Registrare spedizione**. Il risultato consiste nella registrazione dell'output di assemblaggio, incluso il consumo di componenti correlato, oltre che nella registrazione della spedizione della vendita per la quantità corrispondente all'ordine di vendita collegato. Questa procedura dettagliata illustra il processo avanzato in warehouse.  

Nelle configurazioni di base della warehouse, quando una quantità per l'assemblaggio su ordine è pronta per essere spedita, l'addetto warehouse incaricato registra un prelievo da magazzino per le righe ordine di vendita in questione. Questo crea un movimento di magazzino per i componenti, registra l'output di assemblaggio e la spedizione dell'ordine di vendita. Per ulteriori informazioni, vedere [Gestione di articoli da assemblare su ordine in prelievi magazzino](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="about-this-walkthrough" />Informazioni sulla procedura dettagliata

In questa procedura dettagliata sono illustrati i task seguenti:  

### <a name="setting-up-assembly-items" />Impostazione di articoli di assemblaggio

Gli articoli di assemblaggio sono caratterizzati dal sistema di rifornimento e dalla DB di assemblaggio. I criteri di assemblaggio dell'articolo possono essere assemblaggio su ordine (ATO) o assemblaggio per magazzino (ATS). In questa sezione sono descritti i seguenti task:  

-   Impostazione del sistema di rifornimento e dei criteri di assemblaggio appropriati in una nuova scheda dell'articolo di assemblaggio.  
-   Creazione di una DB di assemblaggio che elenca i componenti di assemblaggio e le risorse che costituiscono un articolo di assemblaggio.  

### <a name="selling-customized-assembly-items" />Vendita di articoli di assemblaggio personalizzati

[!INCLUDE[prod_short](includes/prod_short.md)] offre la possibilità di immettere sia una quantità magazzino che una quantità di assemblaggio su ordine in una sola riga dell'ordine di vendita. In questa sezione sono descritti i seguenti task:  

-   Creazione di una riga di ordine di vendita pura di ATO in cui la quantità completa non è disponibile e deve essere assemblata prima della spedizione.  
-   Personalizzazione degli articoli di ATO.  
-   Ricalcolo del prezzo unitario di un articolo di assemblaggio personalizzato.  
-   Creazione di una riga di ordine di vendita mista in cui parti della quantità di vendita vengono fornite dal magazzino e la parte residua deve essere assemblata prima della spedizione.  
-   Informazioni sugli avvisi di disponibilità di ATO.  

### <a name="planning-for-assembly-items" />Pianificazione per gli articoli di assemblaggio

La domanda e l'approvvigionamento di assemblaggio vengono gestiti dal sistema di pianificazione, proprio come per gli acquisti, i trasferimenti e la produzione. In questa sezione sono descritti i seguenti task:  

-   Esecuzione di un piano rigenerativo per gli articoli con domanda di vendita per l'approvvigionamento assemblato.  
-   Generazione di un ordine di assemblaggio per soddisfare la quantità di una riga di vendita in base alla data di spedizione richiesta.  

### <a name="assembling-items" />Assemblaggio di articoli

Gli ordini di assemblaggio funzionano in modo simile agli ordini di produzione, in quanto il consumo e l'output vengono registrati direttamente dall'ordine. Quando gli articoli vengono assemblati per magazzino, l'addetto all'assemblaggio ha accesso completo a tutti i campi della riga e della testata. Quando gli articoli vengono assemblati in un ordine in cui la quantità e la data sono promesse al cliente, determinati campi nell'ordine di assemblaggio non sono modificabili. In questo caso, la registrazione dell'assemblaggio viene eseguita dalla spedizione warehouse dell'ordine di vendita collegato. In questa sezione sono descritti i seguenti task.  

-   Registrazione del consumo in fase di assemblaggio e dell'output nel magazzino.  
-   Accesso a una riga di spedizione warehouse da un ordine di assemblaggio di ATO per registrare il lavoro di assemblaggio.  
-   Accesso a un ordine di assemblaggio di ATO da una riga di spedizione warehouse per rivedere i dati immessi automaticamente.  

### <a name="shipping-assembly-items-from-stock-and-assembled-to-order" />Spedizione degli articoli di assemblaggio dal magazzino e assemblaggio su ordine

La funzionalità speciale consente di gestire la spedizione delle quantità per l'assemblaggio su ordine. In questa sezione sono descritti i seguenti task:  

-   Creazione di un prelievo warehouse per gli articoli di assemblaggio per magazzino e per i componenti di assemblaggio da assemblare prima della spedizione.  
-   Registrazione dei prelievi warehouse per i componenti di assemblaggio, quindi, per gli articoli di assemblaggio.  
-   Accesso a un ordine di assemblaggio da una spedizione warehouse per analizzare i componenti prelevati o consumati.  
-   Spedizione delle quantità dell'assemblaggio su ordine.  
-   Spedizione di articoli di assemblaggio per magazzino.  

## <a name="roles" />Ruoli

Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Gestore degli ordini di vendita  
-   Addetto alla pianificazione  
-   Addetto all'assemblaggio  
-   Addetto al prelievo  
-   Responsabile spedizioni  

## <a name="prerequisites" />Prerequisiti

Prima di svolgere le attività di questa procedura dettagliata, è necessario:  

-   Installare [!INCLUDE[prod_short](includes/prod_short.md)].  
-   È possibile diventare un impiegato warehouse presso l'ubicazione BIANCA effettuando i seguenti passaggi:  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Impiegati warehouse**, quindi scegli il collegamento correlato.  
2.  Selezionare il campo **ID utente** , quindi il proprio account utente nella pagina **Utenti**.  
3.  Nel campo **Codice ubicazione** immettere BIANCO:  
4.  Selezionare il campo **Default**.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Preparare l'ubicazione BIANCA per l'elaborazione dell'assemblaggio effettuando i seguenti passaggi:  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.  
2.  Aprire la scheda Ubicazione dell'ubicazione BIANCA.  
3.  Nella Scheda dettaglio **Collocazioni** immettere **W-10-0001** nel campo **Cod. coll. art. per assembl.**.  

    Immettendo questo codice della collocazione non prelievo, tutte le righe dell'ordine di assemblaggio saranno pronte per ricevere i relativi componenti nella collocazione.  

4.  Nel campo **Cod. coll. art. da assembl.**, immettere **W-01-0001**.  

    Immettendo questo codice della collocazione di prelievo, gli articoli di assemblaggio completati verranno inviati alla collocazione.  

Rimuovere il lead time di default per i processi interni effettuando i seguenti passaggi:  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup manufacturing**, quindi scegli il collegamento correlato.  
2.  Nella pagina **Setup manufacturing**, nella Scheda dettaglio **Pianificazione** rimuovere il valore del campo **Lead time di sicurezza di default**.  

<!-- Create inventory for assembly components by following [Prepare Sample Data](walkthrough-selling-assembling-and-shipping-kits.md#prepare-sample-data).   -->

## <a name="story" />Scenario

Il 23 gennaio, Elisabetta, il gestore degli ordini di vendita, accetta un ordine dal reparto dispositivi, di tre unità del Kit B, che è un articolo di ATO. Tutte e tre le unità sono personalizzate e devono contenere la scheda grafica potente e un blocco aggiuntivo di RAM. Devono essere utilizzate unità disco migliori, i DWD, perché le unità CD non sono disponibili. Elisabetta sa che le unità possono essere assemblate immediatamente, quindi mantiene la data di spedizione suggerita del 23 gennaio.  

Contemporaneamente, il cliente ordina quindici unità del Kit A con una richiesta speciale, ossia che cinque unità vengano personalizzate affinché vengano dotate della potente scheda grafica. Sebbene il Kit A sia in genere un articolo con assemblaggio per magazzino, il gestore degli ordini combina le quantità delle righe di vendita per vendere dieci unità del magazzino e assemblare cinque unità personalizzate nell'ordine. Le dieci unità del Kit A non sono disponibili e devono innanzitutto essere fornite al magazzino da un ordine di assemblaggio in base ai criteri di assemblaggio dell'articolo. Elisabetta viene informata dal reparto di assemblaggio che le unità del Kit A non possono essere completate nella settimana corrente. Elisabetta imposta la data di spedizione della seconda riga dell'ordine di vendita per il 27 gennaio in modo misto, inserendo sia gli articoli di ATO e che la quantità per magazzino; informa inoltre il cliente che le 15 unità del Kit A verranno spedite quattro giorni più tardi rispetto alle tre unità del Kit B. Per segnalare al reparto spedizioni che questo ordine di vendita richiede l'elaborazione dell'assemblaggio, Elisabetta crea il documento di spedizione warehouse dall'ordine di vendita.  

Edoardo, il responsabile della pianificazione, esegue il prospetto pianificazione e genera un ordine di assemblaggio per dieci unità standard del Kit A con una data di scadenza interna fissata per il 27 gennaio.  

Samuele, il responsabile spedizioni, riceve tre righe di spedizione warehouse relative all'ordine di vendita: una riga per le tre unità di ATO pure, una riga per le cinque unità di ATO nella riga dell'ordine di vendita mista e una riga per le dieci unità di ATS nella riga dell'ordine di vendita mista. Samuele crea un documento di prelievo warehouse per tutti i componenti di assemblaggio necessari per l'assemblaggio di tutte e otto unità di ATO nel documento di spedizione warehouse.  

Gianni, l'addetto al prelievo, recupera i componenti per tutte le quantità di ATO indicate nel documento di spedizione warehouse e li porta nell'area di assemblaggio. Gianni immette la quantità da gestire e registra il prelievo warehouse.  

Linda monta le tre unità di ATO del Kit B. I componenti sono già stati prelevati e Linda non registra le quantità dei consumi e di output né l'ordine, poiché entrambe queste operazioni vengono eseguite automaticamente mediante le righe di spedizione warehouse correlate.  

Samuele registra la quantità assemblata nella riga di spedizione warehouse, quindi registra la spedizione delle tre unità del Kit B. La prima riga dell'ordine di vendita viene aggiornata in base alla spedizione. L'ordine di assemblaggio collegato rimane aperto fino alla completa fatturazione dell'ordine di vendita. Le due righe di spedizione warehouse, una di ATO e una di ATS per il Kit A con le date di scadenza del 27 gennaio, rimangono aperte.  

Il 27 gennaio Linda elabora due ordini di assemblaggio per Kit A. Il primo ordine è l'ordine ATO per cinque unità, che viene elaborato in modo diverso da Linda rispetto all'ordine ATO per il Kit B che ha elaborato il 23 gennaio. In questo ordine, Linda è autorizzata ad accedere alla linea di spedizione warehouse per registrare il lavoro di assemblaggio completato. I componenti necessari sono pronti nel reparto di assemblaggio, in quanto sono stati prelevati insieme ai componenti per il Kit B.  

Il secondo ordine di assemblaggio è l'ordine di ATS per dieci unità che sono state create dal sistema di pianificazione. In questo ordine di ATS Linda esegue tutte le azioni implicate dall'ordine di assemblaggio. Linda crea un documento di prelievo warehouse per i componenti di assemblaggio necessari per assemblare le dieci unità. Quando i PC vengono assemblati, Linda registra l'ordine di assemblaggio e segnala che gli articoli saranno disponibili in magazzino e possono essere prelevati per la spedizione.  

Samuele crea un documento di prelievo warehouse per tutte le quantità che rimangono prima che la spedizione warehouse possa essere registrata. Viene creato un documento di prelievo per le dieci unità del Kit A appena completate. I componenti necessari per assemblare le cinque unità del Kit A da ordinare sono stati prelevati il 23 gennaio.  

Gianni sposta le dieci unità del Kit A da warehouse nell'area di spedizione specificata, registra la quantità da gestire, quindi registra il prelievo.  

Samuele imballa le dieci unità di ATS con le cinque unità di ATO che Linda ha assemblato in precedenza. Samuele immette la quantità da spedire in entrambe le righe e registra automaticamente l'ultima spedizione per il reparto dispositivi. L'ordine di assemblaggio correlato per le cinque unità del Kit A viene registrato automaticamente. La seconda riga dell'ordine di vendita viene aggiornata in base alla spedizione. L'ordine di assemblaggio collegato rimane aperto fino alla completa fatturazione e alla chiusura dell'ordine di vendita.  

Quando l'ordine di vendita viene successivamente registrato come totalmente fatturato, tale ordine e gli ordini di assemblaggio collegati vengono rimossi.  

## <a name="prepare-sample-data" />Preparazione dei dati di esempio

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni articoli whse.**, quindi scegli il collegamento correlato.  
2.  Selezionare il campo **Nome batch**, quindi selezionare la registrazione di default.  
3.  Creare le rettifiche di magazzino positive nell'ubicazione BIANCA nella data di elaborazione, ossia il 23 gennaio, immettendo le informazioni riportate di seguito.  

    |**Nr. Articolo**|**Cod. zona**|**Codice collocazione**|**Quantità**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PRELIEVO|W-01-0001|20|  
    |80005|PRELIEVO|W-01-0001|20|  
    |80011|PRELIEVO|W-01-0001|20|  
    |80014|PICK|W-01-0001|20|  
    |80203|PRELIEVO|W-01-0001|20|  
    |80209|PRELIEVO|W-01-0001|20|  

4.  Scegliere l'azione **Registro**, quindi scegliere il pulsante **Sì**.  

    A questo punto, è necessario sincronizzare i nuovi movimenti warehouse con il magazzino.  

5.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni articoli**, quindi scegli il collegamento correlato. Viene visualizzata la pagina **Registrazioni magazzino**.  
6.  Scegliere l'azione **Calcola rettifica whse.**.  
7.  Nella pagina **Calcola rettifica whse.** scegliere il pulsante **OK**.  
8.  Nella pagina **Registrazioni magazzino** scegliere l'azione **Registra** quindi scegliere il pulsante **Sì**.  

### <a name="creating-the-assembly-items" />Creazione degli articoli di assemblaggio

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Articoli**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Creare il primo articolo di assemblaggio in base ai seguenti dati.  

    |Campo|Valore|  
    |---------------------------------|-----------|  
    |**Description**|Kit A - PC di base|  
    |**Unità di misura base**|PZ|  
    |**Codice categoria articolo**|Varie|  
    |**Sistema di rifornimento**|Assemblaggio|  
    |**Criteri di assemblaggio**|Assemblaggio per magazzino|  
    |**Metodo di riordino**|Lotto-per-Lotto|  

    > [!NOTE]  
    >  Il Kit A viene in genere fornito in base all'assemblaggio per magazzino, pertanto presenta un metodo di riordino finalizzato a renderlo parte della pianificazione degli approvvigionamenti generale.  

4.  Scegliere l'azione **Assemblaggio**, quindi scegliere **DB assemblaggio**.  
5.  Definire una DB di assemblaggio per il Kit A con i seguenti dati.  

    |**Tipo**|**Nr.**|**Quantità per**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Articolo|80001|1|  
    |Articolo|80011|1|  
    |Articolo|80209|1|  
    |Risorsa|Linda|1|  

6.  Creare il secondo articolo di assemblaggio in base ai seguenti dati.  

    |Campo|Valore|  
    |---------------------------------|-----------|  
    |**Description**|Kit B - PC avanzato|  
    |**Unità di misura base**|PZ|  
    |**Codice categoria articolo**|Varie|  
    |**Sistema di rifornimento**|Assemblaggio|  
    |**Criteri di assemblaggio**|Assemblaggio su ordine|  

    > [!NOTE]  
    >  Il Kit B viene generalmente fornito in base all'assemblaggio su ordine, pertanto non include un metodo di riordino, perché non deve fare parte della pianificazione degli approvvigionamenti generale.  

7.  Scegliere l'azione **Assemblaggio**, quindi scegliere **DB assemblaggio**.  
8.  Definire una DB di assemblaggio per il Kit B con i seguenti dati.  

    |**Tipo**|**Nr.**|**Quantità per**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Articolo|80005|1|  
    |Articolo|80014|1|  
    |Articolo|80210|1|  
    |Risorsa|Linda|1|  

### <a name="selling-the-assembly-items" />Vendita degli articoli di assemblaggio

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Creare due righe di ordine di vendita per il cliente 62000, reparto dispositivi, per la data di elaborazione con i seguenti dati.  

    |**Tipo**|**descrizione**|**Quantità**|Qtà per assemblaggio su ordine|Data spedizione|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Articolo|Kit B - PC avanzato|3|3|23 gennaio|  
    |Articolo|Kit A - PC di base|15|5|27 gennaio|  

    > [!NOTE]  
    >  Il seguente problema di disponibilità esiste per la riga dell'ordine di vendita relativa al Kit B:  
    >   
    >  -   Il componente di assemblaggio 80210 non è disponibile. Ciò significa che le tre unità specificate per il Kit B non possono essere assemblate e questo è indicato dallo **0** nel campo **In grado di assemblare** della pagina **Disponibilità assemblaggio**.  
    >   
    >  Il seguente problema di disponibilità esiste per la riga dell'ordine di vendita relativa al Kit A:  
    >   
    >  -   Le dieci unità del Kit A non sono disponibili. Ciò indica al sistema di pianificazione che la quantità deve essere assemblata per magazzino.  

    Infine, personalizzare l'ordine di vendita.  

4.  Selezionare la riga dell'ordine di vendita per le tre unità del Kit B.  
5.  Nella Scheda dettaglio **Righe** scegliere **Riga**, **Assemblaggio su ordine**, quindi **Righe di assemblaggio su ordine**.  
6.  Nella pagina **Righe di assemblaggio su ordine**, nella riga dell'ordine di assemblaggio per l'articolo 80014, immettere **2** nel campo **Quantità per**.  
7.  Nella riga dell'ordine di assemblaggio per l'articolo 80210, scegliere il campo **Nr.** e selezionare l'articolo 80209.  
8.  Creare una nuova riga dell'ordine di assemblaggio con i seguenti dati.  

    |Tipo|Nr.|Quantità per|  
    |----------|---------|------------------|  
    |Articolo|80203|1|  

9. Chiudere la pagina **Righe di assemblaggio su ordine**.  

    Quindi, aggiornare il prezzo unitario del Kit B in base alla personalizzazione appena eseguita. Osservare il valore corrente del campo **Prezzo unitario IVA esclusa**.  

10. Nella Scheda dettaglio **Righe** scegliere **Riga**, **Assemblaggio su ordine**, quindi **Roll up del prezzo**.  
11. Scegliere il pulsante **Sì**. Osservare il valore più alto del campo **Prezzo unitario IVA esclusa**.  
12. Selezionare la riga dell'ordine di vendita per 15 unità del Kit A.  
13. Nella Scheda dettaglio **Righe** scegliere **Riga**, **Assemblaggio su ordine**, quindi **Righe di assemblaggio su ordine**.  
14. Nella pagina **Righe di assemblaggio su ordine**, creare una nuova riga dell'ordine di assemblaggio con i seguenti dati.  

    |Tipo|Nr.|Quantità per|  
    |----------|---------|------------------|  
    |Articolo|80203|1|  

     Quindi, modificare la data di spedizione della seconda riga dell'ordine di vendita in base alla programmazione di assemblaggio.  

15. Nella riga dell'ordine di vendita relativa alle 15 unità del kit A, immettere **27-01-2014** nel campo **Data spedizione**.  
16. Scegliere l'azione **Rilascia**.  
17. Scegliere l'azione **Crea spedizione whse**.  
18. Chiudere l'ordine di vendita.  

### <a name="planning-for-the-unavailable-ats-items" />Pianificazione per gli articoli ATS non disponibili

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto pianificazione**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Calcola piano - Rigenerativo**.  
3.  Nella pagina **Calcola piano** immettere i seguenti filtri.  

    |Data inizio|Data fine|Nr.|  
    |-------------------|-----------------|---------|  
    |23/01/2014|27/01/2014|Kit A - PC di base|  

4.  Scegliere il pulsante **OK**.  

    Verrà creata una nuova riga di pianificazione per l'ordine di assemblaggio necessario di dieci unità, con scadenza il 27 gennaio. Non richiede modifiche, pertanto a questo punto è possibile creare l'ordine.  

5.  Scegliere l'azione **Esegui messaggi di azione**.  
6.  Nella pagina **Pianificaz. - Esegui mess. azioni**, selezionare il campo **Ordine di assemblaggio**, quindi selezionare **Crea ordini di assemblaggio**.  
7.  Scegliere il pulsante **OK**.  

### <a name="assembling-and-shipping-the-first-ato-quantity" />Assemblaggio e spedizione della prima quantità di ATO

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizione warehouse**, quindi scegli il collegamento correlato.  

    > [!NOTE]  
    >  In questa sezione la persona responsabile della spedizione è incaricata della registrazione del lavoro di assemblaggio di ATO completato nella riga di spedizione warehouse. Questo flusso di lavoro può verificarsi negli ambienti in cui il lavoro di assemblaggio viene eseguito dalla persona responsabile della spedizione o dagli addetti all'assemblaggio nell'area di spedizione.  
    >   
    >  In questa sezione le operazioni sull'ordine di assemblaggio vengono eseguite indirettamente dalla riga spedizione warehouse. Per ulteriori informazioni sulle modalità di elaborazione diretta di un ordine di assemblaggio, vedere la sezione "Assemblaggio degli articoli per magazzino" in questa procedura dettagliata.  

2.  Aprire la spedizione warehouse più recente creata presso l'ubicazione BIANCA.  

    Notare le tre righe di spedizione warehouse: una riga per la quantità ATO del Kit B, con scadenza il 23 gennaio. Una riga per la quantità ATO del Kit A, con scadenza il 27 gennaio. Una riga per la quantità in giacenza del Kit A, con scadenza il 27 gennaio.  

    Nel campo **Assemblaggio su ordine** è presente il metodo di assemblaggio.

    Quindi, creare un documento di prelievo per tutti i componenti di assemblaggio di ATO necessari nella spedizione warehouse.  

3.  Scegliere l'azione **Crea prelievo**, quindi scegliere il pulsante **OK**.  

    A questo punto, è necessario eseguire il task di prelievo.  

4.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi**, quindi scegli il collegamento correlato.  
5.  Aprire il documento di prelievo warehouse creato nel passaggio 3 di questa sezione.  

    Osservare il valore nel campo **Documento origine** e come tutte le righe di prelievo si riferiscano ai componenti di assemblaggio.  

    Registrare quindi il prelievo senza modificare i dati di default.  

6.  Scegliere l'azione **Autocompil. qtà da gestire**.  
7.  Scegliere l'azione **Registra prelievo**.  

    Tornare all'esecuzione dei task di spedizione.  

8.  Riaprire la pagina **Lista spedizioni warehouse**.  

    Osservare come il campo **Qtà prelevata** sia ancora vuoto in tutte le righe. Questo si verifica perché gli articoli da spedire non sono stati ancora prelevati e sono stati invece prelevati solo i componenti necessari per assemblare le quantità di ATO.  

    Procedere alla revisione dell'ordine di assemblaggio correlato.  

9. Selezionare la riga della spedizione per le tre unità del Kit B.  
10. Nella Scheda dettaglio **Righe** scegliere **Riga**, quindi selezionare **Assemblaggio su ordine**. Verrà visualizzata la pagina **Ordine di assemblaggio**.  

    Osservare come più campi dell'ordine di assemblaggio non siano disponibili in quanto l'ordine è collegato a un ordine di vendita.  

    Nelle righe dell'ordine di assemblaggio osservare come il campo **Qtà prelevata** sia compilato. Ciò è dovuto al prelievo registrato nel passaggio 7 di questa sezione.  

11. Nel campo **Quantità da assemblare** provare a immettere un valore inferiore a **3**.  

    Leggere il messaggio di errore che indica per quale motivo è possibile compilare questo campo solo mediante il campo **Qtà da spedire** della spedizione correlata.  

    Il campo **Quantità da assemblare** è modificabile per supportare le situazioni in cui si desidera eseguire una spedizione parziale di una quantità di magazzino anziché assemblare più unità dell'ordine. Per altre informazioni, vedere la sezione "Scenari di combinazione" in [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Chiudere la pagina **Ordine di assemblaggio** per tornare alla pagina **Spedizione warehouse**.  
13. Nella riga relativa alla spedizione delle tre unità del kit B, nel campo **Qtà da spedire**, immettere **3**.  
14. Scegliere l'azione **Registrare spedizione**, quindi selezionare il pulsante **Spedizione**.  

    Insieme a questa registrazione della spedizione warehouse, vengono registrati il consumo e le quantità di output totali dell'ordine di assemblaggio correlato, mentre il campo **Quantità residua** è vuoto. La riga dell'ordine di vendita per il kit B viene aggiornata per indicare che le tre unità sono state spedite.  

    Sono state completate le attività di warehouse per soddisfare la prima riga ordine di vendita entro il 23 gennaio. In seguito, soddisfare le righe ordine vendita da spedire il 27 gennaio  

### <a name="assembling-and-recording-the-second-ato-quantity" />Assemblaggio e registrazione della seconda quantità di ATO

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di assemblaggio**, quindi scegli il collegamento correlato.  

    Si noti che l'ordine di ATO delle unità spedite è ancora nella lista sebbene **Quantità residua** sia vuoto. Ciò accade perché l'ordine di vendita collegato non è ancora completamente fatturato.  

    > [!NOTE]  
    >  In questa sezione, l'addetto all'assemblaggio responsabile della registrazione del lavoro di assemblaggio completato di ATO nella riga di spedizione warehouse. Questo flusso di lavoro può verificarsi negli ambienti in cui il lavoro di assemblaggio viene eseguito in un reparto di assemblaggio separato e gli addetti all'assemblaggio sono autorizzati a modificare la riga di spedizione warehouse.  

2.  Aprire l'ordine di assemblaggio di ATO per cinque unità di Kit A.  

    Notare che i campi **Quantità da assemblare** e **Quantità da consumare** sono vuoti perché nessun lavoro è ancora registrato.  

    Nelle righe dell'ordine di assemblaggio osservare come il campo **Qtà prelevata** sia compilato. Questa situazione si verifica perché il prelievo è stato registrato il 23 gennaio.  

    Infine, registrare il completamento dell'ordine di assemblaggio.  

3.  Scegliere l'azione **Riga spediz. whse. assem. su ordine**.  
4.  Nella pagina **Riga spediz. whse. assem. su ordine**, immettere **5** nel campo **Qtà da spedire**, quindi chiudere la pagina.  

    Nella pagina **Ordine di assemblaggio** si noti che i campi **Quantità da assemblare** e **Quantità da consumare** sono ora compilati con le quantità consumi e output che verranno registrati insieme alla spedizione.  

5.  Chiudere la pagina **Ordine di assemblaggio**.  

### <a name="assembling-the-ats-quantity" />Assemblaggio della quantità di ATO

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di assemblaggio**, quindi scegli il collegamento correlato.  
2.  Aprire l'ordine di assemblaggio per dieci unità di Kit A.  

    Si noti che il campo **Quantità da assemblare** viene compilato con la quantità prevista.  

    A questo punto, è necessario creare un documento di prelievo per recuperare i componenti necessari.  

3.  Scegliere l'azione **Rilascia**.  
4.  Scegliere l'azione **Crea prelievo whse**, quindi scegliere il pulsante **OK**.  

    A questo punto, è necessario eseguire il task di prelievo.  

5.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi**, quindi scegli il collegamento correlato.  
6.  Aprire il documento di prelievo warehouse creati nel passaggio 4 di questa sezione.  

     Procedere quindi alla registrazione del prelievo senza modificare i dati di default.  

7.  Scegliere l'azione **Autocompil. qtà da gestire**.  
8.  Scegliere l'azione **Registra prelievo**.  

    Tornare all'ordine di assemblaggio per eseguire l'ultimo task di assemblaggio.  

9. In **Ordine di assemblaggio** scegliere l'azione **Registra** quindi scegliere il pulsante **Sì**.  

    Si noti che l'ordine di assemblaggio viene rimosso dalla lista degli ordini aperti.  

### <a name="shipping-the-remaining-items-partly-from-stock-and-partly-assembled-to-the-order" />Spedizione degli articoli restanti, in parte dal magazzino e assemblati su ordine

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Spedizione warehouse**, quindi scegli il collegamento correlato.  
2.  Aprire la spedizione warehouse più recente creata presso l'ubicazione BIANCA.  

    Nella riga relativa a dieci unità di kit A, si noti che i campi **Qtà da spedire** e **Qtà prelevata** sono vuoti.  

    Successivamente, prelevare tutti gli articoli restanti.  

3.  Scegliere l'azione **Crea prelievo**, quindi scegliere il pulsante **OK**.  

    Infine, eseguire l'ultimo task di prelievo relativo a questa spedizione warehouse.  

4.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prelievi**, quindi scegli il collegamento correlato.  
5.  Apri il documento di prelievo warehouse creato nel passaggio 3 di questa sezione.  

    Si noti che il documento di prelievo è riferito all'articolo di assemblaggio, non ai componenti di assemblaggio.  

    Registrare quindi il prelievo senza modificare i dati di default.  

6.  Scegliere l'azione **Autocompil. qtà da gestire**.  
7.  Scegliere l'azione **Registra prelievo**, quindi scegliere il pulsante **Sì**.  

    Tornare alla spedizione warehouse per eseguire l'ultimo task di assemblaggio.  

8.  Riaprire la pagina **Lista spedizioni warehouse**.  

    Nella pagina **Spedizione warehouse**, si noti che nella riga relativa a dieci unità di kit A i campi **Qtà da spedire** e **Qtà prelevata** ora contengono **10**.  

9. Scegliere l'azione **Registrare spedizione**, quindi scegliere **Spedizione**.  

    Il documento di spedizione warehouse viene rimosso ad indicare che le attività di warehouse interessare sono state completate. Infine, verificare che l'ordine di vendita sia stato elaborato.  

10. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini vendita**, quindi seleziona il collegamento correlato  
11. Aprire l'ordine di vendita per il reparto dispositivi.  

    Si noti che il campo **Quantità spedita** contiene la quantità complessiva su entrambe le righe.  

    Quando il reparto dispositivi effettua il pagamento per il carico di 18 PC da CRONUS, l'ordine di vendita e gli ordini di assemblaggio collegati vengono rimossi.  

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

 [Assemblaggio su ordine e assemblaggio per magazzino](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Assemblare articoli](assembly-how-to-assemble-items.md)   
 [Prelevare articoli per la spedizione warehouse](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Vendere articoli assemblati su ordine](assembly-how-to-sell-items-assembled-to-order.md)   
 [Assemblare articoli](assembly-how-to-assemble-items.md)   
 [Dettagli di progettazione: Registrazione dell'ordine di assemblaggio](design-details-assembly-order-posting.md)   
 [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md)   
 [Dettagli di progettazione: Flusso warehouse in uscita](design-details-outbound-warehouse-flow.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]

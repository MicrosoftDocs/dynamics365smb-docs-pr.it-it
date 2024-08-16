---
title: Trasferire articoli tra ubicazioni di warehouse
description: Scopri come spostare il magazzino da un'area o una warehouse a un'altra con le registrazioni di riclassificazione o gli ordini di trasferimento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# Trasferire l'inventario tra le ubicazioni

È possibile trasferire articoli di magazzino tra ubicazioni creando ordini di trasferimento. In alternativa, è possibile utilizzare le registrazioni di riclassificazione articoli.

> [!NOTE]
> Per trasferire gli articoli, devi impostare le ubicazioni e i percorsi di trasferimento. Per saperne di più sulla configurazione delle sedi, vai a [Configura sedi](inventory-how-setup-locations.md). Non puoi utilizzare gli ordini di trasferimento per ubicazioni *vuote*.

## Ordini di trasferimento

Puoi spedire un trasferimento in uscita da un'ubicazione e ricevere un trasferimento in entrata presso un'altra destinazione. È possibile:

* Traccia una quantità in transito.
* Definisci calendari, cicli e tempi di gestione in entrata e in uscita per il calcolo e la pianificazione delle date. Per saperne di più sulla pianificazione, vai a [Informazioni sulla funzionalità di pianificazione](production-about-planning-functionality.md).
* Utilizza funzionalità di warehouse diverse per le ubicazioni in entrata e in uscita.
* Usa ordini di trasferimento per trasferimenti diretti con alcune limitazioni.

## Registrazioni riclassificazione articoli

Puoi utilizzare la pagina **Registrazioni riclassificazione articoli**:

* Trasferimento diretto di articoli tra ubicazioni.
* Sposta gli articoli tra i contenitori. Per saperne di più sul trasferimento degli articoli tra i contenitori, vai a  [Sposta articoli non pianificati nelle configurazioni di magazzino di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Modifica un lotto o un numero di serie con un nuovo lotto o numero di serie. Per ulteriori informazioni sulla riclassificazione dei numeri di serie e di lotto, vai a [Riclassificare i numeri di serie o di lotto](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Modifica la data di scadenza con una nuova data.
* Riclassifica gli articoli da un'ubicazione vuota a un'ubicazione effettiva.
* Crea movimenti di warehouse se non gestisci attività di warehouse.

## Per trasferire gli articoli con un ordine di trasferimento

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di trasferimento**, quindi scegli il collegamento correlato.
2. Nella pagina **Ordine di trasferimento** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Se hai compilato i campi **Codice in transito**, **Cod. spedizioniere** e **Servizi spedizioniere** nella pagina **Specifica percorso trasf.** al momento dell'impostazione del percorso di trasferimento, i dati verranno immessi automaticamente nei campi corrispondenti dell'ordine di trasferimento.

    Se si compila il campo **Servizio spedizioniere**, il programma calcola la data di ricezione nell'ubicazione di trasferimento sommando il tempo di spedizione del servizio spedizioniere alla data di spedizione.

3. Per compilare le righe sono disponibili diverse modalità:

    |Opzione  |Descrizione  |
    |---------|---------|
    |Elaborazione manuale     | Nella scheda dettaglio **Righe** , compila una riga per un articolo o utilizza l'azione **Seleziona articoli** per scegliere più articoli.        |
    |Elaborazione automatica     | * Scegli l'azione **Ottieni contenuto collocazione** per selezionare articoli esistenti da una specifica collocazione nella posizione.<br><br>* Scegli **Ottieni righe di carico** per selezionare articoli appena arrivati nell'ubicazione da cui viene effettuato il trasferimento.        |

    Ora puoi spedire gli articoli.
4. Scegliere l'azione **Registra**, selezionare l'opzione **Spedizione**, quindi il pulsante **OK**.

    Gli articoli sono ora in transito tra le ubicazioni specificate, in base al percorso di trasferimento.

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la ricezione degli articoli. Le righe degli ordini di trasferimento sono le stesse di quelle spedite e non possono essere modificate.
5. Scegliere l'azione **Registra**, selezionare l'opzione **Ricevi**, quindi il pulsante **OK**.

### Annullare una spedizione trasferimento

Se trovi un errore in una quantità su un ordine di trasferimento registrato, finché la spedizione non viene ricevuta puoi facilmente correggere la quantità. Nella pagina  **Spedizione di trasferimento registrata**, l'azione  **Annulla spedizione** crea righe correttive, come segue:

* Il valore nel campo **Quantità spedita** è diminuito della quantità annullata.
* Il valore nel campo **Qtà da spedire** è aumentato della quantità annullata.
* La casella di controllo **Correzione** è selezionata per le righe.

Se la quantità spedita è in una spedizione di magazzino, viene creata una riga correttiva nella spedizione di magazzino registrata.

Per completare la correzione, riapri l'ordine di trasferimento, inserisci la quantità corretta, quindi registra l'ordine. Se l'ordine deve essere spedito tramite una spedizione warehouse, crea e registra una nuova spedizione warehouse.

### Registrare più ordini di trasferimento in un batch

La seguente procedura descrive come registrare in batch di ordini di trasferimento.

1. 1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini di trasferimento**, quindi scegli il collegamento correlato.  
2. Nella pagina **Ordini di trasferimento** seleziona gli ordini da registrare.
3. Nel campo **Nr.** apri il menu contestuale e scegli **Seleziona altro**.
4. Seleziona la casella di controllo per le righe in ogni ordine che vuoi registrare.
5. Selezionare l'azione **Pubblica**, quindi scegliere **Pubblica batch**.
6. Nella pagina **Registra batch ordini di trasferimento** compila i campi secondo le necessità.

   > [!TIP]
    > Per gli ordini di trasferimento che utilizzano un'ubicazione di transito, puoi scegliere **Spedisci** o **Ricevi**. Ripeti questo passaggio se hai bisogno di fare entrambe le cose. Per gli ordini in cui **Registrazione diretta** è attivata, entrambe le opzioni funzionano allo stesso modo e registrano l'ordine completamente.

7. Seleziona **OK**.
8. Per visualizzare i potenziali problemi, apri la pagina **Registro messaggi di errore**.

    > [!NOTE]
    > La registrazione di più documenti potrebbe richiedere del tempo e bloccare altri utenti. Considerare l'abilitazione della registrazione in background. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### Pianificare un movimento coda processi per registrare più documenti in un batch

In alternativa, puoi utilizzare la coda processi per programmare la registrazione in un momento conveniente per la tua organizzazione. Ad esempio, può avere senso per l'attività eseguire determinate procedure quando si è conclusa la maggior parte dell'immissione dati del giorno.

La seguente procedura illustra come impostare il report **Registra batch ordini di trasferimento** per registrare automaticamente gli ordini di trasferimento diretto alle ore 16 nei giorni della settimana. L'orario è solo un esempio. I passaggi sono uguali per gli altri documenti.  

1. Cerca la pagina **Movimenti coda processi**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  
3. Nel campo **Tipo oggetto da eseguire**, selezionare **Report**.  
4. Nel campo **ID oggetto da eseguire**, seleziona **5707, Registra batch ordini di trasferimento**.
5. Seleziona la casella controllo **Pagina di richiesta report**.
6. Nella pagina di richiesta **Registra batch ordini di trasferimento** scegli l'opzione **Spedisci**, filtra su **Trasferimento diretto**, quindi seleziona **OK**.

   > [!IMPORTANT]
   > È importante impostare i filtri. Altrimenti, [!INCLUDE [prod_short](includes/prod_short.md)] pubblica tutti i documenti, anche se non sono pronti. Considerare l'idea di impostare un filtro sul campo **Stato** per il valore **Rilasciato** e un filtro sul campo **Data pubblicazione** per il valore **oggi**. Per ulteriori informazioni sui filtri, vai a [Ordinamento, ricerca e filtro](/dynamics365/business-central/ui-enter-criteria-filters).

7. Seleziona tutte le caselle di controllo da **Esegui di Lunedì** a **Esegui di Venerdì**.
8. Nel campo **Ora inizio**, immetti **16**.
9. Scegliere l'azione **Imposta stato su Pronto**.

### Confronto di diverse impostazioni per gli ordini di trasferimento

È possibile registrare gli ordini di trasferimento in diverse modalità, con o senza indicazione del luogo di transito. Disattivare l'opzione  **Trasferimento diretto** e Seleziona la posizione temporanea nel campo  **Codice in transito** nella pagina  **Ordine di trasferimento** . Quando registri la spedizione di un ordine di trasferimento che utilizza la posizione in transito, gli articoli sulla riga non sono più disponibili in una delle tue posizioni perché sono in transito. Registrazione diretta garantisce che non venga utilizzata una posizione di transito e che la spedizione e la ricezione vengano elaborate simultaneamente. Il comportamento esatto di registrazione diretta potrebbe variare in base al valore selezionato nel campo  **Registrazione trasferimento diretto** nella pagina  **Impostazione inventario** .

La tabella seguente descrive le differenze tra le combinazioni.

|Funzionalità|Il campo  **Trasferimento diretto** è disabilitato nella pagina  **Ordine di trasferimento** |**Il trasferimento diretto** è abilitato nella pagina **Ordine di trasferimento** </br>**La registrazione del trasferimento diretto** è impostata su **Trasferimento diretto** nella pagina **Impostazione inventario** |**Il trasferimento diretto** è abilitato nella pagina **Ordine di trasferimento** </br>**La registrazione del trasferimento diretto** è impostata su **Ricezione e spedizione** nella pagina **Impostazione inventario** |
|---|---|---|---|
|Utilizzare la posizione in transito|Sì|Nr.|Nr.|
|È possibile inviare la ricevuta senza spedirla.</br>Puoi usare **Annulla ricevuta**.|Sì|Nr.|Nr.|
|Pubblicazione parziale|Sì|Nr.|Sì|
|Movimenti contabili articoli|4:</br>Trasferimento da Da-Posizione,</br>Trasferimento a In transito,</br>Trasferimento da In Transito,</br>Trasferimento alla località di destinazione.|2:</br>Trasferimento da Da-Posizione,</br>Trasferimento alla località di destinazione.|4:</br>Trasferimento da Da-Posizione,</br>Trasferisci in *vuoto*,</br>Trasferisci da *vuoto*,</br>Trasferimento alla località di destinazione.|
|Documenti registrati|Spedizione di trasferimento registrata,</br>Ricevuta di bonifico bancario.|Trasferimento diretto pubblicato|Spedizione di trasferimento registrata,</br>Ricevuta di bonifico bancario.|
|Prenotazione: in entrata e in uscita|Sì|Sì|Sì|
|Spese articolo - assegna alla ricevuta di trasferimento registrata|Sì|Nr.|Sì|
|Movimentazione magazzino|Completo|Nr.|Limitato, vedi sotto|

Matrice di movimentazione del magazzino per la configurazione: **Trasferimento diretto** è abilitato nella pagina **Ordine di trasferimento** e **Registrazione trasferimento diretto** è impostato su **Trasferimento diretto** nella pagina **Impostazione inventario** .

|Da \ A|A: Nessuna movimentazione in magazzino|A: Ricevuta di magazzino|A: Inventario Stoccaggio|A: Riporre e prelevare in modo mirato|
|-|-|-|-|-|
|**Da: Nessuna movimentazione in magazzino**|1|Non supportato|1, 4|Non supportato|
|**Da: Spedizione in magazzino**|1, 2|Non supportato|1,2,4|Non supportato|
|**Da: Stoccaggio inventario**|1, 3|Non supportato|1,3,4|Non supportato|
|**Da: Ritiro e ritiro diretti**|2|Non supportato|2|Non supportato|

I numeri nelle celle indicano le opzioni di pubblicazione supportate.

1. Posta dall'ordine di trasferimento. Per alcune combinazioni potrebbe essere necessario compilare il campo  **Quantità da spedire** .
2. Crea e registra una spedizione di magazzino.
3. Crea e pubblica una selezione di inventario.
4. Creare e registrare un inventario da mettere via. Per alcune combinazioni potrebbe essere necessario compilare il campo  **Quantità da spedire** .

Indipendentemente dal metodo, vengono eseguite le operazioni di spedizione e ricezione. Ad esempio, è possibile creare un ordine di trasferimento da una sede che richiede il prelievo dell'inventario a una sede che richiede lo stoccaggio dell'inventario. È possibile creare e registrare lo stoccaggio dell'inventario e vengono create sia le transazioni di spedizione che quelle di ricezione. È possibile registrare tali documenti anche da un ordine di trasferimento o da un prelievo di inventario.  

Per ulteriori informazioni sulla gestione del magazzino, vedere [Panoramica sulla gestione del magazzino](design-details-warehouse-management.md).

## Per trasferire gli articoli con le registrazioni di riclassificazione articolo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni riclass. articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Batch reg. riclass. articoli** compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nel campo **Cod. ubicazione** immettere l'ubicazione in cui gli articoli si trovano attualmente.

    > [!NOTE]  
    > Per trasferire gli articoli che non presentano codice ubicazione, lasciare vuoto il campo **Codice ubicazione**.
4. Nel campo **Nuovo codice ubicazione** immettere l'ubicazione verso cui si intende trasferire gli articoli.
5. Scegli l'azione **Registra**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]


## Vedere anche

[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Impostare le ubicazioni](inventory-how-setup-locations.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

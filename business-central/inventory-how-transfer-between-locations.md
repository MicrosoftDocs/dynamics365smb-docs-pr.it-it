---
title: Trasferire articoli tra le ubicazioni di warehouse
description: Scopri come spostare il magazzino da un'area o una warehouse a un'altra con le registrazioni di riclassificazione o gli ordini di trasferimento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Trasferire il magazzino tra le ubicazioni

È possibile trasferire articoli di magazzino tra ubicazioni creando ordini di trasferimento. In alternativa, è possibile utilizzare le registrazioni di riclassificazione articoli.

> [!NOTE]
> Per trasferire gli articoli, devi impostare le ubicazioni e i percorsi di trasferimento. Per ulteriori informazioni sull'impostazione delle ubicazioni, vai a [Impostazione delle ubicazioni](inventory-how-setup-locations.md). Non puoi utilizzare gli ordini di trasferimento per ubicazioni *vuote*.

## Ordini di trasferimento

Puoi spedire un trasferimento in uscita da un'ubicazione e ricevere un trasferimento in entrata presso un'altra destinazione. È possibile:

* Tenere traccia di una quantità in transito
* Definisci calendari, cicli e tempi di gestione in entrata e in uscita per il calcolo e la pianificazione delle date. Per saperne di più sulla pianificazione, vai a [Informazioni sulla funzionalità di pianificazione](production-about-planning-functionality.md).
* Utilizza funzionalità di warehouse diverse per le ubicazioni in entrata e in uscita.
* Con alcune limitazioni, puoi utilizzare gli ordini di trasferimento per i trasferimenti diretti.

## Registrazioni riclassificazione articoli

* Trasferimento semplice e diretto di articoli da un'ubicazione all'altra.
* Sposta gli articoli tra le collocazioni. Per ulteriori informazioni sul trasferimento di articoli tra collocazioni, vai a [Spostare articoli non pianificati nelle configurazioni warehouse di base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Modifica un lotto o un numero di serie con un nuovo lotto o numero di serie. Per ulteriori informazioni sulla riclassificazione dei numeri di serie e di lotto, vai a [Riclassificare i numeri di serie o di lotto](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Modifica la data di scadenza con una nuova data.
* Riclassifica gli articoli da un'ubicazione *vuota* a un'ubicazione effettiva.
* Le attività di warehouse non sono gestite. Verranno create movimenti di warehouse.

## Per trasferire gli articoli con un ordine di trasferimento

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini di trasferimento**, quindi scegli il collegamento correlato.
2. Nella pagina **Ordine di trasferimento** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Se hai compilato i campi **Codice in transito**, **Cod. spedizioniere** e **Servizi spedizioniere** nella pagina **Specifica percorso trasf.** al momento dell'impostazione del percorso di trasferimento, i dati verranno immessi automaticamente nei campi corrispondenti dell'ordine di trasferimento.

    Se si compila il campo **Servizio spedizioniere**, il programma calcola la data di ricezione nell'ubicazione di trasferimento sommando il tempo di spedizione del servizio spedizioniere alla data di spedizione.

3. Per compilare le righe, immetterle manualmente o scegliere una delle seguenti opzioni sotto l'azione **Funzioni**:

    * Scegliere l'azione **Ottieni contenuto collocazione** per selezionare elementi esistenti da una specifica collocazione nella posizione.
    * Scegliere **Ottieni righe di carico** per selezionare articoli che sono appena arrivati nell'ubicazione da cui viene effettuato il trasferimento.

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la spedizione degli articoli.
4. Scegliere l'azione **Registra**, selezionare l'opzione **Spedizione**, quindi il pulsante **OK**.

    Gli articoli sono ora in transito tra le ubicazioni specificate, in base al percorso indicato per il trasferimento.

    Come lavoratore warehouse nell'ubicazione da cui viene effettuato il trasferimento, continuare con la ricezione degli articoli. Le righe degli ordini di trasferimento sono le stesse di quelle spedite e non possono essere modificate.
5. Scegliere l'azione **Registra**, selezionare l'opzione **Ricevi**, quindi il pulsante **OK**.

## Per trasferire gli articoli con le registrazioni di riclassificazione articolo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni riclass. articoli**, quindi scegli il collegamento correlato.
2. Nella pagina **Batch reg. riclass. articoli** compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nel campo **Cod. ubicazione** immettere l'ubicazione in cui gli articoli si trovano attualmente.

    > [!NOTE]  
    > Per trasferire gli articoli che non presentano codice ubicazione, lasciare vuoto il campo **Codice ubicazione**.
4. Nel campo **Nuovo codice ubicazione** immettere l'ubicazione verso cui si intende trasferire gli articoli.
5. Scegli l'azione **Registra**.

## Vedi il relativo [training Microsoft](/training/modules/transfer-items/)

## Vedere anche

[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Impostare le ubicazioni](inventory-how-setup-locations.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

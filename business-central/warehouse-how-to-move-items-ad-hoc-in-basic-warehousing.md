---
title: Spostare articoli non pianificati nelle configurazioni warehouse di base
description: Questo articolo spiega i movimenti interni non pianificati tra le collocazioni senza una domanda da un documento di origine.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# <a name="move-items-internally-in-basic-warehouse-configurations" />Spostare gli articoli internamente nelle configurazioni della warehouse di base

È possibile spostare gli articoli tra le collocazioni senza una domanda da un documento di origine. Ad esempio, nell'ambito delle seguenti attività:

* Riorganizzare la warehouse.
* Portare gli articoli in un'area di ispezione.
* Spostare articoli extra da e verso un'area di produzione. 

La modalità di spostamento degli articoli dipende dall'impostazione della warehouse come ubicazione. Per ulteriori informazioni vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

Nelle configurazioni warehouse in cui l'interruttore **Collocazione obbligatoria** è attivato, ma non **Prelievo e stoccaggio diretti**, puoi registrare i movimenti non pianificati nelle seguenti pagine:  

* Nella pagina **Movimento interno**.
* Nella pagina **Registrazioni riclassificazione articolo**.  

## <a name="internal-movements" />Movimenti interni

La pagina **Movimenti interni** consente di specificare le righe Prendere e Mettere quando non c'è una domanda da un documento di origine. La pagina del movimento interno è come un prospetto per organizzare le cose. Non puoi elaborare il movimento effettivo direttamente. Quando una riga è compilata, utilizza l'azione **Crea movimento di agazzino** per inviare la riga alla pagina **Movimento di magazzino** dove elabori e registri il movimento.

### <a name="to-move-items-as-an-internal-movement" />Per spostare gli articoli come movimentazione interna

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimenti interni**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Assicurarsi che il campo **Nr.** della Scheda dettaglio **Generale** sia compilato.
3. Nel campo **Cod. ubicazione** immettere l'ubicazione in cui si verifica la movimentazione.  

    Se l'ubicazione è l'ubicazione predefinita come dipendente warehouse, il codice ubicazione viene aggiunto automaticamente.  
4. Nel campo **A codice collocazione** immetti un codice per la collocazione in cui vuoi spostare l'articolo.

    Ad esempio, in produzione, la collocazione potrebbe essere la collocazione produzione aperta, come definito nella scheda Ubicazione o nell'area di produzione.  
5. Nel campo **Data scadenza** immetti la data entro cui la movimentazione deve essere completata.  
6. In ogni riga compila i campi come necessario. I documenti di movimenti interni hanno una riga per movimento. La riga contiene sia l'azione Prendere che Mettere.
7. Scegli il campo **Nr. articolo** per aprire la pagina **Lista contenuto collocazione**. Seleziona l'articolo da spostare in base alla sua disponibilità nelle collocazioni. Puoi anche scegliere l'azione **Ottieni contenuto collocazione** per compilare le righe di movimento interno in base ai tuoi filtri.  

    Dopo aver selezionato l'articolo, il campo **Da codice collocazione** viene compilato automaticamente in base al contenuto collocazione selezionato. Puoi scegliere qualsiasi collocazione in cui l'articolo è disponibile. I campi **Nr. articolo** e **Da codice collocazione** sono correlati. La modifica del valore in un campo può modificare il valore nell'altro.  

    Il campo **A codice collocazione** è compilato con il valore inserito nell'intestazione. Puoi cambiarlo sulla riga con qualsiasi altro codice collocazione che non sia bloccato o dedicato a scopi speciali. Per ulteriori informazioni vedi [Il campo dedicato](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Dopo avere definito le collocazioni nelle quale e dalle quali vuoi spostare gli articoli, immetti la quantità da spostare nel campo **Quantità**.  

    > [!NOTE]  
    > La quantità deve essere disponibile nella collocazione specificata nel campo **Da codice collocazione**.  

9. Quando si è pronti per elaborare il movimento, seleziona l'azione **Crea movimento di magazzino**.  

    > [!NOTE]  
    >  Dopo avere creato il movimento, le righe movimento interno vengono eliminate.  

Esegui il resto del movimento non pianificato nella pagina **Movimento di magazzino** con la stessa procedura utilizzata per un movimento basato su documenti di origine.

### <a name="to-record-the-inventory-movement" />Per registrare il movimento di magazzino

1. Nella pagina **Movimento di magazzino** apri il documento per cui registrare il movimento.  
2. Nel campo **Codice collocazione** sulle righe di movimento, la collocazione da cui gli articoli devono essere prelevati da dove l'articolo è disponibile. Se necessario, puoi modificare la collocazione.
3. Esegui lo spostamento e immetti le informazioni riguardanti la quantità spostata nel campo **Qtà da gestire**. Il valore nelle righe Prendere e Mettere deve essere identico. In caso contrario, non è possibile registrare la movimentazione.

    Se è necessario prendere gli articoli relativi a una riga da più collocazioni, ad esempio perché la collocazione non include tutta la quantità, utilizza l'azione **Dividi riga** della Scheda dettaglio **Righe**. L'azione crea una riga per la quantità rimanente da gestire.  
4. Seleziona l'azione **Registra movimento di magazzino**.  

Durante il processo di registrazione si verifica quanto segue:

* I movimenti warehouse indicano che la quantità viene trasferita dalle collocazioni Prendere alle collocazioni Mettere.

## <a name="to-move-items-with-the-item-reclassification-journal" />Per spostare articoli con le registrazioni di riclassificazione articolo

Anziché utilizzare documenti di movimento, puoi registrare i movimenti riclassificando i codici di collocazione degli articoli. Per ulteriori informazioni vedi [Conteggio, rettifica e riclassificazione dell'inventario utilizzando registrazioni](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> I movimenti registrati con le registrazioni riclassificazione non rendono i documenti di movimento pronti per essere spostati.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Reg. riclass. articoli**, quindi scegli il collegamento correlato.  
2. In ogni riga di registrazione, definisci le collocazioni da cui e in vuoi spostare gli articoli compilando i campi **Cod. collocazione** e **Nuovo cod. collocazione**.  

    1. Per spostare l'intero contenuto di una collocazione in un'altra collocazione, scegliere l'azione **Prendi contenuto collocazione**.  
    2. Usa i filtri per trovare la collocazione con gli articoli che vuoi spostare, quindi scegli **OK**. Le righe di registrazione vengono compilate con il contenuto della collocazione.  
3. Compilare i restanti campi di ogni riga di registrazione.
4. Registrare le registrazioni di riclassificazione.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-related-microsoft-training" />Vedi il relativo [training Microsoft](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also" />Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

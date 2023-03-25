---
title: Creare offerte di vendita
description: Leggi come creare un documento di un'offerta di vendita o una richiesta di offerta (RdO) per registrare la propria offerta a un cliente o prospect per la vendita di prodotti in base a termini determinati.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: edupont
---
# Creare offerte di vendita

Creare un'offerta di vendita per registrare la propria offerta al cliente o prospect per vendere alcuni prodotti a determinate condizioni di consegna e di pagamento. È possibile inviare l'offerta di vendita al cliente per comunicare l'offerta. È possibile inviare il documento via e-mail come allegato PDF. È inoltre possibile fare in modo che il corpo e-mail venga precompilato con un riepilogo dell'offerta. Per ulteriori informazioni, vedere [Inviare documenti via e-mail](ui-how-send-documents-email.md).

Quando si negozia con il cliente o prospect è possibile modificare e inviare nuovamente l'offerta di vendita in base alle esigenze. Se il cliente accetta l'offerta, si converte l'offerta di vendita in un ordine o una fattura di vendita in cui viene elaborata la vendita. Per ulteriori informazioni vedere [Fatturare le vendite](sales-how-invoice-sales.md) o [Vendere prodotti](sales-how-sell-products.md).

Nella maggior parte dei casi, si inviano offerte di vendita a potenziali clienti. Hai spesso una persona di contatto con cui negoziare. Se accetta la tua offerta, trasformi l'offerta di vendita in un ordine e registri il prospect come cliente in [!INCLUDE [prod_short](includes/prod_short.md)]. Nella procedura seguente, ci concentriamo sui contatti, ma puoi anche inviare offerte a clienti esistenti.  

## Per creare un'offerta di vendita

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Offerte di vendita**, quindi seleziona il collegamento correlato.
2. Specifica il contatto o il cliente a cui vuoi inviare l'offerta di vendita.

    - Se l'offerta di vendita riguarda un contatto esistente, specifica il nome nel campo **Nr. contatto** .  

        Se l'offerta di vendita riguarda un cliente esistente, specifica il cliente nel campo **Nr. cliente**.
    - Se il contatto non è registrato, segui la seguente procedura:

        1. Nel campo **Nr. contratto** scegli il pulsante di modifica :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Nella finestra di dialogo sulla selezione del contatto, scegli l'azione **Nuovo** quindi compila i campi pertinenti. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Per ulteriori informazioni, vedi [Creare contatti](marketing-create-contact-companies.md).  
        3. Una volta completata la scheda contatto, seleziona il contatto appena creato nell'elenco dei contatti, quindi scegli il pulsante OK per tornare all'offerta di vendita.

        Diversi campi nell'offerta di vendita sono ora compilati con le informazioni specificate nella nuova scheda contatto.

        > [!NOTE]
        > Per calcolare correttamente le tasse e i prezzi per un'offerta, è necessario scegliere il modello cliente pertinente nel campo **Codice modello cliente**. Il modello verrà utilizzato per convertire il contatto in un cliente una volta convertita l'offerta in un ordine di vendita o in una fattura.
    -  Se l'offerta è per un nuovo cliente, è necessario aggiungere il cliente. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).  

3. Compilare i restanti campi della pagina **Offerta di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    A questo punto puoi compilare le righe di vendita per i prodotti che vendi o per ogni transazione con il cliente o prospect per il quale vuoi effettuare la registrazione in un conto C/G.  

    Se sono state impostate le righe di vendita periodiche per il cliente, ad esempio un ordine di rifornimento mensile, è possibile inserire queste righe nell'ordine scegliendo l'azione **Ottieni righe di vendita ricorrenti**.  

4. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.
5. Nel campo **Nr.** selezionare un record per effettuare la registrazione in base al valore nel campo **Tipo**.

    Lasciare il campo **Nr.** vuoto nei seguenti casi:
    - Se la riga è destinata a un commento. Compilare il commento nel campo **Descrizione**.
    - Se la riga è destinata a un articolo di catalogo. Scegliere l'azione **Seleziona articoli di catalogo**. Per ulteriori informazioni, vedere [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).

6. Nel campo **Quantità** immettere qui il numero di unità di articoli, addebiti o transazioni che la riga registrerà per il cliente.

    > [!NOTE]  
    >  Se l'articolo è di tipo **Assistenza** o se il campo **Tipo** contiene **Risorsa**, la quantità è un'unità temporale, ad esempio le ore, come indicato nel campo **Cod. unità di misura** nella riga. Per ulteriori informazioni, vedere [Impostare unità di misura articolo](inventory-how-setup-units-of-measure.md).

    Il valore nel campo **Importo riga** viene calcolato come *Prezzo unitario* x *Quantità*.  

    Il prezzo e gli importi riga sono con o senza le tasse di vendita a seconda della selezione nel campo **Prezzi IVA inclusa** della scheda cliente.  
7. Se si desidera assegnare uno sconto, immettere una percentuale nel campo **% sconto riga**. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.  

    Se sono stati impostati prezzi articolo speciali nella Scheda dettaglio **Prezzi di vendita e sconti riga di vendita** per il cliente o la scheda articolo, la percentuale di sconto riga, il prezzo e l'importo nella riga dei vendita vengono automaticamente aggiornati se vengono soddisfatti i criteri di prezzo concordati. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Ripeti i passaggi da 4 a 7 per ogni prodotto che vuoi offrire al cliente.

    I totali sotto le righe vengono automaticamente calcolati quando si creano o si modificano le righe.  
9. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

    Se sono stati impostati degli sconti su fattura per il cliente, il valore percentuale specificato viene automaticamente inserito nel campo **% sconto fattura** se vengono soddisfatti i criteri e l'importo correlato viene inserito nel campo **Importo sconto fatt. IVA esclusa**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Per compilare automaticamente il campo **Offerta valida fino alla data** con un determinato numero di giorni dopo la creazione di un'offerta, è possibile compilare il campo **Calcolo validità offerta** nella pagina **Contabilità clienti**.

10. Una volta completate le righe dell'offerta di vendita, scegliere l'azione **Invia tramite messaggio e-mail**.
11. Nella pagina **Invia messaggio e-mail** compilare tutti i campi restanti ed esaminare l'offerta di vendita inclusa. Per ulteriori informazioni, vedi [Inviare documenti via e-mail](ui-how-send-documents-email.md).
12. Se il contatto accetta l'offerta, scegli l'azione **Crea ordine**.  

    In alternativa, se la tua organizzazione preferisce quel processo, scegli l'azione **Crea fattura**.  
    > [!NOTE]
    > Se hai aggiunto un cliente nel passaggio 2, ti verrà chiesto di confermare la conversione dell'offerta in ordine.  
    >
    > Se hai aggiunto un contatto da un potenziale cliente nel passaggio 2, ti verrà chiesto di eseguire i seguenti passaggi:
    >
    >  - Converti il contatto o il prospect in un cliente scegliendo uno dei modelli di conversione dei contatti. Per ulteriori informazioni, vedi [Per creare un contatto come cliente, fornitore, dipendente o conto corrente bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Conferma la conversione dell'offerta in ordine.

La conversione rimuove l'offerta di vendita dal database. Viene creata una fattura, o un ordine, di vendita basata sulle informazioni contenute nell'offerta di vendita e in tal modo puoi elaborare la vendita. Nel campo **Nr. offerta** dell'ordine o della fattura di vendita è presente il numero dell'offerta di vendita da cui è stato convertito. Per ulteriori informazioni vedere [Fatturare le vendite](sales-how-invoice-sales.md) o [Vendere prodotti](sales-how-sell-products.md).  

## Numero di documento esterni

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## Vedi il relativo [training Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Vedere anche

[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Archiviare documenti](across-how-to-archive-documents.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

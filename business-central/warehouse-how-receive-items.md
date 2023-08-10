---
title: Ricevere articoli
description: Questo articolo offre una panoramica dei diversi modi per ricevere gli articoli in una warehouse con un carico warehouse.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts"></a>Ricevere gli articoli con un carico warehouse

In [!INCLUDE[prod_short](includes/prod_short.md)], la ricezione e lo stoccaggio degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in entrata|Richiesto carico|Richiesto stoccaggio|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino||Attivato|Di base: ordine per ordine.|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse|Attivato||Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse|Attivato|Attivato|Avanzate|  

Per ulteriori informazioni su come gestire gli articoli in entrata, vai a [Flusso warehouse in entrata](design-details-inbound-warehouse-flow.md).

Il seguente articolo fa riferimento ai metodi C e D nella precedente tabella.

## <a name="receive-items-with-a-warehouse-receipt"></a>Ricevere gli articoli con un carico warehouse

Quando gli articoli arrivano in una warehouse impostata per elaborare i carichi warehouse, è necessario recuperare le righe del documento di origine rilasciato che ha dato origine al carico. Se utilizzi le collocazioni, puoi accettare la collocazione predefinita o specificare la collocazione in cui inserire gli articoli. Quest'ultima potrebbe essere richiesta quando ricevi un articolo per la prima volta. Quindi, immetti le quantità degli articoli ricevuti e registra il carico.  

Puoi creare un carico warehouse in uno di due modi:

* In modalità push, quando il lavoro viene svolto ordine per ordine. Scegli l'azione **Crea carico warehouse** nel documento di origine, ad esempio Ordine di acquisto, Ordine di reso da vendita o Ordine di trasferimento per creare il carico warehouse per un documento di origine.
* In modalità pull, in cui usi l'azione **Rilascia** nel documento di origine, ad esempio un ordine di acquisto, un ordine di reso da vendita o un ordine di trasferimento per rilasciare il documento al magazzino. Un dipendente della warehouse crea un **Carico warehouse** per uno o più documenti di origine rilasciati. La procedura seguente descrive come creare un carico warehouse nella modalità pull. La procedura seguente descrive come creare un carico warehouse nella modalità pull.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  

    Nella Scheda dettaglio **Generale** compila il campo **Codice ubicazione**. Quando si recuperano le righe dei documenti di origine, alcune informazioni vengono copiate in ciascuna riga.

    Per un'ubicazione che richiede collocazioni, compila il campo **Codice collocazione**. A seconda della tua configurazione, [!INCLUDE[prod_short](includes/prod_short.md)] può aggiungere il codice collocazione automaticamente. Per ulteriori informazioni vedi [Codici zona e collocazione](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Puoi ottenere il documento di origine in due modi:

    1. Scegli l'azione **Prendi documenti origine**. Verrà visualizzata la pagina **Documenti origine - In entrata**. Qui è possibile selezionare uno o più documenti di origine rilasciati alla warehouse che richiedono il carico.
    2. Scegliere l'azione **Usa filtri per richiamare doc. orig.**. Si apre la pagina **Filtri per ottenere documenti di origine - In entrata**. Qui puoi selezionare il filtro del documento di origine ed eseguirlo. Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono aggiunte alla pagina **Carico warehouse**. Per ulteriori informazioni vedi [Procedura: Utilizzare i filtri per ottenere i documenti di origine](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Imposta la quantità da ricevere.

    Il campo **Qtà da ricevere** contiene la quantità inevasa per ciascuna riga, ma è possibile modificare tale quantità in base alle esigenze. 

    Per impostare il valore nel campo **Qtà da ricevere** in tutte le righe su zero, scegli l'azione **Elimina qtà da ricevere**. Ad esempio, l'impostazione delle quantità su zero è utile se utilizzi uno scanner di codici a barre per aggiornare le quantità ricevute. Per aggiungere le quantità inevase dal documento di origine, seleziona l'azione **Autocompilazione qtà da ricevere**.  

    In un documento di carico warehouse in cui la quantità ricevuta è superiore a quella ordinata, immetti la quantità effettivamente ricevuta nel campo **Qtà da ricevere**. Se l'aumento rientra nella tolleranza specificata dal codice di ricezione eccessiva assegnato, il campo **Quantità di ricezione eccessiva** viene aggiornato per mostrare la quantità che il valore nel campo **Quantità** ha superato. Se l'aumento è superiore alla tolleranza, la ricezione eccessiva non è consentita.

5. Registrare il carico warehouse. I campi relativi alle quantità nei documenti di origine vengono aggiornati e gli articoli vengono aggiunti all'inventario.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Se usi lo stoccaggio warehouse, che fa riferimento al metodo D nella tabella all'inizio di questo articolo, gli articoli vengono ricevuti ma non possono essere prelevati finché non sono stati stoccati. Per ulteriori informazioni sullo stoccaggio degli articoli, vai a [Stoccare gli articoli con gli stoccaggi warehouse](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Altrimenti, prendi in considerazione l'utilizzo dell'azione **Invia e stampa**. L'azione registrerà la ricevuta e la stamperà come istruzione di stoccaggio che mostra dove stoccare l'articolo.

    > [!NOTE]  
    > Se la warehouse utilizza il cross-docking, è possibile verificare se è possibile eseguire il cross-docking degli articoli senza stoccarli. Per ulteriori informazioni sul cross-dock, vai a [Sottoporre gli articoli a cross-dock](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents"></a>Come utilizzare i filtri per ottenere i documenti di origine

Da un carico warehouse, puoi utilizzare la pagina **Filtri per ottenere documenti origine** per recuperare le righe del documento di origine rilasciato che definiscono gli articoli da ricevere.

1. Nel carico warehouse, scegli l'azione **Usa filtri per richiamare doc. orig.**.
2. Per impostare un nuovo filtro, immetti un codice descrittivo nel campo **Codice**, quindi scegli l'azione **Modifica**.

    Viene visualizzata la pagina **Scheda filtro documento origine - In entrata**.

3. Utilizza i filtri per definire il tipo di righe del documento di origine da recuperare. Ad esempio, è possibile selezionare i tipi di documenti di origine, come gli ordini di acquisto o di trasferimento.
4. Scegli **Esegui**.  

Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono aggiunte nella pagina **Carico warehouse** in cui hai attivato i filtri.

È possibile creare un numero indefinito di combinazioni di filtri. I filtri vengono salvati nella pagina **Filtri per ottenere documenti origine** e sono disponibili in momento successivo. È possibile modificare i criteri in qualsiasi momento scegliendo l'azione **Modifica**.

## <a name="zone-and-bin-codes"></a>Codici zona e collocazione

Per ricevere gli articoli con codici classe warehouse diversi dal codice classe della collocazione specificato nel campo **Cod. collocazione** della testata del documento, elimina il contenuto del campo **Codice collocazione** della testata prima di recuperare le righe del documento di origine per gli articoli.  
<!-- TBD, table with comparison of various options-->

Se le collocazioni sono obbligatorie per un'ubicazione, i codici zona e collocazione vengono aggiunti ai documenti di carico warehouse come segue:

* Per le configurazioni avanzate che utilizzano lo stoccaggio e il prelievo diretti, [!INCLUDE [prod_short](includes/prod_short.md)] utilizza il codice collocazione di carico dalla pagina **Scheda ubicazione** per l'ubicazione. Se non viene specificato un codice collocazione di carico, non viene specificata alcuna collocazione. Se le collocazioni dell'articolo e di carico non corrispondono, il codice collocazione di carico è vuoto.
* In altre configurazioni, se non è specificato un codice collocazione di carico, [!INCLUDE [prod_short](includes/prod_short.md)] utilizza il codice collocazione del documento di origine.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Vedere anche

[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

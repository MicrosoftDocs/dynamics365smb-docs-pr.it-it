---
title: Creare schede articolo per beni o servizi (video)
description: Crei schede articolo per i servizi che vendi a ore e per prodotti fisici. Gli esempi includono articoli di assemblaggio e prodotti finiti che vendi dal tuo inventario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 11/02/2022
ms.author: bholtorf
---
# <a name="register-new-items"></a>Registrare nuovi articoli

Gli articoli, tra gli altri prodotti, sono alla base dell'azienda, sono i beni o i servizi trattati. Ogni articolo deve essere registrato come scheda articolo.

Le schede articolo contengono le informazioni richieste per l'acquisto, l'archiviazione, la consegna e la contabilità degli articoli.

La scheda articolo può essere di tipo **Inventario**, **Assistenza** o **Non in inventario** per specificare se la scheda articolo rappresenta un'unità fisica di inventario, un'unità di misura del tempo della manodopera o un'unità fisica non registrata in magazzino Per ulteriori informazioni, vedere [Informazioni sui tipi di articolo](inventory-about-item-types.md).

È possibile che un articolo sia strutturato come articolo padre con elementi figlio sottostanti in una distinta base (BOM). Ulteriori informazioni sulle distinte base di assemblaggio e di produzione in [Utilizzare le distinte base](inventory-how-work-BOMs.md).

Se si acquista lo stesso articolo da più di un fornitore, è possibile collegare i fornitori alla scheda articolo. La pagina **Catalogo art. fornitori** visualizza i fornitori in modo da poter selezionare facilmente un fornitore alternativo.

Gli *Articoli di catalogo* sono articoli offerti ai clienti che non devono essere gestiti nel sistema fino a quando non si inizia a venderli. Gli articoli di catalogo non sono articoli normali di tipo **Non in inventario**. Per ulteriori informazioni, vedi [Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Se esistono i modelli articolo per diversi tipi di articolo, allora verrà visualizzata una pagina quando si crea una nuova scheda articolo da cui è possibile selezionare un modello appropriato. Se esiste solo un modello articolo, allora le nuove schede articolo utilizzeranno sempre tale modello.

La seguente procedura illustra come creare manualmente una scheda articolo da zero. È anche possibile creare nuove schede articolo copiando quelle esistenti. Per ulteriori informazioni, vedere [Copiare articoli esistenti per creare nuovi articoli](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Per creare una nuova scheda articolo

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Nel campo **Metodo di costing** si imposta la modalità in cui viene calcolato il costo unitario dell'articolo tramite presupposizioni sul flusso degli articoli nell'azienda. Cinque metodi di costing sono disponibili, a seconda del tipo di articolo. Per ulteriori informazioni, vedere [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md).
>
> Se si seleziona **Media**, il costo unitario di un articolo viene calcolato come il costo unitario medio in ogni momento dopo un acquisto. Il magazzino viene valutato presupponendo che tutte le giacenze siano vendute simultaneamente. Con questa impostazione, è possibile selezionare il campo **Costo unitario** nella pagina **Sintesi calc. costo medio** per visualizzare lo storico delle transazioni da cui viene calcolato il costo medio.

È possibile visualizzare o modificare gli sconti o i prezzi speciali che si concedono o concessi dai fornitori per l'articolo se vengono soddisfatti determinati criteri come un cliente, la quantità minima di ordine o la data di scadenza. È possibile farlo scegliendo le azioni **Imposta prezzi speciali** o **Imposta sconti speciali**. Ogni riga, ad esempio, nella pagina **Prezzi vendita** rappresenta un prezzo speciale. Ogni colonna rappresenta un criterio che deve essere applicato per garantire a un cliente il prezzo speciale immesso nel campo **Prezzo unitario** della pagina **Prezzi di vendita**. Per ulteriori informazioni, vedere [Registrare prezzi di vendita, sconti e accordi di pagamento](sales-how-record-sales-price-discount-payment-agreements.md) o [Registra i prezzi e gli sconti speciali](purchasing-how-record-purchase-price-discount-payment-agreements.md).

L'articolo è ora registrato e la scheda articolo è pronta per essere utilizzata nei documenti di acquisto e vendita.

Se si desidera utilizzare questa scheda articolo come modello quando si creano nuove schede articolo, è possibile salvarla come modello. Per ulteriori informazioni, vedere la seguente sezione:  

### <a name="to-save-the-item-card-as-a-template"></a>Per salvare la scheda articolo come modello

1. Nella pagina **Scheda articolo** scegliere l'azione **Salva come modello**. Nella pagina **Modello articolo** verrà visualizzata la scheda articolo come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per l'articolo.
4. Modifica o immetti i codici di dimensione da applicare alle nuove schede articolo create utilizzando la definizione.
5. Una volta completato il nuovo modello articolo, scegli **OK**.

Il modello articolo viene aggiunto all'elenco dei modelli articolo, in modo che sia possibile utilizzarlo per creare nuove schede articolo.

### <a name="items-used-in-production-orders"></a>Articoli utilizzati negli ordini di produzione

Se vuoi registrare gli articoli che vengono quindi utilizzati negli ordini di produzione, specifica il sistema di rifornimento come *Ordine produzione* nella scheda dettaglio **Rifornimento**. Per ulteriori informazioni, vedere [Informazioni sugli ordini di produzione](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Per impostare più fornitori per un articolo

Se si acquista lo stesso articolo da più di un fornitore, occorre immettere le informazioni relative a ogni singolo fornitore dell'articolo quali il prezzo, il lead time, lo sconto e così via.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articoli**, quindi scegli il collegamento correlato.  
2. Selezionare il relativo articolo, quindi scegliere l'azione **Modifica**.  
3. Scegliere l'azione **Fornitori**.  
4. Selezionare il campo **Nr. fornitore** e selezionare il fornitore che si intende impostare per l'articolo.  
5. Facoltativamente, compilare i campi restanti.  
6. Ripetere i passaggi da 2 a 5 per ogni fornitore da cui si desidera acquistare l'articolo.

I fornitori vengono quindi visualizzati nella pagina **Catalogo art. fornitori** che si apre dalla scheda articolo per poter selezionare facilmente un fornitore alternativo.

## <a name="set-up-item-substitutions"></a>Configurare articoli sostitutivi

È possibile impostare articoli in modo che abbiano articoli sostitutivi, ad esempio altri articoli che possono essere utilizzati al posto dell'articolo originale.

### <a name="to-make-an-item-substitution"></a>Per sostituire un articolo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.  
2. Trova l'elemento pertinente, quindi scegli **Nr. Articolo** per aprire la Scheda articolo.  
3. Scegli l'azione **Correlato**, quindi scegli **Articolo**, **Sostituzioni** per aprire la pagina **Mov. articoli sostitutivi**.  
4. Scegli il campo **Nr. sostituto** quindi seleziona l'articolo sostitutivo nell'elenco.
5. Compila o modifica altri campi nella pagina in base alle necessità.

Quando la quantità richiesta supera la quantità disponibile in magazzino, un messaggio viene visualizzato per informare che esistono articoli sostitutivi.

> [!NOTE]  
> Tieni presente che le sostituzioni non determinano automaticamente la sostituzione di un articolo con un altro articolo, ad esempio durante la creazione di un ordine di vendita o in una distinta base. Invece, sarai avvisato del fatto che un articolo sostitutivo è disponibile.

## <a name="categories-attributes-and-variants"></a>Categorie, attributi e varianti

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Ulteriori informazioni sulle varianti in [Gestire le varianti di prodotto](inventory-item-variants.md).  

## <a name="delete-item-cards"></a>Eliminare schede articolo

Se registri una transazione per un articolo, non puoi eliminare la scheda perché i movimenti contabili potrebbero essere necessari per il controllo o la valutazione del magazzino. Per eliminare le schede articoli con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.  

## <a name="manage-inventory-in-warehouses"></a>Gestione del magazzino in warehouse

Quando registri un nuovo articolo, vengono visualizzati i campi relativi alla gestione del magazzino, in particolare nella scheda dettaglio **Warehouse**. Se l'organizzazione non utilizza le funzionalità di gestione del magazzino in [!INCLUDE [prod_short](includes/prod_short.md)] è possibile ignorare quei campi.  

Se la tua organizzazione in seguito imposta la gestione del magazzino, ti consigliamo di assicurarti che ogni articolo esistente abbia le informazioni corrette nei vari campi. In questo modo, i processi di magazzino possono essere eseguiti come previsto. Le informazioni possono includere campi come **Codice classe warehouse** o **Codice modello stoccaggio**. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).  

## <a name="planning"></a>Piano

Quando la tua azienda utilizza i processi di pianificazione della fornitura in [!INCLUDE [prod_short](includes/prod_short.md)], devi compilare i campi pertinenti nella Scheda dettaglio **Pianificazione**. Per un'introduzione all'area di pianificazione, vedi [Dettagli di progettazione: concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md).  

Per esempi di come è possibile utilizzare i campi nella Scheda dettaglio **Pianificazione**, vedi [Procedure consigliate per la configurazione: parametri di pianificazione](setup-best-practices-planning-parameters.md).  

## <a name="see-also"></a>Vedere anche

[Inventario](inventory-manage-inventory.md)  
[Impostare unità di misura](inventory-how-setup-units-of-measure.md)  
[Gestire le varianti di prodotto](inventory-item-variants.md)  
[Impostare il reporting Intrastat](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Riconciliare i costi di magazzino con la contabilità generale](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Impostazione delle categorie di registrazione](finance-posting-groups.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Informazioni sulla funzionalità di pianificazione](production-about-planning-functionality.md)  
[Impostare le procedure ottimali: Pianificazione dei parametri](setup-best-practices-planning-parameters.md)  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)  
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

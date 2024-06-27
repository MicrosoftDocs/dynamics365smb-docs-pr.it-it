---
title: Creare schede articolo per beni o servizi
description: Crei schede articolo per i servizi che vendi a ore e per prodotti fisici. Gli esempi includono articoli di assemblaggio e prodotti finiti che vendi dal tuo magazzino.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="register-new-items"></a>Registrare nuovi articoli

Gli articoli sono i beni o i servizi che acquisti, immagazzini, vendi e consegni. Usa la pagina **Scheda articolo** per registrare informazioni sui seguenti tipi di articoli:

* **Magazzino** specifica che l'articolo è un'unità fisica gestita e monitorata nel magazzino.
* **Non magazzino** sono unità fisiche che non gestisci o non monitori nel magazzino.
* Gli articoli **In assistenza** sono un'unità di tempo di manodopera, generalmente utilizzata nella gestione dei servizi.

Per ulteriori informazioni su questi tipi di articoli, vai a [Informazioni sui tipi di articoli](inventory-about-item-types.md).

> [!TIP]
> Esistono anche articoli di catalogo, che sono simili agli articoli non di magazzino in quanto sono articoli che offri ai clienti ma che non gestisci finché non li vendi. Per ulteriori informazioni, vedi [Usare gli articoli di catalogo](inventory-how-work-nonstock-items.md).  

## <a name="primary-and-alternate-vendors"></a>Fornitori primari e alternativi

Se acquisti lo stesso articolo da più di un fornitore, puoi collegare questi fornitori all'articolo. Usa l'azione **Fornitori** nella pagina **Scheda articolo** per aprire la pagina **Catalogo art. fornitori**. Nella pagina vengono visualizzati i fornitori da cui acquisti l'articolo, in modo da poter creare o selezionare facilmente un fornitore alternativo quando crei un ordine di acquisto.

## <a name="use-item-templates"></a>Utilizzare modelli di articolo

Per riutilizzare le impostazioni per diversi tipi di articoli quando crei nuovi articoli, puoi salvare gli articoli come modelli di articolo. I modelli di articolo aiutano ad accelerare il processo di aggiunta di nuovi articoli e ad aumentare la coerenza dei dati degli articoli. Quando registri un nuovo articolo, viene visualizzata una pagina che ti consente di scegliere un modello. Dopo aver scelto un modello, le relative impostazioni verranno compilate automaticamente per l'articolo che stai creando. Se disponi di un solo modello di articolo, i nuovi articoli utilizzano sempre tale modello. Per sapere come impostare un modello di articolo, vai a [Salvare una scheda articolo come modello di articolo](#save-an-item-card-as-an-item-template).

## <a name="include-items-in-bills-of-materials"></a>Includere articoli nelle distinte materiali

Puoi strutturare gerarchie composte da un articolo principale con articoli componente sottostanti nelle distinte base di assemblaggio e produzione. Per ulteriori informazioni sulle distinte base, vedi [Utilizzare le distinte base](inventory-how-work-BOMs.md).

## <a name="to-create-a-new-item-card"></a>Per creare una nuova scheda articolo

Il video seguente indica come impostare un articolo nella pagina Scheda articolo. Tuttavia, puoi anche impostare nuovi articoli copiando quelli esistenti. Per ulteriori informazioni, vedi [Copiare articoli esistenti per creare nuovi articoli](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Nel campo **Metodo di costing** si imposta la modalità in cui viene calcolato il costo unitario dell'articolo tramite presupposizioni sul flusso degli articoli nell'azienda. Cinque metodi di costing sono disponibili, a seconda del tipo di articolo. Per saperne di più sui costi, vedi [Dettagli di progettazione: metodi di determinazione dei costi](design-details-costing-methods.md) .
>
> Se selezioni **Media**, il costo unitario di un articolo viene calcolato come costo unitario medio in ogni momento dopo un acquisto. Il magazzino viene valutato presupponendo che tutte le giacenze siano vendute simultaneamente. Con questa impostazione, puoi scegliere il campo **Costo unitario** nella pagina **Sintesi calc. costo medio** per visualizzare le transazioni utilizzate per calcolare il costo medio.

Puoi utilizzare prezzi speciali o sconti che tu o il tuo fornitore avete concesso per l'articolo in base a determinati criteri. Ad esempio, i criteri includono il cliente, la quantità minima dell'ordine o la data di fine. Puoi impostare prezzi speciali scegliendo le azioni **Imposta prezzi speciali** o **Imposta sconti speciali**. Ogni riga, ad esempio, nella pagina **Prezzi vendita** rappresenta un prezzo speciale. Ogni colonna rappresenta un criterio che deve essere applicato per garantire a un cliente il prezzo speciale immesso nel campo **Prezzo unitario** della pagina **Prezzi di vendita**. Per ulteriori informazioni sui prezzi, vedi [Registrare prezzi di vendita, sconti e accordi di pagamento](sales-how-record-sales-price-discount-payment-agreements.md) o [Registra i prezzi e gli sconti speciali](purchasing-how-record-purchase-price-discount-payment-agreements.md).

### <a name="save-an-item-card-as-an-item-template"></a>Salvare una scheda articolo come modello di articolo

1. Nella pagina **Scheda articolo** scegliere l'azione **Salva come modello**. Nella pagina **Modello articolo** viene visualizzata la scheda articolo come modello.
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Puoi anche riutilizzare le dimensioni per gli articoli. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** vengono visualizzate tutte le dimensioni impostate per l'articolo. Modifica o aggiungi dimensioni applicabili a nuovi elementi creati dal modello.

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

[Magazzino](inventory-manage-inventory.md)  
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

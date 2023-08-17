---
title: Dettagli di progettazione - Flusso warehouse in entrata
description: Il flusso di warehouse in entrata inizia quando gli articoli arrivano alla warehouse della società e vengono registrati e abbinati ai documenti di origine in entrata.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2022
ms.author: bholtorf
---
# <a name="design-details-inbound-warehouse-flow"></a>Dettagli di progettazione: Flusso warehouse in entrata

Il flusso in entrata in una warehouse inizia quando gli articoli arrivano nella warehouse dell'ubicazione della società, ricevuti dalle origini esterne o da un'altra ubicazione della società. In linea di principio, il processo di ricezione degli ordini in entrata consiste in due attività:

* Ricevi gli articoli nella zona di ricezione della warehouse, dove identifichi gli articoli, li associ a un documento di origine e registri la quantità ricevuta. 
* Stocca gli articoli in magazzino e registra l'ubicazione in cui li stocchi.

I documenti di origine per il flusso di warehouse in entrata sono:

* Ordini acquisto  
* Ordine di trasferimento in entrata  
* Ordini di reso vendita  

> [!NOTE]
> Anche l'output di produzione e assemblaggio rappresenta documenti di origine in entrata. Per ulteriori informazioni sulla gestione dell'output di produzione e assemblaggio per i processi interni, vedi [Dettagli di progettazione: Flussi warehouse interni](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)], la ricezione e lo stoccaggio degli articoli avvengono utilizzando uno dei quattro metodi, come descritto nella tabella seguente.

|Metodo|Processo in entrata|Richiesto carico|Richiesto stoccaggio|Livello di complessità (ulteriori informazioni in [Panoramica di Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registrare il carico e lo stoccaggio dalla riga ordine|||Nessuna attività di warehouse dedicata.|  
|B|Registrare il carico e lo stoccaggio da un documento di stoccaggio magazzino||Attivato|Di base: ordine per ordine.|  
|C|Registrare il carico e lo stoccaggio da un documento di carico warehouse|Attivato||Di base: registrazione di ricezione e spedizione consolidata per più ordini.|  
|G|Registrare il carico da un documento di carico warehouse e registrare lo stoccaggio da un documento di stoccaggio warehouse|Attivato|Attivato|Avanzate|  

La selezione di un approccio dipende dalle procedure della società e dal livello di complessità organizzativa. Di seguito sono riportati alcuni esempi che potrebbero aiutarti a decidere.

* In un ambiente di warehouse ordine per ordine, in cui la maggior parte del personale della warehouse lavora direttamente con i documenti dell'ordine, potresti decidere di utilizzare il metodo A. 
* Per una warehouse ordine per ordine con un processo di stoccaggio più complesso o in cui il personale della warehouse separa le proprie attività di stoccaggio dal documento dell'ordine, potresti utilizzare il metodo B.
* Le società che hanno la necessità di pianificare la gestione di più ordini possono trovare utile l'utilizzo dei documenti di carico warehouse, metodi C e D.  

Nei metodi A, B e C, il carico e lo stoccaggio sono combinati in un unico passaggio quando si registrano i documenti come ricevuti. Nel metodo D, il carico viene registrato per primo per definire l'aumento di magazzino e gli articoli che sono disponibili per la vendita. L'addetto warehouse registra quindi lo stoccaggio per rendere gli articoli disponibili al prelievo per gli ordini in uscita. 

> [!NOTE]
> Sebbene gli stoccaggi di warehouse e gli stoccaggi di magazzino sembrino simili, i documenti sono diversi e vengono utilizzati in processi diversi.
> * Lo stoccaggio di magazzino utilizzato nel metodo B, insieme alla registrazione delle informazioni di stoccaggio, registra anche la ricezione del documento di origine.
> * Lo stoccaggio di warehouse utilizzato nel metodo D non può essere registrato e registra solo lo stoccaggio. La registrazione rende gli articoli disponibili per l'ulteriore elaborazione ma non registra il carico. Nel flusso in entrata, lo stoccaggio warehouse richiede un carico warehouse.

## <a name="no-dedicated-warehouse-activity"></a>Nessuna attività di warehouse dedicata

I seguenti articoli forniscono informazioni su come elaborare le ricevute per i documenti di origine se non sono disponibili attività di magazzino dedicate.

* [Registrare gli acquisti](purchasing-how-record-purchases.md)
* [Ordini di trasferimento](inventory-how-transfer-between-locations.md)
* [Elaborare gli ordini di restituzione delle vendite](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations"></a>Configurazioni warehouse di base

In una configurazione warehouse di base, l'interruttore **Richiesto stoccaggio** è attivato, ma l'interruttore **Richiesto carico** è disattivato nella pagina Scheda ubicazione per l'ubicazione.

Nel diagramma seguente vengono illustrati i flussi warehouse in entrata per tipo di documento nelle configurazioni di base della warehouse. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Flusso in entrata di base in una warehouse.":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away"></a>1: Rilasciare un documento di origine per creare una richiesta per uno stoccaggio in magazzino

Quando ricevi gli articoli, rilascia il documento di origine, ad esempio un ordine d'acquisto o un ordine di trasferimento in entrata. Il rilascio del documento rende gli articoli disponibili per lo stoccaggio. Puoi anche creare documenti di stoccaggio magazzino per le singole righe ordine, in modalità push, in base alle collocazioni specificate e le quantità da gestire.  

### <a name="2-create-an-inventory-put-away"></a>2: Creare uno stoccaggio magazzino

Nella pagina **Stoccaggio magazzino**, puoi recuperare, in modalità pull, le righe del documento di origine in attesa in base alle richieste warehouse in entrata. In modalità push, puoi anche creare righe stoccaggio di magazzino quando crei il documento di origine.  

### <a name="3-post-an-inventory-put-away"></a>3: Registrare uno stoccaggio di magazzino

In ogni riga per gli articoli che sono stati stoccati, in parte o completamente, compila il campo **Quantità**, quindi registra lo stoccaggio di magazzino. I documenti di origine che sono correlati allo stoccaggio di magazzino vengono registrati come ricevuti.  

* Vengono creati movimenti contabili articoli positivi
* I movimenti di warehouse vengono creati per le ubicazioni che richiedono un codice collocazione per tutte le transazioni articolo.
* La richiesta di stoccaggio viene eliminata, se è stata gestita completamente. Ad esempio, il campo **Quantità ricevuta** nella riga del documento di origine in entrata viene aggiornato.
* Viene creato un documento di carico registrato che corrisponde all'ordine di acquisto, ad esempio, e agli articoli ricevuti.  

## <a name="advanced-warehouse-configurations"></a>Configurazioni avanzate della warehouse

In una configurazione warehouse avanzata, l'interruttore **Richiesto carico** è attivato nella pagina Scheda ubicazione per l'ubicazione. L'interruttore **Richiesto stoccaggio** è facoltativo.

Nel diagramma seguente viene illustrato il flusso warehouse in entrata per tipo di documento. I numeri nel diagramma corrispondono ai passaggi indicati nelle sezioni che seguono il grafico.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Flusso in entrata in una configurazione warehouse avanzata":::

### <a name="1-release-the-source-document"></a>1: Rilasciare il documento di origine

Quando ricevi gli articoli, rilascia il documento di origine, ad esempio l'ordine d'acquisto o un ordine di trasferimento in entrata. Il rilascio del documento rende gli articoli disponibili per lo stoccaggio. Lo stoccaggio conterrà i riferimenti al tipo e al numero del documento di origine.

### <a name="2-create-a-warehouse-receipt"></a>2: Creare un carico warehouse

Nella pagina **Carico warehouse** recupera le righe dei documenti di origine in entrata. Puoi combinare più righe del documento di origine in un unico documento di carico warehouse. Compila il campo **Qtà da gestire** e, se necessario, seleziona la collocazione e l'area ricevimento.  

### <a name="3-post-the-warehouse-receipt"></a>3: Registrare il carico warehouse

Registra il carico warehouse per creare movimenti contabili articoli positivi. Il campo **Quantità ricevuta** nella riga del documento di origine in entrata viene aggiornato.  

Se l'interruttore **Richiesto stoccaggio** non è attivato sulla scheda ubicazione, il processo si interrompe. In caso contrario, la registrazione del documento di origine in entrata rende gli articoli disponibili per lo stoccaggio. Lo stoccaggio contiene i riferimenti al tipo e al numero del documento di origine.  

### <a name="4-optional-generate-put-away-worksheet-lines"></a>4: (Facoltativo) Generare le righe del prospetto di stoccaggio

Recupera le righe di stoccaggio warehouse nel **Prospetto stoccaggio** in base ai carichi warehouse registrati o alle operazioni che producono output. Scegli le righe da stoccare e specifica le seguenti informazioni:

* Le collocazioni da cui prelevare gli articoli.
* Le collocazioni in cui stoccare gli articoli.
* Quante unità gestire.

Le collocazioni possono essere predefinite dall'impostazione dell'ubicazione warehouse o della risorsa che ha eseguito l'operazione.  

Una volta che tutti gli stoccaggi sono pianificati e assegnati agli addetti warehouse, genera i documenti di stoccaggio warehouse. Le righe degli stoccaggi completamente assegnati vengono eliminate dal **Prospetto stoccaggi**.  

> [!NOTE]  
> Se l'interruttore **Usa prospetto stoccaggi** non è attivato nella scheda ubicazione, i documenti di stoccaggio warehouse vengono creati direttamente in base a carichi warehouse registrati. In tal caso, questo passaggio non è necessario.  

### <a name="5-create-a-warehouse-put-away-document"></a>5: Creare un documento di stoccaggio warehouse

Crea un documento di stoccaggio warehouse in modalità pull, in base al carico warehouse registrato. In alternativa, crea il documento di stoccaggio magazzino e assegnalo a un addetto warehouse in modalità push.  

### <a name="6-register-a-warehouse-put-away"></a>6: Registrare uno stoccaggio warehouse

In ogni riga per gli articoli che sono stati stoccati, in parte o completamente, compila il campo **Quantità** della pagina **Stoccaggio warehouse**, quindi registra lo stoccaggio nella warehouse.  

* I movimenti di warehouse vengono creati per le ubicazioni che richiedono un codice collocazione per tutte le transazioni articolo.
* Le righe stoccaggio warehouse vengono eliminate, se gestite completamente.
* Il documento di stoccaggio warehouse rimane aperto fino a quando la quantità completa del carico warehouse registrato correlato non viene registrata.
* Il campo **Qtà stoccata** nelle righe dell'ordine di carico warehouse registrato viene aggiornato.

## <a name="related-tasks"></a>Attività correlate

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.

|**Per**|**Vedere**|  
|------------|-------------|  
|Registra il carico degli articoli nelle ubicazioni di warehouse con un carico warehouse, in caso di processi warehouse parzialmente o completamente automatici nell'ubicazione.|[Ricevere articoli](warehouse-how-receive-items.md)|
|Stocca gli articoli ordine per ordine e registra il carico nella stessa attività, in una configurazione warehouse di base.|[Eseguire lo stoccaggio con Stoccaggi Magazzino](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Stocca gli articoli ricevuti da più ordini di acquisto, reso di vendita e trasferimento in una configurazione warehouse avanzata.|[Eseguire lo stoccaggio con Stoccaggi warehouse:](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  


## <a name="see-also"></a>Vedere anche

[!INCLUDE[footer-include](includes/footer-banner.md)]

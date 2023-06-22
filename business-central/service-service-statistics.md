---
title: Statistiche assistenza
description: 'Ottieni una rapida panoramica del contenuto e delle statistiche di un documento di assistenza, ovvero ordini, offerte, fatture o note di credito, righe di assistenza e altro ancora.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="viewing-service-statistics" />Visualizzazione delle statistiche relative all'assistenza
È possibile utilizzare statistiche che consentono di analizzare i documenti di assistenza e determinare la qualità di gestione dei processi di assistenza. È possibile analizzare contratti, offerte, fatture e note di credito di assistenza nonché articoli in assistenza scegliendo l'azione **Statistiche**. Per gli articoli in assistenza e i contratti di assistenza, è anche possibile utilizzare **Trendscape articolo di assist.** o **Trendscape contratto** per visualizzare un resoconto dei movimenti contabili di assistenza per un articolo in assistenza specifico.   

## <a name="viewing-statistics-for-service-orders" />Visualizzazione delle statistiche relative a ordini di assistenza
La funzionalità di statistiche dell'ordine di assistenza offre una rapida sintesi del contenuto dell'intero ordine di assistenza, dei dettagli delle specifiche righe di assistenza, delle informazioni correlate alla fatturazione, alla spedizione e al consumo nonché del saldo del cliente.  

I dati statistici relativi a un ordine di assistenza vengono visualizzati nella pagina **Statistiche ordine assistenza** relativa all'ordine specifico. È possibile aprire la pagina delle statistiche relativa da un ordine di assistenza. Nella pagina **Ordini assistenza**, scegliere **Statistiche**. Nelle Schede dettaglio di questa pagina sono disponibili informazioni, ad esempio quantità, importo, IVA, costo, profitto e limite di credito del cliente. Salvo diversamente specificato, gli importi presenti nella pagina sono espressi nella valuta dell'ordine di assistenza.  

### <a name="view-totals-for-a-service-order" />Visualizzare i totali per un ordine di assistenza
È possibile visualizzare l'importo totale (IVA inclusa e IVA esclusa), l'importo dell'IVA, il costo e il margine nelle righe di assistenza. In questa pagina sono inoltre visualizzate informazioni relative agli articoli, ad esempio il peso, il volume e la quantità di colli.  

### <a name="view-shipping-information" />Visualizzare le informazioni di spedizione
È possibile visualizzare informazioni relative ad articoli, risorse o costi da spedire. Per fornire tali informazioni vengono utilizzati i valori specificati nel campo **Qtà da spedire** di ciascuna riga di assistenza nell'ordine.  

### <a name="view-order-details" />Visualizzare i dettagli dell'ordine
È possibile visualizzare informazioni sugli articoli e sulle ore e i costi relativi alle risorse da fatturare e consumare. Tali informazioni sono descritte nella tabella seguente.  

|Colonna | Descrizione|  
|------------|---------------------------------------|  
|**Fatturazione**|Vengono visualizzati gli importi dell'ordine di assistenza da registrare come fatturati.|  
|**Consumo**|Visualizza la quantità e il costo di articoli o risorse che verranno registrate come consumate.|  
|**Totale**|Vengono visualizzati gli importi totali dell'ordine di assistenza, risultanti dalla somma degli importi di fatturazione e di quelli di consumo.|  

### <a name="analyze-service-order-lines" />Analizzare le righe dell'ordine di assistenza
È possibile analizzare le informazioni in base ai tipi di righe di assistenza incluse nell'ordine di assistenza. Gli importi vengono visualizzati separatamente per i seguenti elementi:  

* Articoli  
* Risorse  
* Costi e conti di contabilità generale  

### <a name="view-customer-information" />Visualizzare le informazioni sui clienti
È possibile visualizzare il saldo del conto del cliente, nonché il credito massimo che può essere concesso al cliente per cui è stato creato il documento di assistenza.

## <a name="viewing-service-item-statistics" />Visualizzazione delle statistiche relative agli articoli in assistenza
Nella pagina **Statistiche Artic. di Assist.** è possibile visualizzare informazioni aggiornate relative a un articolo in assistenza in base ai seguenti tipi di movimenti contabili di assistenza:  

* Risorse  
* Articoli  
* Costo di assistenza  
* Contratti di assistenza  
* Totale  

Per ogni tipo di movimento è possibile visualizzare l'importo fatturato, l'importo di utilizzo, l'importo di costo, la quantità, la quantità fatturata e consumata, l'importo e la percentuale di margine. La percentuale di margine viene calcolata in base alla formula seguente:  

* (Importo fatturato - Utilizzo (Costo)) x 100 / Importo fatturato  

## <a name="use-trendscapes" />Utilizzare Trendscape
Per gli articoli in assistenza e i contratti di assistenza, le pagine **Trendscape articolo di assist.** e **Trendscape contratto** forniscono un riepilogo a scorrimento dei movimenti contabili di assistenza per uno specifico articolo in assistenza o contratto di assistenza in un determinato periodo di tempo. Per visualizzare il trendscape, aprire l'articolo in assistenza o il contratto di assistenza, scegliere l'azione **Statistiche** e quindi scegliere **Trendscape**.

Scorrendo l'elenco, gli importi vengono calcolati nella valuta locale a seconda dell'intervallo di tempo specificato. Tutti gli importi vengono calcolati dai movimenti contabili di assistenza, ovvero i movimenti creati durante la registrazione di ordini o di fatture di assistenza.

È possibile applicare un filtro all'elenco specificando gli articoli in assistenza da includere.  

> [!Tip]  
>  Se l'intervallo di tempo impostato è **Giorno** e la lista da scorrere è particolarmente lunga, scegliere un intervallo superiore, ad esempio **Trimestre**, per procedere più velocemente. Una volta individuato il periodo desiderato, scegliere nuovamente l'intervallo iniziale per visualizzare i dati in modo più dettagliato.   

## <a name="viewing-gains-and-losses-on-contracts" />Visualizzazione di profitti e perdite nei contratti
Viene generato un movimento di utili o perdite contratto quando un'offerta di contratto viene convertita in un contratto di assistenza, quando le righe di contratto vengono aggiunte o eliminate da un contratto di assistenza o quando un contratto viene annullato. È possibile visualizzare guadagni o perdite dei contratti nelle pagine seguenti.  

|Pagina | Descrizione|  
|----------------|---------------------------------------|  
|**Profitti/perdite contratti (contratti)**|Per visualizzare i profitti/perdite del contratto in base al contratto di assistenza.|  
|**Guad./Perdite contr. (gruppi)**|Per visualizzare i profitti/perdite del contratto in base al gruppo di contratti di assistenza.|  
|**Guad./Perdite contr. (clienti)**|Per visualizzare i profitti/perdite del contratto in base al cliente.|  
|**Guad.i/Perdite contr. (motivi)**|Per visualizzare i profitti/perdite del contratto in base alla causale.|  
|**Guad./Perd. contr. (ce. resp.)**|Per visualizzare i profitti/perdite del contratto in base al centro di responsabilità.|  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti il nome della pagina da visualizzare, quindi scegli il collegamento correlato.  
2. Compilare i criteri di filtro da applicare. Ad esempio, nella pagina **Guad.i/Perdite contr. (motivi)** scegliere un valore per **Filtro codice causa**.  
3. Scegliere l'azione **Mostra matrice**.

## <a name="viewing-statistics-for-posted-service-documents" />Visualizzazione di statistiche per documenti di assistenza registrati
Le statistiche relative all'assistenza consentono di ottenere una panoramica dei dati statistici relativi al contenuto di documenti di assistenza registrati, ad esempio spedizione, fattura o nota di credito registrata.  

Le informazioni statistiche vengono visualizzate nella pagina delle statistiche per il documento di assistenza registrato corrispondente. È possibile aprire la pagina delle statistiche rilevante dai documenti di spedizione assistenza registrata, fattura di assistenza registrata o note di credito di assistenza registrate. Per ciascuno di questi tipi di documento, selezionare l'azione **Statistiche**. Ad esempio, nella pagina **Fatture assistenza registrate**, scegliere l'azione **Statistiche**.  

### <a name="posted-service-shipment-statistics" />Statistiche relative alle spedizioni di assistenza registrate
La pagina **Statistiche spedizioni assistenza** consente di visualizzare una panoramica di una spedizione di assistenza registrata. Le informazioni visualizzate sono relative al contenuto fisico della spedizione, ad esempio la quantità degli articoli spediti, le ore o i costi relativi alle risorse, nonché il peso e il volume degli articoli stessi.  

### <a name="posted-service-invoice-statistics" />Statistiche relative alle fatture di assistenza registrate
È possibile visualizzare un riepilogo dei dati statistici relativi a una fattura di assistenza registrata nella pagina **Statistiche fatture assistenza**. È possibile visualizzare i totali della fattura di assistenza registrata. I dati includono l'importo totale nelle righe di assistenza, con IVA inclusa ed esclusa, registrate come fatturate, l'importo dell'IVA, il costo e il margine nella fattura registrata. Nella pagina sono inoltre visualizzate informazioni relative a:  

* Articoli nelle righe della fattura di assistenza, ad esempio peso, volume e quantità di colli.  
* Il saldo nel conto del cliente e il credito massimo che è possibile concedere al cliente.  

### <a name="posted-service-credit-memo-statistics" />Statistiche relative alle note di credito di assistenza registrate
La pagina **Statistiche note credito assistenza** consente di visualizzare una panoramica dei dati statistici presenti nelle righe di una nota di credito di assistenza. La panoramica può includere:

* I totali nella nota di credito registrata, ad esempio quantità, importo, IVA, costo e profitto. Sono inoltre contenute informazioni specifiche relative agli articoli presenti sulle righe di assistenza della nota di credito registrata, ad esempio quantità, peso e volume.  
* Informazioni generali relative al cliente, ad esempio il limite di credito e il saldo del conto.  

## <a name="see-also" />Vedi anche
[Creare ordini di assistenza](service-how-to-create-service-orders.md)   
[Creare articoli in assistenza](service-how-to-create-service-items.md)   
[Pianificazione dell'assistenza](service-plan-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

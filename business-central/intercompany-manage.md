---
title: Gestione delle transazioni Intercompany
description: 'Utilizzando la funzionalità intercompany, è possibile semplificare i processi aziendali e le transazioni tra società all''interno della stessa organizzazione.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
---
# <a name="managing-intercompany-transactions" />Gestione delle transazioni Intercompany

Le aziende con più di una persona giuridica con funzioni contabili separate possono trarre vantaggio dalle transazioni intercompany. Ad esempio, è utile per le aziende che hanno filiali in più mercati o regioni internazionali. Oppure, un'organizzazione potrebbe essere costituita da più società, ma non disporre di un numero corrispondente di team contabili e amministrativi. Tramite le transazioni intercompany è possibile semplificare le transazioni e i processi aziendali tra le società nella partnership intercompany.

Dopo aver specificato le relazioni cliente e fornitore per le transazioni intercompany, i partner immettono le informazioni una sola volta nei documenti di vendita e acquisto. Un documento corrispondente viene creato per l'altro partner coinvolto nella transazione. La mappatura del piano dei conti e delle dimensioni garantisce che le informazioni vengano visualizzate nelle posizioni appropriate.  

La funzionalità intercompany offre quattro vantaggi principali:  

* Maggiore produttività grazie alla possibilità di risparmiare tempo e a transazioni più semplici.  
* Riduzione al minimo degli errori grazie alla necessità di immettere le informazioni una sola volta e agli aggiornamenti automatici a livello di sistema  
* Audit trail e visibilità completi per quanto riguarda le attività aziendali e lo storico delle transazioni.  
* Transazioni efficaci e convenienti con le consociate e le filiali.  

## <a name="streamline-the-flow-of-business-activities" />Semplificazione del flusso delle attività aziendali

Le transazioni intercompany consentono di distribuire documenti di vendita e di acquisto e movimenti registrazioni COGE a tutti gli uffici satellite, gli uffici vendite o le filiali. La distribuzione delle transazioni consente di risparmiare tempo e aumenta l'efficienza in tutta l'organizzazione riducendo l'immissione dei dati. Riduce la necessità di inviare, ricevere, stampare e archiviare documenti di vendita e acquisto.  

Disponi del controllo completo su tutti i documenti delle transazioni. È ad esempio possibile rifiutare un documento inviato e usare le azioni **Storna registrazioni** e **Annulla carichi/spedizioni** per effettuare correzioni. Oppure, quando si effettua un acquisto da un partner o una filiale, è possibile aggiornare l'ordine di acquisto fino a quando la società venditrice non ha spedito le merci.  

Quando inserisci una transazione, non è necessario specificare i conti da utilizzare. Basta scegliere il partner IC. Tramite la funzionalità intercompany vengono create righe di registrazioni COGE che eseguono il bilancio dei registri di entrambe le società coinvolte nella transazione. Nella contabilità clienti e fornitori è possibile assegnare un codice partner intercompany a qualsiasi cliente o fornitore. Da quel momento in poi, tutti gli ordini e le fatture per le transazioni tra queste società producono documenti corrispondenti nella società partner. Il risultato sono conti correttamente bilanciati.  

Intercompany si concentra sui documenti di vendita e acquisto e sulle righe di registrazioni COGE e consente transazioni tra più database [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio:

* In diversi paesi/aree geografiche
* Più valute
* Diversi piani dei conti
* Diverse dimensioni
* Diversi numeri articolo  

Le transazioni intercompany utilizzano diversi tipi di movimenti e documenti:  

* Movimenti registrazioni COGE
* Ordini di acquisto e di vendita
* Fatture di acquisto e di vendita
* Note di credito
* Ordini di reso

Quando si impostano le transazioni intercompany, si creano un elenco di partner intercompany, un piano dei conti intercompany e le dimensioni intercompany. Successivamente, è possibile creare transazioni nei giornali di registrazioni COGE intercompany.

> [!NOTE]
> Le registrazioni COGE di per sé non includono le valute. Convertono tutti gli importi nella valuta locale al tasso di cambio corrente.

Dopo avere impostato i partner aziendali come clienti e fornitori e avere assegnato loro codici partner intercompany, è possibile scambiare documenti di acquisto e di vendita intercompany, inclusi articoli e addebiti articoli. 

> [!NOTE]
> Le aziende non possono utilizzare intercompany per scambiare tutti i tipi di dati. Le fatture acquisto non vengono inviate ai business partner tramite processi intercompany. Tuttavia, le fatture di vendita inviate tramite processi interaziendali verranno create come fatture di acquisto nella società ricevente.

Il consolidamento dei dati finanziari può risultare utile con i processi intercompany. Per ulteriori informazioni, vedere [Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli articoli che li descrivono.

|A |Vedere|
|---|---|
|Crea i fornitori e i clienti intercompany come partner e imposta un piano dei conti intercompany.|[Impostare la contabilità interaziendale](intercompany-how-setup.md)|
|Utilizzare documenti o registrazioni intercompany per registrare le transazioni con i partner Intercompany.|[Utilizzo di documenti e registrazioni intercompany](intercompany-how-work-documents-journals.md)|
|Organizzare ed elaborare le transazioni in entrata e in uscita che si scambiano con i partner IC.|[Gestire la casella in entrata e in uscita intercompany](intercompany-how-manage-intercompany-inbox.md)|
|Utilizzare le transazioni IC per distribuire i costi tra società partner.|[Allocare costi a partner IC](intercompany-allocate-costs.md)|

## <a name="see-also" />Vedere anche

[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]

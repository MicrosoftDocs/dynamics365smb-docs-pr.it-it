---
title: Gestire i clienti tramite Dynamics 365 for Sales| Documenti Microsoft
description: "È possibile utilizzare Dynamics 365 for Sales tramite Business Central per mappare i dati e sfruttare l'integrazione ottimale e la sincronizzazione nel processo dai lead agli incassi."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 057db7c39834c7be0fb93589e4fc58d740dd259c
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Gestire clienti e vendite creati in Dynamics 365 for Sales
Se si utilizza Dynamics 365 for Sales (Sales) per il customer engagement, si può utilizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] per l'elaborazione degli ordini e i dati finanziari e sfruttare un'integrazione ottimale nel processo dai lead agli incassi.

Quando l'applicazione è impostata per l'integrazione con Sales, è possibile accedere ai dati di vendita da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa, in alcuni casi. Questa integrazione consente di utilizzare e sincronizzare i tipi di dati che sono comuni a entrambi i servizi, quali clienti, contatti e informazioni sulle vendite, e mantenere i dati aggiornati in entrambe le ubicazioni.  

Ad esempio, l'agente in Sales può utilizzare listini prezzi di [!INCLUDE[d365fin](includes/d365fin_md.md)] quando si crea un ordine di vendita. Quando si aggiunge l'articolo alla riga dell'ordine di vendita in Sales, si possono visualizzare il livello di magazzino (disponibilità) dell'articolo da [!INCLUDE[d365fin](includes/d365fin_md.md)].

Viceversa, i gestori ordini in [!INCLUDE[d365fin](includes/d365fin_md.md)] possono gestire le caratteristiche specifiche degli ordini di vendita trasferiti automaticamente o manualmente da Sales, come creare e registrare automaticamente righe di ordini di vendita valide per articoli o risorse che sono stati inseriti in Sales come prodotti aggiunti. Per ulteriori informazioni, vedere la sezione “Gestione di dati di ordini di vendita speciali".

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] si integra solo con Dynamics 365 for Sales. Altre applicazioni o soluzioni all'interno di Dynamics 365 che modificano il workflow standard o il modello dati in Sales, ad esempio Project Service Automation, potrebbero interrompere l'integrazione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Mapping delle entità standard di Sales per la sincronizzazione
Le entità di Sales, quali i conti, sono integrate con i tipi di record equivalenti di [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio i clienti. Per utilizzare i dati di Sales, si impostano i mapping, noti come associazioni, tra i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e i record di entità di Sales. Ad esempio, si imposta un'associazione tra un cliente specifico di [!INCLUDE[d365fin](includes/d365fin_md.md)] e un conto corrispondente di Sales.

Nella tabella seguente sono elencati i tipi di record di [!INCLUDE[d365fin](includes/d365fin_md.md)], ovvero le tabelle, e le entità corrispondenti di Sales che possono essere sincronizzate in modo predefinito.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Vendite|Direzione della sincronizzazione|Filtro predefinito|
|-------------------------------------------|-----|-------------------------|--------------|
|Agenti/Addetti acq.|Utente|Sales -> Business Central|Filtro contatto di Sales: il campo **Stato** è impostato su **No**, **Con licenza utente** è impostato su **Sì**, Modalità utente integrazione è su **No**|
|Cliente|Conto|Business Central -> Sales e Sales -> Business Central|Filtro conto di Sales: il **Tipo di relazione** è **Cliente** e lo **Stato** è **Attivo**.|
|Contatto|Contatto|Business Central -> Sales e Sales -> Business Central|Filtro contatto di Business Central: il **Tipo** è **Persona** e il contatto viene assegnato a una società. Filtro contatto di Sales: il contatto è assegnati a una società e il tipo di cliente padre è **Conto**.|
|Valuta|Valuta transazione|Business Central -> Sales| |
|Unità di misura|Unità di vendita|Business Central -> Sales| |
|Articolo|Prodotto|Business Central -> Sales e Sales -> Business Central|Filtro contatto di Sales: il campo **Tipo prodotto** è **Inventario vendite**|
|Risorsa|Prodotto|Business Central -> Sales e Sales -> Business Central|Filtro contatto di Sales: il campo **Tipo prodotto** è **Servizi**|
|Gruppo prezzi cliente|Listino prezzi|Business Central -> Sales| |
|Prezzo vendita|Listino prezzi prodotto|Business Central -> Sales|Filtro contatto di Business Central: il **Codice vendita** non è vuoto, il **Tipo vendita** è **Gruppo prezzi cliente**|
|Opportunità|Opportunità|Business Central -> Sales e Sales -> Business Central| |
|Testate Fatt. Vendita|Fattura|Business Central -> Sales| |
|Righe Fatt. Vendita|Prodotto di fatturazione|Business Central -> Sales| |

Le entità di Sales e le tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] che vengono sincronizzate sono definite dalla tabella che consente di mappare i movimenti della tabella 5335, **Mapping tabella integrazione**. È possibile visualizzare i mapping e configurare i filtri dalla pagina 5335 **Mapping tabella integrazione**.. Il mapping tra i campi dei record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e i campi delle entità di Sales è definito dai movimenti di mapping di campi nella tabella 5336 **Mapping campi integrazione** e con logica aggiuntiva del mapping.

### <a name="field-mapping-for-the-sales-account-option"></a>Mapping dei campi per l'opzione Conto vendite
Tre tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono mappate ai campi delle opzioni dell'entità **Conto**.   

I record nella tabella non collegati alle opzioni disponibili in Sales verranno ignorati durante la sincronizzazione. Ciò significa che il campo **Opzione** rimarrà vuoto in Sales.

La seguente tabella mostra i mapping delle tabelle di Business Central per il campo **Opzione** nell'entità **Conto**.

|Tavolo|Campo opzioni nell'entità Conto in Sales|
|----------------------|-------------------------------------------|
|Condizioni pagamento|Condizioni pagamento|
|Metodo di spedizione|Indirizzo 1: Termini di spedizione|
|Spedizioniere|Indirizzo 1: metodo di spedizione|

### <a name="synchronization-rules"></a>Regole di sincronizzazione
Nella seguente tabella vengono illustrate le regole che controllano la sincronizzazione tra le entità di Business Central e le tabelle di Sales.

> [!NOTE]  
> Le modifiche apportate ai dati di Sales che vengono eseguite dal conto di connessione di Sales sono ignorate. Le modifiche non verranno sincronizzate. Di conseguenza, viene suggerito di non apportate modifiche ai dati utilizzando il conto di connessione di Sales.

|Tavolo|Regola|
|-----|----|
|Clienti|Prima che un cliente possa essere sincronizzato con un conto, l'agente assegnato al cliente deve essere associato a un utente di Sales. Di conseguenza, quando viene eseguito il processo di sincronizzazione per CLIENTI di Dynamics 365 for Sales e lo si imposta per creare nuovi record, assicurarsi di sincronizzare l'agente con gli utenti di Sales prima di sincronizzare i clienti con i conti di Sales. <br /> <br />Il processo di sincronizzazione per CLIENTI di Dynamics 365 for Sales sincronizza solo i conti di Sales con il tipo di relazione Cliente.|
|Contatti|Solo i contatti di Sales associati a un conto verranno creati in Business Central. Il valore Codice agente indica il proprietario dell'entità associata in Sales.|
|Valute|Le valute vengono associate alle valute di transazione Sales in base ai codici ISO. Solo le valute con un codice dello standard ISO verranno associate e sincronizzate con le valute di transazione.|
|Unità di misura|Le unità di misura vengono sincronizzate con le unità di vendita in Sales. Può essere definita solo un'unità di misura nell'unità di vendita.|
|Articoli|Quando si sincronizzano gli articoli con i prodotti di Sales, Business Central crea automaticamente un listino prezzi in Sales. Per evitare errori di sincronizzazione, è consigliabile non modificare il listino prezzi manualmente.|
|Agenti|Gli agenti vengono associati agli utenti di sistema in Sales. L'utente deve essere abilitato e disporre di licenza e non deve essere l'utente di integrazione. Si noti che questa è la prima tabella che deve essere sincronizzata perché viene utilizzata nei clienti, nei contatti, nelle opportunità e nelle fatture di vendita.|
|Risorse|Le risorse vengono sincronizzate con i prodotti di Sales con tipo di prodotto Assistenza.|
|Gruppi prezzi cliente|Per Gruppi prezzi cliente viene eseguita la sincronizzazione con i listini prezzi di Sales.|
|Prezzi vendita|I prezzi di vendita con tipo di vendita Gruppo prezzi cliente e un codice di vendita definito vengono sincronizzati con le righe del listino prezzi di Sales.|
|Opportunità|Le opportunità vengono sincronizzate con le opportunità di Sales. Il valore Codice agente indica il proprietario dell'entità associata in Sales.|
|Fatture di vendita registrate|Le fatture di vendita registrate vengono sincronizzate con le fatture di Sales. Prima di poter sincronizzare una fattura, è meglio sincronizzare tutte le altre entità che possono essere incluse nella fattura, dai venditori ai listini prezzi. Il valore Codice agente nell'intestazione della fattura indica il proprietario dell'entità associata in Sales.|

## <a name="setting-up-the-connection"></a>Impostazione della connessione
Dalla home page, è possibile accedere alla Guida al setup assistito **Setup connessione a Microsoft Dynamics 365** che fornisce informazioni sull'impostazione della connessione. Una volta fatto questo, si avrà a disposizione un'associazione perfetta tra i record di Sales e i record di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>   Di seguito viene descritto il setup assistito, ma è possibile eseguire manualmente gli stessi task nella finestra **Setup connessione Sales**.

Nella Guida di setup assistito, scegliere quali dati sincronizzare tra i due servizi. È inoltre possibile specificare se si desidera includere la soluzione Sales esistente. In questo caso, specificare le credenziali per un account utente amministrativo.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Impostazione dell'account utente per l'importazione della soluzione
Per importare una soluzione Sales esistente, la Guida di setup utilizza un account amministrativo. Questo account deve corrispondere a un utente valido in Sales con i ruoli di sicurezza seguenti:

* Amministratore di sistema  
* Addetto alla personalizzazione della soluzione  

Per ulteriori informazioni, vedere [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) e [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).  

Questo account è utilizzato solamente durante il setup. Dopo che la soluzione è importata in [!INCLUDE[d365fin](includes/d365fin_md.md)]l'account non è più necessario.

### <a name="setting-up-the-user-account-for-synchronization"></a>Impostazione dell'account utente per la sincronizzazione
L'integrazione si basa su un account utente condiviso. Così nella sottoscrizione di Office 365, è necessario creare un utente dedicato da utilizzare per la sincronizzazione tra i due servizi. Questo account deve già essere valido un utente valido in Sales, ma non è necessario assegnare i ruoli di protezione all'account perché la Guida di setup eseguirà questa operazione automaticamente. È necessario specificare l'account utente una o più volte nella Guida di setup, in base al numero di sincronizzazioni da abilitare. Per ulteriori informazioni, vedere [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Se si sceglie di attivare la *disponibilità degli articoli*, l'account utente di integrazione deve avere una chiave di accesso ai servizi Web. Si tratta di una procedura a due passaggi nella pagina di [!INCLUDE[d365fin](includes/d365fin_md.md)] per l'account utente: è necessario scegliere il pulsante **Modifica chiave di accesso ai servizi Web** e, nella guida di connessione Sales, è necessario specificare tale utente come utente del servizio Web OData.

Se si sceglie di attivare l'*integrazione ordini di vendita*, è necessario specificare un utente che può gestire la sincronizzazione. L'utente dell'integrazione o un altro account utente.

### <a name="coupling-records"></a>Associazione di record
Nella Guida di setup assistito, è possibile scegliere di sincronizzare i due servizi. In seguito, è possibile impostare la sincronizzazione per tipi di dati specifici. Questo processo è detto *associazione* e questa sezione fornisce consigli sugli aspetti che è necessario prendere in considerazione.

Ad esempio, se si desidera visualizzare i conti di Sales come clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario associare i due tipi di record. Non è un 'operazione molto complicata: aprire la finestra **Lista clienti** in [!INCLUDE[d365fin](includes/d365fin_md.md)] e individuare l'azione nella barra multifunzione per associare questi dati con Sales. È quindi possibile specificare quali clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] corrispondono ai conti specifici di Sales.

In certe aree, la funzionalità si bassa sull'associazione di determinati set di dati prima di altri set di dati, come indicato nell'elenco seguente:

* Clienti e conti  
  * Associare prima gli agenti con gli utenti di Sales  
* Articoli e risorse  
  * Associare prima le unità di misura con i gruppi di unità di Sales  
* Articoli e prezzi risorse  
  * Associare prima i gruppi di prezzi cliente con i prezzi di Sales  

> [!NOTE]  
>   Se si utilizzano i prezzi in valuta estera, verificare di associare le valute alle valute della transazione di Sales.

Gli ordini di vendita di Sales si basano su informazioni aggiuntive come clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse. Affinché l'integrazione con gli ordini di vendita funzioni senza problemi, è necessario associare prima clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse.

### <a name="synchronizing-records-fully"></a>Sincronizzazione completa dei record
Alla fine della Guida di setup assistito è possibile scegliere l'azione **Esegui sincronizzazione completa** per iniziare a sincronizzare tutti i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] con tutti i record correlati nella soluzione Sales connessa. Nella finestra **Revisione sincronizzazione completa CRM** scegliere l'azione **Avvia**. La sincronizzazione quindi inizia a eseguire i processi in base alle dipendenze. Ad esempio, i record valuta vengono sincronizzati prima dei record cliente. La sincronizzazione completa può richiedere molto tempo e pertanto venire eseguita in background in modo che sia possibile continuare a lavorare in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per controllare l'avanzamento dei singoli processi in una sincronizzazione completa, eseguire il drill down nel campo **Stato movimento coda processi**, **Stato processo a tabella di integrazione** o **Stato processo da tabella di integrazione** nella finestra **Revisione sincronizzazione completa CRM**.

Nella finestra **Setup connessione Microsoft Dynamics 365** è possibile ottenere in qualsiasi momento le informazioni sulla sincronizzazione completa. Da qui, è anche possibile aprire la finestra **Mapping tabella integrazione** per visualizzare ulteriori dettagli sulle tabelle nella soluzione [!INCLUDE[d365fin](includes/d365fin_md.md)] e in Sales da sincronizzare.

## <a name="handling-special-sales-order-data"></a>Gestione di dati di ordini di vendita speciali
Gli ordini di vendita in Sales verranno trasferiti automaticamente in [!INCLUDE[d365fin](includes/d365fin_md.md)] se si seleziona la casella di controllo **Crea ordini di vendita automaticamente** nella finestra **Setup connessione Microsoft Dynamics 365**. In tali ordini di vendita, il campo **Nome** dell'ordine originale viene trasferito e mappato al campo **Nr. documento esterno** dell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ciò può anche avvenire se l'ordine di vendita originale contiene prodotti aggiunti, ovvero articoli o risorse che non sono registrati nei prodotti. In tal caso, è necessario compilare i campi **Tipo prodotto aggiunto** e **Nr. prodotto aggiunto** nella finestra **Setup contabilità clienti e vendite**, in modo che tali vendite di prodotti non registrate siano mappate a un numero di articolo/risorsa specificato per le analisi finanziarie.

Se la descrizione dell'articolo nell'ordine di vendita originale è molto lunga, una riga aggiuntiva di tipo Commento viene creata per contenere tutto il testo nell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Vedi anche
[Relationship Management](marketing-relationship-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)    
[Aggiungere l'organizzazione e gli utenti in Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


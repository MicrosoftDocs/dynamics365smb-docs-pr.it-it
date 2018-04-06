---
title: Gestire i clienti tramite Dynamics 365 for Sales| Documenti Microsoft
description: "È possibile utilizzare Dynamics 365 for Sales tramite Finance and Operations, Business edition per mappare i dati e sfruttare l'integrazione ottimale e la sincronizzazione nel processo dai lead agli incassi."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: cc1ad2ef812c073e570835e4018ce077b3b45494
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Gestire clienti e vendite creati in Dynamics 365 for Sales
Se si utilizza Dynamics 365 for Sales per l'interazione con i clienti, si può utilizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] per l'elaborazione degli ordini e i dati finanziari e sfruttare un'integrazione ottimale nel processo dai lead agli incassi.

Quando l'applicazione è impostata per l'integrazione con Dynamics 365 for Sales, è possibile accedere ai dati di vendita da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa, in alcuni casi. Questa integrazione consente di utilizzare e sincronizzare i tipi di dati che sono comuni a entrambi i servizi, quali clienti, contatti e informazioni sulle vendite, e mantenere i dati aggiornati in entrambe le ubicazioni.  

Ad esempio, l'agente in Dynamics 365 for Sales può utilizzare i listini prezzi di [!INCLUDE[d365fin](includes/d365fin_md.md)] quando si crea un ordine di vendita. Quando si aggiunge l'articolo alla riga dell'ordine di vendita in Dynamics 365 for Sales, è possibile visualizzare il livello di magazzino (disponibilità) dell'articolo da [!INCLUDE[d365fin](includes/d365fin_md.md)].

Viceversa, i gestori ordini in [!INCLUDE[d365fin](includes/d365fin_md.md)] possono gestire le caratteristiche specifiche degli ordini di vendita trasferiti automaticamente o manualmente da Dynamics 365 for Sales, come creare e registrare automaticamente righe di ordini di vendita valide per articoli o risorse che sono stati inseriti in Sales come prodotti aggiunti. Per ulteriori informazioni, vedere la sezione “Gestione di dati di ordini di vendita speciali".  

## <a name="setting-up-the-connection"></a>Impostazione della connessione
Dalla home page, è possibile accedere alla Guida al setup assistito **Setup connessione a Dynamics 365 for Sales** che fornisce informazioni sull'impostazione della connessione. Una volta fatto questo, si avrà a disposizione un'associazione perfetta tra i record di Dynamics 365 for Sales e i record di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>   Di seguito viene descritto il setup assistito, ma è possibile eseguire manualmente gli stessi task nella finestra **Setup connessione Dynamics 365 for Sales**.

Nella Guida di setup assistito, scegliere quali dati sincronizzare tra i due servizi. È inoltre possibile specificare se si desidera importare la soluzione Dynamics 365 for Sales esistente. In questo caso, specificare le credenziali per un account utente amministrativo.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Impostazione dell'account utente per l'importazione della soluzione
Per importare una soluzione Dynamics 365 for Sales esistente, la Guida al setup utilizza un account amministrativo. Questo account deve corrispondere a un utente valido in Dynamics 365 for Sales con i seguenti ruoli di sicurezza:

* Amministratore di sistema  
* Addetto alla personalizzazione della soluzione  

Per ulteriori informazioni, vedere [Creare utenti e assegnare i ruoli di protezione in Microsoft Finance and Operations, Business edition (online)](https://technet.microsoft.com/library/jj191623.aspx) in techNet e [Procedura: Gestire gli utenti e le autorizzazioni](ui-how-users-permissions.md).  

Questo account è utilizzato solamente durante il setup. Dopo che la soluzione è importata in [!INCLUDE[d365fin](includes/d365fin_md.md)]l'account non è più necessario.

### <a name="setting-up-the-user-account-for-synchronization"></a>Impostazione dell'account utente per la sincronizzazione
L'integrazione si basa su un account utente condiviso. Così nella sottoscrizione di Office 365, è necessario creare un utente dedicato da utilizzare per la sincronizzazione tra i due servizi. Questo account deve già essere un utente valido in Dynamics 365 for Sales, ma non è necessario assegnare i ruoli di protezione all'account perché la Guida al setup eseguirà questa operazione automaticamente. È necessario specificare l'account utente una o più volte nella Guida di setup, in base al numero di sincronizzazioni da abilitare. Per ulteriori informazioni, vedere [Creare utenti e assegnare i ruoli di protezione in Microsoft Finance and Operations, Business edition (online)](https://technet.microsoft.com/library/jj191623.aspx) in TechNet.

Se si sceglie di attivare la *disponibilità degli articoli*, l'account utente di integrazione deve avere una chiave di accesso ai servizi Web. Si tratta di una procedura a due passaggi nella pagina di [!INCLUDE[d365fin](includes/d365fin_md.md)] per quell'account utente: è necessario scegliere il pulsante **Modifica chiave di accesso ai servizi Web** e, nella guida Setup connessione a Dynamics 365 for Sales, è necessario specificare tale utente come utente del servizio Web OData.

Se si sceglie di attivare l' *integrazione ordini di vendita*, è necessario specificare un utente che può gestire la sincronizzazione. L'utente dell'integrazione o un altro account utente.

### <a name="coupling-records"></a>Associazione di record
Nella Guida di setup assistito, è possibile scegliere di sincronizzare i due servizi. In seguito, è possibile impostare la sincronizzazione per tipi di dati specifici. Questo processo è detto *associazione* e questa sezione fornisce consigli sugli aspetti che è necessario prendere in considerazione.

Ad esempio, se si desidera visualizzare i conti di Dynamics 365 for Sales come clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario associare i due tipi di record. Non è un 'operazione molto complicata: aprire la finestra **Lista clienti** in [!INCLUDE[d365fin](includes/d365fin_md.md)] e individuare l'azione nella barra multifunzione per associare questi dati con Dynamics 365 for Sales. È quindi possibile specificare quali clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] corrispondono ai conti specifici di Dynamics 365 for Sales.

In certe aree, la funzionalità si bassa sull'associazione di determinati set di dati prima di altri set di dati, come indicato nell'elenco seguente:

* Clienti e conti  
  * Associare prima gli agenti con gli utenti di Dynamics 365 for Sales  
* Articoli e risorse  
  * Associare prima le unità di misura con i gruppi di unità di Dynamics 365 for Sales  
* Articoli e prezzi risorse  
  * Associare prima i gruppi di prezzi cliente con i prezzi di Dynamics 365 for Sales  

> [!NOTE]  
>   Se si utilizzano i prezzi in valuta estera, verificare di associare le valute a quelle della transazione di Dynamics 365 for Sales.

Gli ordini di vendita di Dynamics 365 for Sales si basano su informazioni aggiuntive come clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse. Affinché gli ordini di vendita di Dynamics 365 for Sales funzionino senza problemi, è necessario associare prima clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse.

### <a name="synchronizing-records-fully"></a>Sincronizzazione completa dei record
Alla fine della Guida al setup assistito è possibile scegliere l'azione **Esegui sincronizzazione completa** per iniziare a sincronizzare tutti i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] con tutti i record correlati nella soluzione Dynamics 365 for Sales connessa. Nella finestra **Revisione sincronizzazione completa CRM** scegliere l'azione **Avvia**. La sincronizzazione quindi inizia a eseguire i processi in base alle dipendenze. Ad esempio, i record valuta vengono sincronizzati prima dei record cliente. La sincronizzazione completa può richiedere molto tempo e pertanto venire eseguita in background in modo che sia possibile continuare a lavorare in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per controllare l'avanzamento dei singoli processi in una sincronizzazione completa, eseguire il drill down nel campo **Stato movimento coda processi**, **Stato processo a tabella di integrazione** o **Stato processo da tabella di integrazione** nella finestra **Revisione sincronizzazione completa CRM**.

Nella finestra **Setup connessione Dynamics 365 for Sales** è possibile ottenere in qualsiasi momento le informazioni sulla sincronizzazione completa. Da qui, è anche possibile aprire la finestra **Mapping tabella integrazione** per visualizzare ulteriori dettagli sulle tabelle nella soluzione Finance and Operations, Business edition e in Dynamics 365 for Sales da sincronizzare.  

## <a name="handling-special-sales-order-data"></a>Gestione di dati di ordini di vendita speciali
Gli ordini di vendita in Dynamics 365 for Sales verranno trasferiti automaticamente in [!INCLUDE[d365fin](includes/d365fin_md.md)] se si seleziona la casella di controllo **Crea ordini di vendita automaticamente** nella finestra **Setup connessione a Microsoft Dynamics 365 for Sales**. In tali ordini di vendita, il campo **Nome** dell'ordine originale viene trasferito e mappato al campo **Nr. documento esterno** dell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ciò può anche avvenire se l'ordine di vendita originale contiene prodotti aggiunti, ovvero articoli o risorse che non sono registrati nei prodotti. In tal caso, è necessario compilare i campi **Tipo prodotto aggiunto** e **Nr. prodotto aggiunto** nella finestra **Setup contabilità clienti e vendite**, in modo che tali vendite di prodotti non registrate siano mappate a un numero di articolo/risorsa specificato per le analisi finanziarie.

Se la descrizione dell'articolo nell'ordine di vendita originale è molto lunga, una riga aggiuntiva di tipo Commento viene creata per contenere tutto il testo nell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Vedi anche
[Relationship Management](marketing-relationship-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizzazione dell'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Gestire utenti e autorizzazioni](ui-how-users-permissions.md)    
[Aggiungere l'organizzazione e gli utenti in Finance and Operations, Business edition (online)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]


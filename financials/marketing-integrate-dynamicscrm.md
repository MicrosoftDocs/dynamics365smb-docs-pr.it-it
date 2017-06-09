---
title: Gestione delle relazioni clienti utilizzando Dynamics 365 for Sales da Dynamics 365 for Financials | Documenti Microsoft
description: "Se si utilizza Dynamics 365 for Sales per l&quot;interazione con i clienti, si può utilizzare Dynamics 365 for Financials per l&quot;elaborazione degli ordini e i dati finanziari e sfruttare un&quot;integrazione ottimale nel processo dai lead agli incassi."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 03/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c0291cc316b49e1f1f4f2196745914daca158f61
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Gestione delle relazioni clienti utilizzando Dynamics 365 for Sales da Dynamics 365 for Financials
Se si utilizza Dynamics 365 for Sales per l'interazione con i clienti, si può utilizzare [!INCLUDE[d365fin](includes/d365fin_md.md)] per l'elaborazione degli ordini e i dati finanziari e sfruttare un'integrazione ottimale nel processo dai lead agli incassi.

Quando l'applicazione è impostata per l'integrazione con Dynamics 365 for Sales, è possibile accedere ai dati di vendita da [!INCLUDE[d365fin](includes/d365fin_md.md)] e viceversa, in alcuni casi. Questa integrazione consente di utilizzare e sincronizzare i tipi di dati che sono comuni a entrambi i servizi, quali clienti, contatti e informazioni sulle vendite, e mantenere i dati aggiornati in entrambe le ubicazioni.  

**Nota**: nella versione corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)], Dynamics 365 for Sales viene indicato come Dynamics CRM. Per semplicità, nella parte rimanente di questo articolo verrà utilizzata la terminologia che viene utilizzata in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Ad esempio, L'agente in Dynamics CRM può utilizzare listini prezzi di [!INCLUDE[d365fin](includes/d365fin_md.md)] quando si crea un ordine di vendita. Quando si aggiunge l'articolo alla riga dell'ordine di vendita in Dynamics CRM, si possono visualizzare il livello di magazzino (disponibilità) dell'articolo da [!INCLUDE[d365fin](includes/d365fin_md.md)]. Questi dati vengono generati nell'ambito della Guida di setup assistito, **Setup connessione a Dynamics CRM**.  

**Nota**: questa funzionalità richiede che l'esperienza sia impostata su ***** Suite *****. Per ulteriori informazioni, vedere [Personalizzazione dell'esperienza di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Impostazione della connessione
Da casa, è possibile accedere alla Guida di setup assistito **Setup connessione a Dynamics CRM** che consente di impostare la connessione. Una volta fatto questo, si avrà a disposizione un'associazione perfetta tra i record di Dynamics CRM e i record di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

**Nota**: di seguito viene descritto il setup assistito, ma è possibile eseguire manualmente le stesse attività nella finestra **Setup connessione CRM**.

Nella Guida di setup assistito, scegliere quali dati sincronizzare tra i due servizi. È inoltre possibile specificare se si desidera includere la soluzione Dynamics CRM esistente. In questo caso, specificare le credenziali per un account utente amministrativo.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Impostazione dell'account utente per l'importazione della soluzione
Per importare una soluzione Dynamics CRM esistente, la Guida di setup utilizza un account amministrativo. Questo account deve corrispondere a un utente valido in Dynamics CRM con i ruoli di sicurezza seguenti:

* Amministratore di sistema  
* Addetto alla personalizzazione della soluzione  

Per ulteriori informazioni, vedere [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) in techNet e [Procedura: Gestire gli utenti e le autorizzazioni](ui-how-users-permissions.md).  

Questo account è utilizzato solamente durante il setup. Dopo che la soluzione è importata in [!INCLUDE[d365fin](includes/d365fin_md.md)]l'account non è più necessario.

### <a name="setting-up-the-user-account-for-synchronization"></a>Impostazione dell'account utente per la sincronizzazione
L'integrazione si basa su un account utente condiviso. Così nella sottoscrizione di Office 365, è necessario creare un utente dedicato da utilizzare per la sincronizzazione tra le due servizi. Questo account deve già essere valido un utente valido in Dynamics CRM, ma non è necessario assegnare i ruoli di protezione all'account perché la Guida di setup eseguirà questa operazione automaticamente. È necessario specificare l'account utente una o più volte nella Guida di setup, in base al numero di sincronizzazioni da abilitare. Per ulteriori informazioni, vedere [Creare utenti e assegnare i ruoli di protezione in Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) in techNet.

Se si sceglie di attivare la *disponibilità degli articoli*, l'account utente di integrazione deve avere una chiave di accesso ai servizi Web. Si tratta di una procedura a due passaggi nella pagina di [!INCLUDE[d365fin](includes/d365fin_md.md)] per l'account utente: è necessario scegliere il pulsante **Modifica chiave di accesso ai servizi Web** e, nella guida di connessione CRM, è necessario specificare tale utente come utente del servizio Web OData.

Se si sceglie di attivare l'*integrazione ordini di vendita*, è necessario specificare un utente che può gestire la sincronizzazione. L'utente dell'integrazione o un altro account utente.

### <a name="coupling-records"></a>Associazione di record
Nella Guida di setup assistito, è possibile scegliere di sincronizzare i due servizi. In seguito, è possibile impostare la sincronizzazione per tipi di dati specifici. Questo processo è detto *associazione* e questa sezione fornisce consigli sugli aspetti che è necessario prendere in considerazione.

Ad esempio, se si desidera visualizzare i conti di Dynamics CRM come clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario associare i due tipi di record. Non è un 'operazione molto complicata: aprire la finestra **Lista clienti** in [!INCLUDE[d365fin](includes/d365fin_md.md)] e individuare l'azione nella barra multifunzione per associare questi dati con Dynamics CRM. È quindi possibile specificare quali clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] corrispondono ai conti specifici di Dynamics CRM.

In certe aree, la funzionalità si bassa sull'associazione di determinati set di dati prima di altri set di dati, come indicato nell'elenco seguente:

* Clienti e conti  
  * Associare prima gli agenti con gli utenti di Dynamics CRM  
* Articoli e risorse  
  * Associare prima le unità di misura con i gruppi di unità di Dynamics CRM  
* Articoli e prezzi risorse  
  * Associare prima i gruppi di prezzi cliente con i prezzi di Dynamics CRM  

**Nota**: se si utilizzano i prezzi in valuta estera, verificare di associare le valute alle valute della transazione di Dynamics CRM,

Gli ordini di vendita di Dynamics CRM si basano su informazioni aggiuntive come clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse. Affinché gli ordini di vendita di Dynamics CRM funzionino senza problemi, è necessario associare prima clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse.

### <a name="synchronizing-records-fully"></a>Sincronizzazione completa dei record
Alla fine della Guida di setup assistito è possibile scegliere l'azione **Esegui sincronizzazione completa** per iniziare a sincronizzare tutti i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] con tutti i record correlati nella soluzione Dynamics CRM connessa. Nella finestra **Revisione sincronizzazione completa CRM** scegliere l'azione **Avvia**. La sincronizzazione quindi inizia a eseguire i processi in base alle dipendenze. Ad esempio, i record valuta vengono sincronizzati prima dei record cliente. La sincronizzazione completa può richiedere molto tempo e pertanto venire eseguita in background in modo che sia possibile continuare a lavorare in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Per controllare l'avanzamento dei singoli processi in una sincronizzazione completa, eseguire il drill down nel campo **Stato movimento coda processi**, **Stato processo a tabella di integrazione** o **Stato processo da tabella di integrazione** nella finestra **Revisione sincronizzazione completa CRM**.

Nella finestra **Setup connessione CRM** è possibile ottenere in qualsiasi momento le informazioni sulla sincronizzazione completa. Da qui, è anche possibile aprire la finestra **Mapping tabella integrazione** per visualizzare ulteriori dettagli sulle tabelle nella soluzione Financials e in Dynamics CRM da sincronizzare.

## <a name="see-also"></a>Vedi anche
[Relationship Management](marketing-relationship-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizzazione dell'interfaccia utente di [!INCLUDE[d365fin](includes/d365fin_md.md)]] (ui-experiences.md)  
[Procedura: Gestire gli utenti e le autorizzazioni](ui-how-users-permissions.md)    
[Aggiungere l'organizzazione e gli utenti in Dynamics 365 (online)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

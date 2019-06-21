---
title: Gestire i clienti tramite Dynamics 365 for Sales | Microsoft Docs
description: È possibile utilizzare Dynamics 365 for Sales da Business Central per mappare i dati e sfruttare l'integrazione ottimale e la sincronizzazione nel processo dai lead agli incassi.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3cc053158581d4fc9b87dc3e505a23ed809c1c8f
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620863"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Utilizzo di Dynamics 365 for Sales da Business Central
Se si utilizza Dynamics 365 for Sales per l'interazione con i clienti, è possibile sfruttare un'integrazione ottimale nel processo dai lead agli incassi utilizzando [!INCLUDE[d365fin](includes/d365fin_md.md)] per le attività backend come elaborare ordini e gestire l'inventario e le finanze.

> [!NOTE]
> In questo argomento si presuppone che si stanno utilizzando le versioni online di [!INCLUDE[d365fin](includes/d365fin_md.md)] e Sales. È possibile combinare le versioni online e locale, ma è necessaria una configurazione speciale. Per ulteriori informazioni, vedere [Preparazione all'integrazione in Dynamics 365 for Sales (locale)](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

L'integrazione delle applicazioni consente di accedere ai dati in Sales da [!INCLUDE[d365fin](includes/d365fin_md.md)] e in alcuni casi di effettuare l'operazione inversa. È possibile utilizzare e sincronizzare i dati che sono comuni a entrambi i servizi, quali clienti, contatti e informazioni sulle vendite, e mantenere i dati aggiornati in entrambe le applicazioni.  

Ad esempio, un agente in Sales può utilizzare listini prezzi di [!INCLUDE[d365fin](includes/d365fin_md.md)] quando si crea un ordine di vendita. Quando si aggiunge l'articolo alla riga dell'ordine di vendita in Sales, può visualizzare il livello di magazzino (disponibilità) dell'articolo da [!INCLUDE[d365fin](includes/d365fin_md.md)].

Viceversa, i gestori ordini in [!INCLUDE[d365fin](includes/d365fin_md.md)] possono gestire gli ordini di vendita che vengono trasferiti automaticamente o manualmente da Sales Ad esempio, può creare e registrare righe di ordini di vendita valide per articoli o risorse che sono stati inseriti in Sales come prodotti aggiunti. Per ulteriori informazioni, vedere [Gestione di dati di ordini di vendita](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] è integrabile solo con Dynamics 365 for Sales. Altre applicazioni di Dynamics 365 che modificano il workflow standard o il modello dati in Sales, ad esempio Project Service Automation, possono interrompere l'integrazione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e Sales.

### <a name="coupling-records"></a>Associazione di record
La guida al setup assistito consente di scegliere i dati da sincronizzare. In seguito, è anche possibile impostare la sincronizzazione per specifici record. Questa operazione è definita *associazione*. Ad esempio, è possibile associare un conto specifico in Sales a un cliente specifico in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In questa sezione viene descritto cosa prendere in considerazione quando si associano record.

Ad esempio, se si desidera visualizzare i conti in Sales come clienti in [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario associare i due tipi di record. A questo proposito, nella pagina elenco **Clienti** in [!INCLUDE[d365fin](includes/d365fin_md.md)], utilizzare l'azione **Imposta associazione**. Specificare quindi quali clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] corrispondono ai conti in Sales.

È inoltre possibile creare (e associare) un conto in Sales basato, ad esempio, sul record cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando **Crea conto in Dynamics 365 for Sales** o viceversa utilizzando **Crea cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Quando si imposta l'associazione tra due record, è anche possibile richiedere manualmente il record corrente, ad esempio un cliente, da sovrascrivere immediatamente con i dati del conto in Sales (o da [!INCLUDE[d365fin](includes/d365fin_md.md)]) utilizzando l'azione **Sincronizza adesso**. L'azione**Sincronizza ora** che chiederà se sovrascrivere i dati dei record di Sales o di  [!INCLUDE[d365fin](includes/d365fin_md.md)].

In alcuni casi, è necessario associare determinati set di dati prima di altri, come indicato nella tabella seguente.

|Dati|Cosa associare per primo|
|-----|----|
|Clienti e conti|Associare agenti a utenti di Sales|
|Articoli e risorse|Associare unità di misura a gruppi di unità di Sales|
|Articoli e prezzi risorse|Associare gruppi di prezzi cliente a prezzi di Sales|

> [!NOTE]  
> Se i prezzi o i clienti utilizzano valuta estera, verificare di associare le valute alle valute della transazione di Sales.

Gli ordini di vendita di Sales dipendono da informazioni come clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse. Affinché l'integrazione con gli ordini di vendita funzioni, è necessario associare clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse.

### <a name="fully-synchronizing-records"></a>Sincronizzazione completa dei record
Alla fine della guida al setup assistito è possibile scegliere l'azione **Esegui sincronizzazione completa** per iniziare a sincronizzare tutti i record di [!INCLUDE[d365fin](includes/d365fin_md.md)] con tutti i record correlati in Sales. Nella pagina **Revisione sincronizzazione completa di Dynamics 365 for Sales**, scegliere l'azione **Avvia**. Il completamento della sincronizzazione completa può richiedere tempo, ma è possibile continuare a lavorare in [!INCLUDE[d365fin](includes/d365fin_md.md)] mentre viene eseguita in background.

Per controllare l'avanzamento dei singoli processi in una sincronizzazione completa, nella pagina **Revisione sincronizzazione completa di Dynamics 365 for Sales** scegliere un record per visualizzare i dettagli. Per aggiornare lo stato durante la sincronizzazione, aggiornare la pagina.

Nella finestra **Setup connessione Microsoft Dynamics 365** è possibile ottenere in qualsiasi momento le informazioni sulla sincronizzazione completa. Da qui, è anche possibile aprire la pagina **Mapping tabella integrazione** per visualizzare ulteriori dettagli sulle tabelle in [!INCLUDE[d365fin](includes/d365fin_md.md)] e in Sales da sincronizzare.

## <a name="handling-sales-order-data"></a>Gestione di dati di ordini di vendita
Gli ordini di vendita inviati in [!INCLUDE[crm_md](includes/crm_md.md)] verranno trasferiti automaticamente a [!INCLUDE[d365fin](includes/d365fin_md.md)] se si seleziona la casella di controllo **Crea ordini di vendita automaticamente** nella pagina **Setup connessione Microsoft Dynamics 365**.
In alternativa, è possibile convertire manualmente gli ordini di vendita inviati da [!INCLUDE[crm_md](includes/crm_md.md)] utilizzando l'azione **Crea in [!INCLUDE[d365fin](includes/d365fin_md.md)]** disponibile nella pagina **Ordini di vendita - Dynamics 365 for Sales**.
In tali ordini di vendita, il campo **Nome** dell'ordine originale viene trasferito e mappato al campo **Nr. documento esterno** dell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ciò può anche avvenire se l'ordine di vendita originale contiene prodotti aggiunti, ovvero articoli o risorse che non sono registrati nelle app. In tal caso, è necessario compilare i campi **Tipo prodotto aggiunto** e **Nr. prodotto aggiunto** nella pagina **Setup contabilità clienti e vendite**, in modo che tali vendite di prodotti non registrate siano mappate a un numero di articolo/risorsa specificato per le analisi finanziarie.

Se la descrizione dell'articolo nell'ordine di vendita originale è molto lunga, una riga aggiuntiva di tipo **Commento** viene creata per contenere tutto il testo nell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Gli aggiornamenti dei campi nella testata dell'ordine di vendita, ad esempio Data ultima spedizione o Data di consegna richiesta, che sono mappati nel **Mapping tabella integrazione** SALESORDER-ORDER sono sincronizzati periodicamente con [!INCLUDE[crm_md](includes/crm_md.md)]. I processi come il rilascio e la spedizione o la fatturazione di un ordine di vendita vengono registrati nella relativa sequenza temporale in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Introduzione a feed di attività](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

## <a name="handling-sales-quotes-data"></a>Gestione di dati di offerte di vendita
Le offerte di vendita attivate in [!INCLUDE[crm_md](includes/crm_md.md)] verranno trasferiti a [!INCLUDE[d365fin](includes/d365fin_md.md)] se si seleziona la casella di controllo **Elabora automaticamente offerte di vendita** nella pagina **Setup connessione Microsoft Dynamics 365**.
In alternativa, è possibile convertire manualmente offerte di vendita attivate da [!INCLUDE[crm_md](includes/crm_md.md)] utilizzando l'azione **Elabora in [!INCLUDE[d365fin](includes/d365fin_md.md)]** nella pagina **Offerte di vendita - Dynamics 365 for Sales**.
In tali offerte di vendita, il campo **Nome** nell'offerta originale viene trasferito e mappato al campo **Nr. documento esterno** dell'ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Anche il campo **Data di validità finale** nell'offerta viene trasferito e mappato al campo **Offerta valida fino alla data** in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Le offerte di vendita sono sottoposte a numerose revisioni durante la finalizzazione. Sia l'elaborazione manuale che quella automatica delle offerte di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiscono l'archiviazione delle versioni precedenti delle offerte di vendita prima dell'elaborazione di nuove revisioni delle offerte di vendita da [!INCLUDE[crm_md](includes/crm_md.md)]. 

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Gestione di spedizioni vendita registrate, pagamenti clienti e statistiche
Dopo l'evasione di un ordine di vendita, verranno create le fatture per lo stesso. Quando si fattura l'ordine di vendita, è possibile trasferire le spedizioni vendita registrate a [!INCLUDE[crm_md](includes/crm_md.md)] se si seleziona **Crea fattura in [!INCLUDE[crm_md](includes/crm_md.md)]** nella pagina Fattura di vendita registrata. Le fatture registrate vengono trasferite a [!INCLUDE[crm_md](includes/crm_md.md)] con lo stato **Fatturato**. Dopo il ricevimento del pagamento cliente per la fattura di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)], lo stato della fattura diventerà **Pagato** con Motivo stato impostato su **Parziale**, se pagata parzialmente, o su **Completo**, se pagata completamente, quando si esegue **Aggiorna statistiche account** nella pagina del cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. **Aggiorna statistiche account** aggiornerà anche valori come Saldo e Totale vendite nel Dettaglio informazioni statistiche conto di [!INCLUDE[d365fin](includes/d365fin_md.md)] in [!INCLUDE[crm_md](includes/crm_md.md)].
In alternativa, è possibile avere dei processi programmati (Statistiche cliente e POSTEDSALESINV-INV) che eseguono automaticamente entrambi i processi in background. 

## <a name="see-also"></a>Vedere anche
[Preparazione all'integrazione in Dynamics 365 for Sales (locale)](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Gestione delle relazioni](marketing-relationship-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)    
[Aggiungere l'organizzazione e gli utenti in Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

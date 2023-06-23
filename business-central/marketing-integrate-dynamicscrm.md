---
title: Gestire i clienti tramite Dynamics 365 Sales (video) | Microsoft Docs
description: È possibile utilizzare Dynamics 365 Sales da Business Central con l'integrazione ottimale e la sincronizzazione nel processo dai lead agli incassi.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'integration, synchronize, map, Sales'
ms.search.forms: '9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250'
ms.date: 09/16/2022
ms.author: bholtorf
---
# <a name="use-dynamics-365-sales-from-business-central" />Utilizzare Dynamics 365 Sales da Business Central
Se si utilizza Dynamics 365 Sales for Customer Engagement, è possibile sfruttare un'integrazione ottimale nel processo dai lead agli incassi utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] per le attività backend come elaborare ordini e gestire inventario e finanze.

Prima di poter utilizzare le funzionalità di integrazione, l'amministratore di sistema deve impostare la connessione e definire gli utenti in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Questi passaggi descrivono il processo Integrazione online delle versioni di [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)]. Per informazioni sulla configurazione locale, vedere [Preparazione di Dynamics 365 Sales per l'integrazione locale](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

L'integrazione delle applicazioni consente di accedere ai dati in Sales da [!INCLUDE[prod_short](includes/prod_short.md)] e in alcuni casi di effettuare l'operazione inversa. È possibile utilizzare e sincronizzare i dati che sono comuni a entrambi i servizi, quali clienti, contatti e informazioni sulle vendite, e mantenere i dati aggiornati in entrambe le applicazioni.  

Ad esempio, un agente di vendita in [!INCLUDE[crm_md](includes/crm_md.md)] può utilizzare listini prezzi di [!INCLUDE[prod_short](includes/prod_short.md)] quando si crea un ordine di vendita. Quando si aggiunge l'articolo alla riga dell'ordine di vendita in [!INCLUDE[crm_md](includes/crm_md.md)], può visualizzare il livello di magazzino (disponibilità) dell'articolo da [!INCLUDE[prod_short](includes/prod_short.md)].

Viceversa, i gestori ordini in [!INCLUDE[prod_short](includes/prod_short.md)] possono gestire gli ordini di vendita che vengono trasferiti automaticamente o manualmente da [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, può creare e registrare righe di ordini di vendita valide per articoli o risorse che sono stati inseriti in [!INCLUDE[crm_md](includes/crm_md.md)] come prodotti aggiunti. Per ulteriori informazioni, vedere [Gestione di dati di ordini di vendita](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] è integrabile solo con [!INCLUDE[crm_md](includes/crm_md.md)]. Altre applicazioni di Dynamics 365 che modificano il workflow standard o il modello dati in [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio Project Service Automation, possono interrompere l'integrazione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="coupling-records" />Associazione di record
La guida al setup assistito consente di scegliere i dati da sincronizzare. In seguito, è anche possibile impostare la sincronizzazione per specifici record. Questa operazione è definita *associazione*. Ad esempio, è possibile associare un conto specifico in [!INCLUDE[crm_md](includes/crm_md.md)] a un cliente specifico in [!INCLUDE[prod_short](includes/prod_short.md)]. In questa sezione viene descritto cosa prendere in considerazione quando si associano record.

Ad esempio, se si desidera visualizzare i conti di [!INCLUDE[crm_md](includes/crm_md.md)] come clienti in [!INCLUDE[prod_short](includes/prod_short.md)], è necessario associare i due tipi di record. A questo proposito, nella pagina elenco **Clienti** in [!INCLUDE[prod_short](includes/prod_short.md)], utilizzare l'azione **Imposta associazione**. Specificare quindi quali clienti di [!INCLUDE[prod_short](includes/prod_short.md)] corrispondono ai conti in [!INCLUDE[crm_md](includes/crm_md.md)].

È inoltre possibile creare (e associare) un conto in [!INCLUDE[crm_md](includes/crm_md.md)] basato, ad esempio, sul record cliente in [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando **Crea conto in Dynamics 365 Sales** o viceversa utilizzando **Crea cliente in [!INCLUDE[prod_short](includes/prod_short.md)]**.

Quando si imposta l'associazione tra due record, è anche possibile richiedere manualmente il record corrente, ad esempio un cliente, da sovrascrivere immediatamente con i dati del conto in Sales (o da [!INCLUDE[prod_short](includes/prod_short.md)]) utilizzando l'azione **Sincronizza adesso**. L'azione**Sincronizza ora** che chiederà se sovrascrivere i dati dei record di Sales o di  [!INCLUDE[prod_short](includes/prod_short.md)].

In alcuni casi, è necessario associare determinati set di dati prima di altri, come indicato nella tabella seguente.

|Dati|Cosa associare per primo|
|-----|----|
|Clienti e conti|Associare agenti a utenti di [!INCLUDE[crm_md](includes/crm_md.md)]|
|Articoli e risorse|Associare unità di misura con le unità di vendita [!INCLUDE[crm_md](includes/crm_md.md)]|
|Articoli e prezzi risorse|Associare gruppi di prezzi cliente a prezzi di [!INCLUDE[crm_md](includes/crm_md.md)]|

> [!NOTE]  
> Se i prezzi o i clienti utilizzano valuta estera, verificare di associare le valute alle valute della transazione di Sales.

Gli ordini di vendita di [!INCLUDE[crm_md](includes/crm_md.md)] dipendono da informazioni come clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse. Affinché l'integrazione con gli ordini di vendita funzioni, è necessario associare clienti, unità di misura, valute, gruppi di prezzi cliente, articoli e/o risorse.

## <a name="fully-synchronizing-records" />Sincronizzazione completa dei record
Alla fine della guida al setup assistito è possibile scegliere l'azione **Esegui sincronizzazione completa** per iniziare a sincronizzare tutti i record di [!INCLUDE[prod_short](includes/prod_short.md)] con tutti i record correlati in [!INCLUDE[crm_md](includes/crm_md.md)]. Nella pagina **Revisione sincronizzazione completa di Dynamics 365 Sales** scegliere l'azione **Avvia**. Il completamento della sincronizzazione completa può richiedere tempo, ma è possibile continuare a lavorare in [!INCLUDE[prod_short](includes/prod_short.md)] mentre viene eseguita in background.

Per controllare l'avanzamento dei singoli processi in una sincronizzazione completa, nella pagina **Revisione sincronizzazione completa di Dynamics 365 Sales** scegliere un record per visualizzare i dettagli. Per aggiornare lo stato durante la sincronizzazione, aggiornare la pagina.

Nella finestra **Setup connessione a Microsoft Dynamics 365** è possibile ottenere in qualsiasi momento le informazioni sulla sincronizzazione completa. Da qui, è anche possibile aprire la pagina **Mapping tabella integrazione** per visualizzare ulteriori dettagli sulle tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] e in Sales da sincronizzare.

## <a name="handling-sales-order-data" />Gestione di dati di ordini di vendita
Gli ordini di vendita che le persone inviano in [!INCLUDE[crm_md](includes/crm_md.md)] vengono automaticamente trasferiti a [!INCLUDE[prod_short](includes/prod_short.md)] se selezioni la casella di controllo **Crea automaticamente ordini vendita** nella pagina **Setup connessione a Microsoft Dynamics 365**.
In alternativa, è possibile convertire manualmente gli ordini di vendita inviati da [!INCLUDE[crm_md](includes/crm_md.md)] utilizzando l'azione **Crea in [!INCLUDE[prod_short](includes/prod_short.md)]** disponibile nella pagina **Ordini di vendita - Dynamics 365 for Sales**.
In tali ordini di vendita, il campo **Nome** dell'ordine originale viene trasferito e mappato al campo **Nr. documento esterno** dell'ordine di vendita in [!INCLUDE[prod_short](includes/prod_short.md)].

Ciò può anche avvenire se l'ordine di vendita originale contiene prodotti aggiunti, ovvero articoli o risorse che non sono registrati nelle app. In tal caso, è necessario compilare i campi **Tipo prodotto aggiunto** e **Nr. prodotto aggiunto** nella pagina **Setup contabilità clienti e vendite**, in modo che le vendite di prodotti non registrati siano mappate a un numero di articolo o risorsa specificato.

> [!NOTE]
> Non è possibile mappare un'aggiunta a un articolo o una risorsa in [!INCLUDE[prod_short](includes/prod_short.md)] che è associato a un prodotto in [!INCLUDE[crm_md](includes/crm_md.md)]. Per consentire le aggiunte è consigliabile creare un articolo o una risorsa appositamente per quello scopo e non associarlo a un prodotto in [!INCLUDE[crm_md](includes/crm_md.md)]. 

Se la descrizione dell'articolo nell'ordine di vendita originale è molto lunga, una riga aggiuntiva di tipo **Commento** viene creata per contenere tutto il testo nell'ordine di vendita in [!INCLUDE[prod_short](includes/prod_short.md)].

Gli aggiornamenti dei campi nelle testate dell'ordine di vendita, ad esempio Data ultima spedizione o Data di consegna richiesta, che sono mappati nel Mapping tabella integrazione **SALESORDER-ORDER** sono sincronizzati periodicamente con [!INCLUDE[crm_md](includes/crm_md.md)]. I processi come il rilascio, la spedizione e la fatturazione di un ordine di vendita vengono registrati nella relativa sequenza temporale in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Introduzione a feed di attività](/dynamics365/sales-enterprise/manage-activities). Per abilitare la registrazione e le attività per gli ordini in [!INCLUDE[crm_md](includes/crm_md.md)], vedi [Configurare il controllo delle note per accedere alle informazioni sui post per un'entità personalizzata](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) nella documentazione di Customer Engagement. L'articolo fa riferimento a Customer Engagement on-premises, ma i passaggi sono gli stessi per la versione online. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> La sincronizzazione periodica basata sul Mapping tabella integrazione **SALESORDER-ORDER** funzionerà solo quando l'integrazione dell'ordine cliente è abilitata. Per ulteriori informazioni, vedere [Impostazioni di connessione nella pagina di impostazione della connessione di vendita](admin-prepare-dynamics-365-for-sales-for-integration.md). Solo gli ordini cliente creati da ordini cliente inviati in [!INCLUDE[crm_md](includes/crm_md.md)] vengono sincronizzati. Per ulteriori informazioni, vedere [Abilitare l'integrazione dell'elaborazione degli ordini di vendita](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data" />Gestione di dati di offerte di vendita
Le offerte di vendita attivate in [!INCLUDE[crm_md](includes/crm_md.md)] verranno trasferiti a [!INCLUDE[prod_short](includes/prod_short.md)] se si seleziona la casella di controllo **Elabora automaticamente offerte di vendita** nella pagina **Setup connessione a Microsoft Dynamics 365**.
In alternativa, è possibile convertire manualmente offerte di vendita attivate da [!INCLUDE[crm_md](includes/crm_md.md)] utilizzando l'azione **Elabora in [!INCLUDE[prod_short](includes/prod_short.md)]** nella pagina **Offerte di vendita - Dynamics 365 Sales**.
In tali offerte di vendita, il campo **Nome** nell'offerta originale viene trasferito e mappato al campo **Nr. documento esterno** dell'ordine di vendita in [!INCLUDE[prod_short](includes/prod_short.md)]. Anche il campo **Data di validità finale** nell'offerta viene trasferito e mappato al campo **Offerta valida fino alla data** in [!INCLUDE[prod_short](includes/prod_short.md)].  

Le offerte di vendita sono sottoposte a numerose revisioni durante la finalizzazione. Sia l'elaborazione manuale che quella automatica delle offerte di vendita in [!INCLUDE[prod_short](includes/prod_short.md)] garantiscono l'archiviazione delle versioni precedenti delle offerte di vendita prima dell'elaborazione di nuove revisioni delle offerte di vendita da [!INCLUDE[crm_md](includes/crm_md.md)].

Quando si sceglie **Processi** in [!INCLUDE[prod_short](includes/prod_short.md)] per un'offerta nello stato **Vinta**, viene creato un ordine cliente in [!INCLUDE[prod_short](includes/prod_short.md)] solo se viene inviato un ordine di vendita corrispondente in [!INCLUDE[crm_md](includes/crm_md.md)]. In caso contrario, l'offerta viene rilasciata solo in [!INCLUDE[prod_short](includes/prod_short.md)]. Se un ordine di vendita corrispondente viene inviato in [!INCLUDE[crm_md](includes/crm_md.md)] in seguito e da esso viene creato un ordine di vendita, il **numero di offerta** viene aggiornato sull'ordine di vendita e l'offerta viene archiviata.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics" />Gestione di spedizioni vendita registrate, pagamenti clienti e statistiche
Dopo l'evasione di un ordine di vendita, verranno create le fatture per lo stesso. Quando si fattura un ordine di vendita, è possibile trasferire le spedizioni vendita registrate a [!INCLUDE[crm_md](includes/crm_md.md)] se si seleziona la casella di controllo **Crea fattura in [!INCLUDE[crm_md](includes/crm_md.md)]** nella pagina **Fattura vendita registrata**. Le fatture registrate vengono trasferite a [!INCLUDE[crm_md](includes/crm_md.md)] con lo stato **Fatturato**.

Quando si riceve il pagamento cliente per la fattura di vendita in [!INCLUDE[prod_short](includes/prod_short.md)], lo stato della fattura diventerà **Pagato** con **Motivo stato** impostato su **Parziale**, se pagata parzialmente, o su **Completo**, se pagata completamente, quando si sceglie l'azione **Aggiorna statistiche account** nella pagina del cliente in [!INCLUDE[prod_short](includes/prod_short.md)]. La funzione **Aggiorna statistiche account** aggiornerà anche i valori come i campi **Saldo** e **Totale vendite** nel Dettaglio informazioni **Statistiche conto di [!INCLUDE[prod_short](includes/prod_short.md)]** in [!INCLUDE[crm_md](includes/crm_md.md)]. In alternativa, è possibile avere i processi programmati, Statistiche cliente e POSTEDSALESINV-INV che eseguono automaticamente questi processi in background. 

## <a name="handling-sales-prices" />Gestione dei prezzi di vendita
> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 abbiamo rilasciato processi semplificati per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti che utilizzano questa versione, trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

I passaggi per completare questo processo differiscono a seconda se l'amministratore ha abilitato o meno la nuova esperienza di prezzo. 

> [!NOTE]
> Se la sincronizzazione dei prezzi standard non funziona, ti consigliamo di utilizzare le funzionalità di personalizzazione dell'integrazione. Per ulteriori informazioni, vedi [Personalizzazione di un'integrazione con Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Esperienza corrente](#tab/current-experience/)
Nell'attuale esperienza di determinazione dei prezzi [!INCLUDE[prod_short](includes/prod_short.md)] sincronizza i prezzi di vendita che: 

* Si applicano a tutti i clienti. I listini prezzi di vendita predefiniti vengono creati in base al prezzo nel campo **Prezzo unitario** nella pagine **Scheda articolo** degli articoli.
* Si applicano a un gruppo di prezzi cliente specifico. Ad esempio, i prezzi di vendita per i tuoi clienti al dettaglio o all'ingrosso. Per sincronizzare i prezzi in base a un gruppo di prezzi cliente, procedi come segue:

    1. Associa gli articoli per i quali i prezzi sono impostati dal gruppo di prezzi del cliente.
    2. Nella pagina **Gruppi prezzi cliente** associa il gruppo prezzi cliente scegliendo **Correlati**, quindi **Dynamics 365 Sales**, **Associazione**, quindi **Imposta associazione**. L'associazione creerà un listino prezzi attivo in [!INCLUDE[prod_short](includes/prod_short.md)] con lo stesso nome del gruppo di prezzi del cliente in [!INCLUDE[crm_md](includes/crm_md.md)] e sincronizza automaticamente tutti gli articoli per i quali il gruppo di prezzi del cliente definisce il prezzo.

:::image type="content" source="media/customer-price-group.png" alt-text="Pagina Gruppo prezzi cliente.":::

#### [Nuova esperienza](#tab/new-experience/)  

La nuova esperienza di determinazione del prezzo sincronizza i listini prezzi che soddisfano i seguenti criteri:

* **Consenti aggiornamento impostazioni predefinite** è disattovato.
* Il tipo di prezzo è Vendita.
* Il tipo di importo è Prezzo.
* Il tipo di prodotto nelle righe deve essere Articolo o Risorsa. 
* Non è specificata una quantità minima.

[!INCLUDE[prod_short](includes/prod_short.md)] sincronizza i prezzi di vendita che si applicano a tutti i clienti. I listini prezzi di vendita predefiniti vengono creati in base al prezzo nel campo **Prezzo unitario** nella pagine **Scheda articolo** degli articoli.

Per sincronizzare i listini prezzi, nella pagina **Listino prezzi di vendita** scegli **Correlato**, **Dynamics 365 Sales**, **Associazione**, quindi **Imposta associazione**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Pagina Listino prezzi di vendita.":::

---


## <a name="see-also" />Vedere anche
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gestione delle relazioni](marketing-relationship-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)    
[Panoramica di Sales e dell'Hub delle vendite](/dynamics365/customer-engagement/sales-enterprise/overview)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]

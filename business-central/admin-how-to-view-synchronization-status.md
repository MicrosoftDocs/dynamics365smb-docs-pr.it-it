---
title: Visualizzare lo stato dei processi di sincronizzazione (video)
description: Utilizza la pagina Errori di sincronizzazione dati associati per visualizzare lo stato dei lavori di sincronizzazione che sono stati eseguiti per i record associati in integrazioni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
---

# <a name="view-the-status-of-synchronization-jobs"></a><a name="view-the-status-of-synchronization-jobs"></a>Visualizzare lo stato dei processi d sincronizzazione


Utilizzare la pagina **Errori di sincronizzazione dati associati** per visualizzare lo stato dei lavori di sincronizzazione che sono stati eseguiti per i record associati in un'integrazione di Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. Ciò include i processi eseguiti dalla coda processi e i processi di sincronizzazione manuale eseguiti sui record di [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, la visualizzazione del relativo stato è utile per risolvere problemi in quanto consente di accedere ai dettagli degli errori relativi ai record associati. In genere, questi tipi di errori sono causati da azioni dell'utente, ad esempio, quando:  

* Due persone hanno apportato una modifica agli stessi dati in entrambe le app aziendali.
* Qualcuno ha cancellato dei dati in una delle app, ma non entrambe.

> [!Note]
> La pagina **Errori di sincronizzazione dati associati**mostra informazioni sui processi relativi ai record associati. Se si risolvono tutti gli errori ma i record continuano a non essere sincronizzati, è possibile che il problema sia dovuto all'impostazione per l'integrazione. In genere, l'amministratore dovrà risolvere questi tipi di errori.   

## <a name="example"></a><a name="example"></a>Esempio
Questo video mostra un esempio di come risolvere gli errori che si sono verificati durante la sincronizzazione con [!INCLUDE[prod_short](includes/cds_long_md.md)]. Il processo sarà lo stesso per tutte le integrazioni. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a><a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Per visualizzare e risolvere gli errori di sincronizzazione per record associati
1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Errori di sincronizzazione dati associati** e scegli il collegamento correlato.
2. Nella pagina **Errori di sincronizzazione dati associati** vengono visualizzati i problemi verificatisi durante la sincronizzazione di record associati. La seguente tabella include le azioni che è possibile utilizzare per risolvere i problemi singolarmente:

|Azione|Descrizione|
|----|----|
|**Rimuovi associazione**|Elimina l'associazione dei record, che non verranno più sincronizzati. Per riavviare la sincronizzazione è necessario associarli nuovamente. |
|**Riprova** e **Riprova tutto**|Per ogni record in cui viene rilevato un errore, la sincronizzazione viene saltata a meno che non si risolva il problema. Riprova includerà il record selezionato nella sincronizzazione successiva e **Riprova tutto** include tutti i record.|
|**Sincronizza**|L'app proverà a risolvere un conflitto in cui i dati sono stati modificati in entrambe le app aziendali. È possibile scegliere i dati da utilizzare.|
|**Ripristina record**ed **Elimina record**|Sono utili quando un record è stato eliminato in una delle app aziendali. Elimina record elimina il record o la riga nell'app in cui è ancora presente. Ripristina record ricrea il record o la riga nell'app aziendale in cui è stato eliminato.|

> [!NOTE]
> Per ridurre il numero di conflitti da risolvere, è possibile impostare i mapping della tabella di integrazione in modo che applichino automaticamente queste azioni. Per ulteriori informazioni, vedere [Mapping delle tabelle di integrazione](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a><a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Per visualizzare il registro di sincronizzazione per uno specifico record (sincronizzato manualmente)
1. Aprire, ad esempio, un cliente, un articolo o qualunque altro record che esegue la sincronizzazione dei dati tra [!INCLUDE[prod_short](includes/prod_short.md)] e Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)].
2. Scegliere l'azione **Registro sincronizzazione** per visualizzare il registro di sincronizzazione per un record selezionato. Ad esempio, un cliente specifico sincronizzato manualmente.

## <a name="remove-couplings-between-records"></a><a name="remove-couplings-between-records"></a>Rimuovere associazioni tra record
Quando qualcosa va storto nell'integrazione ed è necessario annullare l'associazione dei record per interrompere la sincronizzazione, è possibile farlo per uno o più record alla volta. È possibile annullare l'associazione di uno o più record nelle pagine di elenco o nella pagina **Errori di sincronizzazione dati associati** scegliendo una o più righe e quindi **Elimina associazione**. È inoltre possibile rimuovere tutte le associazioni per una o più mapping di tabella nella pagina **Mapping tabella integrazione**. 

Se un'entità con un'associazione unidirezionale viene eliminata in [!INCLUDE[prod_short](includes/prod_short.md)], è necessario eliminare manualmente l'associazione interrotta. A tale scopo, nella pagina **Errori di sincronizzazione dati associati** scegliere l'azione **Trova per eliminate** ed eliminare le associazioni.

## <a name="see-also"></a><a name="see-also"></a>Vedere anche
[Impostazione di account utente per l'integrazione con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Utilizzare Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

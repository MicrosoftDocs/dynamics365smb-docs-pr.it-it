---
title: Sincronizzazione manuale di mapping di tabella | Microsoft Docs
description: La sincronizzazione copia i dati tra i movimenti di Dynamics 365 for Sales e Business Central per mantenere aggiornati entrambi i sistemi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 368bfc191aea4ae00c53d0c7ee892f3cc82c0ff7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245733"
---
# <a name="manually-synchronize-table-mappings"></a>Sincronizzare manualmente i mapping di tabella
Un mapping di tabella di integrazione associa una tabella [!INCLUDE[crm_md](includes/crm_md.md)] (tipo di record), come un cliente, a un'entità di [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio un conto. La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record della tabella di [!INCLUDE[d365fin](includes/d365fin_md.md)] e dell'entità di [!INCLUDE[crm_md](includes/crm_md.md)] associati. Inoltre, a seconda della configurazione di un mapping di tabella, la sincronizzazione può creare e associare nuovi record nella soluzione di destinazione per i record non associati nell'origine.  

La sincronizzazione manuale di mapping di tabella di integrazione può essere utile durante l'impostazione iniziale di un integrazione e nella diagnostica degli errori di sincronizzazione.  

In questo articolo vengono descritti tre metodi per la sincronizzazione manuale dei mapping di tabella di integrazione. Ogni metodo fornisce un diverso livello di sincronizzazione.

## <a name="run-a-full-synchronization"></a>Eseguire una sincronizzazione completa
Una sincronizzazione completa esegue tutti i processi di sincronizzazione di Integrazione di default per la sincronizzazione dei record di [!INCLUDE[d365fin](includes/d365fin_md.md)] e delle entità di [!INCLUDE[crm_md](includes/crm_md.md)], come definito nella pagina **Mapping tabella integrazione**. 

Una sincronizzazione completa esegue le seguenti operazioni per i record di [!INCLUDE[crm_md](includes/crm_md.md)] o [!INCLUDE[d365fin](includes/d365fin_md.md)]:

* Non associato, un nuovo record corrispondente verrà creato e associato nella soluzione opposta.
Se e dove un record viene creato dipende dalla direzione della sincronizzazione. Ad esempio, per sincronizzare i dati dei clienti di [!INCLUDE[d365fin](includes/d365fin_md.md)] ai conti di [!INCLUDE[crm_md](includes/crm_md.md)], se esiste un cliente che non è associato a un conto, un nuovo conto verrà automaticamente aggiunto in [!INCLUDE[crm_md](includes/crm_md.md)] e associato al cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il contrario è vero quando la direzione della sincronizzazione è da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ogni conto che non è già associato a un cliente, un nuovo cliente corrispondente verrà creato in [!INCLUDE[crm_md](includes/crm_md.md)] e associato al conto in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

     > [!NOTE]  
     >  Per eseguire questa operazione, la sincronizzazione completa deseleziona temporaneamente l'opzione **Sinc. solo record associati** nel mapping di tabella di integrazione utilizzato dal processo di sincronizzazione. Al termine del processo di sincronizzazione completa, verrà richiesto se si desidera mantenere questa opzione deselezionata per tutti i processi.  

* Associata, la direzione di sincronizzazione (ad esempio da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]) è predeterminata dai mapping di tabella di integrazione. Per ulteriori informazioni, vedere [Mapping delle entità standard di Sales per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization).  

I processi sono eseguiti nel seguente ordine per evitare di associare dipendenze tra entità.  

1.  Processo di sincronizzazione VALUTA - Dynamics 365 for Sales  
2.  Processo di sincronizzazione AGENTI - Dynamics 365 for Sales  
3.  Processo di sincronizzazione UNITÀDIMISURA - Dynamics 365 for Sales  
4.  Processo di sincronizzazione CLIENTE - Dynamics 365 for Sales  
5.  Processo di sincronizzazione CONTATTO - Dynamics 365 for Sales  
6.  Processo di sincronizzazione RISORSA-PRODOTTO - Dynamics 365 for Sales  
7.  Processo di sincronizzazione ARTICOLO-PRODOTTO - Dynamics 365 for Sales  

> [!IMPORTANT]  
>  In genere si utilizza la sincronizzazione completa solo quando si imposta l'integrazione inizialmente tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] e una sola delle soluzioni contiene dati, che si desidera copiare nell'altra soluzione. Una sincronizzazione completa può risultare utile in un ambiente dimostrativo. Poiché la sincronizzazione completa crea e associa automaticamente record tra soluzioni, rende più rapido iniziare a lavorare con dati di sincronizzazione tra record. D'altro canto, è necessario eseguire la sincronizzazione completa solo se si desidera un record in [!INCLUDE[d365fin](includes/d365fin_md.md)] per ogni record in [!INCLUDE[crm_md](includes/crm_md.md)] per i mapping di tabella specificati. In caso contrario, è possibile avere record indesiderati o duplicati in [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[crm_md](includes/crm_md.md)].  

### <a name="see-the-process-for-a-full-synchronization"></a>Vedere il processo per una sincronizzazione completa
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### <a name="to-run-a-full-synchronization"></a>Per eseguire una sincronizzazione completa  
1.  Scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione Microsoft Dynamics 365 for Sales** e quindi scegliere il collegamento correlato.
2.  Scegliere l'azione **Esegui sincronizzazione completa**, quindi scegliere il pulsante **Sì**.  
3.  Al termine della sincronizzazione completa, è possibile specificare se consentire la creazione di nuovi record con i processi di sincronizzazione programmati.  

    Se tutti i processi di sincronizzazione devono creare nuovi record nella destinazione dei record non associati nell'origine, scegliere **Sì**. In questo modo, il campo **Sinc. solo record associati** viene impostato nei mapping di tabella utilizzati dai processi di sincronizzazione.  

    Se si desidera che i processi di sincronizzazione siano eseguiti prima della sincronizzazione completa in relazione alla creazione di nuovi record, scegliere **No**. Cosi facendo, il campo **Sinc. solo record associati** viene impostato sul valore che aveva prima della sincronizzazione completa.  

È possibile visualizzare i risultati della sincronizzazione completa nella pagina **Processi di sincronizzazione integrazione**. Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Sincronizzazione di tutti i record modificati
È possibile utilizzare la pagina **Setup connessione a Microsoft Dynamics 365 for Sales** per sincronizzare le modifiche ai dati in tutti i mapping di tabella di integrazione. Ciò è simile a una sincronizzazione completa. I dati saranno sincronizzati in tutti i record associati nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] e nelle entità di [!INCLUDE[crm_md](includes/crm_md.md)] che sono definiti nei mapping di tabella. Per impostazione predefinita, solo i record che sono stati modificati dopo l'ultima sincronizzazione verranno sincronizzati. I mapping di tabella vengono sincronizzati nel seguente ordine per evitare di associare dipendenze tra entità:  

1.  Processo di sincronizzazione VALUTA - Dynamics 365 for Sales  
2.  Processo di sincronizzazione AGENTI - Dynamics 365 for Sales  
3.  Processo di sincronizzazione UNITÀDIMISURA - Dynamics 365 for Sales  
4.  Processo di sincronizzazione CLIENTE - Dynamics 365 for Sales  
5.  Processo di sincronizzazione CONTATTO - Dynamics 365 for Sales  
6.  Processo di sincronizzazione RISORSA-PRODOTTO \- Dynamics 365 for Sales  
7.  Processo di sincronizzazione ARTICOLO-PRODOTTO - Dynamics 365 for Sales  

È possibile visualizzare i risultati della sincronizzazione nella pagina **Processi di sincronizzazione integrazione**. Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Modificando il mapping di tabella di integrazione in anticipo, è possibile configurare la sincronizzazione con filtri per verificare quali record sono sincronizzati, o configurarla per creare nuovi record nella soluzione di destinazione per record non associati nell'origine. Per ulteriori informazioni, vedere [Modificare i mapping di tabella per la sincronizzazione](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Per sincronizzare record per tutte le tabelle  
1.  Scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione Microsoft Dynamics 365 for Sales** e quindi scegliere il collegamento correlato.
2.  Scegliere l'azione **Sincronizza record modificati**, quindi scegliere il pulsante **Sì**.  

## <a name="synchronize-individual-table-mappings"></a>Sincronizzare singoli mapping di tabella
È possibile utilizzare la pagina **Mapping tabella integrazione** per eseguire mapping di tabella specifici specifici del processo di sincronizzazione. In questo modo i dati saranno sincronizzati in tutti i record associati nelle tabelle di [!INCLUDE[d365fin](includes/d365fin_md.md)] e nelle entità di [!INCLUDE[crm_md](includes/crm_md.md)] che sono definiti dal mapping di tabella. Per impostazione predefinita, solo i record che sono stati modificati dopo l'ultima sincronizzazione verranno sincronizzati.  

Modificando il mapping di tabella di integrazione in anticipo, è possibile configurare il processo di sincronizzazione per creare nuovi record nella soluzione di destinazione per record non associati nell'origine.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Per sincronizzare i record di un mapping di tabella di integrazione  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.
2.  Scegliere l'azione **Sincronizza record modificati**, quindi scegliere il pulsante **Sì**.  

## <a name="see-also"></a>Vedere anche  
[Sincronizzazione di Business Central e Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Configurare l'integrazione di Dynamics 365 for Sales in Business Central](admin-setting-up-integration-with-dynamics-sales.md)   

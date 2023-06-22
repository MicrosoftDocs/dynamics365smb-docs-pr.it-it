---
title: Sincronizzazione manuale di mapping di tabella | Microsoft Docs
description: La sincronizzazione copia i dati tra le tabelle di Microsoft Dataverse e Business Central per mantenere aggiornati entrambi i sistemi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="manually-synchronize-table-mappings" />Sincronizzare manualmente i mapping di tabella


Un mapping di tabella di integrazione associa una tabella [!INCLUDE[prod_short](includes/cds_long_md.md)], come un cliente, a una tabella di [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio un conto. La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record della tabella di [!INCLUDE[prod_short](includes/prod_short.md)] e della tabella di [!INCLUDE[prod_short](includes/cds_long_md.md)] associati. Inoltre, a seconda della configurazione di un mapping di tabella, la sincronizzazione può creare e associare nuovi record nella soluzione di destinazione per i record non associati nell'origine.  

La sincronizzazione manuale di mapping di tabella di integrazione può essere utile durante l'impostazione iniziale di un integrazione e nella diagnostica degli errori di sincronizzazione.  

In questo articolo vengono descritti tre metodi per la sincronizzazione manuale dei mapping di tabella di integrazione. Ogni metodo fornisce un diverso livello di sincronizzazione.

## <a name="run-a-full-synchronization" />Eseguire una sincronizzazione completa
Una sincronizzazione completa esegue tutti i processi di sincronizzazione di Integrazione di default per la sincronizzazione dei record di [!INCLUDE[prod_short](includes/prod_short.md)] e delle tabelle di [!INCLUDE[prod_short](includes/cds_long_md.md)], come definito nella pagina **Mapping tabella integrazione**. 

Una sincronizzazione completa esegue le seguenti operazioni per i record di [!INCLUDE[prod_short](includes/cds_long_md.md)] o [!INCLUDE[prod_short](includes/prod_short.md)]:

* Non associata, una nuova riga corrispondente verrà creata e associata nella soluzione opposta.
Se e dove una riga viene creata dipende dalla direzione della sincronizzazione. Ad esempio, per sincronizzare i dati dei clienti di [!INCLUDE[prod_short](includes/prod_short.md)] ai conti di [!INCLUDE[prod_short](includes/cds_long_md.md)], se esiste un cliente che non è associato a un conto, un nuovo conto verrà automaticamente aggiunto in [!INCLUDE[prod_short](includes/cds_long_md.md)] e associato al cliente in [!INCLUDE[prod_short](includes/prod_short.md)]. Il contrario è vero quando la direzione della sincronizzazione è da [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)]. Per ogni conto che non è già associato a un cliente, un nuovo cliente corrispondente verrà creato in [!INCLUDE[prod_short](includes/cds_long_md.md)] e associato al conto in [!INCLUDE[prod_short](includes/prod_short.md)].  

     > [!NOTE]  
     >  Per eseguire questa operazione, la sincronizzazione completa deseleziona temporaneamente l'opzione **Sinc. solo record associati** nel mapping di tabella di integrazione utilizzato dal processo di sincronizzazione. Al termine del processo di sincronizzazione completa, verrà richiesto se si desidera mantenere questa opzione deselezionata per tutti i processi.  

* Associata, la direzione di sincronizzazione (ad esempio da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[prod_short](includes/cds_long_md.md)] o da [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)]) è predeterminata dai mapping di tabella di integrazione. Per ulteriori informazioni, vedere [Mapping delle tabelle standard per la sincronizzazione](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  In genere si utilizza la sincronizzazione completa solo quando si imposta l'integrazione inizialmente tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[prod_short](includes/cds_long_md.md)] e una sola delle soluzioni contiene dati, che si desidera copiare nell'altra soluzione. Una sincronizzazione completa può risultare utile in un ambiente dimostrativo. Poiché la sincronizzazione completa crea e associa automaticamente record tra soluzioni, rende più rapido iniziare a lavorare con dati di sincronizzazione tra record. D'altro canto, è necessario eseguire la sincronizzazione completa solo se si desidera una riga in [!INCLUDE[prod_short](includes/prod_short.md)] per ogni riga in [!INCLUDE[prod_short](includes/cds_long_md.md)] per i mapping di tabella specificati. In caso contrario, è possibile avere record indesiderati o duplicati in [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[prod_short](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization" />Per eseguire una sincronizzazione completa
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup connessione a Dataverse**, quindi scegli il collegamento correlato.

    > [!NOTE]
    > Se desideri eseguire una sincronizzazione completa per le tabelle tramite Dynamics 365 Sales, usa invece la pagina **Configurazione della connessione Microsoft Dynamics 365 Sales**.

2.  Scegliere l'azione **Esegui sincronizzazione completa**, quindi scegliere il pulsante **Sì**.  
3.  Al termine della sincronizzazione completa, è possibile specificare se consentire la creazione di nuovi record con i processi di sincronizzazione programmati.  

    Se tutti i processi di sincronizzazione devono creare nuovi record nella destinazione dei record non associati nell'origine, scegliere **Sì**. In questo modo, il campo **Sinc. solo record associati** viene impostato nei mapping di tabella utilizzati dai processi di sincronizzazione.  

    Se si desidera che i processi di sincronizzazione siano eseguiti prima della sincronizzazione completa in relazione alla creazione di nuovi record, scegliere **No**. Cosi facendo, il campo **Sinc. solo record associati** viene impostato sul valore che aveva prima della sincronizzazione completa.  

È possibile visualizzare i risultati della sincronizzazione completa nella pagina **Processi di sincronizzazione integrazione**. Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records" />Sincronizzazione di tutti i record modificati
È possibile utilizzare la pagina **Setup connessione a Common Data Service** per sincronizzare le modifiche ai dati in tutti i mapping di tabella di integrazione. Ciò è simile a una sincronizzazione completa. I dati saranno sincronizzati in tutti i record associati nelle tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] e di [!INCLUDE[prod_short](includes/cds_long_md.md)] che sono definiti nei mapping di tabella. Per impostazione predefinita, solo i dati che sono stati modificati dopo l'ultima sincronizzazione verranno sincronizzati. I processi di sincronizzazione sincronizzano i mapping di tabella nel seguente ordine per evitare di associare dipendenze tra tabelle:  

1.  VALUTA  
2.  AGENTI  
3.  FORNITORE  
4.  CLIENTE  
5.  CONTATTI  

È possibile visualizzare i risultati della sincronizzazione nella pagina **Processi di sincronizzazione integrazione**. Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Modificando il mapping di tabella di integrazione in anticipo, è possibile creare filtri per verificare i dati da sincronizzare, o configurare i mapping per creare nuovi dati nella soluzione di destinazione per record o righe non associati nell'origine. Per ulteriori informazioni, vedere [Modificare i mapping di tabella per la sincronizzazione](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables" />Sincronizzare dati per tutte le tabelle
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup connessione a Microsoft Dynamics 365 Sales**, quindi scegli il collegamento correlato.
2.  Scegliere l'azione **Sincronizza record modificati**, quindi scegliere il pulsante **Sì**.  

## <a name="synchronize-individual-table-mappings" />Sincronizzare singoli mapping di tabella
È possibile utilizzare la pagina **Mapping tabella integrazione** per eseguire un processo di sincronizzazione per mapping di tabella. In questo modo i dati saranno sincronizzati per tutti i record e le righe associati nelle tabelle di [!INCLUDE[prod_short](includes/prod_short.md)] e di [!INCLUDE[prod_short](includes/cds_long_md.md)] definite dal mapping di tabella. Per impostazione predefinita, solo i dati che sono stati modificati dopo l'ultima sincronizzazione verranno sincronizzati.  

### <a name="to-synchronize-records-of-an-integration-table-mapping" />Per sincronizzare i record di un mapping di tabella di integrazione
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Mapping tabella integrazione**, quindi scegli il collegamento correlato.
2.  Scegliere l'azione **Sincronizza record modificati**, quindi scegliere il pulsante **Sì**.  

## <a name="see-also" />Vedere anche
[Sincronizzazione di Business Central e Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Impostazione di account utente per l'integrazione con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]

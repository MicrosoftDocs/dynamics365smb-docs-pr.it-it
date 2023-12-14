---
title: Sincronizzazione di Business Central e Dataverse
description: Ottenere informazioni sulla sincronizzazione di dati tra Business Central e Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Pianificazione di una sincronizzazione tra Business Central e Dataverse

È possibile sincronizzare [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a intervalli pianificati impostando i processi nella coda processi. I processi di sincronizzazione sincronizzano i dati nei record di [!INCLUDE[prod_short](includes/prod_short.md)] e nei record di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] che sono stati associati. Per i record che non sono ancora associati, a seconda della direzione e delle regole di sincronizzazione, i processi di sincronizzazione possono creare e associare nuovi record nel sistema di destinazione.

Esistono vari processi di sincronizzazione predefiniti disponibili. I processi sono eseguiti nel seguente ordine per evitare di associare dipendenze tra tabelle. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

1. Processo di sincronizzazione VALUTA - Common Data Service.
2. Processo di sincronizzazione FORNITORE - Common Data Service.
3. Processo di sincronizzazione CONTATTO - Common Data Service.
4. Processo di sincronizzazione CLIENTE - Common Data Service.
5. Processo di sincronizzazione AGENTI - Common Data Service.

È possibile visualizzare i processi nella pagina **Movimenti coda processi**. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Movimenti coda processi di sincronizzazione predefiniti

Nella tabella seguente sono descritti i processi di sincronizzazione predefiniti per [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Movimento coda processi | Descrizione | Direzione | Mapping tabella integrazione | Frequenza di sincronizzazione predefinita (minuti) | Tempo di inattività predefinito (minuti) |
|--|--|--|--|--|--|--|
| Processo di sincronizzazione CONTATTO - Common Data Service | Sincronizza i contatti di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con i contatti di [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidirezionale | CONTATTO | 30 | 720 <br>(12 ore) |
| Processo di sincronizzazione VALUTA - Common Data Service | Sincronizza le valute di transazione di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con le valute di [!INCLUDE[prod_short](includes/prod_short.md)]. | Da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | VALUTA | 30 | 720 <br> (12 ore) |
| Processo di sincronizzazione CLIENTE - Common Data Service | Sincronizza i conti di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e i clienti di [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidirezionale | CLIENTE | 30 | 720<br> (12 ore) |
| Processo di sincronizzazione FORNITORE - Common Data Service. | Sincronizza i conti di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e i clienti di [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidirezionale | FORNITORE | 30 | 720<br> (12 ore) |
| Processo di sincronizzazione AGENTI - Common Data Service | Sincronizza gli agenti di [!INCLUDE[prod_short](includes/prod_short.md)] con gli utenti di [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. | Da [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)] | AGENTI | 30 | 1440<br> (24 ore) |

## <a name="synchronization-process"></a>Processo sincronizzazione

Ogni movimento coda processi di sincronizzazione utilizza un mapping di tabella di integrazione che specifica quale tabella di [!INCLUDE[prod_short](includes/prod_short.md)] e quale tabella di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sincronizzare. I mapping di tabella includono anche alcune impostazioni che controllano quali record della tabella di [!INCLUDE[prod_short](includes/prod_short.md)] e della tabella di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sincronizzare.  

Per sincronizzare i dati, i record di tabella di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] devono essere associati a record di [!INCLUDE[prod_short](includes/prod_short.md)]. Ad esempio, un cliente di [!INCLUDE[prod_short](includes/prod_short.md)] deve essere associato a un conto di [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. È possibile impostare le associazioni manualmente, prima di eseguire i processi di sincronizzazione, oppure permettere ai processi di sincronizzazione di impostare le associazioni automaticamente. Nel seguente elenco viene descritto come i dati vengono sincronizzati tra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)] quando si utilizzano i movimenti coda processi di sincronizzazione. Per ulteriori informazioni, vedere [Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md).

- La casella di controllo **Sinc. solo record associati** controlla se vengono creati nuovi record durante la sincronizzazione. Per impostazione predefinita, la casella di controllo è selezionata, il che significa che verranno sincronizzati solo i record associati. Nel mapping di tabella di integrazione, è possibile modificare il mapping di tabella tra una tabella di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e una tabella di [!INCLUDE[prod_short](includes/prod_short.md)], in modo che i processi di sincronizzazione di integrazione creeranno nuovi record nel database di destinazione per ogni riga del database di origine che non è associato. Per altre informazioni, vedere [Creazione di nuovi record](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Esempio** Se si deseleziona la casella di controllo **Snc. solo record associati**, quando si sincronizzano i clienti in [!INCLUDE[prod_short](includes/prod_short.md)] con account in [!INCLUDE[cds_long_md](includes/cds_long_md.md)], un nuovo account viene creato e automaticamente associato per ciascun cliente in [!INCLUDE[prod_short](includes/prod_short.md)]. Inoltre, poiché in questo caso la sincronizzazione è bidirezionale, un nuovo cliente viene creato e associato per ogni account di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] che non è già associato.  

    > [!NOTE]  
    > Esistono regole e filtri che determinano quali dati vengono sincronizzati. Per ulteriori informazioni, vedi [Regole di sincronizzazione](admin-synchronizing-business-central-and-sales.md).

- Quando vengono creati nuovi record in [!INCLUDE[prod_short](includes/prod_short.md)], i record utilizzano il modello che viene definito per il mapping di tabella di integrazione o il modello predefinito disponibile per il tipo di riga. I campi vengono popolati con i dati di [!INCLUDE[prod_short](includes/prod_short.md)] o di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] in base alla direzione della sincronizzazione. Per ulteriori informazioni, vedere [Modificare i mapping di tabella per la sincronizzazione](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Con le sincronizzazioni successive, verranno aggiornati solo i record che sono stati modificati o aggiunti dopo l'ultimo processo di sincronizzazione completato per la tabella.  

     I nuovi record in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vengono aggiunti in [!INCLUDE[prod_short](includes/prod_short.md)]. Se i dati nei campi dei record di [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vengono modificati, i dati vengono copiati nel campo corrispondente di [!INCLUDE[prod_short](includes/prod_short.md)].  

- Con la sincronizzazione bidirezionale, il processo sincronizza da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] e quindi da [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Informazioni sui timeout di inattività

Alcuni movimenti coda processi, come quelli che pianificano la sincronizzazione tra [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[cds_long_md](includes/cds_long_md.md)], utilizzano il campo **Timeout inattività** nella scheda **Movimento coda processi** per impedire l'esecuzione non necessaria del movimento coda processi.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Diagramma di flusso per quando i movimenti coda processi vengono sospesi a causa di inattività.":::

Quando il valore in questo campo non è zero e la coda processi non ha trovato alcuna modifica durante l'ultima esecuzione, [!INCLUDE[prod_short](includes/prod_short.md)] sospende il movimento coda processi. Quando ciò accade, il campo **Stato della coda processi** visualizzerà **In sospeso a causa di inattività** e [!INCLUDE[prod_short](includes/prod_short.md)] attenderà il periodo di tempo specificato nel campo **Timeout inattività** prima di eseguire nuovamente il movimento coda processi.  

Ad esempio, per impostazione predefinita, il movimento coda processi CURRENCY, che sincronizza le valute in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con tassi di cambio in [!INCLUDE[prod_short](includes/prod_short.md)], cercherà le modifiche ai tassi di cambio ogni 30 minuti. Se non vengono rilevate modifiche, [!INCLUDE[prod_short](includes/prod_short.md)] sospende il movimento coda processi CURRENCY per 720 minuti (dodici ore). Se un tasso di cambio viene modificato in [!INCLUDE[prod_short](includes/prod_short.md)] quando il movimento coda processi viene sospeso, [!INCLUDE[prod_short](includes/prod_short.md)] riattiverà automaticamente tale movimento e riavvierà la coda processi. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] attiverà automaticamente i movimenti coda processi sospesi solo quando si verificano delle modifiche in [!INCLUDE[prod_short](includes/prod_short.md)]. Le modifiche in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] non attiveranno i movimenti coda processi.

## <a name="to-view-the-synchronization-job-log"></a>Per visualizzare il log processi di sincronizzazione

1. Scegliere l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false":::, immettere **Log processi di sincronizzazione** e quindi scegliere il collegamento correlato.
2. Se si sono verificati uno o più errori per un processo di sincronizzazione, il numero di errori viene visualizzato nella colonna **Operazione non riuscita**. Per visualizzare gli errori per il processo, selezionare il numero.  

    > [!TIP]  
    > È possibile visualizzare tutti gli errori dei processi di sincronizzazione aprendo direttamente il log errori processi di sincronizzazione.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Per visualizzare il log processi di sincronizzazione dai mapping di tabella

1. Scegliere l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false":::, immettere **Mapping tabella integrazione** e quindi scegliere il collegamento correlato.
2. Nella pagina **Mapping tabella integrazione**, selezionare un movimento quindi scegliere **Log processi di sincronizzazione integrazione**.  

## <a name="to-view-the-synchronization-error-log"></a>Per visualizzare il log processi di sincronizzazione

- Scegliere l'icona :::image type="icon" source="media/ui-search/search_small.png" border="false":::, immettere **Errori di sincronizzazione integrazione** e quindi scegliere il collegamento correlato.

## <a name="see-also"></a>Vedere anche

[Sincronizzazione di dati in Business Central e [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Sincronizzare manualmente i mapping di tabella](admin-manual-synchronization-of-table-mappings.md)  
[Pianificazione di una sincronizzazione tra Business Central e [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Informazioni sull'integrazione di Dynamics 365 Business Central con [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

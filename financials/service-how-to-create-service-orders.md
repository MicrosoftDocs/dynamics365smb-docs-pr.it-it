---
title: Creare ordini di assistenza | Documenti Microsoft
description: La finestra **Ordine assistenza** consente di creare documenti in cui vengono immesse informazioni relative a un servizio di assistenza, ad esempio riparazione e manutenzione, svolto su articoli in assistenza su richiesta del cliente.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5460f50c4c556a74b518976d5d5fa90203f16967
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-orders"></a>Creare ordini di assistenza
La finestra **Ordine assistenza** consente di creare documenti in cui vengono immesse informazioni relative a un servizio di assistenza, ad esempio riparazione e manutenzione, svolto su articoli in assistenza su richiesta del cliente.  
  
Quando si crea un ordine di assistenza, è sufficiente compilare alcuni campi. Alcuni campi sono facoltativi e molti vengono compilati automaticamente durante la compilazione dei campi correlati.  
  
## <a name="to-create-a-service-order"></a>Per creare un ordine di assistenza    
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini assistenza**, quindi scegliere il collegamento correlato.  
2. Creare un nuovo ordine di assistenza.  
3. Nel campo **Nr.** immettere un numero per l'ordine di assistenza.  
  
     In alternativa, se è stata impostata una numerazione per gli ordini di assistenza nella finestra **Setup gest. assist.**, per selezionare il successivo numero di ordine di assistenza disponibile, premere INVIO.  
  
4. Nel campo **Nr. cliente** selezionare il cliente appropriato dalla lista. I campi rilevanti per il cliente vengono compilati con le informazioni della tabella **Cliente**.  
  
5. In base alle impostazioni nella Scheda dettaglio **Campi obbligatori** della finestra **Setup gest. assist.** potrebbe essere necessario compilare il campo **Tipo ordine assistenza** e il campo **Cod. agente**.  
6. Facoltativamente, compilare i campi restanti.  
7. Registrare le righe di articolo in assistenza.  

## <a name="to-create-a-service-order-from-a-contract"></a>Per creare un ordine di assistenza da un contratto  
È possibile creare automaticamente ordini di assistenza per la manutenzione degli articoli in assistenza in base ai contratti di assistenza.  
  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Crea ordini assistenza a contratto**, quindi scegliere il collegamento correlato.  
2. Nella Scheda dettaglio **Testata contratto assistenza** impostare i filtri da applicare.  
3. Nella Scheda dettaglio **Opzioni** compilare i campi **Data inizio** e **Data fine** in base al periodo per cui si desidera creare gli ordini di assistenza contratto. Il processo batch procederà alla creazione di ordini di assistenza che includono articoli in contratti di assistenza con le prossime date di assistenza pianificate in tale periodo.  
  
    > [!NOTE]  
    >  Esiste un limite al numero di giorni che si può utilizzare come intervallo di date ogni volta che si utilizza questo processo batch. Questo limite viene impostato nel campo **Max. giorni ord. assist. da contratto** nella finestra **Setup gest. assist.**  
  
4. Nel campo **Azione** selezionare **Crea ordine di assistenza**.  

## <a name="to-convert-a-service-quote-to-a-service-order"></a>Per convertire un'offerta di assistenza in un ordine di assistenza
Quando un'offerta di assistenza è stata accettata dal cliente, è possibile convertirla in un ordine di assistenza. L'offerta verrà eliminata e verrà impostato un nuovo ordine di assistenza con la stessa descrizione dell'offerta di assistenza. Verranno inoltre ricalcolate la data e l'ora di risposta per l'ordine di assistenza, il cui stato passerà a **Non inviato**. Anche lo stato di riparazione degli articoli in assistenza nell'ordine verrà modificato in **Iniziale**.  
  
In [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono ricercati i movimenti di assegnazione per tutti gli articoli in assistenza nell'offerta di assistenza con lo stato **Attivo**. Se tali movimenti di assegnazione vengono trovati, lo stato di assegnazione verrà aggiornato in **Riassegnazione necessaria**. Quando si riassegnano gli articoli in assistenza nell'ordine di assistenza, lo stato dei movimenti di assegnazione registrati per l'offerta verrà modificato in **Completato**.   

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Offerte contratto assistenza**, quindi scegliere il collegamento correlato.  
2. Scegliere l'offerta di assistenza da convertire in un ordine di assistenza.  
3. Scegliere l'azione **Crea ordine**.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>Per verificare la disponibilità di un articolo per uno o più ordini  
È possibile controllare se un articolo necessario per soddisfare un ordine è in stock e, in caso contrario, quando lo sarà. Inoltre, se un articolo è disponibile per l'impegno, è possibile impegnarlo per assicurarne la disponibilità all'utilizzo. È possibile verificare la disponibilità di un determinato ordine o di tutti gli ordini.  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Quadro attività**, quindi scegliere il collegamento correlato.  
2. Effettuare una delle seguenti operazioni:  
  
    * Per un determinato ordine, selezionare l'ordine quindi scegliere l'azione **Sintesi domanda**.  
    * Per tutti gli ordini, scegliere **Mostra documento**. Viene visualizzata la finestra **Ordine assistenza**.  
  
3. Nella pagina **Sintesi domanda** espandere il raggruppamento dell'articolo e visualizzare le informazioni sulla disponibilità dell'articolo. Ad esempio, è possibile visualizzare il numero di articoli in magazzino. È inoltre possibile verificare se e quando un articolo sarà disponibile se è in ordine arretrato, ovvero Tipo origine = Acquisto, o se è stato impegnato. 

## <a name="to-reserve-an-item-for-a-service-order"></a>Per impegnare un articolo per un ordine di assistenza
Se è necessario assicurarsi che un articolo sia disponibile per un ordine di assistenza, è possibile impegnare l'articolo. 

1. Nella casella **Cerca** immettere **Ordini assistenza**, quindi selezionare il collegamento correlato.  
2. Scegliere l'ordine di assistenza, quindi scegliere **Modifica**.  
3. Scegliere **Azioni**, quindi **Ordine** e infine **Righe assistenza**.  
4. Nella pagina **Righe assistenza** selezionare l'articolo da impegnare, quindi scegliere l'azione **Impegna**.  
5. Nella pagina **Impegni** scegliere **Impegna da riga corrente**. 

## <a name="to-insert-lines-based-on-standard-service-codes"></a>Per inserire righe in base a codici di assistenza standard  
Se sono stati impostati codici di servizio standard successivamente assegnati a gruppi di articoli in assistenza, è possibile inserire righe standard collegate ai codici sui documenti di assistenza. Per ulteriori informazioni, vedere [Impostare codici di servizio standard](service-how-setup-service-coding.md).   

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini assistenza**, quindi scegliere il collegamento correlato.  
2. Creare un nuovo ordine di assistenza.  
3. Compilare i campi in base alle esigenze.  
4. Compilare le righe di articolo in assistenza con le informazioni necessarie.  
5. Scegliere la riga con l'articolo in assistenza per cui si desidera creare le righe di assistenza e scegliere **Ottieni codici servizio std**. Verrà visualizzata la finestra **Cod. gr. art. ass. standard** con i codici standard per il gruppo di articoli in assistenza specificato nella riga.  
6. Scegliere il codice appropriato, quindi scegliere **OK** per immettere righe di assistenza standard.  
  
> [!NOTE]  
>  Se il campo **Cod. gruppo articoli assist.** nella riga dell'articolo in assistenza del documento è vuoto, significa che l'articolo in assistenza non appartiene ad alcun gruppo di articoli in assistenza. In questo caso, la finestra **Cod. gr. art. ass. standard** conterrà una lista di tutti i codici di servizio standard. È necessario selezionare dalla lista per inserire righe di assistenza standard nel documento. È inoltre possibile selezionare dalla lista dei codici di servizio standard assegnati a un gruppo di articoli in assistenza specifico. Per visualizzare la lista, selezionare il codice appropriato nel campo **Cod. gruppo articoli assist.** nella finestra **Cod. gr. art. ass. standard** .  

## <a name="to-register-internal-or-public-comments"></a>Per registrare i commenti interni o pubblici
È possibile aggiungere commenti da stampare su ordini di assistenza e offerte di assistenza per fornire informazioni aggiuntive. È possibile aggiungere fino a 80 caratteri, spazi inclusi. Se è necessario più spazio, scegliere un'altra riga. Per registrare un commento, selezionare una riga, quindi scegliere l'azione **Commenti**.  

## <a name="to-delete-invoiced-service-orders"></a>Per eliminare ordini di assistenza fatturati  
Gli ordini vengono in genere eliminati automaticamente dopo che sono stati completamente fatturati. Quando si registra una fattura, viene creato un movimento corrispondente nella finestra **Fatture assistenza registrate**. Il documento registrato può essere visualizzato nella pagina **Fattura assistenza registrata**.  
  
Gli ordini di assistenza non vengono, tuttavia, eliminati automaticamente se la quantità totale indicata nell'ordine è stata registrata non dall'ordine stesso, ma dalla finestra **Fattura assistenza**. In questo caso può essere necessario eliminare ordini fatturati che non sono stati eliminati. Per eseguire questa operazione, utilizzare il processo batch **Elimina ordini assistenza fatturati**.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Elimina ordini assistenza fatturati**, quindi scegliere il collegamento correlato. Verrà visualizzata la finestra di richiesta del processo batch **Elimina ordini assistenza fatturati**.  
2. Per selezionare gli ordini da eliminare, è possibile impostare filtri nei campi **Nr.**, **Nr. cliente** e **Fatturare a - Nr. cliente**. .  
3. Selezionare **OK**.  


## <a name="see-also"></a>Vedi anche  
[Registrazione di assistenza](service-service-posting.md)  
[Registrare un ordine di assistenza](service-how-to-post-service-orders.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  
[Utilizzare i compiti di assistenza](service-how-to-work-on-service-tasks.md)  
[Assegnare risorse](service-how-to-allocate-resources.md)  


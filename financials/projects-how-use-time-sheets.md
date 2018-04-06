---
title: Utilizzare i fogli presenza per le commesse| Documenti Microsoft
description: Descrive come creare un foglio presenze per una commessa, copiarvi le righe di pianificazione, definire i tipi di lavoro, compilare il foglio di presenze e inviarlo per l'approvazione.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 545b06fac95994229ec0442c7aacb57cc56001ff
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="use-time-sheets-for-jobs"></a>Utilizzare i fogli presenze per le commesse
Utilizzare il processo batch **Crea fogli presenze** per impostare i fogli presenze per un numero specificato di periodi di tempo o settimane. È necessario disporre dei permessi necessari per creare i fogli presenze.

È possibile copiare e utilizzare le righe di pianificazione commessa in un foglio presenze. In questo modo, sarà sufficiente immettere le informazioni in un punto per essere sicuri che le informazioni siano sempre corrette.

Dopo avere approvato i movimenti del foglio presenze per una commessa, è possibile registrarli nelle registrazioni commesse o nelle registrazioni risorse corrispondenti.

Prima di poter utilizzare i fogli presenze, è necessario impostare le informazioni generali e specificare un amministratore e uno o più responsabili approvazione dei fogli presenze. Per ulteriori informazioni, vedere [Impostare fogli presenze](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Per creare un foglio presenze
È possibile utilizzare il processo batch **Crea fogli presenze** per impostare i fogli presenze per un numero specificato di periodi di tempo o settimane. Il proprietario potrà così aprirlo e registrarvi il tempo dedicato a un task.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fogli presenze**, quindi scegliere il collegamento correlato.
2. Nella finestra **Lista fogli presenze** scegliere l'azione **Crea fogli presenze**.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   I campi **Usa foglio presenze** e **ID utente proprietario foglio presenze** devono essere compilati nella scheda della risorsa del foglio presenze.

1. Scegliere il pulsante **OK**.  

È possibile visualizzare i fogli presenze creati nella finestra **Lista fogli presenze**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Per copiare le righe pianificazione commessa in un foglio presenze
Nella procedura riportata di seguito viene descritto come aggiungere rapidamente righe pianificazione commessa a un foglio presenze.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fogli presenze**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Lista fogli presenze** selezionare un foglio presenze per il periodo di tempo interessato, quindi scegliere l'azione **Modifica foglio presenze**.  
3. Scegliere l'azione **Crea righe da pianificazione commessa**. Tutte le righe di pianificazione commessa nel periodo di tempo del foglio di presenze verranno copiate nel foglio di presenze della persona o della macchina indicata nel campo **Nr. risorsa** del foglio presenze.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Per definire i tipi di lavoro e aggiungerne uno a un foglio presenze
È possibile definire il tipo di lavoro per tutte le righe del foglio presenze relativo alle commesse. In questo modo, sarà possibile aggiungere le informazioni necessarie per fatturare al cliente diversi tipi di lavoro.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fogli presenze**, quindi scegliere il collegamento correlato.   
2. Aprire il foglio presenze appropriato.
3. Scegliere il campo **Descrizione**.  
4. Nella finestra **Dettaglio commessa righe foglio presenze** scegliere il campo **Codice tipo lavoro**, quindi selezionare un tipo di lavoro dall'elenco, ad esempio **Miglia**.  
5. Se non esiste alcun tipo di lavoro, scegliere l'azione **Nuovo**.
6. Nella finestra **Tipi di lavoro** compilare i campi in base alle esigenze.
7. Ripetere il passaggio 4 per assegnare il nuovo tipo di lavoro al foglio presenze.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Per riutilizzare le righe del foglio presenze in altri fogli presenze
Se le informazioni del foglio presenze rimangono invariate da un periodo di tempo a un altro, è possibile risparmiare tempo copiando le righe dal periodo di tempo precedente. In questo modo, sarà sufficiente immettere l'utilizzo del tempo per il nuovo periodo.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fogli presenze**, quindi scegliere il collegamento correlato.  
2. Aprire il foglio presenze per un periodo successivo al periodo per un foglio presenze esistente con le righe.  
3. Scegliere l'azione **Copia righe da foglio presenze precedente**.

Verranno copiate le righe e tutti i dettagli quali tipo e descrizione. Ad esempio, se la riga è correlata a una commessa, viene copiato **Nr. commessa**. Tutte le righe copiate presentano lo stato **Aperto**. È ora possibile modificare le righe in base alle esigenze.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Per compilare le righe di un foglio presenze e inviarle per l'approvazione
La registrazione del foglio presenze avviene in ore, l'unità di misura base standard per le risorse. Per impostazione predefinita, un foglio presenze mostra i giorni lavorativi normali dal lunedì al venerdì.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Fogli presenze**, quindi scegliere il collegamento correlato.  
2. Selezionare un foglio presenze per il periodo pertinente, quindi scegliere l'azione **Modifica foglio presenze**.  
3. Compilare i campi su una riga in base alle esigenze. Immettere il numero di ore utilizzate dalla risorsa ogni giorno della settimana.

    > [!TIP]  
>   È possibile esaminare la somma delle ore del foglio presenze immessa nel Dettaglio informazioni **Riepilogo effettivo/previsto**.  
4. Ripetere il passaggio 3 per altri tipi di lavoro eseguiti dalla risorsa.
5. Scegliere l'azione **Invia**, quindi scegliere l'azione **Tutte le righe aperte** per inviare tutte le righe oppure l'azione **Solo le righe selezionate** per inviare solo le righe che sono selezionate nella finestra **Foglio presenze**.  

    > [!NOTE]  
>   È possibile inviare solo le righe del foglio presenze per le quali è stato specificato il tempo.  
6. Per modificare le informazioni in una riga impostata sullo stato **Inviato**, selezionare la riga e scegliere l'azione **Riapri**.

    > [!NOTE]  
>   Un manager può rifiutare una riga del foglio presenze che è stata inviata per l'approvazione. Se una riga presenta lo stato **Rifiutato**, è possibile apportare modifiche alla riga e scegliere nuovamente **Invia**.  
7. Scegliere il pulsante **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Per approvare o rifiutare un foglio presenze
Un foglio presenze deve essere inviato per l'approvazione prima di poter essere utilizzato. È possibile approvare e rifiutare le singole righe di un foglio presenze o inviarle al mittente per un'ulteriore azione. Un foglio presenze può essere approvato in due modi:

* Un amministratore di fogli presenze può approvare qualsiasi foglio presenze.
* La persona specificata nel campo **ID utente resp. approvazione foglio presenze** in una scheda risorsa può approvare i fogli presenze di quella risorsa. Per ulteriori informazioni, vedere [Impostare fogli presenze](projects-how-setup-time-sheets.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Foglio presenze manager**, quindi scegliere il collegamento correlato.
2. Selezionare un foglio presenze dall'elenco.  
3. Nella finestra **Foglio presenze** scegliere l'azione **Approva**, quindi scegliere l'azione **Tutte le righe inviate** per approvare tutte le righe oppure l'azione **Solo le righe selezionate** per approvare solo le righe che sono state selezionate nella finestra **Foglio presenze**.
4. Scegliere il pulsante **OK**.  
5. In alternativa, scegliere l'azione **Rifiuta** e seguire i passaggi 4 e 5.  

> [!TIP]  
>   Utilizzare i Dettagli informazioni **Stato foglio presenze** e **Riepilogo effettivo/previsto** per ottenere una panoramica delle informazioni del foglio presenze.

Una volta approvato o rifiutato, un foglio presenze non può essere modificato a meno che non venga prima riaperto. La procedura riportata di seguito spiega come riaprire un foglio presenze approvato o rifiutato.

## <a name="to-reopen-a-time-sheet"></a>Per riaprire un foglio presenze
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Foglio presenze manager** o **Fogli presenze**, quindi scegliere il collegamento correlato.
2. Aprire un foglio presenze dall'elenco.  

    > [!NOTE]  
>   È possibile riaprire solo le righe con lo stato **Approvato**. Non è possibile riaprire le righe con lo stato **Rifiutato**. Non è possibile riaprire un foglio presenze se è stato registrato.  
3. Nella finestra **Foglio presenze** scegliere l'azione **Riapri**, quindi scegliere l'azione **Tutte le righe inviate** per riaprire tutte le righe oppure l'azione **Solo le righe selezionate** per riaprire solo le righe che sono state selezionate nella finestra **Foglio presenze**.
4. Scegliere il pulsante **OK**. Lo stato della riga o delle righe del foglio presenze cambia in **Inviato**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Per registrare le righe del foglio presenze nelle registrazioni risorse
Dopo avere approvato i movimenti del foglio presenze per una risorsa, è possibile registrarli nelle registrazioni risorse corrispondenti.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni risorse**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Suggerisci righe da fogli presenze**.  
3. Compilare i campi, se necessario.  
4. Scegliere il pulsante **OK**. I movimenti per l'utilizzo verranno creati nelle registrazioni risorse, dove sarà possibile modificare le informazioni in base alle esigenze.  
5. Scegliere l'azione **Registra**.  
6. Per verificare la registrazione, scegliere l'azione **Mov. contabili**. Verrà visualizzata la finestra **Mov. contabili risorse** nella quale verrà visualizzato il risultato della registrazione delle registrazioni risorse.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Per registrare le righe del foglio presenze nelle registrazioni commesse
Dopo avere approvato i movimenti del foglio presenze per una commessa è possibile registrarli nelle registrazioni commesse corrispondenti.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni commesse**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Suggerisci righe da fogli presenze**.  
3. Compilare i campi, se necessario.  
4. Scegliere il pulsante **OK**. I movimenti per l'utilizzo verranno creati nelle registrazioni commesse, dove sarà possibile modificare le informazioni in base alle esigenze.  

    > [!NOTE]  
>   Le informazioni sul tipo di lavoro e l'indicazione se il lavoro è addebitabile o meno vengono copiate dalla riga del foglio presenze. Se necessario, è possibile ridurre la quantità di ore ed effettuare una registrazione parziale. Se si riduce la quantità, alla successiva selezione dell'azione **Suggerisci righe da fogli presenze** la riga creata conterrà la quantità residua di ore.  
5. Scegliere l'azione **Registra**.  
6. Per verificare la registrazione, scegliere l'azione **Mov. contabili**. Verrà visualizzata la finestra **Movimenti cont. commesse** nella quale verrà visualizzato il risultato della registrazione delle registrazioni commesse.

## <a name="to-archive-time-sheets"></a>Per archiviare fogli presenze
Dopo avere registrato i fogli presenze, è possibile archiviarli per riferimento futuro. Tutte le righe dei fogli presenze devono essere registrate prima che il foglio presenze possa essere archiviato.

> [!NOTE]  
>   Quando si archivia un foglio presenze, questo viene rimosso dalle liste sia della finestra **Fogli presenze** sia della finestra **Fogli presenze manager**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Sposta fogli presenze in archivio**, quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze, quindi scegliere **OK**.  
3. Per esaminare i fogli presenze archiviati, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Archivi foglio presenze** o **Archivi foglio presenze manager**, quindi scegliere il collegamento correlato.

## <a name="see-also"></a>Vedi anche
[Gestione progetti](projects-manage-projects.md)  
[Impostazione della Gestione progetti](projects-setup-projects.md)    
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)     
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


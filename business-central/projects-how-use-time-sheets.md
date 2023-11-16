---
title: Usare i fogli presenze
description: Scopri come creare fogli presenze e inviarli per l'approvazione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 07/27/2023
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Usare i fogli presenze

Usa i fogli presenze per tenere traccia delle assenzee nonché del tempo e delle risorse impiegati per un progetto. Il tracciamento del tempo ti aiuta a identificare in anticipo i problemi per evitare ritardi e sovraccarichi di costo. I fogli presenze consentono a una risorsa di registrare più facilmente l'utilizzo del tempo per una persona fisica o una macchina di modo che i responsabili possano esaminare l'utilizzo e la relativa assegnazione. In questo articolo viene descritto come utilizzare i fogli presenze.  

È possibile copiare e utilizzare le righe di pianificazione commessa in un foglio presenze. In questo modo, sarà sufficiente immettere le informazioni in un punto per essere sicuri che le informazioni siano sempre corrette. Per ulteriori informazioni, vedi [Per copiare le righe pianificazione commessa in un foglio presenze](#copy-job-planning-lines-to-a-time-sheet).

Dopo avere approvato i movimenti del foglio presenze per una commessa, è possibile registrarli nelle registrazioni commesse o nelle registrazioni risorse corrispondenti. Per ulteriori informazioni, vedi [Per registrare le righe del foglio presenze nelle registrazioni commesse](#to-post-time-sheet-lines-in-a-job-journal) e [Per registrare le righe del foglio presenze nelle registrazioni risorse](#post-time-sheet-lines-in-a-resource-journal).

Prima di poter utilizzare i fogli presenze, è necessario impostare le informazioni generali e specificare un amministratore e uno o più responsabili approvazione dei fogli presenze. Per ulteriori informazioni sull'impostazione di fogli presenze, vedi [Impostare fogli presenze](projects-how-setup-time-sheets.md).  

> [!TIP]
> Puoi utilizzare i fogli presenze in un dispositivo mobile. Per fare ciò, è possibile che sia necessario attivare l'interruttore **Usa la nuova esperienza del foglio presenze** nella pagina [Setup risorse](https://businesscentral.dynamics.com/?page=462).

## <a name="create-time-sheets"></a>Creare fogli presenze

Puoi utilizzare la pagina **Crea fogli presenze** per impostare i fogli presenze per un numero specificato di periodi di tempo o settimane. Il proprietario potrà così aprirlo e registrarvi il tempo dedicato a un task. Puoi anche [pianificare l'esecuzione automatica del processo batch](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> È necessario disporre dei permessi necessari per creare i fogli presenze. Per ulteriori informazioni sulle autorizzazioni, vedi [Impostare fogli presenze](projects-how-setup-time-sheets.md).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Crea fogli presenze**, quindi scegli il collegamento correlato.

    > [!TIP]
    > Puoi anche utilizzare l'azione **Crea fogli presenze** nella pagina di elenco **Risorse** e nella pagina **Scheda risorsa**.
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Prima di creare fogli presenze per una risorsa, assicurati che i campi **Usa foglio presenze** e **ID utente proprietario foglio presenze** siano specificati nella pagina **Scheda risorsea**.

    Eventualmente, scegli l'azione **Programma** per specificare la frequenza alla quale desideri che l'attività venga eseguita automaticamente. Ad esempio, per configurare l'attività in modo che venga eseguita settimanalmente per quattro settimane, nella pagina **Programma un report - Crea fogli presenze**, nel campo **Prossima esecuzione formula della data** immetti **4S**. Per saperne di più sulla programmazione di report, vedi [Programmazione di un report da eseguire](ui-work-report.md#ScheduleReport)  

È possibile visualizzare i fogli presenze creati nella pagina **Fogli presenze**. Ogni foglio presenze è costituito da una o più righe che definiscono l'ora che si desidera inviare per l'approvazione. La tabella seguente descrive i tipi di righe che è possibile aggiungere al foglio presenze.

| **Campo** | **Descrizione** |
|---|---|
| | Consente di aggiungere una nota o un contrassegno nel campo **Descrizione** della riga del foglio presenze. Ad esempio, è possibile utilizzare questo campo per classificare i movimenti del foglio presenze. Se si lascia vuoto il campo **Tipo** per una riga del foglio presenze, non è possibile immettere i valori temporali nei campi relativi al giorno della settimana per la riga specificata. |
| Assenze | Consente di registrare il tempo di assenza durante la settimana lavorativa. Per completare le informazioni per la riga, specificare il tipo di assenza nel campo **Codice causa di assenza**. |
| Ordine di assemblaggio | Utilizzato per registrare il tempo per gli ordini di assemblaggio. Una riga del foglio presenze di questo tipo viene creata durante la registrazione delle righe degli ordini di assemblaggio per i quali l'impostazione prevede che la risorsa utilizzi i fogli presenze. Non è possibile selezionare manualmente una riga di questo tipo. |
| Posizione | Utilizzare per registrare l'utilizzo del tempo per un progetto. Per completare le informazioni per la riga, specificare il numero di commessa e il numero di task commessa per cui si desidera registrare il tempo. È possibile registrare il tempo per le righe non pianificate.|
| Risorsa | Utilizzare per registrare l'utilizzo del tempo per una risorsa. Per completare le informazioni per la riga, immettere una descrizione del lavoro. |
| Assistenza | Utilizzare per registrare l'utilizzo del tempo per un ordine di assistenza o una nota di credito di assistenza. |

Ad esempio, vuoi inviare un foglio presenze per una settimana in cui hai svolto attività di pulizia e hai avuto un giorno libero per una visita medica. La tabella seguente mostra come aggiungere righe al foglio presenze.

| Tipo | Descrizione | Codice tipo lavoro | Codice tipo di assenza |
|--|--|--|--|
| Risorsa | Orario di lavoro | Pulizia |  |
| Assenze | Indisponibilità |  | Integrità |
|  | Martedì ho dovuto prendere un giorno libero per un appuntamento medico. |  |  |

In questo esempio ipotetico, vengono registrate le ore pertinenti nei giorni specifici nei campi per ogni giorno della settimana.  

> [!TIP]
> Nella maggior parte dei casi, per l'azienda sono presenti tipi di lavoro predefiniti per i vari tipi di righe. In questi casi, scegliere semplicemente il tipo di lavoro pertinente dall'elenco, quindi aggiungere la propria descrizione.  
>
> Per selezionare il tipo di lavoro, scegliere il pulsante :::image type="icon" source="media/assist-edit-icon.png" border="false"::: nel campo **Descrizione**, scegliere l'azione **Dettagli attività**, quindi specificarlo nella pagina visualizzata oppure sceglierlo nel campo **Codice tipo lavoro** o **Codice tipo di assenza**, rispettivamente. In questo caso, è possibile ignorare la sezione [Per definire i tipi di lavoro e aggiungerne uno a un foglio presenze](#define-work-types-and-add-one-to-a-time-sheet).  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Riutilizzare le righe di un foglio presenze in altri fogli presenze

Se le informazioni del foglio presenze rimangono invariate da un periodo di tempo a un altro, è possibile risparmiare tempo copiando le righe dal periodo di tempo precedente. In questo modo, sarà sufficiente immettere l'utilizzo del tempo per il nuovo periodo.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fogli presenze**, quindi scegli il collegamento correlato.  
2. Aprire il foglio presenze per un periodo successivo al periodo per un foglio presenze esistente con le righe.  
3. Scegliere l'azione **Copia righe da foglio presenze precedente**.

Verranno copiate le righe e tutti i dettagli quali tipo e descrizione. Ad esempio, se la riga è correlata a una commessa, viene copiato **Nr. commessa**. Tutte le righe copiate presentano lo stato **Aperto**. È ora possibile modificare le righe in base alle esigenze.

## <a name="copy-job-planning-lines-to-a-time-sheet"></a>Copiare le righe pianificazione commessa in un foglio presenze

Nella procedura riportata di seguito viene descritto come aggiungere rapidamente righe pianificazione commessa a un foglio presenze.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immettere **Fogli presenze**, quindi scegliere il collegamento correlato.  
2. Selezionare un foglio presenze per il periodo pertinente nella pagina **Fogli presenze**.  
3. Scegliere l'azione **Crea righe da pianificazione commessa**. Tutte le righe di pianificazione commessa nel periodo di tempo del foglio di presenze verranno copiate nel foglio di presenze della persona o della macchina indicata nel campo **Nr. risorsa** del foglio presenze.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Definire i tipi di lavoro e aggiungerne uno a un foglio presenze

Puoi definire il tipo di lavoro per tutte le righe del foglio presenze per ordini di assistenza, ordini commessa e risorse. In questo modo, sarà possibile aggiungere le informazioni necessarie per fatturare al cliente diversi tipi di lavoro.  

1. Nella pagina **Fogli presenze** scegliere il foglio presenze rilevante.
2. Sulla prima riga della sezione **Righe**, scegliere il campo **Tipo**, quindi scegliere il tipo rilevante, ad esempio *Risorsa*.  
3. Scegliere il campo **Descrizione**, quindi nella pagina **Dettaglio risorse righe foglio presenze** compilare i campi. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Se non esiste alcun tipo di lavoro, sceglie l'azione **Nuovo**.
    2. Nella pagina **Tipi di lavoro** compilare i campi necessari, quindi tornare al foglio presenze.
4. Compilare il resto dei campi del foglio presenze. Per ulteriori informazioni, vedere la sezione [Per compilare le righe di un foglio presenze e inviarle per l'approvazione](#fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Passaggi simili si applicano alla definizione dei codici assenza.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Compilare le righe di un foglio presenze e inviarle per l'approvazione

La registrazione del foglio presenze avviene in ore, l'unità di misura base standard per le risorse. Per impostazione predefinita, un foglio presenze mostra i giorni lavorativi normali dal lunedì al venerdì.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fogli presenze**, quindi scegli il collegamento correlato.  
2. Seleziona un foglio presenze per il periodo in questione.
3. Compilare i campi su una riga in base alle esigenze. Immettere il numero di ore utilizzate dalla risorsa ogni giorno della settimana.  

    Nella maggior parte dei casi, per tenere traccia del lavoro, aggiungere una riga di tipo *Risorsa*, quindi registrare le ore trascorse ogni giorno. Se si desidera registrare l'assenza, aggiungere una riga di tipo *Assenza*.  

    > [!TIP]  
    > È possibile esaminare la somma delle ore del foglio presenze immessa nel Dettaglio informazioni **Riepilogo effettivo/previsto**.  
4. Ripetere il passaggio 3 per altri tipi di lavoro eseguiti dalla risorsa.  

    Successivamente, decidi se inviare tutte le righe o quelle selezionate nel foglio presenze.  

    * Per inviare il foglio presenze per una o più righe, scegliere la riga pertinente, quindi scegliere l'azione **Invia**.

        Nella pagina di invio scegliere l'opzione **Solo le righe selezionate**. Lo stato della riga cambia da **Aperto** a **Inviato**.
    * Per inviare il foglio presenze per tutte le righe aperte, scegliere l'azione **Invia** nella parte supeiore della pagina **Foglio presenze**.  

        Conferma che vuoi inviare tutte le righe aperte nel foglio presenze corrente.  

    > [!NOTE]  
    > È possibile inviare solo le righe del foglio presenze per le quali è stato specificato il tempo.  
5. Per modificare le informazioni in una riga impostata sullo stato **Inviato**, selezionare la riga e scegliere l'azione **Riapri**.

    > [!NOTE]  
    > Un manager potrebbe rifiutare una riga del foglio presenze che è stata inviata per l'approvazione. Se una riga presenta lo stato **Rifiutato**, puoi apportare modifiche alla riga e scegliere nuovamente **Invia**.  
6. Scegliere il pulsante **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Per approvare o rifiutare un foglio presenze

Un foglio presenze deve essere inviato per l'approvazione prima di poter essere utilizzato. Puoi approvare e rifiutare singole righe di un foglio presenze o inviarle al mittente per un'ulteriore azione. Un foglio presenze può essere approvato in due modi:

* Un amministratore di fogli presenze può approvare qualsiasi foglio presenze.
* La persona specificata nel campo **ID utente resp. approvazione foglio presenze** in una scheda risorsa può approvare i fogli presenze di quella risorsa. Per ulteriori informazioni sull'impostazione dell'approvazione, vedi [Impostare fogli presenze](projects-how-setup-time-sheets.md).

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fogli presenze manager**, quindi scegli il collegamento correlato.
2. Selezionare un foglio presenze dall'elenco.  
3. Nella pagina **Foglio presenze**: 
    1. Scegli l'azione **Processo**, quindi scegli l'azione **Approva**.
    2. Scegli l'azione **Tutte le righe inviate** per approvare tutte le righe o l'azione **Solo le righe selezionate** per approvare solo le righe selezionate nella pagina **Foglio presenze**.
4. Scegliere il pulsante **OK**.  
5. In alternativa, scegliere l'azione **Rifiuta** e seguire i passaggi 4 e 5.  

> [!TIP]  
> Utilizzare i Dettagli informazioni **Stato foglio presenze** e **Riepilogo effettivo/previsto** per ottenere una panoramica delle informazioni del foglio presenze.

Una volta approvato o rifiutato, un foglio presenze non può essere modificato a meno che non venga prima riaperto. La procedura riportata di seguito spiega come riaprire un foglio presenze approvato o rifiutato.

## <a name="reopen-a-time-sheet"></a>Riaprire un foglio presenze

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fogli presenze manager** o **Fogli presenze**, quindi scegli il collegamento correlato.
2. Aprire un foglio presenze dall'elenco.  

    > [!NOTE]  
    > È possibile riaprire solo le righe con lo stato **Approvato**. Non puoi riaprire le righe con lo stato **Rifiutato** o che sono state registrate.  
3. Nella pagina **Foglio presenze** scegli l'azione **Riapri**, quindi scegli l'azione **Tutte le righe inviate** per riaprire tutte le righe oppure l'azione **Solo le righe selezionate** per riaprire solo le righe che sono state selezionate nella pagina **Foglio presenze**.
4. Scegliere il pulsante **OK**. Lo stato della riga o delle righe del foglio presenze cambia in **Inviato**.  

## <a name="view-and-approve-time-sheets-by-job"></a>Visualizzare e approvare fogli presenze in base alla commessa

Per una commessa, è possibile specificare una persona responsabile della commessa. Tali informazioni sono collegate alle righe del foglio presenze. Il collegamento fornisce ai project manager un elenco dei fogli presenze da approvare. Ad esempio, il project manager del team potrebbe essere responsabile di alcune commesse nella società. In questo caso, deve essere designato come **Persona responsabile** nella pagina Scheda commessa. Questa visualizzazione delle informazioni del foglio presenze mostra le attività associate a una commessa e la quantità di ore utilizzate.

> [!NOTE]
> Per approvare i fogli presenze nella pagina **Foglio presenze manager per commessa**, devi selezionare un'opzione **Foglio presenze per approvazione commesse** nella pagina **Setup risorse**. Per ulteriori informazioni sull'impostazione delle approvazioni per le risorse, vedi [Impostare risorse](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-job"></a>Approvare o rifiutare un foglio presenze in base alla commessa

1. Nella casella **Cerca** immettere **Foglio presenze manager per commessa**, quindi selezionare il collegamento correlato. [!INCLUDE[prod_short](includes/prod_short.md)] visualizza un elenco di righe del foglio presenze associate alle commesse di cui sei responsabile.
2. Scegliere l'azione **Approva**, quindi scegli l'azione **Tutte le righe inviate** per approvare tutte le righe oppure l'azione **Solo le righe selezionate** per approvare solo le righe che sono selezionate nella pagina **Foglio presenze**.

    > [!NOTE]
    > È possibile approvare solo i fogli presenze che presentano lo stato **Inviato**.

3. Per fornire ulteriori informazioni sull'approvazione o il rifiuto, seleziona l'azione **Correlato**, quindi seleziona **Commenti** e quindi **Commenti riga**.
4. Scegli il pulsante **OK**.

> [!NOTE]
> Dopo aver approvato o rifiutato una riga del foglio presenze in base alla commessa, non puoi riaprirla o modificarla nella pagina **Foglio presenze**.

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Registrare le righe di un foglio presenze nelle registrazioni risorse

Dopo avere approvato i movimenti del foglio presenze per una risorsa, è possibile registrarli nelle registrazioni risorse corrispondenti.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni risorse**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Suggerisci righe da fogli presenze**.  
3. Nella pagina **Suggerisci righe reg. ris.** compila i campi come necessario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Scegli il pulsante **OK**. I movimenti per l'utilizzo verranno creati nelle registrazioni risorse, dove sarà possibile modificare le informazioni in base alle esigenze.  
5. Scegliere l'azione **Registra**.  
6. Per verificare la registrazione, scegliere l'azione **Mov. contabili**. Verrà visualizzata la pagina **Mov. contabili risorse** nella quale verrà visualizzato il risultato della registrazione delle registrazioni risorse.

## <a name="post-time-sheet-lines-in-a-job-journal"></a>Registrare le righe di un foglio presenze nelle registrazioni commesse

Dopo avere approvato i movimenti del foglio presenze per una commessa è possibile registrarli nelle registrazioni commesse corrispondenti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni commesse**, quindi scegli il collegamento correlato.  
2. Scegli l'azione **Suggerisci righe da fogli presenze**.  
3. Nella pagina **Suggerisci righe reg. comm.** compila i campi come necessario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Scegli il pulsante **OK**. I movimenti per l'utilizzo verranno creati nelle registrazioni commesse, dove sarà possibile modificare le informazioni in base alle esigenze.  

    > [!NOTE]  
    > Le informazioni sul tipo di lavoro e l'indicazione se il lavoro è addebitabile o meno vengono copiate dalla riga del foglio presenze. Se necessario, è possibile ridurre la quantità di ore ed effettuare una registrazione parziale. Se si riduce la quantità, alla successiva selezione dell'azione **Suggerisci righe da fogli presenze** la riga conterrà la quantità residua di ore.  
5. Scegli l'azione **Registra**.  
6. Per verificare la registrazione, scegliere l'azione **Mov. contabili**. Verrà visualizzata la pagina **Movimenti cont. commesse** nella quale verrà visualizzato il risultato della registrazione delle registrazioni commesse.

## <a name="to-archive-time-sheets"></a>Per archiviare fogli presenze

Dopo avere registrato i fogli presenze, puoi archiviarli per riferimento futuro. Devi registrare tutte le righe di un foglio presenze prima di poterlo archiviare.

> [!NOTE]  
> Quando archivi un foglio presenze, viene rimosso dalle liste nelle pagine **Fogli presenze** e **Fogli presenze manager**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immettere **Fogli presenze**, quindi scegliere il collegamento correlato.
2. Seleziona l'azione **Sposta fogli presenze in archivio**.  
3. Nella pagina **Sposta fogli presenze in archivio**, compila i campi in base alle esigenze, quindi scegli **OK**.  
4. Per rivedere i fogli presenze archiviati, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità relativa alla informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Archivi foglio presenze** o **Archivi foglio presenze manager**, quindi scegli il collegamento correlato.

## <a name="see-also"></a>Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: 'Impostare progetti, prezzi e categorie di registrazioni progetti'
description: Descrive come impostare le informazioni generali sui progetti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-projects-prices-and-project-posting-groups"></a>Impostare progetti, prezzi e categorie di registrazioni progetti

In veste di project manager, è possibile configurare i progetti che definiscono ogni progetto gestito in [!INCLUDE[prod_short](includes/prod_short.md)]. Utilizza la pagina **Setup progetto** per definire come utilizzerai le funzionalità del progetto.

Per ogni progetto, specifica varie informazioni:

* Prezzi per articoli di progetto
* Risorse di progetto
* Conti C/G progetto
* Categorie di registrazioni progetti (obbligatorio)

## <a name="to-set-general-information-for-projects"></a>Per impostare informazioni generali per progetti

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup progetto**, quindi scegli il collegamento correlato.
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> L'interruttore **Applica collegamento utilizzo per default** nella pagina **Setup progetti** indica se i movimenti contabili del progetto sono collegati alle righe di pianificazione progetto per impostazione predefinita. Attiva l'interruttore per applicare questa impostazione a tutti i nuovi progetti. Puoi abilitare o disabilitare il monitoraggio dell'utilizzo dei progetti per un progetto specifico abilitando o disabilitando l'interruttore **Applica collegamento utilizzo** nella pagina **Scheda progetto**.

### <a name="specify-a-default-location-for-project-items"></a>Specificare un'ubicazione predefinita per gli articoli del progetto

Puoi risparmiare tempo nell'immissione dei dati specificando un'ubicazione e una collocazione predefinite per i progetti nella pagina **Scheda progetto** . Quando crei attività di progetto, righe di pianificazione progetto e righe di registrazione progetto per il progetto, l'ubicazione e la collocazione predefinite vengono assegnati automaticamente. Se necessario, puoi tuttavia modificare il codice ubicazione e la collocazione nelle attività e nelle righe.

Se definisci un **Codice collocazione A progetto** per l'ubicazione, il codice collocazione viene popolato quando selezioni il codice ubicazione. Se il flusso di warehouse richiede prelievi di warehouse, è anche possibile definire altre collocazioni da cui consumare gli articoli.

Questi campi sono quelli predefiniti quando si creano attività di progetto. Le attività di progetto esistenti non cambiano.

Ci sono alcune cose da sapere sull'utilizzo delle ubicazioni predefinite:

* Per le attività di progetto, se definisci un **Codice collocazione A progetto** per l'ubicazione, il codice collocazione viene assegnato quando selezioni il codice ubicazione. Se il flusso di warehouse richiede prelievi di warehouse, è anche possibile definire altre collocazioni da cui consumare gli articoli.
* Per le righe di pianificazione progetto, il **Codice ubicazione** si basa sul valore selezionato nella riga di pianificazione progetto quando selezioni un articolo. Se non è definito un codice collocazione per l'attività di progetto, viene selezionata la collocazione dal contenuto collocazione predefinito. Puoi modificare entrambi i valori manualmente.
* Per le righe di registrazione progetto, il **Codice ubicazione** si basa sul valore selezionato nella riga di registrazione commesse quando selezioni un articolo. Se un codice collocazione non è definito per l'attività di progetto, viene selezionata la collocazione dal contenuto collocazione predefinito. Puoi modificare entrambi i valori manualmente.

### <a name="invoice-multiple-customers-for-project-tasks"></a>Fatturare a più clienti per attività di progetto

Quando i progetti comportano più clienti, fatturare ai clienti giusti le attività appropriate può risultare difficile. [!INCLUDE [prod_short](includes/prod_short.md)] rende la fatturazione meno complessa consentendoti di specificare i clienti a cui fatturare e a cui vendere su ciascuna riga di attività di progetto, in modo da poter generare automaticamente fatture per i clienti corretti. Per ulteriori informazioni sulla fatturazione a più clienti, vedi [Fatturare a uno o più clienti per attività di progetto](projects-how-create-jobs.md#invoice-one-or-more-customers-for-project-tasks).

### <a name="to-set-up-project-usage-tracking"></a>Per impostare la tracciabilità dell'utilizzo di un progetto

Quando lavori su un progetto, è possibile che tu voglia sapere come viene eseguita la tracciabilità dell'utilizzo rispetto al piano. Per esplorare l'uso puoi creare un collegamento tra le righe di pianificazione progetto e l'utilizzo effettivo. Il collegamento ti consente di monitorare i tuoi costi e capire il lavoro residuo da svolgere. Per impostazione predefinita, il tipo di riga di pianificazione progetto è **Budget**, ma utilizzando il tipo di riga **Budget e fatturabile** si ottengono effetti simili.

Dopo aver impostato la tracciabilità dell'utilizzo abilitando l'interruttore **Applica collegamento utilizzo per default**, è possibile esaminare le informazioni nella riga di pianificazione progetto. Ad esempio, è possibile impostare la quantità della risorsa, dell'articolo o del conto di contabilità generale. Puoi impostare inoltre la quantità da trasferire nella registrazione progetti. Il campo **Quantità residua** nella riga di pianificazione progetto indica ciò che resta da trasferire e registrare nelle registrazioni progetti.

>[!NOTE]
> Se la casella di controllo **Applica collegamento utilizzo** viene selezionata nel progetto e il campo **Tipo riga** nella riga di acquisto o nella riga di registrazione progetto è **Fatturabile**, vengono create nuove righe di pianificazione progetto di tipo **Budget e fatturabile** quando si registra la registrazione progetti o il documento di acquisto.  
>
> Per ulteriori informazioni, vedi [Registrare l'utilizzo per i progetti](projects-how-record-job-usage.md) e [Gestire gli approvvigionamenti dei progetti](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Se non specifichi un valore nel campo **Tipo riga** nella riga di registrazione progetto o nella riga acquisto, non viene creata alcuna riga di pianificazione progetto quando si registra la registrazione progetto o il documento di acquisto.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-projects"></a>Per impostare i prezzi per risorse, articoli e conti di contabilità generale per progetti

> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 sono stati rilasciati nuovi processi per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

È possibile impostare i prezzi per articoli, risorse e conti di contabilità generale correlati a un progetto. 

#### [Esperienza corrente](#tab/current-experience)

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetto**, quindi scegli il collegamento correlato.  
2. Selezionare il progetto, quindi scegliere l'azione **Risorsa**, **Articolo** o **Conto C/G**.
3. Nelle pagine **Prezzi risorse progetto**, **Prezzi articoli progetto** o **Prezzi conti C/G progetto** compilare i campi come necessario.

Quando scegli una risorsa, un articolo o un conto di contabilità generale per un progetto, [!INCLUDE [prod_short](includes/prod_short.md)] utilizza le informazioni nei campi facoltativi nelle righe di pianificazione progetto e nelle registrazioni progetti. La tabella seguente spiega come.

|Colonna1  |Colonna2  |
|---------|---------|
|**Risorse di progetto**|Campi **Nr. attività di progetto**, **Tipo di lavoro**, **Codice valuta**, **% sconto riga** e **Fattore costo unitario**. Il valore nel campo **Prezzo unitario** per la risorsa viene utilizzato nelle righe di pianificazione progetto e nelle registrazioni progetti quando viene immessa una risorsa o una risorsa assegnata al gruppo di risorse. Il prezzo sostituisce sempre qualsiasi prezzo impostato nella pagina **Prezzi risorse/Prezzo gruppo risorse**.|
|**Articoli di progetto**|Campi **Nr. attività di progetto**, **Codice valuta** e **% sconto riga**. Il valore nel campo **Prezzo unitario** per l'articolo verrà utilizzato nelle righe di pianificazione progetto e nelle registrazioni progetti quando viene immesso questo articolo. Questo prezzo sostituisce sempre il normale prezzo cliente (il meccanismo "prezzo migliore") per gli articoli. Per utilizzare il normale prezzo del cliente, non specificare i prezzi degli articoli del progetto per il progetto.|
|**Conti di contabilità generale**|Le informazioni nei campi **Nr. attività di progetto**, **Codice valuta**, **% sconto riga**, **Fattore costo unitario** e **Costo unitario** verranno utilizzate nelle righe di pianificazione progetto e nelle registrazioni progetti quando questo conto di contabilità generale viene immesso o aggiunto a un progetto. Quando scegli un conto di contabilità generale, le righe di pianificazione progetto e le registrazioni progetti usano il valore nel campo **Prezzo unitario** per la spesa del progetto contabile.|

#### [Nuova esperienza](#tab/new-experience)

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Selezionare il progetto pertinente, quindi scegli l'azione **Listini prezzi di vendita**.

---

## <a name="to-set-up-project-posting-groups"></a>Per impostare le categorie di registrazione progetti

Un aspetto della pianificazione dei progetti è decidere quali conti di registrazione utilizzare per il costing dei progetti. Perché sia possibile registrare commesse, è necessario impostare conti per la registrazione per ciascuna categoria di registrazione progetti. La categoria di registrazione rappresenta un collegamento tra il progetto e come deve essere considerata nella contabilità generale. Quando si crea un progetto, si specifica una categoria di registrazione e, per impostazione predefinita, ogni attività che crei per il progetto viene associata a tale categoria di registrazione. Tuttavia, quando si creano i task, è possibile sostituire l'impostazione di default e selezionare una categoria di registrazione più appropriata.  

> [!NOTE]  
> È necessario configurare l'installazione degli account nel Piano dei Conti prima delle categorie di registrazione. Per ulteriori informazioni, vedere [Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md).  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie di registrazioni progetti**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

| Campo Conto | Descrizione | Usato in tipo WIP |
| --- | --- |  --- |
| **Codice** |Codice per la categoria di registrazione È possibile immettere fino a 10 caratteri, spazi inclusi. | |
| **Conto costi WIP** |Conto WIP per il costo calcolato del WIP per il progetto, corrispondente a un conto cespiti patrimoniali. | Costo collegato, Costi riconosciuti|
| **Conto costi sospesi WIP** |Un conto per il metodo Valore di costo o Costo del venduto del calcolo WIP. Questo conto è per le passività patrimoniali nel bilancio patrimoniale. Quando la rettifica WIP richiede l'aumento dei costi di utilizzo registrati nel conto economico, è possibile registrare questo conto. | Costi sospesi|
| **Conto costi applicati progetto** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. Utilizzato quando **Metodo di registrazione WIP utilizzato** è impostato su *Progetto*. | Costi collegati, Costi riconosciuti|
| **Conto costi articolo collegati** |Uguale a **Conto costi applicati progetto**, ma utilizzato quando **Metodo di registrazione WIP utilizzato** è impostato su *Movimento contabile progetto*.| |
| **Conto costi risorse collegati** |Uguale a **Conto costi applicati progetto**, ma utilizzato quando **Metodo di registrazione WIP utilizzato** è impostato su *Movimento contabile progetto*.| |
| **Conto costi C/G collegati** |Uguale a **Conto costi applicati progetto**, ma utilizzato quando **Metodo di registrazione WIP utilizzato** è impostato su *Movimento contabile progetto*.| |
| **Conto rettifica costi progetto** |Contropartita per il conto costi sospesi WIP, corrispondente a un conto spesa. | Costi sospesi|
| **Conto spesa C/G (Budget)** |Conto vendite da utilizzare per le spese di contabilità generale nelle attività di progetto con la categoria di registrazione corrente. Se lasciato vuoto, viene utilizzato il conto C/G immesso nella riga di pianificazione progetto. | |
| **Conto vendite sospese WIP** |Conto WIP per il valore delle vendite calcolato dei semilavorati, corrispondente a un conto ricavi sospesi patrimoniale. Quando la rettifica WIP richiede l'aumento dei ricavi riconosciuti, puoi eseguire la registrazione a questo conto. | Vendite sospese, Vendite riconosciute|
| **Conto vendite fatturate WIP** |Conto per il valore delle vendite fatturate dei semilavorati che non può essere riconosciuto. Si tratta di un conto patrimoniale per i ricavi da capitale. | Vendite riconosciute, Vendite collegate|
| **Conto vendite applicate progetto** |Contropartita per il conto vendite fatturate WIP, che rappresenta un conto avere opposto. | Vendite collegate, Vendite riconosciute|
| **Conto rettifica vendite progetto** |Conto di contropartita per il conto vendite WIP per il progetto, che rappresenta un conto economico. | Vendite sospese|
| **Conto costi riconosciuti** |Conto spesa contenente i costi riconosciuti per il progetto. In genere si tratta di un conto di addebito. | Costi riconosciuti|
| **Conto vendite riconosciute** |Conto economico contenente le entrate riconosciute per il progetto. In genere si tratta di un conto di accredito. | Vendite riconosciute|

## <a name="see-also"></a>Vedere anche

[Impostare la gestione dei progetti](projects-setup-projects.md)  
[Video: Come creare un progetto in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Gestione di progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

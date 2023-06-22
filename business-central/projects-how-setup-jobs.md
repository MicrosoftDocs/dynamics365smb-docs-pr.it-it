---
title: 'Impostare commesse, prezzi e categorie di registrazione commesse'
description: Descrive come impostare le informazioni generali sui lavori.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
---
# <a name="set-up-jobs-prices-and-job-posting-groups" />Impostare commesse, prezzi e categorie di registrazione commesse

In veste di manager del progetto, è possibile configurare le commesse che definiscono ogni progetto gestito in [!INCLUDE[prod_short](includes/prod_short.md)]. Utilizza la pagina **Setup commesse** per definire come utilizzerai le caratteristiche della commessa.

Per ogni commessa, specificare varie informazioni:

* Prezzi per gli articoli di commessa
* Risorse commesse
* Conti C/G commesse
* Categorie di registrazione delle commesse (obbligatorio)

## <a name="to-set-general-information-for-jobs" />Per impostare le informazioni generali relative alle commesse

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup commesse**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> L'interruttore **Applica collegamento utilizzo per default** nella pagina **Setup commesse** indica se i movimenti contabili della commessa sono collegati alle righe di pianificazione commessa per impostazione predefinita. Attiva l'interruttore per applicare questa impostazione a tutti i nuovi lavori. È possibile abilitare o disabilitare il monitoraggio dell'utilizzo delle commesse per una commessa specifica abilitando o disabilitando l'interruttore **Applica collegamento utilizzo per default** nella pagina **Scheda commessa**.

### <a name="to-set-up-job-usage-tracking" />Per impostare la tracciabilità dell'utilizzo in una commessa

Quando si lavora su una commessa, potrebbe essere necessario tenere traccia dell'utilizzo rispetto al piano. Per esplorare l'uso è possibile creare un collegamento tra le righe di pianificazione commessa e l'utilizzo effettivo. Il collegamento ti consente di monitorare i tuoi costi e capire il lavoro residuo da svolgere. In base all'impostazione predefinita, il tipo di riga di pianificazione commessa è **Budget**, ma con il tipo di riga **Budget e fatturabile** si ottengono effetti simili.

Dopo aver impostato il campo la tracciabilità dell'utilizzo abilitando l'interruttore **Applica collegamento utilizzo per default**, è possibile esaminare le informazioni nella riga di pianificazione commessa. Ad esempio, è possibile impostare la quantità della risorsa, dell'articolo o del conto di contabilità generale. Puoi impostare inoltre la quantità da trasferire nella registrazione commesse. Il campo **Quantità residua** nella riga di pianificazione commessa indica ciò che resta da trasferire e registrare nelle registrazioni commesse.

>[!NOTE]
> Se la casella di controllo **Applica collegamento utilizzo** viene selezionata nella singola commessa e il campo **Tipo riga** nella riga di registrazione o nella riga di acquisto è **Fatturabile**, quindi vengono create nuove righe di pianificazione commessa di tipo **Sia Budget sia fatturabile** quando si registrano le righe di registrazione commessa o il documento di acquisto.  
>
> Per ulteriori informazioni, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md) e [Gestire gli approvvigionamenti delle commesse](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Se non specifichi un valore nel campo **Tipo riga** nella riga di registrazione della commessa o nella riga acquisto, non viene creata alcuna riga di pianificazione commessa quando si registra la registrazione commesse o il documento di acquisto.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs" />Per impostare i prezzi per risorse, articoli e conti di contabilità generale per le commesse

> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 sono stati rilasciati nuovi processi per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

È possibile impostare i prezzi per articoli, risorse e conti di contabilità generale correlati a una commessa. 

#### [Esperienza corrente](#tab/current-experience)

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Selezionare la commessa, quindi scegliere l'azione **Risorsa**, **Articolo** o **Conto C/G**.
3. Nelle pagine **Prezzi risorse commesse**, **Prezzi articoli commesse** o **Prezzi conti C/G commesse** compilare i campi come necessario.

Quando scegli una risorsa, un articolo o un conto di contabilità generale per una commessa, [!INCLUDE [prod_short](includes/prod_short.md)] utilizza le informazioni nei campi facoltativi nelle righe di pianificazione commessa e nei giornali di registrazione commessa. La tabella seguente spiega come.

|Colonna1  |Colonna2  |
|---------|---------|
|**Risorse commesse**|Campi **Nr. task commessa**, **Tipo di lavoro**, **Cod. valuta**, **% sconto riga** e **Fattore costo unitario**. Il valore nel campo **Prezzo unitario** per la risorsa viene utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immessa questa risorsa, una risorsa assegnata al gruppo di risorse. Il prezzo sostituisce sempre qualsiasi prezzo impostato nella pagina **Prezzi risorse/Prezzo gruppo risorse**.|
|**Articoli commessa**|Campi **Nr. task commessa**, **Cod. valuta** e **% sconto riga**. Il valore nel campo **Prezzo unitario** per l'articolo verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo articolo. Questo prezzo sostituisce sempre il normale prezzo cliente (il meccanismo "prezzo migliore") per gli articoli. Per utilizzare il normale prezzo del cliente, non specificare i prezzi degli articoli della commessa per il lavoro.|
|**Conti di contabilità generale**|Le informazioni nei campi **Nr. task commessa**, **Codice valuta**, **% sconto riga**, **Fattore costo unitario** e **Costo unitario** verranno utilizzate nelle righe di pianificazione commessa e nelle registrazioni commessa quando questo conto di contabilità generale verrà immesso o aggiunto a una commessa. Quando scegli un account di contabilità generale, le righe di pianificazione e le registrazioni commesse usa il valore nel campo **Prezzo unitario** per la spesa di commessa contabile.|

#### [Nuova esperienza](#tab/new-experience)

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Listini prezzi di vendita**.

---

## <a name="to-set-up-job-posting-groups" />Per impostare le categorie di registrazione commesse

Un aspetto della pianificazione delle commesse è decidere quali conti di registrazione utilizzare per il calcolo dei costi. Perché sia possibile registrare commesse, è necessario impostare conti per la registrazione di ciascuna categoria di registrazione commessa. La categoria di registrazione rappresenta un collegamento tra la commessa e come deve essere considerata nella contabilità generale. Quando si crea una commessa, si specifica una categoria di registrazione e, per default, ogni task creato per la commessa viene associato a tale categoria di registrazione. Tuttavia, quando si creano i task, è possibile sostituire l'impostazione di default e selezionare una categoria di registrazione più appropriata.  

> [!NOTE]  
> È necessario configurare l'installazione degli account nel Piano dei Conti prima delle categorie di registrazione. Per ulteriori informazioni, vedere [Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazione commesse**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

| Campo Conto | Descrizione |
| --- | --- |
| **Codice** |Codice per la categoria di registrazione È possibile immettere fino a 10 caratteri, spazi inclusi. |
| **Conto costi WIP** |Conto WIP per il costo calcolato dei semilavorati per la commessa, corrispondente a un conto cespiti patrimoniali. |
| **Conto costi sospesi WIP** |Un conto per il metodo Valore di costo o Costo del venduto del calcolo WIP. Questo conto è per le passività patrimoniali nel bilancio patrimoniale. Quando la rettifica WIP richiede l'aumento dei costi di utilizzo registrati nel conto economico, è possibile registrare questo conto. |
| **Conto costi comm. coll.** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto costi articolo collegati** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto costi risorse collegati** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto costi collegati** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto rettifica costi comm.** |Contropartita per il conto costi sospesi WIP, corrispondente a un conto spesa. |
| **Conto spesa C/G (Budget)** |Conto vendite da utilizzare per le spese di contabilità generale nei task commesse con la categoria di registrazione corrente. Se questo campo viene lasciato vuoto, verrà utilizzato il conto C/G immesso nella riga di pianificazione commessa. |
| **Conto vendite sospese WIP** |Conto WIP per il valore delle vendite calcolato dei semilavorati, corrispondente a un conto ricavi sospesi patrimoniale. Quando la rettifica WIP richiede l'aumento dei ricavi riconosciuti, puoi eseguire la registrazione a questo conto. |
| **Conto vendite fatturate WIP** |Conto per il valore delle vendite fatturate dei semilavorati che non può essere riconosciuto. Si tratta di un conto patrimoniale per i ricavi da capitale. |
| **Conto vendite commesse coll.** |Contropartita per il conto vendite fatturate WIP, che rappresenta un conto avere opposto. |
| **Conto rettifica vendite commesse** |Contropartita per il conto vendite WIP per la commessa, che rappresenta un conto avere. |
| **Conto costi riconosciuti** |Conto spesa contenente i costi riconosciuti per la commessa. In genere si tratta di un conto di addebito. |
| **Conto vendite riconosciute** |Conto avere contenente le entrate riconosciute per la commessa. In genere si tratta di un conto di accredito. |

## <a name="see-related-microsoft-trainingtrainingpathsset-up-jobs-resources" />Vedi il relativo [training Microsoft](/training/paths/set-up-jobs-resources/)

## <a name="see-also" />Vedere anche

[Impostare Gestione progetti](projects-setup-projects.md)  
[Video: Come creare una commessa in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Gestione di progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

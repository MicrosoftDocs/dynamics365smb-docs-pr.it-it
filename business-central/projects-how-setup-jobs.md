---
title: 'Impostare commesse, prezzi e categorie di registrazione commesse'
description: 'Descrive come impostare informazioni generali sulle commesse e i prezzi per articoli, risorse e gruppi di registrazione conti G/L e commesse per le commesse.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.date: 04/01/2021
ms.author: edupont
---
# Impostare commesse, prezzi e categorie di registrazione commesse

In veste di manager del progetto, è possibile configurare le commesse che definiscono ogni progetto gestito in [!INCLUDE[prod_short](includes/prod_short.md)]. Nella pagina **Setup commesse** è necessario specificare come si desidera utilizzare determinate funzionalità di commessa.

Per ogni commessa, si specificano quindi singole schede commessa con informazioni sui prezzi per gli articoli di commessa, le risorse di commessa e i conti C/G commesse ed è necessario impostare le categorie di registrazione commesse.

## Per impostare le informazioni generali relative alle commesse

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup commesse**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Il campo **Applica collegamento utilizzo per default** indica se i movimenti contabili della commessa sono collegati alle righe di pianificazione commessa per impostazione predefinita. Scegliere il campo se si desidera applicare questa impostazione a tutte le nuove commesse create. È possibile abilitare o disabilitare il monitoraggio dell'utilizzo delle commesse per una commessa specifica modificando il valore del campo **Applica collegamento di utilizzo** nella singola scheda commessa. Le conseguenze sono descritte nella sezione seguente.

### Per impostare la tracciabilità dell'utilizzo in una commessa

Quando si lavora su una commessa, potrebbe essere necessario tenere traccia dell'utilizzo rispetto al piano. Per eseguire questa operazione, è possibile creare un collegamento tra le righe di pianificazione commessa e l'utilizzo effettivo. Ciò consente di tenere traccia dei costi e di visualizzare facilmente il lavoro residuo da svolgere. In base all'impostazione predefinita, il tipo di riga di pianificazione commessa è *Budget*, ma con il tipo di riga **Budget e fatturabile** si ottengono effetti simili.

Dopo aver impostato il campo la tracciabilità dell'utilizzo scegliendo **Applica collegamento utilizzo**, è possibile esaminare le informazioni nella riga di pianificazione commessa. È possibile impostare la quantità della risorsa, dell'articolo o il conto di contabilità generale e indicare la quantità da trasferire nelle registrazioni commesse. Il campo **Quantità residua** nella riga di pianificazione commessa indicherà ciò che resta da trasferire e registrare nelle registrazioni commesse.

>[!NOTE]
> Se la casella di controllo **Applica collegamento utilizzo** viene selezionata nella singola commessa e il campo **Tipo riga** nella riga di registrazione o nella riga di acquisto è *Fatturabile*, quindi vengono create nuove righe di pianificazione commessa di tipo *Budget* quando si registrano le righe di registrazione commessa o il documento di acquisto.  
> Per ulteriori informazioni, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md) e [Gestire gli approvvigionamenti delle commesse](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Se il campo **Tipo riga** nella riga di registrazione della commessa o nella riga acquisto è vuoto, non viene creata alcuna riga di pianificazione commessa quando si registra la registrazione commesse o il documento di acquisto.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## Per impostare i prezzi per risorse, articoli e conti di contabilità generale per le commesse

> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 sono stati rilasciati nuovi processi per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

È possibile impostare i prezzi per articoli, risorse e conti di contabilità generale correlati a una commessa. 

#### [Esperienza corrente](#tab/current-experience)

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Selezionare la commessa, quindi scegliere l'azione **Risorsa**, **Articolo** o **Conto C/G**.
3. Nelle pagine **Prezzi risorse commesse**, **Prezzi articoli commesse** o **Prezzi conti C/G commesse** compilare i campi come necessario.

La tabella seguente mostra come le informazioni nei campi facoltativi verranno utilizzate nelle righe di pianificazione commessa e nei giornali di registrazione quando la risorsa, l'articolo o il conto di contabilità generale è stato scelto per la commessa.

|Colonna1  |Colonna2  |
|---------|---------|
|**Risorse commesse**|Campi **Nr. task commessa**, **Tipo di lavoro**, **Cod. valuta**, **% sconto riga** e **Fattore costo unitario**. Il valore nel campo **Prezzo unitario** per la risorsa verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immessa questa risorsa, una risorsa assegnata al gruppo di risorse, o qualsiasi risorsa. Questo prezzo sostituirà sempre qualsiasi prezzo impostato nella pagina **Prezzi risorse/Prezzo gruppo risorse**.|
|**Articoli commessa**|Campi **Nr. task commessa**, **Cod. valuta** e **% sconto riga**. Il valore nel campo **Prezzo unitario** per l'articolo verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo articolo. Questo prezzo sostituirà sempre il normale prezzo cliente (meccanismo "prezzo migliore") per gli articoli. Se si desidera utilizzare i normali meccanismi per il prezzo cliente, evitare di creare prezzi articoli commesse per la commessa.|
|**Conti di contabilità generale**|Le informazioni nei campi **Nr. task commessa**, **Codice valuta**, **% sconto riga**, **Fattore costo unitario** e **Costo unitario** verranno utilizzate nelle righe di pianificazione commessa e nelle registrazioni commessa quando questo conto di contabilità generale verrà immesso o aggiunto a una commessa. Il valore nel campo **Prezzo unitario** per la spesa di commessa contabile verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo conto C/G.|

#### [Nuova esperienza](#tab/new-experience)

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Listini prezzi di vendita**.

---

## Per impostare le categorie di registrazione commesse

Un aspetto della pianificazione delle commesse è decidere quali conti di registrazione utilizzare per il calcolo dei costi. Perché sia possibile registrare commesse, è necessario impostare conti per la registrazione di ciascuna categoria di registrazione commessa. La categoria di registrazione rappresenta un collegamento tra la commessa e come deve essere considerata nella contabilità generale. Quando si crea una commessa, si specifica una categoria di registrazione e, per default, ogni task creato per la commessa viene associato a tale categoria di registrazione. Tuttavia, quando si creano i task, è possibile sostituire l'impostazione di default e selezionare una categoria di registrazione più appropriata.  

> [!NOTE]  
>   I conti necessari devono essere impostati nel Piano dei Conti prima delle categorie di registrazione. Per ulteriori informazioni, vedere [Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Categorie registrazione commesse**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**, quindi compilare i campi dei conti come descritto nella tabella che segue.  

| Campo Conto | Descrizione |
| --- | --- |
| **Codice** |Codice per la categoria di registrazione. È possibile immettere fino a 10 caratteri, spazi inclusi. |
| **Conto costi WIP** |Conto WIP per il costo calcolato dei semilavorati per la commessa, corrispondente a un conto cespiti patrimoniali. |
| **Conto costi sospesi WIP** |Conto per il metodo Valore costo o Costo del venduto del calcolo WIP, corrispondente a un conto passività patrimoniale per le spese sospese. La registrazione verrà eseguita quando la rettifica WIP richiede l'aumento dei costi di utilizzo registrati nel conto economico. |
| **Conto costi comm. coll.** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto costi articolo collegati** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto costi risorse collegati** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto costi collegati** |Contropartita per il conto costi WIP, opposto del conto spesa negativa. |
| **Conto rettifica costi comm.** |Contropartita per il conto costi sospesi WIP, corrispondente a un conto spesa. |
| **Conto spesa C/G (Budget)** |Conto vendite da utilizzare per le spese di contabilità generale nei task commesse con la categoria di registrazione corrente. Se questo campo viene lasciato vuoto, verrà utilizzato il conto C/G immesso nella riga di pianificazione commessa. |
| **Conto vendite sospese WIP** |Conto WIP per il valore delle vendite calcolato dei semilavorati, corrispondente a un conto ricavi sospesi patrimoniale. La registrazione in questo conto verrà eseguita quando la rettifica WIP richiede l'aumento dei ricavi riconosciuti. |
| **Conto vendite fatturate WIP** |Conto per il valore delle vendite fatturate dei semilavorati che non può essere riconosciuto. Si tratta di un conto patrimoniale per i ricavi da capitale. |
| **Conto vendite commesse coll.** |Contropartita per il conto vendite fatturate WIP, che rappresenta un conto avere opposto. |
| **Conto rettifica vendite commesse** |Contropartita per il conto vendite WIP per la commessa, che rappresenta un conto avere. |
| **Conto costi riconosciuti** |Conto spesa contenente i costi riconosciuti per la commessa. In genere si tratta di un conto di addebito. |
| **Conto vendite riconosciute** |Conto avere contenente le entrate riconosciute per la commessa. In genere si tratta di un conto di accredito. |

## Vedi il relativo [training Microsoft](/training/paths/set-up-jobs-resources/)

## Vedere anche

[Impostare Gestione progetti](projects-setup-projects.md)  
[Video: Come creare una commessa in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Gestione di progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

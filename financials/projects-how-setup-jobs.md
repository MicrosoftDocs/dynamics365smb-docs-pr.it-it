---
title: Impostare prezzi delle commesse e categorie di registrazione commesse| Documenti Microsoft
description: Descrive come impostare informazioni generali sulle commesse e i prezzi per articoli, risorse e gruppi di registrazione conti G/L e commesse per le commesse.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: aa7669c5f7762de647346039e0023c93603fbc10
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-jobs"></a>Procedura: Impostare le commesse
Nella finestra **Setup commesse** è necessario specificare come si desidera utilizzare determinate funzionalità di commessa.

Nelle singole schede commessa, è necessario impostare i prezzi per gli articoli di commessa, le risorsa di commessa e i conti C/G commesse ed è necessario impostare le categorie di registrazione commesse.

## <a name="to-set-general-information-for-jobs"></a>Per impostare le informazioni generali relative alle commesse
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup commesse**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   La casella di controllo **Applica collegamento utilizzo** è piuttosto complessa, quindi viene spiegata nella sezione che segue.

## <a name="to-set-up-job-usage-tracking"></a>Per impostare la tracciabilità dell'utilizzo in una commessa
Quando viene eseguita una commessa, potrebbe essere necessario tenere traccia dell'utilizzo rispetto al piano. Per eseguire questa operazione, è possibile creare un collegamento tra le righe di pianificazione commessa e l'utilizzo effettivo. Ciò consente di tenere traccia dei costi e di visualizzare facilmente il lavoro residuo da svolgere. In base all'impostazione predefinita, il tipo di riga di pianificazione commessa è **Budget**, ma con il tipo di riga **Budget e fatturabile** si ottengono effetti simili.

Se si seleziona la casella di controllo **Applica collegamento utilizzo**, è possibile esaminare le informazioni nella riga di pianificazione commessa. È possibile impostare la quantità della risorsa, dell'articolo o il conto di contabilità generale e quindi indicare la quantità da trasferire nelle registrazioni commesse. Il campo **Quantità residua** nella riga di pianificazione commessa indicherà ciò che resta da trasferire e registrare nelle registrazioni commesse.

Se la casella di controllo **Applica collegamento utilizzo** è selezionata e il tipo di riga di pianificazione commessa è **Fatturabile**, Financials crea una riga di pianificazione commessa di tipo **Budget** dopo che viene registrata la riga di registrazione.

> [!NOTE]  
>   Se la casella di controllo **Applica collegamento utilizzo** nella scheda commessa è selezionata e il campo **Tipo riga** nelle registrazioni commesse è vuoto, vengono create nuove righe di pianificazione commessa di tipo **Budget** quando si registrano le righe di registrazione commessa. Se la casella di controllo **Applica collegamento utilizzo** non è selezionata e il campo **Tipo riga** nella riga di registrazione commessa è vuoto, non vengono create righe di pianificazione commessa quando si registrano le righe di registrazione commessa. Per ulteriori informazioni, vedere [Procedura: Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup commesse**, quindi scegliere il collegamento correlato.
2. Selezionare o deselezionare la casella di controllo **Applica collegamento utilizzo**.

> [!NOTE]  
>   È possibile impostare diversamente la casella di controllo **Applica collegamento utilizzo** nelle singole schede commessa. In questo caso, l'impostazione di tale commessa ignora il default generale descritto sopra.

## <a name="to-set-up-prices-for-job-resources"></a>Per impostare i prezzi per le risorse di commessa
È possibile impostare prezzi specifici per le risorse per una commessa. A tale scopo, utilizzare la finestra **Prezzi risorse commesse**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Risorsa**.
3. Nella finestra **Prezzi risorse commesse** compilare i campi in base alle esigenze.

Le informazioni opzionali nei campi **Nr. task commessa**, **Tipo di lavoro**, **Codice valuta**, **% sconto riga** e **Fattore costo unitario** verranno visualizzate nelle righe di pianificazione commessa e nelle registrazioni utilizzo quando questa risorsa viene immessa e aggiunta alla commessa.  

Il valore nel campo **Prezzo unitario** per la risorsa verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immessa questa risorsa, una risorsa assegnata al gruppo di risorse, o qualsiasi risorsa.  

> [!NOTE]  
>   Il prezzo sostituisce sempre qualsiasi prezzo impostato nella finestra **Prezzo risorse/Prezzo gruppo risorse**.

## <a name="to-set-up-prices-for-job-items"></a>Per impostare i prezzi per gli articoli di commessa
È possibile impostare prezzi specifici per gli articoli per una commessa. A tale scopo, utilizzare la finestra **Prezzi articoli commesse**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Articolo**.
3. Nella finestra **Prezzi articoli commesse** compilare i campi in base alle esigenze.

Le informazioni opzionali nei campi **Nr. task commessa**, **Codice valuta** e **% sconto riga** verranno utilizzati nelle righe di pianificazione commessa e nelle registrazioni commesse quando questo articolo verrà immesso o aggiunto alla commessa.  

Il valore nel campo **Prezzo unitario** per l'articolo verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo articolo.  

> [!NOTE]  
>   Questo prezzo sostituisce sempre il normale prezzo cliente (il meccanismo "prezzo migliore") per gli articoli. Se si desidera utilizzare i normali meccanismi per il prezzo cliente, evitare di creare prezzi articoli commesse per la commessa.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Per impostare i prezzi dei conti di contabilità generale delle commesse
È possibile impostare prezzi specifici per le spese di contabilità generale relative a una commessa. A tale scopo, utilizzare la finestra **Prezzi conti C/G commesse**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Commesse**, quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Conto C/G**.  
3. Nella finestra **Prezzi conti C/G commesse** compilare i campi in base alle esigenze.

Le informazioni opzionali nei campi **Nr. task commessa**, **Codice valuta**, **% sconto riga**, **Fattore costo unitario** e **Costo unitario** verranno utilizzate nelle righe di pianificazione commessa e nelle registrazioni commessa quando questo conto C/G verrà immesso o aggiunto a una commessa.  

Il valore nel campo **Prezzo unitario** per la spesa di commessa contabile verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo conto C/G.

## <a name="to-set-up-job-posting-groups"></a>Per impostare le categorie di registrazione commesse
Un aspetto della pianificazione delle commesse è decidere quali conti di registrazione utilizzare per il calcolo dei costi. Perché sia possibile registrare commesse, è necessario impostare conti per la registrazione di ciascuna categoria di registrazione commessa. La categoria di registrazione rappresenta un collegamento tra la commessa e come deve essere considerata nella contabilità generale. Quando si crea una commessa, si specifica una categoria di registrazione e, per default, ogni task creato per la commessa viene associato a tale categoria di registrazione. Tuttavia, quando si creano i task, è possibile sostituire l'impostazione di default e selezionare una categoria di registrazione più appropriata.  

> [!NOTE]  
>   I conti necessari devono essere impostati nel Piano dei Conti prima delle categorie di registrazione. Per ulteriori informazioni, vedere [Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. commesse**, quindi scegliere il collegamento correlato.  
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

## <a name="see-also"></a>Vedi anche
[Impostare Gestione progetti](projects-setup-projects.md)  
[Gestire progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)         
[Vendite](sales-manage-sales.md)      
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


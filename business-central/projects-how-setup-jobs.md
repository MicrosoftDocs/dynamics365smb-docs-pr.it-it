---
title: Impostare prezzi delle commesse e categorie di registrazione commesse| Documenti Microsoft
description: Descrive come impostare informazioni generali sulle commesse e i prezzi per articoli, risorse e gruppi di registrazione conti G/L e commesse per le commesse.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 34dfdb463d3423d823b8f1439361d05296ca3c8a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253828"
---
# <a name="set-up-jobs"></a>Imposta commesse

In veste di manager del progetto, è possibile configurare le commesse che definiscono ogni progetto gestito in [!INCLUDE [prodshort](includes/prodshort.md)]. Nella pagina **Setup commesse** è necessario specificare come si desidera utilizzare determinate funzionalità di commessa.

Per ogni commessa, si specificano quindi singole schede commessa con informazioni sui prezzi per gli articoli di commessa, le risorse di commessa e i conti C/G commesse ed è necessario impostare le categorie di registrazione commesse.

## <a name="to-set-general-information-for-jobs"></a>Per impostare le informazioni generali relative alle commesse
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup commesse** e quindi scegliere il collegamento correlato.
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> L'impatto del campo **Applica collegamento utilizzo per default** è piuttosto complesso, quindi viene spiegato nella sezione che segue.

### <a name="to-set-up-job-usage-tracking"></a>Per impostare la tracciabilità dell'utilizzo in una commessa

Quando viene eseguita una commessa, potrebbe essere necessario tenere traccia dell'utilizzo rispetto al piano. Per eseguire questa operazione, è possibile creare un collegamento tra le righe di pianificazione commessa e l'utilizzo effettivo. Ciò consente di tenere traccia dei costi e di visualizzare facilmente il lavoro residuo da svolgere. In base all'impostazione predefinita, il tipo di riga di pianificazione commessa è **Budget**, ma con il tipo di riga **Budget e fatturabile** si ottengono effetti simili.

Se si seleziona il campo **Applica collegamento utilizzo per default**, è possibile esaminare le informazioni nella riga di pianificazione commessa. È possibile impostare la quantità della risorsa, dell'articolo o il conto di contabilità generale e quindi indicare la quantità da trasferire nelle registrazioni commesse. Il campo **Quantità residua** nella riga di pianificazione commessa indicherà ciò che resta da trasferire e registrare nelle registrazioni commesse.

> [!TIP]  
> È possibile abilitare o disabilitare la tracciabilità dell'utilizzo in una commessa per una specifica commessa. Il valore del campo **Applica collegamento utilizzo** nella singola scheda commessa sostituisce l'impostazione nella pagina **Setup commesse**.  

Se la casella di controllo **Applica collegamento utilizzo per default** è selezionata e il tipo di riga di pianificazione commessa è **Fatturabile**, viene creata una riga di pianificazione commessa di tipo **Budget** dopo la registrazione di una riga di registrazione commessa.

> [!IMPORTANT]
> Se la tracciabilità dell'utilizzo in una commessa è abilitata nella pagina **Jobs Setup** e il campo **Tipo riga** nelle registrazioni commesse è vuoto, vengono create nuove righe di pianificazione commessa di tipo **Budget** quando si registrano le righe di registrazione commessa.  
>  
> Se la tracciabilità dell'utilizzo in una commessa *non* è abilitata nella pagina **Setup commesse** o nella singola commessa e il campo **Tipo riga** nelle registrazioni commesse è vuoto, non viene creata nessuna riga di pianificazione commessa quando si registrano le righe di registrazione commessa. Per ulteriori informazioni, vedere [Registrare l'utilizzo nelle commesse](projects-how-record-job-usage.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup commesse**, quindi scegliere il collegamento correlato.
2. Selezionare la casella di controllo **Applica collegamento utilizzo per default**.

## <a name="to-set-up-prices-for-job-resources"></a>Per impostare i prezzi per le risorse di commessa
È possibile impostare prezzi specifici per le risorse per una commessa. A tale scopo, utilizzare la pagina **Prezzi risorse commesse**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Commesse** e quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Risorsa**.
3. Nella pagina **Prezzi risorse commesse** compilare i campi in base alle esigenze.

Le informazioni opzionali nei campi **Nr. task commessa**, **Tipo di lavoro**, **Codice valuta**, **% sconto riga** e **Fattore costo unitario** verranno visualizzate nelle righe di pianificazione commessa e nelle registrazioni utilizzo quando questa risorsa viene immessa e aggiunta alla commessa.  

Il valore nel campo **Prezzo unitario** per la risorsa verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immessa questa risorsa, una risorsa assegnata al gruppo di risorse, o qualsiasi risorsa.  

> [!NOTE]  
>   Il prezzo sostituisce sempre qualsiasi prezzo impostato nella pagina **Prezzi risorse/Prezzo gruppo risorse**.

## <a name="to-set-up-prices-for-job-items"></a>Per impostare i prezzi per gli articoli di commessa
È possibile impostare prezzi specifici per gli articoli per una commessa. A tale scopo, utilizzare la pagina **Prezzi articoli commesse**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Commesse** e quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Articolo**.
3. Nella pagina **Prezzi articoli commesse** compilare i campi in base alle esigenze.

Le informazioni opzionali nei campi **Nr. task commessa**, **Codice valuta** e **% sconto riga** verranno utilizzati nelle righe di pianificazione commessa e nelle registrazioni commesse quando questo articolo verrà immesso o aggiunto alla commessa.  

Il valore nel campo **Prezzo unitario** per l'articolo verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo articolo.  

> [!NOTE]  
>   Questo prezzo sostituisce sempre il normale prezzo cliente (il meccanismo "prezzo migliore") per gli articoli. Se si desidera utilizzare i normali meccanismi per il prezzo cliente, evitare di creare prezzi articoli commesse per la commessa.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Per impostare i prezzi dei conti di contabilità generale delle commesse
È possibile impostare prezzi specifici per le spese di contabilità generale relative a una commessa. A tale scopo, utilizzare la pagina **Prezzi conti C/G commesse**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Commesse** e quindi scegliere il collegamento correlato.  
2. Selezionare la relativa commessa, quindi scegliere l'azione **Conto C/G**.  
3. Nella pagina **Prezzi conti C/G commesse** compilare i campi in base alle esigenze.

Le informazioni opzionali nei campi **Nr. task commessa**, **Codice valuta**, **% sconto riga**, **Fattore costo unitario** e **Costo unitario** verranno utilizzate nelle righe di pianificazione commessa e nelle registrazioni commessa quando questo conto C/G verrà immesso o aggiunto a una commessa.  

Il valore nel campo **Prezzo unitario** per la spesa di commessa contabile verrà utilizzato nelle righe di pianificazione commessa e nelle registrazioni commesse quando verrà immesso questo conto C/G.

## <a name="to-set-up-job-posting-groups"></a>Per impostare le categorie di registrazione commesse
Un aspetto della pianificazione delle commesse è decidere quali conti di registrazione utilizzare per il calcolo dei costi. Perché sia possibile registrare commesse, è necessario impostare conti per la registrazione di ciascuna categoria di registrazione commessa. La categoria di registrazione rappresenta un collegamento tra la commessa e come deve essere considerata nella contabilità generale. Quando si crea una commessa, si specifica una categoria di registrazione e, per default, ogni task creato per la commessa viene associato a tale categoria di registrazione. Tuttavia, quando si creano i task, è possibile sostituire l'impostazione di default e selezionare una categoria di registrazione più appropriata.  

> [!NOTE]  
>   I conti necessari devono essere impostati nel Piano dei Conti prima delle categorie di registrazione. Per ulteriori informazioni, vedere [Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md).  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Categorie registrazione commesse** e quindi scegliere il collegamento correlato.  
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

## <a name="see-also"></a>Vedere anche

[Impostare Gestione progetti](projects-setup-projects.md)  
[Video: Come creare una commessa in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Gestione di progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

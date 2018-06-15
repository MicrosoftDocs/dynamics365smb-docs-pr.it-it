---
title: Scegliere l'esperienza utente per visualizzare o nascondere le funzioni avanzate | Documenti Microsoft
description: "Informazioni sulle caratteristiche dei livelli dell'esperienza utente Base ed Essenziale che hanno effetto su interfaccia utente, aree di applicazione e società."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: dc7e739bc2b8ac9e8efce3a0f52acb945352416e
ms.openlocfilehash: 0a94d94e58b2aa3f04639a00904b5370c91b1132
ms.contentlocale: it-it
ms.lasthandoff: 04/19/2018

---
# <a name="changing-which-features-are-displayed"></a>Modifica delle funzionalità visualizzate
[!INCLUDE[d365fin](includes/d365fin_md.md)] è progettato per aiutare a gestire l'attività dell'azienda, indipendentemente dalla line of business attiva. Al centro di [!INCLUDE[d365fin](includes/d365fin_md.md)] si trovano la creazione di rendiconti finanziari e i processi di vendita e acquisto. Aggiungere esperienze in base alle esigenze aziendali aggiungendo estensioni da AppSource o modificando l'impostazione Esperienza per l'azienda. Per ulteriori informazioni, vedere la sezione [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md) oppure la sezione "Scelta di un'esperienza utente per visualizzare o nascondere le funzionalità" di seguito.

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Scelta di un'esperienza utente per visualizzare o nascondere le funzionalità
L'utilizzo dell'esperienza utente determina la quantità di funzionalità core disponibile quando l'utente e i suoi colleghi usano [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile scegliere l'esperienza utente per la propria società nel campo **Esperienza** della finestra **Informazioni società**.

> [!NOTE]  
> Questa impostazione si applica a tutti gli utenti della società. Gli utenti possono personalizzare la propria esperienza anche cambiando i layout e il contenuto delle pagine. Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro e delle pagine](ui-personalization-user.md).  

Nella tabella seguente sono elencate le esperienze che sono attualmente disponibili.

| Esperienza | Impatto sull'interfaccia utente |
| --- | --- |
| **Di base** |Mostra solo campi e azioni di base delle funzionalità aziendali più comuni, come vendite, acquisti, inventario, finanza. |
| **Essenziale** |Mostra le azioni e i campi per tutte le funzionalità aziendali comuni.|
| **Premium** |Mostra le azioni e i campi per tutte le funzionalità aziendali, incluse Manufacturing e Gestione assistenza.|

> [!NOTE]  
> Le esperienze che è possibile selezionare in [!INCLUDE[d365fin](includes/d365fin_md.md)] dipendono dalla licenza della soluzione, denominata piano. Per informazioni sui piani **Essenziale** e **Premium**, vedere [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) nel sito marketing di Microsoft Dynamics 365.

> [!IMPORTANT]  
> A tutti gli utenti abituali di una soluzione deve essere assegnato lo stesso piano, Essential o Premium, prima che l'esperienza possa essere selezionata per la società. Di conseguenza, un utente non può accedere alle funzionalità Premium se uno o più altri utenti possono accedere solo alle funzionalità Essential. Questo non è il caso per gli utenti non abituali di tipo Membro team, Amministratore interno, Contabile esterno e Amministratore delegato, a cui può essere assegnato un piano diverso rispetto agli altri utenti della soluzione.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Abilitazione delle funzioni Premium dopo l'aggiornamento di un piano
Agli utenti vengono assegnati i piani tramite l'interfaccia di amministrazione di Office 365 in relazione al lavoro generale per creare gli utenti di Business Central. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

È quindi possibile definire le funzioni e finestre specifiche all'interno dell'esperienza a cui gli utenti sono autorizzati ad accedere assegnando set di autorizzazioni. Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Per aggiornare le modifiche di piano in gruppi di utenti
Dopo aver apportato una modifica ai piani utenti dell'interfaccia di amministrazione di Office 365, ad esempio dopo avere assegnato più utenti al piano Premium, è necessario riflettere la modifica in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Accedere come amministratore.
2. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Utenti**, quindi scegliere il collegamento correlato.
3. Nella finestra **Utenti** scegliere l'azione **Aggiorna tutti i gruppi di utenti**.

Tutte le nuove informazioni sui piani degli utenti e sui gruppi di utenti assegnati vengono ora aggiornate in base alle modifiche del piano.

### <a name="to-select-the-premium-experience"></a>Per selezionare l'esperienza Premium
È ora possibile selezionare la nuova esperienza.
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Informazioni società**, quindi scegliere il collegamento correlato.
2. Nella Scheda dettaglio **Esperienza utente** della finestra **Informazioni società** selezionare Premium nel campo **Esperienza**.

## <a name="see-also"></a>Vedere anche
[Creazione di nuove società](about-new-company.md)  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)    
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]


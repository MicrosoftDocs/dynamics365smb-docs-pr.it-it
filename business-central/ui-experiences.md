---
title: Scegliere l'esperienza utente per visualizzare o nascondere le funzioni avanzate | Documenti Microsoft
description: Informazioni sulle caratteristiche dei livelli dell'esperienza utente Essential e Premium che hanno effetto su interfaccia utente, aree di applicazione e società.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 9110ee79e4d1788f41c8f1960f282cb490a3cc8a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "912416"
---
# <a name="changing-which-features-are-displayed"></a>Modifica delle funzionalità visualizzate
[!INCLUDE[d365fin](includes/d365fin_md.md)] è progettato per aiutare a gestire l'attività dell'azienda, indipendentemente dalla line of business attiva. Al centro di [!INCLUDE[d365fin](includes/d365fin_md.md)] si trovano la creazione di rendiconti finanziari e i processi di vendita e acquisto. Aggiungere esperienze in base alle esigenze aziendali aggiungendo estensioni da AppSource o modificando l'impostazione Esperienza per l'azienda. Per ulteriori informazioni, vedere [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md) oppure [Scelta di un'esperienza utente per visualizzare o nascondere le funzionalità](ui-experiences.md#choosing-a-user-experience-to-show-or-hide-features).

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Scelta di un'esperienza utente per visualizzare o nascondere le funzionalità
L'utilizzo dell'esperienza utente determina la quantità di funzionalità core disponibile quando l'utente e i suoi colleghi usano [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile scegliere l'esperienza utente per la propria società nel campo **Esperienza** della pagina **Informazioni società**.

> [!NOTE]  
> Questa impostazione si applica a tutti gli utenti della società. Gli utenti possono personalizzare la propria esperienza anche cambiando i layout e il contenuto delle pagine. Per ulteriori informazioni, vedere [Personalizzazione dell'area di lavoro e delle pagine](ui-personalization-user.md).  

Nella tabella seguente sono elencate le esperienze che sono attualmente disponibili.

| Esperienza | Impatto sull'interfaccia utente |
| --- | --- |
| **Essential** |Mostra le azioni e i campi per tutte le funzionalità aziendali comuni.|
| **Premium** |Mostra le azioni e i campi per tutte le funzionalità aziendali, incluse Manufacturing e Gestione assistenza.|

> [!NOTE]  
> Le esperienze che è possibile selezionare in [!INCLUDE[d365fin](includes/d365fin_md.md)] dipendono dalla licenza della soluzione, denominata piano. Per informazioni sui piani **Essenziale** e **Premium**, vedere [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) nel sito marketing di Microsoft Dynamics 365. Vedere anche [Guida alle licenze di [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?linkid=2068931) (richiede l'accesso a CustomerSource o PartnerSource).

> [!IMPORTANT]  
> A tutti gli utenti abituali di una soluzione deve essere assegnato lo stesso piano, Essential o Premium, prima che l'esperienza possa essere selezionata per la società. Di conseguenza, un utente non può accedere alle funzionalità Premium se uno o più altri utenti possono accedere solo alle funzionalità Essential. Questo non è il caso per gli utenti non abituali di tipo Membro team, Amministratore interno, Contabile esterno e Amministratore delegato, a cui può essere assegnato un piano diverso rispetto agli altri utenti della soluzione.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Abilitazione delle funzioni Premium dopo l'aggiornamento di un piano
Agli utenti vengono assegnati i piani tramite l'interfaccia di amministrazione di Office 365 in relazione al lavoro generale per creare gli utenti di Business Central. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

È quindi possibile definire le funzioni e pagina specifiche all'interno dell'esperienza a cui gli utenti sono autorizzati ad accedere assegnando set di autorizzazioni. Per ulteriori informazioni, vedere [Gestione di utenti e autorizzazioni](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Per aggiornare le modifiche di piano in gruppi di utenti
Dopo aver apportato una modifica ai piani utenti dell'interfaccia di amministrazione di Office 365, ad esempio dopo avere assegnato più utenti al piano Premium, è necessario riflettere la modifica in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Accedere come amministratore.
2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Utenti** e quindi scegliere il collegamento correlato.
3. In alternativa, nella pagina **Utenti** scegliere l'azione **Aggiorna tutti i gruppi di utenti**.

Tutte le nuove informazioni sui piani degli utenti e sui gruppi di utenti assegnati vengono ora aggiornate in base alle modifiche del piano.

### <a name="to-select-the-premium-experience"></a>Per selezionare l'esperienza Premium
È ora possibile selezionare la nuova esperienza.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Informazioni società** e quindi scegliere il collegamento correlato.
2. Nella Scheda dettaglio **Esperienza utente** della pagina **Informazioni società** selezionare Premium nel campo **Esperienza**.

## <a name="help-assumes-premium-experience"></a>La Guida presuppone un'esperienza Premium
Tutte le descrizioni delle caratteristiche nella documentazione per [!INCLUDE[d365fin](includes/d365fin_md.md)] presuppongono l'esperienza **Premium**, ovvero le descrizioni riguardano l'intero ambito degli elementi dell'interfaccia utente. Una nota di testo viene inserita negli argomenti di alto livello della Guida per le aree delle funzioni Manufacturing e Gestione assistenza che richiedono l'esperienza **Premium**.

## <a name="see-also"></a>Vedere anche
[Creazione di nuove società](about-new-company.md)  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)    
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Guida alle licenze](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

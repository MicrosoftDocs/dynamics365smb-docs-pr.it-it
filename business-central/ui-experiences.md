---
title: Scegliere l'esperienza utente per visualizzare o nascondere le funzioni avanzate | Documenti Microsoft
description: Informazioni sulle caratteristiche dei livelli dell'esperienza utente Essential e Premium che hanno effetto su interfaccia utente, aree di applicazione e società.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/08/2019
ms.author: sgroespe
ms.openlocfilehash: 8c9223176968d048d167b3b8509cab26343ee9f1
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775333"
---
# <a name="change-which-features-are-displayed"></a>Modifica delle funzionalità visualizzate
[!INCLUDE[d365fin](includes/d365fin_md.md)] è progettato per aiutare l'utente a gestire la propria attività indipendentemente dalle dimensioni e dalla complessità. Alla base del prodotto sono disponibili funzionalità essenziali, come la gestione di report finanziari, vendite, acquisti e magazzino. Con l'aumentare della complessità aziendale,è possibile ad esempio attivare la funzionalità per la produzione e la gestione dell'assistenza.

È possibile definire il livello di complessità del prodotto e, di conseguenza, a quali funzionalità gli utenti della società possono accedere, modificando l'impostazione **Esperienza** nella pagina **Informazioni società**. L'impostazione dell'esperienza può anche essere modificata aggiungendo alcune estensioni da AppSource. Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md).

Nella tabella seguente sono elencate le esperienze che sono attualmente disponibili.

| Esperienza | Impatto sull'interfaccia utente |
| --- | --- |
| **Essential** |Mostra le azioni e i campi per tutte le funzionalità aziendali comuni.|
| **Premium** |Mostra le azioni e i campi per tutte le funzionalità aziendali, incluse Manufacturing e Gestione assistenza.|

Le esperienze che possono essere selezionate in [!INCLUDE[d365fin](includes/d365fin_md.md)] riflettono licenze della soluzione, denominate piani, definite per il prodotto. Per informazioni sui piani Essenziale e Premium, vedere [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) nel sito di marketing di Microsoft Dynamics 365. Vedere anche [Guida alle licenze di [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?linkid=2068931) (richiede l'accesso a CustomerSource o PartnerSource).

> [!IMPORTANT]  
> A tutti gli utenti abituali di una soluzione deve essere assegnato lo stesso piano, Essential o Premium, prima che l'esperienza possa essere selezionata per la società. Di conseguenza, un utente non può accedere alle funzionalità Premium se uno o più altri utenti possono accedere solo alle funzionalità Essential. Questo non è il caso per gli utenti non abituali di tipo Membro team, Amministratore interno, Contabile esterno e Amministratore delegato, a cui può essere assegnato un piano diverso rispetto agli altri utenti della soluzione.<br /><br /> Solo gli utenti di tipo Valutazione o Premium possono modificare il valore nel campo **Esperienza** da Essential a Premium.

Prima di definire l'impostazione dell'esperienza di una società, definire l'accesso degli utenti a funzioni e pagine specifiche assegnando set di autorizzazioni. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

L'impostazione **Esperienza** si applica a tutti gli utenti di una società, ma ogni utente può personalizzare ulteriormente la propria esperienza modificando il layout e il contenuto della pagina. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Abilitazione delle funzioni Premium dopo l'aggiornamento di un piano
Agli utenti vengono assegnati i piani tramite l'interfaccia di amministrazione di Office 365 in relazione al lavoro generale per creare gli utenti di Business Central. Per ulteriori informazioni, vedere [Aggiungere utenti a Office 365 per l'azienda](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

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
Tutte le descrizioni delle caratteristiche nella documentazione per [!INCLUDE[d365fin](includes/d365fin_md.md)] presuppongono l'esperienza **Premium**, ovvero le descrizioni riguardano l'intero ambito degli elementi dell'interfaccia utente.

## <a name="see-also"></a>Vedere anche
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Personalizzazione di Business Central](ui-customizing-overview.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Creazione di nuove società](about-new-company.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Guida alle licenze](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

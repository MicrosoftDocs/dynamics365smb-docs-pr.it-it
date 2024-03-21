---
title: Modifica delle funzionalità visualizzate
description: 'Informazioni sulle caratteristiche dei livelli dell''esperienza utente Essential e Premium che hanno effetto su interfaccia utente, aree di applicazione e società.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: 1
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Modifica delle funzionalità visualizzate
[!INCLUDE[prod_short](includes/prod_short.md)] è progettato per aiutare l'utente a gestire la propria attività indipendentemente dalle dimensioni e dalla complessità. Alla base del prodotto sono disponibili funzionalità essenziali, come la gestione di report finanziari, vendite, acquisti e magazzino. Con l'aumentare della complessità aziendale,è possibile ad esempio attivare la funzionalità per la produzione e la gestione dell'assistenza.

È possibile definire il livello di complessità del prodotto e, di conseguenza, a quali funzionalità gli utenti della società possono accedere, modificando l'impostazione **Esperienza** nella pagina **Informazioni società**. L'impostazione dell'esperienza può anche essere modificata aggiungendo alcune estensioni da AppSource. Per maggiori informazioni, vedere [Personalizzazione di [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le estensioni](ui-extensions.md).

Nella tabella seguente sono elencate le esperienze che sono attualmente disponibili.

| Esperienza | Impatto sull'interfaccia utente |
| --- | --- |
| **Essential** |Mostra le azioni e i campi per tutte le funzionalità aziendali comuni.|
| **Premium** |Mostra le azioni e i campi per tutte le funzionalità aziendali, incluse Manufacturing e Gestione assistenza.|

Le esperienze che possono essere selezionate in [!INCLUDE[prod_short](includes/prod_short.md)] riflettono licenze della soluzione, denominate piani, definite per il prodotto. Per informazioni sui piani Essenziale e Premium, vedere [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) nel sito di marketing di Microsoft Dynamics 365. Vedere anche la Guida alle licenze di [[!INCLUDE[prod_short](includes/prod_short.md)]](https://go.microsoft.com/fwlink/?linkid=2068931).

> [!IMPORTANT]  
> A tutti gli utenti abituali di una soluzione deve essere assegnato lo stesso piano, Essential o Premium, prima che l'esperienza possa essere selezionata per la società. Di conseguenza, un utente non può accedere alle funzionalità Premium se uno o più altri utenti possono accedere solo alle funzionalità Essential. Questo non è il caso per gli utenti non abituali di tipo Membro team, Amministratore interno, Contabile esterno e Amministratore delegato, a cui può essere assegnato un piano diverso rispetto agli altri utenti della soluzione.<br /><br /> Solo gli utenti di tipo Valutazione o Premium possono modificare il valore nel campo **Esperienza** da Essential a Premium.

Prima di definire l'impostazione dell'esperienza di una società, definire l'accesso degli utenti a funzioni e pagine specifiche assegnando set di autorizzazioni. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

L'impostazione **Esperienza** si applica a tutti gli utenti di una società, ma ogni utente può personalizzare ulteriormente la propria esperienza modificando il layout e il contenuto della pagina. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

## Abilitazione delle funzioni Premium dopo l'aggiornamento di un piano
Agli utenti vengono assegnati i piani tramite l'interfaccia di amministrazione di Microsoft 365 in relazione al lavoro generale per creare gli utenti di Business Central. Per ulteriori informazioni, vedere[Aggiungere utenti e assegnare licenze allo stesso tempo](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### Per aggiornare le modifiche di piano in gruppi di utenti

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Dopo aver apportato una modifica ai piani utenti dell'interfaccia di amministrazione di Microsoft 365, ad esempio dopo avere assegnato più utenti al piano Premium, è necessario riflettere la modifica aggiornando [!INCLUDE[prod_short](includes/prod_short.md)].

1. Accedere come amministratore.
2. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Utenti**, quindi scegli il collegamento correlato.
3. Nella pagina **Utenti**, scegli l'azione **Aggiorna utenti da Microsoft 365**.

### Per selezionare l'esperienza Premium
È ora possibile selezionare la nuova esperienza.
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Informazioni società**, quindi scegli il collegamento correlato.
2. Nella Scheda dettaglio **Esperienza utente** della pagina **Informazioni società** selezionare Premium nel campo **Esperienza**.

## La Guida presuppone un'esperienza Premium
Tutte le descrizioni delle caratteristiche nella documentazione per [!INCLUDE[prod_short](includes/prod_short.md)] presuppongono l'esperienza **Premium**, ovvero le descrizioni riguardano l'intero ambito degli elementi dell'interfaccia utente.

## Vedere anche
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Personalizzazione di Business Central](ui-customizing-overview.md)  
[Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md)  
[Creazione di nuove società](about-new-company.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Guida alle licenze](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
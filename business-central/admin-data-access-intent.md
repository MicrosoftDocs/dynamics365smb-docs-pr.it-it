---
title: Gestire gli intenti di accesso al database in Business Central | Microsoft Docs
description: Modifica l'intento di accesso al database per report, pagine API e query.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5fe04fc290f10324105d4d9ca01e13166bf2ad8f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773081"
---
# <a name="managing-database-access-intent"></a>Gestione dell'intento di accesso al database 

In qualità di utente con privilegi avanzati o amministratore, puoi modificare l'intento di accesso al database su report, pagine di tipo API e query per migliorare le prestazioni del servizio.

## <a name="overview"></a>Sintesi

[!INCLUDE[prod_short](includes/prod_short.md)] può essere configurata per utilizzare repliche di sola lettura del database primario (lettura-scrittura). L'uso della replica del database riduce il carico sul database primario. In alcuni casi, migliorerà anche le prestazioni durante la visualizzazione dei dati nel client. Le repliche sono utili per oggetti, come report, query e pagine API, che vengono utilizzati solo per visualizzare i dati, non per modificarli.

Quando gli oggetti vengono eseguiti, l'intento di accesso al database determina se utilizzare una replica di sola lettura, se disponibile, o il database primario. Report, pagine API e query sono sviluppati con un intento di accesso al database predefinito (vedere [Proprietà DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

La pagina **Elenco di intenti di accesso al database** consente di ignorare l'intento di accesso al database predefinito per gli oggetti quando vengono eseguiti.

In termini di database, questa funzione è comunemente nota come *scale-out di lettura*. Per ulteriori informazioni sullo scale-out di lettura e sull'intento di accesso ai dati in [!INCLUDE[prod_short](includes/prod_short.md)], vedere [Utilizzo dello scale-out di lettura per prestazioni migliori](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) nella Guida di amministrazione e per sviluppatori di [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-change-the-database-access-intent"></a>Per modificare l'intento di accesso al database

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Elenco di intenti di accesso al database** e quindi scegliere il collegamento correlato.

    La pagina elenca tutti i report, le pagine e le query. La colonna **Intento di accesso** include uno dei seguenti valori:

    |**Impostazione**|**descrizione**|  
    |------------|-------------|  
    |**Default**|Indica che l'oggetto utilizza l'intento di accesso al database predefinito.|
    |**Consenti scrittura**|Imposta l'oggetto per utilizzare il database primario, consentendo all'utente di modificare i dati.|
    |**Sola lettura**|Imposta l'oggetto per utilizzare la replica del database, il che significa che l'utente può solo visualizzare i dati, non modificarli.|

2. Scegliere l'azione **Modifica lista**.

3. Nella pagina **Modifica - Elenco intenti di accesso al database**, modifica il campo **Intento di accesso** per gli oggetti.

    > [!NOTE]
    > Se un oggetto modificabile, come la scheda cliente, è impostato su **Sola lettura**, il database primario verrà comunque utilizzato, indipendentemente dall'intento di accesso, consentendo agli utenti di apportare modifiche normalmente.

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Vedere anche
[Funzionalità aziendale](across-business-functionality.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Preparazione al business](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
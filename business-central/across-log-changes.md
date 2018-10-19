---
title: "Tenere traccia dell'attività dell'utente in un log modifiche| Documenti Microsoft"
description: "È possibile attivare un registro utente in modo da disporre di uno storico di tutte le modifiche apportate ai dati delle tabelle tracciate."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a>Registrazione di modifiche in Business Central
È possibile abilitare il log modifiche in [!INCLUDE[d365fin](includes/d365fin_md.md)] in modo da disporre di uno storico delle attività. Il log è basato sulle modifiche apportate ai dati nelle tabelle che si traccia. Nel log modifiche, i movimenti vengono ordinati cronologicamente e mostrano le modifiche apportate ai campi nelle tabelle specificate. Il log modifiche raccoglie tutte le modifiche apportate alla tabella.  

## <a name="working-with-the-change-log"></a>Utilizzo del log modifiche
Un problema comune in diversi sistemi finanziari è individuare l'origine degli errori e delle modifiche dei dati. Potrebbe trattarsi di un numero di telefono errato del cliente o di una registrazione errata nella contabilità generale. Il log modifiche consente di tenere traccia di tutte le modifiche dirette apportate da un utente ai dati nel database. È necessario specificare cosa si desidera venga registrato per ciascuna tabella e campo, quindi attivare il log modifiche.  

Il log modifiche viene attivato e disattivato nella finestra **Setup log modifiche**. Quando si attiva o disattiva il log modifiche, questa attività viene registrata, in modo da poter visualizzare sempre quale utente ha disattivato o riattivato il log modifiche. Non è possibile disattivare tale funzione.  

Nella finestra **Setup log modifiche** se si sceglie l'azione **Tabelle** è possibile specificare le tabelle di cui si desidera tracciare le modifiche e le modifiche da tracciare. [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene traccia anche di una serie di tabelle di sistema.

Dopo avere impostato e attivato il log modifiche e apportato una modifica ai dati, è possibile visualizzare e filtrare le modifiche nella finestra **Movimenti log modifiche**. Se si desidera rimuovere i movimenti, è possibile farlo nella finestra **Elimina mov. log modifiche**, in cui è possibile impostare filtri in base alle date e all'ora.  

## <a name="see-also"></a>Vedi anche
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Ordinamento](ui-sorting.md)  
[Utilizzo della funzionalità Cerca pagina o report](ui-search.md)  
[Gestione di utenti e autorizzazioni](ui-how-users-permissions.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


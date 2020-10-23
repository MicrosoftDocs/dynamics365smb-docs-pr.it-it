---
title: Visualizzare blocchi di database
description: Informazioni su come visualizzare le informazioni sui blocchi di database direttamente dall'interfaccia client in Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922319"
---
# <a name="viewing-database-locks"></a>Visualizzazione di blocchi di database

Il blocco del database controlla l'accesso da parte di più utenti agli stessi dati contemporaneamente. Per proteggere una transazione dalla modifica degli stessi dati da parte di altre transazioni, la prima transazione blocca i dati. Il blocco rimane fino al termine della transazione.

Agli utenti potrebbe essere impedito di completare le transazioni sui dati bloccati. In genere riceveranno un messaggio che indica la condizione di blocco.

## <a name="to-view-database-locks"></a>Per visualizzare i blocchi di database

Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immetti **Blocchi database**, quindi scegli il collegamento correlato.

La pagina **Blocchi di database** fornisce uno snapshot di tutti i blocchi del database correnti.

Per ulteriori informazioni sul blocco del database, consultare [Monitoraggio dei blocchi del database](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) nella guida per sviluppatori e professionisti IT di Business Central.

## <a name="see-also"></a>Vedere anche

[Monitorare i blocchi del database](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 

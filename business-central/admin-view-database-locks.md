---
title: Visualizzare blocchi di database
description: Informazioni su come visualizzare le informazioni sui blocchi di database del cliente direttamente dall'interfaccia client in Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 0a2561eea331ffbaeb058dee2ee13caf0a82d18c
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143688"
---
# <a name="viewing-database-locks"></a>Visualizzazione di blocchi di database

Il blocco del database controlla l'accesso da parte di più utenti agli stessi dati contemporaneamente. Per proteggere una transazione dalla modifica degli stessi dati da parte di altre transazioni, la prima transazione blocca i dati. Il blocco rimane fino al termine della transazione.

Agli utenti potrebbe essere impedito di completare le transazioni sui dati bloccati. In genere riceveranno un messaggio che indica la condizione di blocco.

## <a name="to-view-database-locks"></a>Per visualizzare i blocchi di database

Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Blocchi database**, quindi scegli il collegamento correlato.

La pagina **Blocchi di database** fornisce uno snapshot di tutti i blocchi del database correnti.

Per ulteriori informazioni sul blocco del database, consultare [Monitoraggio dei blocchi del database](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) nella guida per sviluppatori e professionisti IT di Business Central.

## <a name="see-also"></a>Vedere anche

[Monitorare i blocchi del database](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]
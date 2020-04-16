---
title: Visualizzare blocchi di database
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196384"
---
# <a name="viewing-database-locks"></a>Visualizzazione di blocchi di database

## <a name="about-locks"></a>Informazioni sui blocchi

Il blocco del database controlla l'accesso da parte di più utenti agli stessi dati contemporaneamente. Per proteggere una transazione dalla modifica degli stessi dati da parte di altre transazioni, la prima transazione blocca i dati. Il blocco rimane fino al termine della transazione.

Agli utenti potrebbe essere impedito di completare le transazioni sui dati bloccati. In genere riceveranno un messaggio che indica la condizione di blocco.

## <a name="to-view-database-locks"></a>Per visualizzare i blocchi di database

Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immetti **Blocchi database**, quindi scegli il collegamento correlato.

La pagina **Blocchi di database** fornisce uno snapshot di tutti i blocchi del database correnti.

Per ulteriori informazioni sul blocco del database, consultare [Monitoraggio dei blocchi del database](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) nella guida per sviluppatori e professionisti IT di Business Central.

## <a name="see-also"></a>Vedere anche

[Monitorare i blocchi del database](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 

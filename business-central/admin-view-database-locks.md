---
title: Visualizzare blocchi di database
description: Informazioni su come visualizzare le informazioni sui blocchi di database direttamente dall'interfaccia client in Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b53677ab57d6c48b015bb0dd47ea6e315f8e80c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776918"
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


[!INCLUDE[footer-include](includes/footer-banner.md)]
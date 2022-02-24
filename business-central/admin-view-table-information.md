---
title: Visualizzare Informazioni tabella
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275320"
---
# <a name="viewing-table-information"></a>Visualizzazione di Informazioni tabella

La pagina **Informazioni sulla tabella 8700** fornisce informazioni su tutte le tabelle di sistema e aziendali in una soluzione Business Central. In particolare, la pagina visualizza informazioni sulla quantità di dati contenuta nelle tabelle.

Queste informazioni sono utili per la risoluzione dei problemi di prestazioni, perché consente di vedere la distribuzione delle dimensioni dei dati tra le tabelle.

## <a name="viewing-table-information"></a>Visualizzazione di Informazioni tabella

Per aprire questa pagina, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immettere **Informazioni tabella** e quindi scegliere il collegamento correlato.

La tabella seguente descrive le informazioni fornite per ciascuna tabella:

|Colonna|Descrizione|
|------|-----------|
|Nome società|Nome della società, se presente, a cui appartiene la tabella.|
|Nome tabella|Il nome della tabella.|
|Nr. tabella|L'ID della tabella.|
|No. di record|Il numero totale di record archiviati nella tabella.|
|Dim. record|La dimensione media del record in KB/record. Il valore viene calcolato utilizzando la seguente formula: 1024 (Dimensione)/(N. di record). |

## <a name="see-also"></a>Vedere anche

[Controllo di pagine](across-inspect-page.md)  
[Articoli sulle prestazioni per gli sviluppatori](/dynamics365/business-central/dev-itpro/performance/performance-developer)  

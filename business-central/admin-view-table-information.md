---
title: Visualizzare Informazioni tabella
description: Informazioni su come visualizzare le informazioni sulle tabelle di database direttamente dall'interfaccia client in Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: db1a5ef84d4174b960de6f3e20f7d4e29c8c44c8
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133098"
---
# <a name="viewing-table-information"></a>Visualizzazione di Informazioni tabella

La pagina **Informazioni sulla tabella 8700** fornisce informazioni su tutte le tabelle di sistema e aziendali in una soluzione Business Central. In particolare, la pagina visualizza informazioni sulla quantità di dati contenuta nelle tabelle.

Queste informazioni sono utili per la risoluzione dei problemi di prestazioni, perché consente di vedere la distribuzione delle dimensioni dei dati tra le tabelle.

## <a name="viewing-table-information"></a>Visualizzazione di Informazioni tabella

Per aprire questa pagina, seleziona l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") immetti **Informazioni tabella**, quindi scegli il collegamento correlato.

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


[!INCLUDE[footer-include](includes/footer-banner.md)]
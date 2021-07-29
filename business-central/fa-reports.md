---
title: Report cespiti e analisi
description: Vedi quali report e analisi sono disponibili nella versione standard di Business Central in modo da poter tenere traccia dei tuoi cespiti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543354"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Report cespiti e analisi in Business Central

Per aiutarti a gestire i tuoi cespiti in [!INCLUDE [prod_short](includes/prod_short.md)], report standard e analisi sono integrati. Va oltre i tradizionali vincoli di creazione di report per consentire di progettare in modo efficiente vari tipi di report.  

## <a name="reports"></a>Report

La tabella seguente descrive alcuni dei report cespiti chiave.

| Report | ID oggetto | Descrizione |
|--|--|--|
| **Lista cespiti** | 5601 | Mostra l'elenco dei cespiti e le relative informazioni di configurazione per un determinato registro beni ammortizzabili. |
| **Cespiti - Lista acquisti** | 5608 | Elenca tutte le risorse acquisite in un determinato intervallo di date. Puoi includere anche cespiti creati ma non ancora acquisiti. |
| **Dettagli cespiti** | 5604 | Mostra i movimenti contabili per i cespiti. |
| **Analisi dei cespiti** | 5600 | Un report di analisi in cui è possibile specificare due colonne di data e tre colonne di dati da visualizzare nel report. Ad esempio, per generare un report da utilizzare per la riconciliazione con la contabilità generale, aggiungi le colonne per il costo di acquisizione alla data di fine, l'ammortamento alla data di fine e il valore contabile alla data di fine. Un report verifica potrebbe contenere acquisizioni/saldo periodo, svalutazioni/saldo periodo e rivalutazioni/saldo periodo, quindi ogni modifica al cespite può essere verificata se necessario. Se selezioni il campo **Report budget** e specifichi una data di fine nel futuro, il report calcola l'ammortamento futuro e può fornire stime per l'ammortamento futuro e valori contabili, se hai selezionato quei campi come colonne del report. |
| **Valore previsto cespiti** | 5607 | Mostra gli importi di ammortamento previsti e il valore contabile per un periodo futuro per i cespiti. Il report è utile quando si utilizzano metodi di ammortamento diversi per i cespiti e vuoi, ad esempio, stimare l'ammortamento dell'anno successivo. Utilizza il report per creare gli importi di budget per l'ammortamento selezionando un budget e il campo **Copia in budget C/G**. |
| **Valore contabile cespiti 01** | 5605 | Mostra informazioni dettagliate sul costo di acquisto, sul valore dell'ammortamento e sul valore contabile relativi sia ai cespiti singoli che ai gruppi di cespiti. Ciascuno di questi tre tipi di importo viene calcolato all'inizio e alla fine di un determinato periodo e relativamente al periodo stesso. Se selezioni il campo **Report budget**, il report calcolerà l'ammortamento previsto per il periodo. Immetti un *tipo di gruppo* se si desidera raggruppare i cespiti e stampare i totali del gruppo. Ad esempio, se sono state impostate sei classi di cespiti, per stampare i totali dei gruppi relativi a ciascuno dei codici delle sei classi, seleziona l'opzione *Classe cespite*.|
| **Valore contabile cespiti 02** | 5606 |Mostra la ripartizione del valore contabile del cespite per modifiche di acquisizione, deprezzamento e rivalutazione nel periodo con un'ulteriore ripartizione per aggiunte e cessioni nel periodo. Utilizza questo report per descrivere le modifiche ai cespiti per un determinato periodo quando si verificano molti cambiamenti diversi nel raggruppamento dei cespiti. Se selezioni il campo **Report budget**, il report calcolerà l'ammortamento previsto per il periodo. Immetti un *tipo di gruppo* se si desidera raggruppare i cespiti e stampare i totali del gruppo. Ad esempio, se sono state impostate sei classi di cespiti, per stampare i totali dei gruppi relativi a ciascuno dei codici delle sei classi, seleziona l'opzione *Classe cespite*. |
| **Analisi C/G cespiti**| 5610 |Mostra un'analisi dei cespiti che comprende diversi tipi di dati relativi sia a cespiti singoli che a gruppi di cespiti. Se vuoi includere nel report solo determinati cespiti, imposta filtri nella Scheda dettaglio Cespiti. Nella Scheda dettaglio Opzioni, personalizza il report in base alle tue esigenze specifiche. Il report è simile al report **Analisi dei cespiti** ma specificamente per la riconciliazione con la contabilità generale e specificamente per la convalida dei movimenti di cessione. Il report presuppone che si conoscano i conti C/G specificati nell'impostazione della registrazione. |
| **Registro cespiti** |5603  |Mostra i movimenti contabili dei cespiti registrati e suddivisi per numero di registro. Impostando i filtri è possibile specificare quali movimenti di registro vengano visualizzati. Impostare i filtri è importante al fine di evitare la visualizzazione di informazioni eccessive. |

## <a name="see-also"></a>Vedere anche

[Analisi dei rendiconti finanziari in Microsoft Excel](finance-analyze-excel.md)  
[Utilizzo delle dimensioni](finance-dimensions.md)  
[Gestione dei cespiti](fa-manage.md)  
[Panoramica delle funzionalità locali](about-localization.md)  
[Esperienze di contabile in [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

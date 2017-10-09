---
title: Pianificazione approvvigionamento | Microsoft Docs
description: Preparare un piano eseguibile dettagliato e la pianificazione della produzione di assemblaggio finale per la domanda di vendita e di produzione.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b2a4a682100b0963b540f6f032c4b90061265cc1
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="planning"></a>Pianificazione
A seconda del volume e della natura dei prodotti, è necessario pianificare quotidianamente o settimanalmente le operazioni di produzione richieste per trasformare gli input in prodotti finiti. In [!INCLUDE[d365fin](includes/d365fin_md.md)] sono disponibili funzionalità per gestire la domanda anticipata ed effettiva dei reparti vendite, assemblaggio e produzione, nonché funzionalità per la pianificazione della distribuzione tramite unità di stockkeeping e trasferimenti di ubicazione.

> [!NOTE]
> Questo argomento descrive principalmente la pianificazione per le società coinvolte nella gestione della produzione o dell'assemblaggio dove gli ordini di approvvigionamento risultanti possono essere ordini di produzione, assemblaggio, trasferimento o acquisto. L'interfaccia principale per questo lavoro di pianificazione è la finestra **Prospetto pianificazione**.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta inoltre anche la pianificazione degli approvvigionamenti per le società di vendita all'ingrosso dove gli ordini di approvvigionamento risultanti possono essere soltanto ordini di trasferimento e di acquisto. L'interfaccia principale per questo lavoro di pianificazione è la finestra **Richiesta di approvvigionamento**, descritta indirettamente in questo argomento in quanto la funzionalità di pianificazione è in larga parte applicabile a entrambi i prospetti.

Prima di pianificare ed eseguire gli ordini di produzione, è necessario configurare le capacità di produzione, ad esempio la creazione di calendari del reparto produzione, cicli, DB di produzione e centri di lavoro. Per ulteriori informazioni, vedere [Impostazione della produzione](production-configure-production-processes.md).

La pianificazione può essere considerata come gli ordini di approvvigionamento necessari alle preparazione nei reparti di produzione o di assemblaggio per soddisfare la domanda. Per ulteriori informazioni, vedere [Gestione assemblaggio](assembly-assemble-items.md) e [Manufacturing](production-manage-manufacturing.md).

Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Ottenere una breve introduzione su come utilizzare il sistema di pianificazione per individuare la domanda e assegnarvi una priorità, nonché definire un piano di approvvigionamento bilanciato.|[Informazioni sulla funzionalità di pianificazione](production-about-planning-functionality.md)|
|Comprendere tutti gli aspetti del sistema di pianificazione e come modificare gli algoritmi per soddisfare i requisiti di pianificazione in vari ambienti.|[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)|
|Sapere in che modo nella logica di pianificazione viene fatta distinzione tra domanda nelle ubicazioni in base all'impostazione della USK e domanda senza codici ubicazione.|[Pianificazione con o senza ubicazioni](production-planning-with-without-locations.md)|
|Prevedere la domanda di produzione illustrata negli ordini di produzione e di vendita previsti.|[Procedura: Creare una previsione di produzione](production-how-to-create-a-forecast.md)|  
|Creare automaticamente ordini di produzione basati su una relazione uno a uno da un ordine di vendita in modo da coprire la domanda esatta prevista da tale riga dell'ordine di vendita.|[Procedura: Creare gli ordini di produzione dagli ordini di vendita](production-how-to-create-production-orders-from-sales-orders.md)|
|Creare un ordine di produzione previsto direttamente da un ordine di produzione comprendente più righe e che rappresenta un progetto di produzione.|[Procedura: Pianificare gli ordini di progetto](production-how-to-plan-project-orders.md)|
|Utilizzare la finestra **Pianificazione ordini** per pianificare manualmente la domanda di vendita o di produzione sulla base di un solo livello della DB di produzione alla volta.|[Procedura: Pianificare una nuova domanda ordine per ordine](production-how-to-plan-for-new-demand.md)|
|Utilizzare la finestra **Prospetto pianificazione** per eseguire le opzioni MRP che MPS e creare automaticamente un piano di approvvigionamento di alto livello o dettagliato a tutti i livelli dell'articolo.|[Procedura: Eseguire la pianificazione completa, MPS o MRP](production-how-to-run-mps-and-mrp.md)|
|Eseguire la richiesta di approvvigionamento per creare automaticamente un piano di approvvigionamento dettagliato in modo da coprire la domanda relativa ad articoli il cui rifornimento viene effettuato solo tramite acquisto o trasferimento.|Pagina **Richiesta di approvvigionamento**|  
|Avviare o aggiornare un ordine di produzione sotto forma di operazioni pianificate in modo approssimativo in MPS.|[Procedura: Ripianificare o aggiornare direttamente gli ordini di produzione](production-how-to-replan-refresh-production-orders.md)|
|Ricalcolare i calendari dell'area di produzione o del centro di lavoro in seguito alle modifiche alla pianificazione.|La sezione "Per calcolare un calendario aree di produzione" in [Procedura: Impostare i calendari del reparto produzione](production-how-to-create-work-center-calendars.md)|
|Tenere traccia della richiesta dell'ordine (quantità tracciata), della previsione, dell'ordine di vendita programmato o del parametro di pianificazione (quantità non tracciata) che ha generato la riga di pianificazione in questione.|[Procedura: Tenere traccia delle relazioni tra domanda e approvvigionamento](production-how-track-demand-supply.md)|
|Visualizzare le scorte disponibili previste di un articolo in modi diversi e sapere quali fattori, tra domanda lorda, carico ordini pianificati e di altro tipo, influiscono nel tempo sulla giacenza.|[Procedura: Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)|  
|Eseguire le attività di pianificazione selezionate, come la modifica o aggiunta di riga del prospetto di pianificazione, in una visualizzazione grafica del piano di approvvigionamento.|[Procedura: Modificare i suggerimenti di pianificazione in una visualizzazione grafica](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Vedi anche
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


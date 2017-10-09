---
title: "Dettagli di progettazione: Progettazione tracciabilità articolo | Microsoft Docs"
description: "Questo argomento descrive la progettazione alla base della tracciabilità articolo in [! INCLUDA] [d365fin (includes/d365fin_md.md])."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1d47b646b1908987648ebe13f53693f6782f6cdf
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-design"></a>Dettagli di progettazione: Progettazione tracciabilità articolo
Nella prima versione della funzionalità di tracciabilità articolo in [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60, i numeri seriali o di lotto venivano registrati direttamente nei movimenti contabili articoli. Questa progettazione forniva informazioni complete sulla disponibilità e sulla tracciabilità semplice dei movimenti storici, ma mancava di flessibilità e funzionalità.  

Da [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00, la funzione di tracciabilità articolo rientra in una struttura oggetto separata con collegamenti complessi ai documenti registrati e i movimenti contabili articoli. Questa progettazione era flessibile e piena di funzionalità, ma i movimenti di tracciabilità articolo non erano inclusi completamente nei calcoli della disponibilità.  

Da [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 la funzione di tracciabilità articolo è integrata con il sistema di impegno, che gestisce l'impegno, la tracciabilità ordine e la messaggistica di azione. Per ulteriori informazioni, vedere “Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni" in "Dettagli progettazione: Pianificazione degli approvvigionamenti".  

Quest'ultima progettazione incorpora i movimenti di tracciabilità articolo nei calcoli della disponibilità totale in tutto il sistema, inclusa la pianificazione, la produzione e il warehouse. Il vecchio concetto di inserire i numeri seriali e di lotto nei movimenti contabili articoli viene reintrodotto per garantire il semplice accesso ai dati storici a scopo di tracciabilità. In relazione ai miglioramenti di tracciabilità articolo in [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60, il sistema di impegno è stato esteso alle entità della rete diverse dagli ordini, ad esempio le registrazioni, le fatture e le note di credito.  

Con l'aggiunta dei numeri seriali o di lotto, gli attributi permanenti dell'articolo vengono gestiti dal sistema di impegno contemporaneamente alla gestione dei collegamenti intermittenti tra approvvigionamento e domanda sotto forma di movimenti di tracciabilità ordini e di movimenti impegni. Un'altra caratteristica diversa dei numeri seriali o di lotto confrontati ai dati di impegno convenzionali è il fatto che possono essere registrati, parzialmente o completamente. Di conseguenza, la tabella **Movimenti impegni** (T337) utilizza ora una tabella correlata denominata **Specifica tracciabilità** (T336) che gestisce e visualizza le somme delle quantità di tracciabilità articolo registrate e attive. Per ulteriori informazioni, vedere [Dettagli di progettazione: Movimenti di tracciabilità articolo storici e attivi](design-details-active-versus-historic-item-tracking-entries.md).  

Nel diagramma seguente viene descritta la progettazione della funzionalità di tracciabilità articolo in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

![Progettazione tracciabilità articolo](media/design_details_item_tracking_design.png "design_details_item_tracking_design")  

L'oggetto di registrazione centrale è riprogettato per gestire la sottoclassificazione univoca di una riga di documento sotto forma di numero seriale o di numeri di lotto. Speciali tabelle di relazione vengono aggiunte per creare relazioni uno a molti tra i documenti registrati e i relativi movimenti contabili articoli e movimenti contabili di valorizzazione.  

Codeunit 22, **Reg. magazzino - registra righe**, ora suddivide la registrazione in base ai numeri di tracciabilità articolo specificati nella riga del documento. Ciascun numero di tracciabilità articolo sulla riga crea il proprio movimento contabile articolo per l'articolo. Ciò significa che il collegamento dalla riga del documento registrato ai movimenti contabili articoli associati è una relazione uno a molti. Tale relazione viene gestita dalle seguenti tabelle di relazione di tracciabilità articolo.  

|Campo|Description|  
|---------------|---------------------------------------|  
|**Relazione movimento articolo** (T6507)|Correla la righe spedite o ricevute ai movimenti contabili articoli|  
|**Relazione movimento valorizz.** (T6508)|Correla le righe fatturate ai movimenti di valorizzazione|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Struttura di registrazione di tracciabilità articolo](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)


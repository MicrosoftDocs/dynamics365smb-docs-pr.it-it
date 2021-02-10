---
title: 'Dettagli di progettazione: Progettazione tracciabilità articolo | Microsoft Docs'
description: Questo argomento descrive la progettazione alla base della tracciabilità articolo in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87c85de9f501e093679512b709841d0027fe17bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751332"
---
# <a name="design-details-item-tracking-design"></a>Dettagli di progettazione: Progettazione tracciabilità articolo
Nella prima versione della funzionalità di tracciabilità articolo in [!INCLUDE[prod_short](includes/prod_short.md)] 2.60, i numeri seriali o di lotto venivano registrati direttamente nei movimenti contabili articoli. Questa progettazione forniva informazioni complete sulla disponibilità e sulla tracciabilità semplice dei movimenti storici, ma mancava di flessibilità e funzionalità.  

Da [!INCLUDE[prod_short](includes/prod_short.md)] 3.00, la funzione di tracciabilità articolo rientra in una struttura oggetto separata con collegamenti complessi ai documenti registrati e i movimenti contabili articoli. Questa progettazione era flessibile e piena di funzionalità, ma i movimenti di tracciabilità articolo non erano inclusi completamente nei calcoli della disponibilità.  

Da [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 la funzione di tracciabilità articolo è integrata con il sistema di impegno, che gestisce l'impegno, la tracciabilità ordine e la messaggistica di azione. Per ulteriori informazioni, vedere “Dettagli di progettazione: Impegno, tracciabilità dell'ordine e messaggistica di azioni" in "Dettagli progettazione: Pianificazione degli approvvigionamenti".  

Quest'ultima progettazione incorpora i movimenti di tracciabilità articolo nei calcoli della disponibilità totale in tutto il sistema, inclusa la pianificazione, la produzione e il warehouse. Il vecchio concetto di inserire i numeri seriali e di lotto nei movimenti contabili articoli viene reintrodotto per garantire il semplice accesso ai dati storici a scopo di tracciabilità. In relazione ai miglioramenti di tracciabilità articolo in [!INCLUDE[prod_short](includes/prod_short.md)] 3.60, il sistema di impegno è stato esteso alle entità della rete diverse dagli ordini, ad esempio le registrazioni, le fatture e le note di credito.  

Con l'aggiunta dei numeri seriali o di lotto, gli attributi permanenti dell'articolo vengono gestiti dal sistema di impegno contemporaneamente alla gestione dei collegamenti intermittenti tra approvvigionamento e domanda sotto forma di movimenti di tracciabilità ordini e di movimenti impegni. Un'altra caratteristica diversa dei numeri seriali o di lotto confrontati ai dati di impegno convenzionali è il fatto che possono essere registrati, parzialmente o completamente. Di conseguenza, la tabella **Movimenti impegni** (T337) utilizza ora una tabella correlata denominata **Specifica tracciabilità** (T336) che gestisce e visualizza le somme delle quantità di tracciabilità articolo registrate e attive. Per ulteriori informazioni, vedere [Dettagli di progettazione: Movimenti di tracciabilità articolo storici e attivi](design-details-active-versus-historic-item-tracking-entries.md).  

Nel diagramma seguente viene descritta la progettazione della funzionalità di tracciabilità articolo in [!INCLUDE[prod_short](includes/prod_short.md)].  

![Esempio di flusso di tracciabilità articolo](media/design_details_item_tracking_design.png "Esempio di flusso di tracciabilità articolo")  

L'oggetto di registrazione centrale è riprogettato per gestire la sottoclassificazione univoca di una riga di documento sotto forma di numero seriale o di numeri di lotto. Speciali tabelle di relazione vengono aggiunte per creare relazioni uno a molti tra i documenti registrati e i relativi movimenti contabili articoli e movimenti contabili di valorizzazione.  

Codeunit 22, **Reg. magazzino - registra righe**, ora suddivide la registrazione in base ai numeri di tracciabilità articolo specificati nella riga del documento. Ciascun numero di tracciabilità articolo sulla riga crea il proprio movimento contabile articolo per l'articolo. Ciò significa che il collegamento dalla riga del documento registrato ai movimenti contabili articoli associati è una relazione uno a molti. Tale relazione viene gestita dalle seguenti tabelle di relazione di tracciabilità articolo.  

|Campo|Descrizione|  
|---------------|---------------------------------------|  
|**Relazione movimento articolo** (T6507)|Correla la righe spedite o ricevute ai movimenti contabili articoli|  
|**Relazione movimento valorizz.** (T6508)|Correla le righe fatturate ai movimenti di valorizzazione|  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Struttura di registrazione di tracciabilità articolo](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Vedere anche  
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)

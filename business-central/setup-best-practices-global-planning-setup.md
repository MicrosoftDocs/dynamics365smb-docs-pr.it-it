---
title: Impostare le procedure ottimali per il setup di pianificazione globale | Microsoft Docs
description: La Scheda dettaglio Pianificazione della pagina Setup manufacturing contiene vari campi che definiscono le regole globali per la pianificazione forniture.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 69c7ea885cd9c89619dd87b209de2e139d6ef50e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912898"
---
# <a name="setup-best-practices-global-planning-setup"></a>Impostare le procedure ottimali: Setup di pianificazione globale
La Scheda dettaglio **Pianificazione** della pagina **Setup manufacturing** contiene vari campi che definiscono le regole globali per la pianificazione forniture.  

 Nella seguente tabella vengono fornite le procedure consigliate sulla modalità di impostazione dei campi dei parametri di pianificazione globali selezionati. Per ulteriori informazioni su un campo, scegliere il collegamento nella colonna **Campo setup**.  

|Campo Setup|Procedura consigliata|Commento|  
|-----------------|-------------------|-------------|  
|Usa previsioni per le ubicazioni|Selezionare se vi sono previsioni per ubicazioni specifiche.||  
|Componenti nell'ubicazione|Se gli articoli non sono definiti come unità di stockkeeping, selezionare il codice ubicazione della warehouse principale.|Ciò è valido anche se si utilizza solo la richiesta di approvvigionamento.|  
|Livello di overflow vuoto|Selezionare **Consenti calcolo di default** se si sta migrando da Microsoft Dynamics NAV 5.0 o versione precedente.|Utilizzare solo se si desidera consentire a tutti o alcuni articoli di eseguire l'overflow del punto di riordino.|  
|Periodo di stabilizzazione di default|Impostare un valore compreso tra 1D e 5D.<br /><br /> Se non si è esperti della pianificazione in [!INCLUDE[d365fin](includes/d365fin_md.md)], impostare un periodo più lungo.|Quando gli utenti sono più esperti sui diversi motivi dei messaggi di azione, abbreviare il periodo di stabilizzazione per consentire più suggerimenti di modifica.|  
|Percentuale quantità di smorzamento di default|Impostare tra il 5 e il 20 percento della dimensione del lotto dell'articolo.||  

## <a name="see-also"></a>Vedere anche  
 [Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
 [Impostare aree di applicazione complesse utilizzando le procedure ottimali](set-up-complex-application-areas-using-best-practices.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

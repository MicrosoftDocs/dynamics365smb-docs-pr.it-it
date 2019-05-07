---
title: Definizione dei centri di costo e degli oggetti di costo per il piano dei conti | Microsoft Docs
description: È possibile trasferire automaticamente i movimenti delle entrate e delle spese della contabilità generale alla contabilità industriale per ogni registrazione di contabilità generale o tramite un processo batch. Durante il trasferimento, il sistema trasferisce solo i movimenti che sono già stati collegati a un centro di costo o a un oggetto di costo. Per stabilire un trasferimento significativo, è necessario assicurarsi che i centri di costo e gli oggetti di costi siano correttamente definiti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "923324"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definizione dei centri di costo e degli oggetti di costo per il piano dei conti
È possibile trasferire automaticamente i movimenti delle entrate e delle spese della contabilità generale alla contabilità industriale per ogni registrazione di contabilità generale o tramite un processo batch. Durante il trasferimento, con [!INCLUDE[d365fin](includes/d365fin_md.md)] è possibile trasferire solo i movimenti che sono già stati collegati a un centro di costo o a un oggetto di costo. Per stabilire un trasferimento significativo, è necessario assicurarsi che i centri di costo e gli oggetti di costi siano correttamente definiti.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definizione dei valori dimensioni di default per i conti di contabilità generale  
Per ogni conto di contabilità generale, è possibile definire i valori dimensioni di default nella tabella **Dimensione di default**. Nell'esempio seguente viene illustrato come sia sempre necessaria la presenza di un centro di costo REPARTO e mai quella di un oggetto di costo PROGETTO quando si effettua una registrazione in un conto di contabilità generale.  

|**Codice dimensione**|**Registrazione valore**|  
|------------------------------------------|-----------------------------------------|  
|Reparto|Codice obbligatorio|  
|Progetto|Nessun Cod.|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definizione dei valori dimensioni per i costi generali e diretti  
 È possibile trasferire i costi generali a un centro di costo e i costi diretti a un oggetto di costo. Nella tabella seguente viene mostrata la combinazione ottimale dei valori di impostazione delle dimensioni.  

|Trasferisci a|Registrazione del centro di costo|Registrazione dell'oggetto di costo|  
|-----------------|-------------------------|-------------------------|  
|Centro di costo|Codice obbligatorio|Nessun Cod.|  
|Oggetto di costo|Nessun Cod.|Codice obbligatorio|  

> [!NOTE]  
>  Per garantire che il centro di costo e l'oggetto di costo predefiniti impostati nella contabilità generale vengano riportati automaticamente nella contabilità industriale, selezionare la casella di controllo **Verifica registrazioni CG** nella pagina Setup contabilità industriale.  

## <a name="see-also"></a>Vedi anche  
[Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
[Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

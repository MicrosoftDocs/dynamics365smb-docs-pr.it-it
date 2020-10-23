---
title: Aggiornamento di un'integrazione con Dynamics 365 Sales
description: Informazioni su come passare l'integrazione di Dynamics 365 Business Central con Dynamics 365 Sales alla versione più recente.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3bb6b26e011afc515fbd4f492f56b3090c56e860
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922369"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Aggiornamento di un'integrazione con Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] si integra con [!INCLUDE[d365fin](includes/cds_long_md.md)], che semplifica la connessione e la sincronizzazione dei dati con altre applicazioni di Dynamics 365, come [!INCLUDE[crm_md](includes/crm_md.md)] o anche le app che crei autonomamente. Se stai effettuando l'integrazione per la prima volta, ti consigliamo di farlo tramite [!INCLUDE[d365fin](includes/cds_long_md.md)]. Per ulteriori informazioni, vedi [Integrazione con Common Data Service](admin-common-data-service.md).

Se hai già integrato [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puoi continuare a sincronizzare i dati utilizzando la tua configurazione. Tuttavia, se aggiorni [!INCLUDE[d365fin](includes/d365fin_md.md)] o disattivi la tua integrazione [!INCLUDE[crm_md](includes/crm_md.md)], per riattivarla devi connetterti tramite [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> La riconnessione tramite [!INCLUDE[d365fin](includes/cds_long_md.md)] applicherà le impostazioni di sincronizzazione predefinite e sovrascriverà tutte le configurazioni a tua disposizione. Ad esempio, verranno applicati i mapping di tabella predefiniti.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Per aggiornare la connessione per utilizzare Common Data Service
1. Apri la pagina **Configurazione connessione Microsoft Dynamics 365**, scegli l'opzione **Abilita** per disattivare la connessione esistente a [!INCLUDE[crm_md](includes/crm_md.md)].
2. Apri la pagina **Configurazione connessione Common Data Service** e scegli l'opzione **Abilita** per attivare la connessione.
  
   Dopo aver abilitato la connessione CDS, viene distribuita la soluzione di integrazione di base CDS di Business Central a Common Data Service.
3. Disinstallare la soluzione di integrazione Microsoft Dynamics 365 Business Central da Dynamics 365 Sales. Per ulteriori informazioni, vedere [Disinstallare o eliminare un argomento della soluzione](/powerapps/developer/common-data-service/uninstall-delete-solution). 

4. Nella pagina **Configurazione connessione Microsoft Dynamics 365** attivare l'interruttore **Abilita** per connettersi a [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Dopo aver abilitato la connessione a Sales, viene distribuita la soluzione di integrazione di Business Central a Sales. Ciò consente l'integrazione con entità specifiche di [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio ordini di vendita, offerte e fatture.
5. Nella pagina **Impostazione della connessione di vendita**, scegli **Usa impostazione di sincronizzazione predefinita** per inizializzare i mapping della tabella di integrazione per [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Vedere anche
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrazione con Common Data Service](admin-common-data-service.md)

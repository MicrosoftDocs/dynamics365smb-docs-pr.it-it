---
title: Aggiornamento di un'integrazione con Dynamics 365 Sales | Microsoft Docs
description: Informazioni su come prepararsi all'integrazione di Dynamics 365 Business Central con Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 95098397bd9554be6c993b6107963eba9a99c067
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196874"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Aggiornamento di un'integrazione con Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] si integra anche con [!INCLUDE[d365fin](includes/cds_long_md.md)], che semplifica la connessione e la sincronizzazione dei dati con altre applicazioni di Dynamics 365, come [!INCLUDE[crm_md](includes/crm_md.md)] o anche le app che crei autonomamente. Se stai effettuando l'integrazione per la prima volta, ti consigliamo di farlo tramite [!INCLUDE[d365fin](includes/cds_long_md.md)]. Per ulteriori informazioni, vedi [Integrazione con Common Data Service](admin-common-data-service.md).

Se hai già integrato [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puoi continuare a sincronizzare i dati utilizzando la tua configurazione. Tuttavia, se aggiorni [!INCLUDE[d365fin](includes/d365fin_md.md)] o disattivi la tua integrazione [!INCLUDE[crm_md](includes/crm_md.md)], per riattivarla devi connetterti tramite [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> La riconnessione tramite [!INCLUDE[d365fin](includes/cds_long_md.md)] applicherà le impostazioni di sincronizzazione predefinite e sovrascriverà tutte le configurazioni a tua disposizione. Ad esempio, verranno applicati i mapping di tabella predefiniti.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Per aggiornare la connessione per utilizzare Common Data Service
1. Apri la pagina **Configurazione connessione Microsoft Dynamics 365**, scegli l'opzione **Abilita** per disattivare la connessione esistente a [!INCLUDE[crm_md](includes/crm_md.md)].
2. Apri la pagina **Configurazione connessione Common Data Service** e scegli l'opzione **Abilita** per attivare la connessione.
3. Dopo aver abilitato la connessione CDS, viene distribuita la soluzione di integrazione di base CDS di Business Central a Common Data Service.
4. Nella pagina Configurazione connessione Microsoft Dynamics 365 scegli l'opzione Abilita per attivare la connessione a [!INCLUDE[crm_md](includes/crm_md.md)].
5. Dopo aver abilitato la connessione a Sales, viene distribuita la soluzione di integrazione di Business Central a Sales. Ciò consente l'integrazione con entità specifiche di [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio ordini di vendita, offerte e fatture.
6. Nella pagina **Impostazione della connessione di vendita**, scegli **Usa impostazione di sincronizzazione predefinita** per inizializzare i mapping della tabella di integrazione per [!INCLUDE[crm_md](includes/crm_md.md)].
7. Ora scegli **Ridistribuzione soluzione di integrazione** per installare e configurare la soluzione di integrazione di Business Central aggiornata.

## <a name="see-also"></a>Vedere anche
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrazione con Common Data Service](admin-common-data-service.md)
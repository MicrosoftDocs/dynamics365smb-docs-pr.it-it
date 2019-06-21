---
title: Utilizzare i dati per creare un'app| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un'app aziendale utilizzando PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540271"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Collegamento ai dati Business Central per creare un'app aziendale utilizzando PowerApps
È possibile rendere disponibili i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps.  

> [!NOTE]  
>   È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps
1. Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), quindi accedere.
2. Nella home page, scegliere il modello **Inizia dai dati** per creare una nuova app canvas. Questa app verrà progettata per l'uso su un dispositivo mobile, ma è anche possibile scegliere di utilizzare un altro modello.

    Il passaggio successivo per creare una PowerApp è selezionare i dati. Scegliere l'icona della freccia, quindi scegliere l'opzione **Nuova connessione** nella parte in alto a sinistra della pagina.
3. Nell'elenco delle connessioni disponibili, scegliere **Business Central**, quindi scegliere il pulsante **Crea**.

    PowerApps verrà collegato a [!INCLUDE [prodshort](includes/prodshort.md)] utilizzando le credenziali di accesso. Se non si è un amministratore di [!INCLUDE [prodshort](includes/prodshort.md)], è possibile che sia necessario eseguire l'accesso con un altro account.  

4. Se si dispone di più società in [!INCLUDE [prodshort](includes/prodshort.md)], è necessario scegliere quella à cui connettersi. Successivamente, PowerApps visualizza un elenco di *tabelle* disponibili in [!INCLUDE [prodshort](includes/prodshort.md)]. Queste cosiddette tabelle fanno parte dell'API [!INCLUDE [prodshort](includes/prodshort.md)]. Non è necessario configurare personalmente i punti finali in quanto questa operazione viene eseguita dal connettore [!INCLUDE [prodshort](includes/prodshort.md)] per PowerApps.  

    Se si desidera includere dati di altre tabelle in [!INCLUDE [prodshort](includes/prodshort.md)] nell'app, è necessario lavorare con un sviluppatore per definire un API personalizzata in [!INCLUDE [prodshort](includes/prodshort.md)] e quindi utilizzare tale API mediante un connettore personalizzato in PowerApps. Per ulteriori informazioni, vedere [Creare un connettore personalizzato da zero](/connectors/custom-connectors/define-blank).  

A questo punto, si è eseguita la connessione ai dati di [!INCLUDE [prodshort](includes/prodshort.md)] e si è pronti per iniziare a creare PowerApp. È possibile aggiungere ulteriori schermi ed eseguire la connessione a ulteriori dati di [!INCLUDE [prodshort](includes/prodshort.md)]. Per ulteriori informazioni, vedere [Creare un'app canvas da un modello in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Dopo avere pianificato e creato l'app, è possibile condividerla con i colleghi. Per ulteriori informazioni, vedere [Salvare e pubblicare un'app canvas in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Se si desidera eseguire la connessione a [!INCLUDE [prodshort](includes/prodshort.md)] in locale, è necessario scegliere il connettore **Business Central (locale)** nel passaggio 3.  

## <a name="see-also"></a>Vedere anche

[Creare un'app canvas da un modello in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  
[Introduzione](product-get-started.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanze](finance.md)  
[Introduzione allo sviluppo di app di connessione per Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

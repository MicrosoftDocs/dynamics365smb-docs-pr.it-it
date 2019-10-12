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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305027"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Collegamento ai dati Business Central per creare un'app aziendale utilizzando PowerApps
È possibile rendere disponibili i dati di [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps.  

> [!NOTE]  
>   È necessario disporre di un account valido con [!INCLUDE[d365fin](includes/d365fin_md.md)] e con PowerApps.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>Per aggiungere [!INCLUDE[d365fin](includes/d365fin_md.md)] come origine dati in PowerApps
1. Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), quindi accedere.
2. Nella home page, scegliere **App**, **Crea un'app** e **Canvas** per creare una nuova app canvas. Questa app verrà progettata per l'uso su un dispositivo mobile, ma è anche possibile scegliere di utilizzare un altro modello.

    Il passaggio successivo per creare una PowerApp è selezionare i dati. Scegliere l'icona della freccia, quindi scegliere l'opzione **Nuova connessione** nella parte in alto a sinistra della pagina.
3. Nell'elenco delle connessioni disponibili, scegliere **Business Central**, quindi scegliere il pulsante **Crea**.

    PowerApps verrà collegato a [!INCLUDE [prodshort](includes/prodshort.md)] utilizzando le credenziali di accesso. Se non si è un amministratore di [!INCLUDE [prodshort](includes/prodshort.md)], è possibile che sia necessario eseguire l'accesso con un altro account.  

4.  In PowerApps verrà visualizzato un elenco di *Ambienti e società* disponibili tramite [!INCLUDE [prodshort](includes/prodshort.md)]. Scegliere l'ambiente e l'azienda che contiene i dati a cui si intende connettersi. Successivamente, verrà visualizzato un elenco di API. Selezionare l'**API** a cui connettersi.

Queste cosiddette tabelle fanno parte dell'API [!INCLUDE [prodshort](includes/prodshort.md)]. Non è necessario configurare personalmente i punti finali in quanto questa operazione viene eseguita dal connettore [!INCLUDE [prodshort](includes/prodshort.md)] per PowerApps.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

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

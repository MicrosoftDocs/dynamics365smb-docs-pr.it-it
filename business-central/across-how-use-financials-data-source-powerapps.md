---
title: Utilizzare i dati per creare un'app| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un'app aziendale utilizzando Power Apps.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2021
ms.author: edupont
---
# Collegamento ai dati Business Central per creare un'app aziendale utilizzando Power Apps

È possibile rendere disponibili i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Apps.  

> [!NOTE]  
> È necessario disporre di un account valido con [!INCLUDE[prod_short](includes/prod_short.md)] e con Power Apps.  

## Per aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Apps

1. Nel browser passare a [powerapps.microsoft.com](https://powerapps.microsoft.com/), quindi accedere.
2. Nella home page, nella sezione **Inizia dai dati** scegliere il riquadro **Altre origini dati**.  

    Viene aperto Power Apps Studio. Al primo accesso, è necessario specificare il paese/area geografica.  
3. Nell'elenco delle connessioni disponibili, scegliere **Business Central**, quindi scegliere il pulsante **Crea**.

    Power Apps verrà collegato a [!INCLUDE[prod_short](includes/prod_short.md)] utilizzando le credenziali di accesso. Se non si è un amministratore di [!INCLUDE[prod_short](includes/prod_short.md)], è possibile che sia necessario eseguire l'accesso con un altro account.  

4. In Power Apps verrà visualizzato un elenco di *Ambienti e società* disponibili tramite [!INCLUDE[prod_short](includes/prod_short.md)]. Scegliere l'ambiente e l'azienda che contiene i dati a cui si intende connettersi, ad esempio *PRODUCTION - My Company*.  

5. Successivamente, verrà visualizzato un elenco di tabelle che sono esposte come parte dell'API per l'ambiente. Selezionare la tabella a cui connettersi quindi scegliere **Connetti**.

Queste cosiddette tabelle sono esposte come endpoint dal connettore [!INCLUDE[prod_short](includes/prod_short.md)] per Power Apps.  

> [!NOTE]
> Se si desidera includere dati di altre tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] nell'app, è necessario lavorare con un sviluppatore per definire un API personalizzata in [!INCLUDE[prod_short](includes/prod_short.md)] e quindi utilizzare tale API mediante un connettore personalizzato in Power Apps. Per ulteriori informazioni, vedere [Creare un connettore personalizzato da zero](/connectors/custom-connectors/define-blank).  

A questo punto, si è eseguita la connessione ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] e si è pronti per iniziare a creare PowerApp. È possibile aggiungere ulteriori schermi ed eseguire la connessione a ulteriori dati di [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Creare un'app canvas da un esempio in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Dopo avere pianificato e creato l'app, è possibile condividerla con i colleghi. Per ulteriori informazioni, vedere [Salvare e pubblicare un'app canvas in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Se si desidera eseguire la connessione a [!INCLUDE[prod_short](includes/prod_short.md)] in locale, è necessario scegliere il connettore **Business Central (locale)** nel passaggio 3.  

## Vedi il relativo [training Microsoft](/training/paths/power-apps-power-automate-business-central/)

## Vedere anche

[Creare un'app canvas da un modello in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introduzione allo sviluppo di app di connessione per Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

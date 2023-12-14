---
title: Utilizzare i dati per creare un'app| Documenti Microsoft
description: È possibile rendere disponibili i dati di Business Central come origine dati e specificare un URL OData dei service Web per creare un'app aziendale utilizzando Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# Collegamento ai dati Business Central per creare un'app aziendale utilizzando Power Apps

È possibile rendere disponibili i dati di [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Apps.  

> [!TIP]  
> Business Central ora offre supporto per lo sviluppo e le operazioni per Power Platform in AL-Go e campioni per iniziare a creare le tue app con Power Apps. Queste funzionalità sono attualmente in anteprima. Per ulteriori informazioni, vai a [Business Central e Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) nella guida per sviluppatori e professionisti IT.

## Prerequisiti

È necessario disporre di un account valido con [!INCLUDE[prod_short](includes/prod_short.md)] e con Power Apps.  

## Aggiungere [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati in Power Apps

Questi passaggi aggiungono una tabella di Business Central, come clienti o articoli, come origine dati di un'app Power Apps .

1. Nel browser, vai a [powerapps.microsoft.com](https://powerapps.microsoft.com/), quindi accedi.
2. Nel riquadro di navigazione a sinistra, seleziona **+ Crea**, quindi **Altre origini dati** nella pagina **Crea app**.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. L'elenco **Connessioni** mostra tutte le connessioni dati esistenti.

   - Se è già presente una connessione **Business Central**, selezionala, quindi seleziona **Crea**.

   - Se non vedi una connessione Business Central, seleziona **+ Nuova connessione**, cerca e seleziona **Business Central**, quindi seleziona **Crea**.

   > [!NOTE]
   > Se desideri eseguire la connessione a [!INCLUDE[prod_short](includes/prod_short.md)] in locale, è necessario scegliere il connettore **Business Central (locale)**.  
  
4. Power Apps si connette a [!INCLUDE[prod_short](includes/prod_short.md)]. Accedi usando l'account Business Central con nome utente e password validi. Se non si è un amministratore di [!INCLUDE[prod_short](includes/prod_short.md)], è possibile che sia necessario eseguire l'accesso con un altro account.  
5. Una volta effettuato l'accesso, Power Apps visualizza un elenco di *Ambienti e società* disponibili tramite [!INCLUDE[prod_short](includes/prod_short.md)]. Scegliere l'ambiente e l'azienda che contiene i dati a cui si intende connettersi, ad esempio *PRODUCTION - My Company*.  
6. Successivamente, verrà visualizzato un elenco di tabelle che sono esposte come parte dell'API per l'ambiente. Selezionare la tabella a cui connettersi quindi scegliere **Connetti**.

Queste cosiddette tabelle sono esposte come endpoint dal connettore [!INCLUDE[prod_short](includes/prod_short.md)] per Power Apps.  

> [!NOTE]
> Se si desidera includere dati di altre tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] nell'app, è necessario lavorare con un sviluppatore per definire un API personalizzata in [!INCLUDE[prod_short](includes/prod_short.md)].  

A questo punto, si è eseguita la connessione ai dati di [!INCLUDE[prod_short](includes/prod_short.md)] e si è pronti per iniziare a creare Power App. È sempre possibile aggiungere ulteriori schermi ed eseguire la connessione a ulteriori dati. Per ulteriori informazioni, vedi [Creare un'app canvas da un esempio in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Dopo avere pianificato e creato l'app, è possibile condividerla con i colleghi. Per ulteriori informazioni, vedere [Salvare e pubblicare un'app canvas in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## Vedere anche

[Creare un'app canvas da un modello in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introduzione allo sviluppo di app di connessione per Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Connettersi a Dynamics 365 Sales | Microsoft Docs
description: È possibile eseguire l'integrazione con Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6a23cdf9a13461db92977cc46d7f4fcaa7c715f7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304518"
---
# <a name="set-up-a-connection-to-dynamics-365-sales"></a>Impostare una connessione a Dynamics 365 Sales
Per eseguire l'integrazione con [!INCLUDE[crm_md](includes/crm_md.md)], è necessario impostare una connessione tra [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Operazioni preliminari
Prima di iniziare a connettere le app, è necessario disporre di alcuni informazioni:  

* Un URL per l'app [!INCLUDE[crm_md](includes/crm_md.md)]. Un modo rapido di ottenere l'URL è di aprire [!INCLUDE[crm_md](includes/crm_md.md)] e copiare l'URL e quindi incollarlo nel campo **URL di Dynamics 365 Sales** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] correggerà automaticamente la formattazione.  
* Un nome utente e la password di un account utente utilizzato solo per l'integrazione.  
* Il nome utente e la password dell'account che dispone di autorizzazioni di amministratore.  

> [!Note]
> Tali passaggi descrivono la procedura per la versione online di [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrm_mdincludescrm_mdmd"></a>Impostare, verificare e abilitare una connessione a [!INCLUDE[crm_md](includes/crm_md.md)]  
Per tutti i tipi di autenticazione diversi dall'autenticazione di Office 365, si imposta la connessione a Dynamics 365 Sales nella pagina **Setup connessione a Microsoft Dynamics 365 Sales**. Per l'autenticazione di Office 365, è possibile anche utilizzare la guida al setup assistito **Setup connessione a Dynamics 365 Sales**, che consente di fornire le informazioni necessarie.

### <a name="to-use-an-assisted-setup-guide"></a>Per utilizzare una guida al setup assistito:
La guida al setup assistito **Setup connessione a Dynamics 365 Sales** è utile per impostare la connessione e specificare se abilitare le funzionalità avanzate, ad esempio l'associazione tra record.

1. Scegliere **Setup ed estensioni** quindi **Setup assistito**.
2. Scegliere **Setup connessione a Dynamics 365 Sales** per avviare la guida al setup assistito.
3. Compilare i campi in base alle esigenze.
4. Eventualmente, esistono delle impostazioni avanzate che possono migliorare la sicurezza e abilitare ulteriori funzionalità di [!INCLUDE[crm_md](includes/crm_md.md)], come l'elaborazione degli ordini di vendita e la visualizzazione dei livelli di magazzino. Nella seguente tabella vengono illustrate le impostazioni avanzate.  

|Campo|Descrizione|
|-----|-----|
|**Importa soluzione di Dynamics 365 Sales**|Abilitare questa impostazione per installare e configurare la soluzione di integrazione in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Informazioni sulla soluzione di integrazione di Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Pubblica servizio Web Disponibilità articolo**|Consentire alla persone che utilizzano [!INCLUDE[crm_md](includes/crm_md.md)] di visualizzare la disponibilità degli articoli (prodotti) in magazzino in [!INCLUDE[d365fin](includes/d365fin_md.md)]. A questo proposito, è necessario un account utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] con una chiave di accesso ai servizi Web. L'assegnazione della chiave è un processo in due tappe. Nell'account utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] è necessario scegliere l'azione **Modifica chiave del servizio Web**. Nella guida al setup assistito Setup connessione a Dynamics 365 Sales, è necessario specificare l'URL del servizio Web OData di Dynamics 365 Business Central e fornire le credenziali utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] per l'accesso al servizio. Per ulteriori informazioni, vedere [Servizi Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL servizi Web OData di Dynamics 365 Business Central**|Se si abilita il servizio Web Disponibilità articolo, viene fornito l'URL del service Web OData.|
|**Nome utente servizi Web OData di Dynamics 365 Business Central**|Il nome dell'account utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per recuperare informazioni sulla disponibilità degli articoli in [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante il servizio Web OData.|
|**Chiave di accesso servizi Web OData di Dynamics 365 Business Central**|La chiave di accesso per l'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante il servizio Web OData. La chiave viene assegnato all'utente selezionato nel campo **Nome utente servizi Web OData di Dynamics 365 Business Central**. Per ottenere la chiave, scegliere il pulsante **Cerca valore** accanto al nome utente, scegliere l'utente, scegliere **Gestisci**, e quindi **Modifica**. Nella scheda utente, scegliere **Azioni**, **Autenticazione** e quindi **Modifica chiave del servizio Web**.|
|**Abilita integrazione ordini di vendita**|Quando le persone creano ordini di vendita in [!INCLUDE[crm_md](includes/crm_md.md)] e completano gli ordini in [!INCLUDE[d365fin](includes/d365fin_md.md)], questo integra il processo in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Abilitare l'integrazione dell'elaborazione degli ordini di vendita](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). A questo proposito si forniscono le credenziali per un account utente amministratore in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Gestione di dati di ordini di vendita](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Abilita connessione a Dynamics 365 for Sales**|Abilitare la connessione a [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Versione Dynamics 365 SDK**|Ciò è pertinente solo se si esegue l'integrazione con una versione locale di [!INCLUDE[crm_md](includes/crm_md.md)]. Si tratta del Dynamics 365 software development kit (denominato anche Xrm) utilizzato per connettere [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versione deve essere compatibile con la versione SDK utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)] ed è uguale o più recente della versione utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> La guida al setup assistito **Setup connessione a Dynamics 365 Sales** assegna automaticamente i ruoli di sicurezza **Amministratore di integrazione** e **Utente integrazione** all'account utente utilizzato per l'integrazione.

### <a name="to-create-or-maintain-the-connection-manually"></a>Per creare o gestire la connessione manualmente
La procedura seguente illustra come compilare manualmente i campi nella pagina **Setup connessione a Microsoft Dynamics 365 Sales**. Questa è anche la pagina in cui si gestiscono le impostazioni per l'integrazione.

1. Scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione a Microsoft Dynamics 365** e quindi scegliere il collegamento correlato.
2. Immettere le seguenti informazioni per la connessione da [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)].

|Campo|Descrizione|
|-----|-----|
|**URL di Dynamics 365 Sales**|L'URL per l'istanza di [!INCLUDE[crm_md](includes/crm_md.md)]. Per ottenere l'URL, aprire [!INCLUDE[crm_md](includes/crm_md.md)], copiare l'URL dalla barra degli indirizzi nel browser quindi immettere l'URL nel campo. [!INCLUDE[d365fin](includes/d365fin_md.md)] assicurerà la correttezza del formato.|
|**Nome utente** e **Password**|Le credenziali dell'account utente dedicato per l'integrazione. Per ulteriori informazioni, vedere [Impostazione di account utente per l'integrazione con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Abilitato**|Iniziare a utilizzare l'integrazione. Se non si abilita la connessione subito, le impostazioni di connessione verranno salvate, ma gli utenti non potranno accedere ai dati di [!INCLUDE[crm_md](includes/crm_md.md)] da [!INCLUDE[d365fin](includes/d365fin_md.md)]. È possibile tornare a questa pagina e abilitare la connessione in un secondo momento.  |
|**Versione Dynamics 365 SDK**|Se si esegue l'integrazione con una versione locale di [!INCLUDE[crm_md](includes/crm_md.md)], si tratta del Dynamics 365 software development kit (denominato anche Xrm) utilizzato per connettere [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versione selezionata deve essere compatibile con la versione SDK utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)]. Questa versione è uguale o superiore alla versione utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Se si connette una versione locale di [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] e si intende configurare una connessione a un'istanza di [!INCLUDE[crm_md](includes/crm_md.md)] con un tipo di autenticazione specifico, compilare i campi della Scheda dettaglio **Dettagli tipo di autenticazione**. Per ulteriori informazioni, vedere [Utilizzare stringhe di connessione negli strumenti XRM per la connessione a Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Questo passaggio non è necessario quando si connette una versione online di [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Immettere le seguenti informazioni per la connessione da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Campo|Descrizione|
|-----|-----|
|**URL Dynamics 365 Business Central Web Client**|L'URL dell'istanza di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ciò consente agli utenti di [!INCLUDE[crm_md](includes/crm_md.md)] di aprire record corrispondenti in [!INCLUDE[d365fin](includes/d365fin_md.md)] dai record di [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio un conto o un prodotto. I record di [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono aperti in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Impostare il campo sull'URL dell'istanza di [!INCLUDE[d365fin](includes/d365fin_md.md)] da utilizzare.<br /><br /> Per reimpostare il campo sull'URL predefinito per [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'azione **Reimposta URL client Web**.<br /><br /> Questo campo è pertinente solo se la soluzione di integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] è installata in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Servizio Web Disponibilità articolo abilitato**|Consentire alla persone che utilizzano [!INCLUDE[crm_md](includes/crm_md.md)] di visualizzare la disponibilità degli articoli (prodotti) in magazzino in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se si abilita questa funzionalità, è inoltre necessario fornire un nome utente e una chiave di accesso per [!INCLUDE[crm_md](includes/crm_md.md)] da utilizzare per eseguire una query sul servizio Web OData per la disponibilità degli articoli (prodotti). Per ulteriori informazioni, vedere [Servizi Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL servizi Web OData di Dynamics 365 Business Central**|Se si abilita il servizio Web Disponibilità articolo, viene fornito l'URL del service Web OData.|
|**Nome utente servizi Web OData di Dynamics 365 Business Central**|Il nome dell'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante il servizio Web OData.|
|**Chiave di accesso servizi Web OData di Dynamics 365 Business Central**|La chiave di accesso dell'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante il servizio Web OData. La chiave viene assegnato all'utente selezionato nel campo **Nome utente servizi Web OData di Dynamics 365 Business Central**. Per ottenere la chiave, scegliere il pulsante **Cerca valore** accanto al nome utente, scegliere l'utente, scegliere **Gestisci**, e quindi **Modifica**. Nella scheda utente, scegliere **Azioni**, **Autenticazione** e quindi **Modifica chiave del servizio Web**.|

4. Immettere le impostazioni seguenti per [!INCLUDE[crm_md](includes/crm_md.md)].

|Campo|Descrizione|
|-----|-----|
|**Integrazione ordini di vendita abilitata**|Consentire agli utenti di inviare ordini di vendita e offerte attivate in [!INCLUDE[crm_md](includes/crm_md.md)] e quindi visualizzarli ed elaborarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Questa operazione integra il processo in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Abilitare l'integrazione dell'elaborazione degli ordini di vendita](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Crea automaticamente ordini vendita**|Creare un ordine di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)] quando un utente ne crea e ne invia uno in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Elabora automaticamente offerte di vendita**|Elaborare un'offerta di vendita in [!INCLUDE[d365fin](includes/d365fin_md.md)] quando un utente ne crea e ne attiva una in [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Immettere le impostazioni avanzate seguenti.

|Campo|Descrizione|
|-----|-----|
|**Gli utenti [!INCLUDE[d365fin](includes/d365fin_md.md)] devono essere mappati a quelli di Dynamics 365 Sales**|Specificare se gli account utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] devono avere account utente corrispondenti in [!INCLUDE[crm_md](includes/crm_md.md)]. L'**indirizzo e-mail di autenticazione di Office 365** dell'utente di [!INCLUDE[d365fin](includes/d365fin_md.md)] deve essere uguale all'**indirizzo e-mail principale** dell'utente di [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Se si imposta il valore **Sì**, gli utenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] che non hanno un account utente corrispondente in [!INCLUDE[crm_md](includes/crm_md.md)] non disporranno della funzionalità di integrazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] nell'interfaccia utente. L'accesso ai dati di [!INCLUDE[crm_md](includes/crm_md.md)] direttamente da [!INCLUDE[d365fin](includes/d365fin_md.md)] viene eseguito per conto dell'account utente di [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Se si imposta il valore **No**, tutti gli utenti di [!INCLUDE[d365fin](includes/d365fin_md.md)] disporranno della funzionalità di integrazione di [!INCLUDE[crm_md](includes/crm_md.md)] nell'interfaccia utente. L'accesso ai dati di [!INCLUDE[crm_md](includes/crm_md.md)] viene eseguito per conto dell'utente di connessione (integrazione) [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Utente di Business Central corrente mappato a un utente di Dynamics 365 Sales**|Indica se l'account utente utilizzato viene mappato a account in [!INCLUDE[crm_md](includes/crm_md.md)]|

6. Per verificare le impostazioni di connessione, scegliere **Test connessione**.  

    > [!NOTE]  
    >  Se la crittografia dei dati non è abilitata in [!INCLUDE[d365fin](includes/d365fin_md.md)], verrà richiesto se si desidera abilitarla. Per abilitare la crittografia dei dati, scegliere **Sì** e immettere le informazioni necessarie. In caso contrario, scegliere **No**. È possibile abilitare la crittografia dei dati in un secondo momento. Per ulteriori informazioni, vedere [Crittografia di dati in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) nella Guida per sviluppatori e professionisti IT.  

7. Se la sincronizzazione di [!INCLUDE[crm_md](includes/crm_md.md)] non è ancora impostata, verrà richiesto se si desidera utilizzare l'impostazione di sincronizzazione predefinita. A seconda se si desidera conservare o meno i record allineati in [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)]  scegliere **Sì** o **No**.

> [!Note]
> La connessione a Dynamics 365 Sales mediante la pagina **Setup connessione a Microsoft Dynamics 365 Sales** può richiedere l'assegnazione dei ruoli di sicurezza Amministratore di integrazione e Utente integrazione all'account utente utilizzato per l'integrazione. Per ulteriori informazioni, vedere [Assegnare un ruolo di sicurezza a un utente](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> La connessione a Dynamics 365 Sales mediante la pagina **Setup connessione a Microsoft Dynamics 365 Sales** può richiedere l'assegnazione dei [ruoli di sicurezza **Amministratore di integrazione** e **Utente integrazione**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) all'account utente utilizzato per l'integrazione.


### <a name="to-disconnect-from-includecrm_mdincludescrm_mdmd"></a>Per disconnettersi da [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup connessione a Microsoft Dynamics 365 Sales** e quindi scegliere il collegamento correlato.
2. Nella pagina **Setup connessione a Microsoft Dynamics 365 Sales**, deselezionare la casella di controllo **Abilitato**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Vedere anche  
[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  

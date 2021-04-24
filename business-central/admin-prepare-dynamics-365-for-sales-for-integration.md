---
title: Integrazione con Dynamics 365 Sales | Microsoft Docs
description: Informazioni su come prepararsi all'integrazione di Dynamics 365 Business Central con Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 136a96c880c7abf9b082d7f8859e484be54da4e1
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777331"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integrazione con Dynamics 365 Sales
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Il ruolo di agente è spesso considerato come rivolto verso l'esterno in un'azienda. Tuttavia, può essere utile per gli agenti essere in grado di guardare dentro l'azienda e di osservare ciò che avviene nel back end. L'integrazione di [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] fornire agli agenti tale possibilità consentendo agli stessi di visualizzare informazioni in [!INCLUDE[prod_short](includes/prod_short.md)] mentre lavorano in [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, durante la preparazione di un'offerta di vendita può essere utile sapere se si dispone di giacenza sufficiente per soddisfare l'ordine. Per ulteriori informazioni, vedere [Utilizzo di Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Questo argomento descrive il processo di integrazione delle versioni online di [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)] tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per informazioni sulla configurazione locale, vedere [Preparazione di Dynamics 365 Sales per l'integrazione locale](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integrazione tramite Dataverse
[!INCLUDE[prod_short](includes/prod_short.md)] si integra anche con [!INCLUDE[prod_short](includes/cds_long_md.md)], che semplifica la connessione e la sincronizzazione dei dati con altre applicazioni di Dynamics 365, come [!INCLUDE[crm_md](includes/crm_md.md)] o anche le app che crei autonomamente. Se stai effettuando l'integrazione per la prima volta, ti consigliamo di farlo tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ulteriori informazioni, vedi [Integrazione con Dataverse](admin-common-data-service.md).

Se hai già integrato [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puoi continuare a sincronizzare i dati utilizzando la tua configurazione. Tuttavia, se aggiorni o disattivi la tua integrazione [!INCLUDE[crm_md](includes/crm_md.md)], per riattivarla devi connetterti tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ulteriori informazioni, vedi [Aggiornamento di un'integrazione con Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> La riconnessione tramite [!INCLUDE[prod_short](includes/cds_long_md.md)] applicherà le impostazioni di sincronizzazione predefinite e sovrascriverà tutte le configurazioni a tua disposizione. Ad esempio, verranno applicati i mapping di tabella predefiniti.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Impostazioni di integrazione specifiche per un'integrazione [!INCLUDE[crm_md](includes/crm_md.md)]
L'integrazione con [!INCLUDE[prod_short](includes/prod_short.md)] avviene tramite [!INCLUDE[prod_short](includes/cds_long_md.md)] e sono molte le impostazioni e le tabelle standard fornite dall'integrazione. Oltre alle impostazioni standard, ce ne sono alcune specifiche di [!INCLUDE[crm_md](includes/crm_md.md)]. Queste ultime vengono elencate nelle seguenti sezioni.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Autorizzazioni e ruoli di sicurezza per gli account utente nelle vendite
Quando si installa la soluzione di integrazione, le autorizzazioni per l'account utente di integrazione sono configurate. Se tali autorizzazioni vengono modificate, potrebbe essere necessario ripristinarle. Puoi farlo reinstallando la soluzione di integrazione scegliendo **Ridistribuisci soluzione di integrazione** nella pagina **Setup connessione Dynamics 365**. Vengono distribuiti i seguenti ruoli di sicurezza:

* Amministratore di integrazione Dynamics 365 Business Central
* Utente integrazione Dynamics 365 Business Central
* Utente disponibilità prodotto Dynamics 365 Business Central

### <a name="connection-settings-in-the-setup-guide"></a>Impostazioni di connessione nella Guida al setup

Puoi utilizzare guida al setup assistito per impostare rapidamente la connessione e specificare le funzionalità avanzate, ad esempio l'associazione tra record.

1. Scegliere **Setup ed estensioni** quindi **Setup assistito**.
2. Scegli **Setup connessione a Dynamics 365 Sales** per avviare la guida al setup assistito.
3. Compilare i campi in base alle esigenze.
4. Eventualmente, esistono delle impostazioni avanzate che possono migliorare la sicurezza e abilitare ulteriori funzionalità di , come l'elaborazione degli ordini di vendita e la visualizzazione dei livelli di magazzino. Nella seguente tabella vengono illustrate le impostazioni avanzate.  

| Campo | Descrizione |
|--|--|
| **Importa soluzione di Dynamics 365 Sales** | Abilitare questa impostazione per installare e configurare la soluzione di integrazione in [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Pubblica servizio Web Disponibilità articolo** | Consentire alla persone che utilizzano [!INCLUDE[crm_md](includes/crm_md.md)] di visualizzare la disponibilità degli articoli (prodotti) in magazzino in [!INCLUDE[prod_short](includes/prod_short.md)]. A questo proposito, è necessario un account utente di [!INCLUDE[prod_short](includes/prod_short.md)] con una chiave di accesso ai servizi Web. L'assegnazione della chiave è un processo in due tappe. Nell'account utente di [!INCLUDE[prod_short](includes/prod_short.md)] è necessario scegliere l'azione **Modifica chiave del servizio Web**. Nella guida al setup assistito Setup connessione a Dynamics 365 Sales, è necessario specificare l'URL del servizio Web OData di Dynamics 365 Business Central e fornire le credenziali utente di [!INCLUDE[prod_short](includes/prod_short.md)] per l'accesso al servizio. Per ulteriori informazioni, vedere [Servizi Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **URL servizi Web OData di Business Central** | Se si abilita il servizio Web per la visualizzazione della disponibilità degli articoli, viene fornito l'URL del service Web OData. |
| **Nome utente servizi Web OData di Business Central** | Il nome dell'account utente di [!INCLUDE[prod_short](includes/prod_short.md)] che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per recuperare informazioni sulla disponibilità degli articoli in [!INCLUDE[prod_short](includes/prod_short.md)] mediante il servizio Web OData. |
| **Chiave di accesso servizi Web OData di Business Central** | La chiave di accesso per l'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[prod_short](includes/prod_short.md)] mediante il servizio Web OData. La chiave viene assegnata all'utente selezionato nel campo **Nome utente servizi Web OData di Business Central**. Per ottenere la chiave, scegliere il pulsante **Cerca valore** accanto al nome utente, scegliere l'utente, scegliere **Gestisci**, e quindi **Modifica**. Nella scheda utente, scegliere **Azioni**, **Autenticazione** e quindi **Modifica chiave del servizio Web**. |
| **Abilita integrazione ordini di vendita** | Quando le persone creano ordini di vendita in [!INCLUDE[crm_md](includes/crm_md.md)] e completano gli ordini in [!INCLUDE[prod_short](includes/prod_short.md)], questo integra il processo in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Abilitare l'integrazione dell'elaborazione degli ordini di vendita](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). A questo proposito si forniscono le credenziali per un account utente amministratore in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Gestione di dati di ordini di vendita](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **Abilita connessione CDS** | Abilitare la connessione a [!INCLUDE[prod_short](includes/cds_long_md.md)]. |
| **Versione Dynamics 365 SDK** | Ciò è pertinente solo se si esegue l'integrazione con una versione locale di [!INCLUDE[crm_md](includes/crm_md.md)]. Si tratta del Dynamics 365 software development kit (denominato anche Xrm) utilizzato per connettere [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versione deve essere compatibile con la versione SDK utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)] ed è uguale o più recente della versione utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Impostazioni di connessione nella pagina Setup connessione Microsoft Dynamics 365

Immettere le seguenti informazioni per la connessione da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)].

| Campo | Descrizione |
|--|--|
| **URL di Dynamics 365 Sales** | L'URL dell'istanza di [!INCLUDE[crm_md](includes/crm_md.md)]. Ciò consente agli utenti di aprire record corrispondenti in [!INCLUDE[prod_short](includes/prod_short.md)] dai record di [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio un conto o un prodotto. I record di [!INCLUDE[prod_short](includes/prod_short.md)] vengono aperti in [!INCLUDE[prod_short](includes/prod_short.md)]. |
|**URL di Dynamics 365 Sales**|L'URL dell'istanza di [!INCLUDE[crm_md](includes/crm_md.md)]. Ciò consente agli utenti di aprire record corrispondenti in [!INCLUDE[prod_short](includes/prod_short.md)] dai record di [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio un conto o un prodotto. I record di [!INCLUDE[prod_short](includes/prod_short.md)] vengono aperti in [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Servizio Web Disponibilità articolo abilitato**|Consentire alla persone che utilizzano [!INCLUDE[crm_md](includes/crm_md.md)] di visualizzare la disponibilità degli articoli (prodotti) in magazzino in [!INCLUDE[prod_short](includes/prod_short.md)]. Se si abilita questa funzionalità, è inoltre necessario fornire un nome utente e una chiave di accesso per [!INCLUDE[crm_md](includes/crm_md.md)] da utilizzare per eseguire una query sul servizio Web OData per la disponibilità degli articoli (prodotti). Per ulteriori informazioni, vedere [Servizi Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL servizi Web OData di Dynamics 365 Business Central**|Se si abilita il servizio Web Disponibilità articolo, viene fornito l'URL del service Web OData. Impostare il campo sull'URL dell'istanza di [!INCLUDE[prod_short](includes/prod_short.md)] da utilizzare.<br /><br /> Per reimpostare il campo sull'URL predefinito per [!INCLUDE[prod_short](includes/prod_short.md)], scegliere l'azione **Reimposta URL client Web**.<br /><br /> Questo campo è pertinente solo se la soluzione di integrazione di [!INCLUDE[prod_short](includes/prod_short.md)] è installata in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Nome utente servizi Web OData di Dynamics 365 Business Central**|Il nome dell'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[prod_short](includes/prod_short.md)] mediante il servizio Web OData.|
|**Chiave di accesso servizi Web OData di Dynamics 365 Business Central**|La chiave di accesso dell'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[prod_short](includes/prod_short.md)] mediante il servizio Web OData. La chiave viene assegnato all'utente selezionato nel campo **Nome utente servizi Web OData di Dynamics 365 Business Central**. Per ottenere la chiave, scegliere il pulsante **Cerca valore** accanto al nome utente, scegliere l'utente, scegliere **Gestisci**, e quindi **Modifica**. Nella scheda utente, scegliere **Azioni**, **Autenticazione** e quindi **Modifica chiave del servizio Web**.|
|**Versione Dynamics 365 SDK**|Se si esegue l'integrazione con una versione locale di [!INCLUDE[crm_md](includes/crm_md.md)], si tratta del Dynamics 365 software development kit (denominato anche Xrm) utilizzato per connettere [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versione selezionata deve essere compatibile con la versione SDK utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)]. Questa versione è uguale o superiore alla versione utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)].|

Oltre alle impostazioni sopra, immetti le seguenti impostazioni per [!INCLUDE[crm_md](includes/crm_md.md)].

| Campo | Descrizione |
|--|--|
| **Integrazione ordini di vendita abilitata** | Consentire agli utenti di inviare ordini di vendita e offerte attivate in [!INCLUDE[crm_md](includes/crm_md.md)] e quindi visualizzarli ed elaborarli in [!INCLUDE[prod_short](includes/prod_short.md)]. Questa operazione integra il processo in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Abilitare l'integrazione dell'elaborazione degli ordini di vendita](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Crea automaticamente ordini vendita** | Creare un ordine di vendita in [!INCLUDE[prod_short](includes/prod_short.md)] quando un utente ne crea e ne invia uno in [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Elabora automaticamente offerte di vendita** | Elaborare un'offerta di vendita in [!INCLUDE[prod_short](includes/prod_short.md)] quando un utente ne crea e ne attiva una in [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Mapping delle entità standard di Sales per la sincronizzazione

Le entità in [!INCLUDE[crm_md](includes/crm_md.md)], come gli ordini, vengono integrate con i tipi di tabelle equivalenti in [!INCLUDE[prod_short](includes/prod_short.md)], quali gli ordini vendita. Per utilizzare i dati di [!INCLUDE[crm_md](includes/crm_md.md)] si impostano collegamenti, denominati associazioni, tra le tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[crm_md](includes/crm_md.md)].

Nella seguente tabella elenca il mapping standard tra le tabelle in [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] che [!INCLUDE[prod_short](includes/prod_short.md)] fornisce.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Direzione della sincronizzazione | Filtro predefinito |
|--|--|--|--|
| Unità di misura | Unità di vendita | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Articolo | Prodotto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro contatto di Sales: il campo **Tipo prodotto** è **Inventario vendite** |
| Risorsa | Prodotto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro contatto di Sales: il campo **Tipo prodotto** è **Servizi** |
| Gruppo prezzi cliente | Listino prezzi | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Prezzo vendita | Listino prezzi prodotto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro contatto di [!INCLUDE[prod_short](includes/prod_short.md)]: il campo **Codice vendita** non è vuoto; il campo **Tipo vendita** è **Gruppo prezzi cliente** |
| Opportunità | Opportunità | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Testate Fatt. Vendita | Fattura | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Righe Fatt. Vendita | Prodotto di fatturazione | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Testate ordine cliente | Ordini Vendita | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro Testate vendita di [!INCLUDE[prod_short](includes/prod_short.md)]: il campo **Tipo di documento** è Ordine; il campo **Stato** è Rilasciato |
| Note dell'ordine di vendita | Note dell'ordine di vendita | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

### <a name="synchronization-rules"></a>Regole di sincronizzazione

Nella seguente tabella vengono elencate le regole che controllano la sincronizzazione tra [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)]. Queste si aggiungono alle regole definite per Dataverse che sono altrettanto applicabili. Per ulteriori informazioni, vedi [Mappatura entità standard](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Le modifiche ai dati effettuate dall'account utente di integrazione non vengono sincronizzate. Di conseguenza, si consiglia di non modificare i dati quando si utilizza quell'account Per ulteriori informazioni, vedere [Impostazione di account utente per l'integrazione con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tavolo|Regola|
|-----|----|
|Unità di misura|Le unità di misura vengono sincronizzate con le unità di vendita in [!INCLUDE[crm_md](includes/crm_md.md)]. Può essere definita solo un'unità di misura nell'unità di vendita.|
|Articoli|Quando si sincronizzano gli articoli con i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)] crea automaticamente un listino prezzi in [!INCLUDE[crm_md](includes/crm_md.md)]. Per evitare errori di sincronizzazione, è consigliabile non modificare il listino prezzi manualmente.|
|Risorse|Le risorse vengono sincronizzate con i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con tipo di prodotto Assistenza.|
|Gruppi prezzi cliente|Per Gruppi prezzi cliente viene eseguita la sincronizzazione con i listini prezzi di Sales.|
|Prezzi vendita|I prezzi di vendita con tipo di vendita Gruppo prezzi cliente e un codice di vendita definito vengono sincronizzati con le righe del listino prezzi di [!INCLUDE[crm_md](includes/crm_md.md)].|
|Opportunità|Le opportunità vengono sincronizzate con le opportunità di [!INCLUDE[crm_md](includes/crm_md.md)]. Il valore Codice agente indica il proprietario della tabella associata in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Fatture di vendita registrate|Le fatture di vendita registrate vengono sincronizzate con le fatture di Sales. Prima di poter sincronizzare una fattura, è meglio sincronizzare tutte le altre tabelle che possono essere incluse nella fattura, dai venditori ai listini prezzi. Il valore Codice agente nella testata della fattura indica il proprietario della tabella associata in Sales.|
|Ordini vendita|Quando l'integrazione dell'ordine cliente è abilitata, gli ordini cliente in [!INCLUDE[prod_short](includes/prod_short.md)] creati dagli ordini cliente inviati in  [!INCLUDE[crm_md](includes/crm_md.md)] sono sincronizzati con ordini di vendita in INCLUDE SALES quando vengono rilasciati. Prima di sincronizzare gli ordini, si consiglia di sincronizzare innanzitutto tutte le tabelle che sono coinvolte nell'ordine, come addetti alle vendite e listini prezzi. Il campo Codice agente nell'intestazione dell'ordine definisce il proprietario della tabella associata in [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Processi di sincronizzazione un'integrazione delle vendite.

I processi sono eseguiti nel seguente ordine per evitare di associare dipendenze tra tabelle. Sono disponibili altri processi da Dataverse. Per ulteriori informazioni, vedi [Utilizzare le code processi per pianificare i task](./admin-job-queues-schedule-tasks.md).

1. Processo di sincronizzazione UNITÀDIMISURA - Dynamics 365 Sales  
2. Processo di sincronizzazione RISORSA-PRODOTTO - Dynamics 365 Sales  
3. Processo di sincronizzazione ARTICOLO-PRODOTTO - Dynamics 365 Sales  
4. Processo di sincronizzazione GRPPRZCLNT-PREZZO - Dynamics 365 Sales.
5. Processo di sincronizzazione PRZVNDT-PRZPRODOTTI - Dynamics 365 Sales.
6. Processo di sincronizzazione FATTVNDTRGSTR-FATT - Dynamics 365 Sales.

### <a name="default-synchronization-job-queue-entries"></a>Movimenti coda processi di sincronizzazione predefiniti

Nella tabella seguente sono descritti i processi di sincronizzazione predefiniti per le vendite.  

|Movimento coda processi|Descrizione|Direzione|Mapping tabella integrazione|Frequenza di sincronizzazione predefinita (minuti)|Tempo di inattività predefinito (minuti)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Processo di sincronizzazione UNITÀDIMISURA - Dynamics 365 Sales|Sincronizza le unità di vendita di [!INCLUDE[crm_md](includes/crm_md.md)] con le unità di misura di [!INCLUDE[prod_short](includes/prod_short.md)].|Da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|UNITÀ DI MISURA|30|720<br> (12 ore)|
|Processo di sincronizzazione RISORSA-PRODOTTO - Dynamics 365 Sales|Sincronizza i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con le risorse di [!INCLUDE[prod_short](includes/prod_short.md)].|Da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|RISORSA-PRODOTTO|30|720<br> (12 ore)|
|Processo di sincronizzazione ARTICOLO-PRODOTTO - Dynamics 365 Sales|Sincronizza i prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con articoli di [!INCLUDE[prod_short](includes/prod_short.md)].|Da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|ARTICOLO-PRODOTTO|30|1440<br> (24 ore)|
|Processo di sincronizzazione GRPPRZCLNT-PREZZO - Dynamics 365 Sales|Sincronizza i listini prezzi di vendita di [!INCLUDE[crm_md](includes/crm_md.md)] con gruppi di prezzi cliente di [!INCLUDE[prod_short](includes/prod_short.md)].| |GRUPPI DI PREZZI CLIENTE-LISTINI PREZZI DI VENDITA|30|1440<br> (24 ore)|
|Processo di sincronizzazione PRZVNDT-PRZPRODOTTI - Dynamics 365 Sales|Sincronizza i prezzi dei prodotti di [!INCLUDE[crm_md](includes/crm_md.md)] con i prezzi di vendita di [!INCLUDE[prod_short](includes/prod_short.md)].||PREZZO DEL PRODOTTO - PREZZO DI VENDITA|30|1440<br> (24 ore)|
|Processo di sincronizzazione FATTVNDTRGSTR-FATT - Dynamics 365 Sales|Sincronizza le fatture di [!INCLUDE[crm_md](includes/crm_md.md)] con le fatture di vendita registrate di [!INCLUDE[prod_short](includes/prod_short.md)].|Da [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|FATTURE-FATTURE DI VENDITA REGISTRATE|30|1440<br> (24 ore)|
|Processo di sincronizzazione Statistiche cliente - Dynamics 365 Sales|Aggiorna i conti di [!INCLUDE[crm_md](includes/crm_md.md)] con i dati cliente di [!INCLUDE[prod_short](includes/prod_short.md)] più recenti. In [!INCLUDE[crm_md](includes/crm_md.md)], questa informazione viene visualizzata nel modulo di visualizzazione rapida **Statistiche conto Business Central** dei conti associati ai clienti di [!INCLUDE[prod_short](includes/prod_short.md)].<br /><br /> Questi dati possono anche essere aggiornati manualmente da ogni record cliente. Per ulteriori informazioni, vedere [Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Nota:** questo movimento coda processi è pertinente solo se la soluzione di integrazione di [!INCLUDE[prod_short](includes/prod_short.md)] è installata in [!INCLUDE[crm_md](includes/crm_md.md)]. |Non applicabile|Non applicabile|30|Non applicabile| 

## <a name="connecting-business-central-on-premises-versions-earlier-than-version-16"></a>Collegamento di versioni locali di Business Central precedenti alla versione 16
Il team Microsoft Power Platform ha [annunciato](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) che sta deprecando il tipo di autenticazione di Office365. Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] locale precedente alla versione 16, devi utilizzare il tipo di autenticazione OAuth per la connessione a [!INCLUDE[crm_md](includes/crm_md.md)] online. I passaggi in questa sezione descrivono come effettuare la connessione.

### <a name="prerequisites"></a>Prerequisiti

- Devi avere una sottoscrizione Microsoft Azure. Un account di prova funzionerà per la registrazione dell'applicazione.
- [!INCLUDE[crm_md](includes/crm_md.md)] è configurato per utilizzare uno dei seguenti tipi di autenticazione:

   - Office365 (legacy)

     > [!IMPORTANT]
     > A partire da aprile 2022, Office365 (legacy) non sarà più supportato. Per ulteriori informazioni, vedi [Importanti modifiche (deprecazioni) in arrivo per Power Apps, Power Automate e app per il coinvolgimento dei clienti](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### <a name="to-connect-a-version-of-business-central-earlier-than-version-16"></a>Eseguire la connessione a una versione di Business Central precedente alla versione 16

1. Importa la Soluzione di integrazione di Microsoft Dynamics 365 Business Central nell'ambiente [!INCLUDE[crm_md](includes/crm_md.md)]. La soluzione di integrazione è disponibile nella cartella CrmCustomization sul DVD di installazione di Business Central. Sono disponibili più versioni della soluzione, ad esempio DynamicsNAVIntegrationSolution_v8 o DynamicsNAVIntegrationSolution_v9 o DynamicsNAVIntegrationSolution_v91. La soluzione da importare dipende dalla versione di [!INCLUDE[crm_md](includes/crm_md.md)] a cui ti stai connettendo. [!INCLUDE[crm_md](includes/crm_md.md)] online richiede la soluzione di integrazione DynamicsNAVIntegrationSolution_v91.
2. Crea un utente di integrazione non interattivo nell'ambiente [!INCLUDE[crm_md](includes/crm_md.md)] e assegna all'utente i seguenti ruoli di sicurezza. Per ulteriori informazioni, vedi [Creare un account utente non interattivo](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Amministratore di integrazione Dynamics 365 Business Central
   * Utente integrazione Dynamics 365 Business Central

   > [!Important]
   > Questo utente non deve avere il ruolo di sicurezza Amministratore di sistema. Inoltre, non è possibile utilizzare l'account dell'amministratore di sistema come utente di integrazione.

3.  Nel portale di Azure crea una registrazione dell'app per [!INCLUDE[prod_short](includes/prod_short.md)]. Per i passaggi, vedi [Registrare un'applicazione in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Le impostazioni specifiche per la connessione a [!INCLUDE[crm_md](includes/crm_md.md)] sono le autorizzazioni delegate. La tabella seguente elenca e descrive le autorizzazioni.

   |Nome API/autorizzazione |Tipo  |Descrizione  |
   |---------|---------|---------|
   |Financials.ReadWrite.All     |Delegato|Necessario per [!INCLUDE[prod_short](includes/prod_short.md)].    |
   |user_impersonation     |Delegato|Necessario per [!INCLUDE[crm_md](includes/crm_md.md)].|
   
4. In [!INCLUDE[prod_short](includes/prod_short.md)], cerca **Setup connessione Microsoft Dynamics 365** e quindi scegli il collegamento correlato. 
5. Nella pagina **Setup connessione Microsoft Dynamics 365**, nel campo **Tipo di autenticazione**, scegli l'opzione per OAuth. 
6. Scegli la versione dell'SDK CRM che corrisponde alla versione della soluzione importata nel passaggio 1.
7. Nel campo **Indirizzo server**, immetti l'URL dell'ambiente [!INCLUDE[crm_md](includes/crm_md.md)], quindi immetti il nome utente e la password per l'utente di integrazione.
8. Nel campo **Stringa di connessione**, specifica l'ID della registrazione dell'app. Questo campo ha due token in cui deve essere specificato l'ID dell'applicazione.

   |Token           |Descrizione  |
   |----------------|-------------|
   |**AppId**       |Imposta l'ID dell'applicazione.      |
   |**RedirectUri** |Imposta l'ID dell'applicazione, ma aggiungi il prefisso **app://**.         |

    **Esempio** L'esempio seguente mostra una stringa di connessione.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Abilita la connessione.

> [!Note]
> Se intendi configurare una connessione a un'istanza di [!INCLUDE[crm_md](includes/crm_md.md)] con un tipo di autenticazione specifico, compila i campi della Scheda dettaglio **Dettagli tipo di autenticazione**. Per ulteriori informazioni, vedi [Autenticazione con i servizi Web di Microsoft Dataverse](/powerapps/developer/data-platform/authentication). Questo passaggio non è necessario quando si connette una versione online di [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Vedere anche

[Impostazione di account utente per l'integrazione con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Impostare una connessione a [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sincronizzazione di Business Central e [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Preparazione di Dynamics 365 Sales per l'integrazione locale](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]

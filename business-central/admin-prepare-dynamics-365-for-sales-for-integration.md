---
title: Integrazione con Dynamics 365 Sales
description: Scopri come ottenere Dynamics 365 Business Central pronto per l'integrazione con Dynamics 365 Sales per vedere cosa sta succedendo nel backend.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: c0c1d4504a75a07ead734ad74e67567129e43dd5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130672"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integrazione con Dynamics 365 Sales


Il ruolo di agente è spesso considerato come rivolto verso l'esterno in un'azienda. Tuttavia, può essere utile per gli agenti essere in grado di guardare dentro l'azienda e di osservare ciò che avviene nel back end. L'integrazione di [!INCLUDE[prod_short](includes/prod_short.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] fornire agli agenti tale possibilità consentendo agli stessi di visualizzare informazioni in [!INCLUDE[prod_short](includes/prod_short.md)] mentre lavorano in [!INCLUDE[crm_md](includes/crm_md.md)]. Ad esempio, durante la preparazione di un'offerta di vendita può essere utile sapere se si dispone di giacenza sufficiente per soddisfare l'ordine. Per ulteriori informazioni, vedere [Utilizzo di Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Questo argomento descrive il processo di integrazione delle versioni online di [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)] tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per informazioni sulla configurazione locale, vedere [Preparazione di Dynamics 365 Sales per l'integrazione locale](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integrazione tramite Dataverse
[!INCLUDE[prod_short](includes/prod_short.md)] si integra anche con [!INCLUDE[prod_short](includes/cds_long_md.md)], che semplifica la connessione e la sincronizzazione dei dati con altre applicazioni di Dynamics 365, come [!INCLUDE[crm_md](includes/crm_md.md)] o anche le app che crei autonomamente. Se stai integrando per la prima volta, devi farlo tramite [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per ulteriori informazioni, vedi [Integrazione con Dataverse](admin-common-data-service.md).

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
|**Nome utente servizi Web OData di Business Central** | Il nome dell'account utente di [!INCLUDE[prod_short](includes/prod_short.md)] che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per recuperare informazioni sulla disponibilità degli articoli in [!INCLUDE[prod_short](includes/prod_short.md)] mediante il servizio Web OData. |
| **Chiave di accesso servizi Web OData di Business Central** | La chiave di accesso per l'account utente che [!INCLUDE[crm_md](includes/crm_md.md)] utilizza per ottenere informazioni sulla disponibilità degli articoli da [!INCLUDE[prod_short](includes/prod_short.md)] mediante il servizio Web OData. La chiave viene assegnata all'utente selezionato nel campo **Nome utente servizi Web OData di Business Central**. Per ottenere la chiave, scegliere il pulsante **Cerca valore** accanto al nome utente, scegliere l'utente, scegliere **Gestisci**, e quindi **Modifica**. Nella scheda utente, scegliere **Azioni**, **Autenticazione** e quindi **Modifica chiave del servizio Web**. |
| **Abilita integrazione ordini di vendita** | Quando le persone creano ordini di vendita in [!INCLUDE[crm_md](includes/crm_md.md)] e completano gli ordini in [!INCLUDE[prod_short](includes/prod_short.md)], si ha l'integrazione del processo in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Abilitare l'integrazione dell'elaborazione degli ordini di vendita](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). A questo proposito si forniscono le credenziali per un account utente amministratore in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Gestione di dati di ordini di vendita](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
|**Abilita connessione a Dynamics 365 Sales** | Abilitare la connessione a [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Versione Dynamics 365 SDK** | Ciò è pertinente solo se si esegue l'integrazione con una versione locale di [!INCLUDE[crm_md](includes/crm_md.md)]. Si tratta del Dynamics 365 software development kit (denominato anche Xrm) utilizzato per connettere [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versione deve essere compatibile con la versione SDK utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)] ed è uguale o più recente della versione utilizzata da [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Impostazioni di connessione nella pagina Setup connessione Microsoft Dynamics 365

Immettere le seguenti informazioni per la connessione da [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)].

| Campo | Descrizione |
|--|--|
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
| **Elabora automaticamente offerte di vendita** | Elaborare un'offerta di vendita in [!INCLUDE[prod_short](includes/prod_short.md)] quando un utente ne crea e ne attiva una in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Gestione di dati di offerte di vendita](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |

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
| Unità di misura articoli | Unità di misura CRM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Unità di misura risorse | Unità di misura CRM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Unità di vendita | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Gruppo prezzi cliente | Listino prezzi | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Prezzo vendita | Listino prezzi prodotto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro contatto di [!INCLUDE[prod_short](includes/prod_short.md)]: il campo **Codice vendita** non è vuoto; il campo **Tipo vendita** è **Gruppo prezzi cliente** |
| Opportunità | Opportunità | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Testate Fatt. Vendita | Fattura | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Righe Fatt. Vendita | Prodotto di fatturazione | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Testate ordine cliente | Ordini Vendita | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro Testate vendita di [!INCLUDE[prod_short](includes/prod_short.md)]: il campo **Tipo di documento** è Ordine; il campo **Stato** è Rilasciato |
| Note dell'ordine di vendita | Note dell'ordine di vendita | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Le mappature per le tabelle Unità di misura articoli, Unità di misura risorse e Unità di vendita sono disponibili solo se l'amministratore ha attivato l'opzione di funzionalità **Aggiornamento funzionalità: sincronizzazione di più unità di misura con Dynamics 365 Sales** nella pagina **Gestione funzionalità**. Per ulteriori informazioni, vedi [Sincronizzazione di articoli e risorse con prodotti in diverse unità di misura](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronizing-items-and-resources-with-products-with-different-units-of-measure).

## <a name="synchronizing-items-and-resources-with-products-with-different-units-of-measure"></a>Sincronizzazione di articoli e risorse con prodotti in diverse unità di misura
Le aziende spesso producono o acquistano gli articoli in un'unità di misura e poi li vendono in un'altra. Per sincronizzare articoli che utilizzano più unità di misura, è necessario attivare l'opzione di funzionalità **Aggiornamento funzionalità: sincronizzazione di più unità di misura con Dynamics 365 Sales** nella pagina **Gestione funzionalità**. 

Quando lo fai, viene creata una nuova tabella Unità di vendita e assegnata a ciascun articolo e risorsa in [!INCLUDE[prod_short](includes/prod_short.md)]. Ciò consente di mappare le tabelle Unità di vendita, Unità di misura articolo e Unità di misura risorsa in [!INCLUDE[prod_short](includes/prod_short.md)] all'unità di vendita di Dynamics 365 Sales <!--Need to verify this name--> in [!INCLUDE[crm_md](includes/crm_md.md)], come mostrato nell'immagine seguente.

:::image type="content" source="media/unit group 1.png" alt-text="Mappature di tabelle per unità di vendita":::

Puoi creare più unità di misura per ogni unità di vendita e assegnare le unità ai prodotti in [!INCLUDE[crm_md](includes/crm_md.md)]. Successivamente, sarai in grado di sincronizzare i prodotti con articoli e risorse in [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile associare manualmente unità di misura articolo o unità di misura risorsa con un'unità di vendita. Quando lo fai, se l'unità di vendita per l'articolo o la risorsa non è associata a un'unità di vendita in [!INCLUDE[crm_md](includes/crm_md.md)], ad esempio, perché l'unità di vendita non esisteva, [!INCLUDE[prod_short](includes/prod_short.md)] creerà automaticamente l'unità di vendita in [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="mapping-items-and-resources-to-products"></a>Mappatura di articoli e risorse a prodotti
Quando attivi l'opzione di funzionalità **Aggiornamento funzionalità: sincronizzazione di più unità di misura con Dynamics 365 Sales**, accade quanto segue:

* Vengono create nuove mappature per articoli e risorse.
* Le mappature esistenti vengono eliminate. <!--which mappings?-->
* Un aggiornamento dei dati crea unità di vendita per articoli e risorse.

Per utilizzare le nuove mappature, è necessario sincronizzare le unità di vendita, l'unità di misura dell'articolo e l'unità di misura della risorsa. È inoltre necessario risincronizzare articoli e risorse. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] non consente di modificare un'unità di vendita per un prodotto. Pertanto, è necessario ritirare i prodotti e dissociare gli articoli e le risorse, quindi sincronizzare creando nuovi prodotti in [!INCLUDE[crm_md](includes/crm_md.md)]. 

I passaggi seguenti descrivono i passaggi per avviare la mappatura delle unità di vendita:

1. Assicurati che i prodotti in [!INCLUDE[crm_md](includes/crm_md.md)] non siano associati a articoli o risorse in [!INCLUDE[prod_short](includes/prod_short.md)]. Se lo sono, vai alle pagine **Articoli** e/o **Risorse** e utilizza le opzioni di filtro per selezionare i record associati. Quindi scegli l'azione **Dynamics 365 Sales** e seleziona **Annulla associazione**. Questo pianifica un processo in background per annullare l'associazione dei record. Mentre il processo è in esecuzione, puoi verificarne lo stato utilizzando l'azione **Registro sincronizzazione**. Per ulteriori informazioni, vedere [Associazione e sincronizzazione](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Dal momento che i nuovi prodotti verranno creati in [!INCLUDE[crm_md](includes/crm_md.md)] con nuove unità di vendita, per evitare nomi duplicati, esegui una delle seguenti operazioni:
    
    * Rinomina i tuoi prodotti e poi ritirali in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Ritirare i prodotti (hub delle vendite)](/dynamics365/sales-enterprise/retire-product). Per modificare in blocco i prodotti in Microsoft Excel, accedi a Power Apps, scegli l'ambiente, vai nella tabella **Prodotto** e scegli la scheda **Dati**, Cancella qualsiasi filtro applicato. Nel gruppo **Dati** scegli l'azione **Modifica dati in Excel**. Aggiungi un prefisso o un suffisso ai prodotti associati, quindi ritirali.
    * Ritira i tuoi prodotti ed eliminali. 

3. Segui questi passaggi per sincronizzare **Unità di vendita**, **Unità di misura**, **Articoli** e **Risorse**:
    1. In [!INCLUDE[prod_short](includes/prod_short.md)], apri la pagina **Setup connessione a Dynamics 365 Sales**.
    2. Utilizza l'azione **Esegui sincronizzazione completa** per aprire la pagina **Revisione sincronizzazione completa Dataverse**.
    3. Per le mappature **UDM ARTICOLO**, **UDM RISORSA** E **UNITÀ DI VENDITA** scegli l'azione **Sincronizzazione completa consigliata**.
    4. Scegliere l'azione **Sincronizza tutto**.

    > [!NOTE]
    > Per le mappature che non sono state ancora completamente sincronizzate, questa azione le sincronizzerà completamente. Per impedire la sincronizzazione di tali mappature, elimina le mappature dalla pagina. Questo le rimuove solo dalla sincronizzazione completa corrente e non elimina le mappature.
    
5. Scegli la mappatura **ARTICOLO-PRODOTTO** quindi scegli l'azione **Riavvia**. Questo crea nuovi prodotti dagli articoli in [!INCLUDE[crm_md](includes/crm_md.md)] e assegna un nuova unità di vendita specifica per l'articolo.
6. Scegli la mappatura **RISORSA-PRODOTTO** quindi scegli l'azione **Riavvia**. Questo crea nuovi prodotti dalle risorse in [!INCLUDE[crm_md](includes/crm_md.md)] e assegna un nuova unità di vendita specifica per le risorse.

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

## <a name="connecting-to-on-premises-versions-of-business-central-2019-release-wave-1-and-microsoft-dynamics-nav-2018"></a>Connessione alle versioni locali del primo ciclo di rilascio di Business Central 2019 e Microsoft Dynamics NAV 2018
Il team Microsoft Power Platform ha [annunciato](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) che sta deprecando il tipo di autenticazione di Office365. Se stai usando [!INCLUDE[prod_short](includes/prod_short.md)] locale precedente al primo ciclo di rilascio di Business Central 2019 devi utilizzare il tipo di autenticazione OAuth per la connessione a [!INCLUDE[crm_md](includes/crm_md.md)] online. I passaggi in questa sezione descrivono come effettuare la connessione alle seguenti versioni del prodotto:

* Primo ciclo di rilascio di Business Central 2019
* Microsoft Dynamics NAV 2018

### <a name="prerequisites"></a>Prerequisiti

- Devi avere una sottoscrizione Microsoft Azure. Un account di prova funzionerà per la registrazione dell'applicazione.
- [!INCLUDE[crm_md](includes/crm_md.md)] è configurato per utilizzare uno dei seguenti tipi di autenticazione:

   - Office365 (legacy)

     > [!IMPORTANT]
     > A partire da aprile 2022, Office365 (legacy) non sarà più supportato. Per ulteriori informazioni, vedi [Importanti modifiche (deprecazioni) in arrivo per Power Apps, Power Automate e app per il coinvolgimento dei clienti](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### <a name="to-connect-business-central-2019-release-wave-1-and-dynamics-nav-2018"></a>Per connettere il primo ciclo di rilascio di Business Central 2019 e Dynamics NAV 2018

1. Importa la Soluzione di integrazione di Microsoft Dynamics 365 Business Central nell'ambiente [!INCLUDE[crm_md](includes/crm_md.md)]. La soluzione di integrazione è disponibile nella cartella CrmCustomization sul DVD di installazione di [!INCLUDE[prod_short](includes/prod_short.md)] o Dynamics NAV 2018. A seconda della versione del prodotto, importa uno dei seguenti:

   * Per [!INCLUDE[prod_short](includes/prod_short.md)], la cartella contiene le soluzioni DynamicsNAVIntegrationSolution_v9 e DynamicsNAVIntegrationSolution_v91 . La soluzione da importare dipende dalla versione di [!INCLUDE[crm_md](includes/crm_md.md)] a cui ti stai connettendo. [!INCLUDE[crm_md](includes/crm_md.md)] online richiede la soluzione di integrazione DynamicsNAVIntegrationSolution_v91.
   * Per Dynamics NAV 2018, installare la soluzione DynamicsNAVIntegrationSolution.

2. Crea un utente di integrazione non interattivo nell'ambiente [!INCLUDE[crm_md](includes/crm_md.md)] e assegna all'utente i seguenti ruoli di sicurezza. Per ulteriori informazioni, vedi [Creare un account utente non interattivo](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Amministratore di integrazione Dynamics 365 Business Central
   * Utente integrazione Dynamics 365 Business Central

   > [!Important]
   > Questo utente non deve avere il ruolo di sicurezza Amministratore di sistema. Inoltre, non è possibile utilizzare l'account dell'amministratore di sistema come utente di integrazione.

3.  Nel portale di Azure crea una registrazione dell'app per [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedi [Registrare l'applicazione in Azure Active Directory](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Ti consigliamo di registrare l'app nello stesso tenant del tuo ambiente Dataverse in modo da non dover consentire all'app di accedere all'ambiente. Se registri l'app in un altro ambiente, devi accedere ad Azure AD utilizzando l'account amministratore per il tuo ambiente Dataverse e dare il consenso.
   >
   > Inoltre, l'app che registri non deve avere un segreto. Collegamento di un'app con un segreto per Dataverse è disponibile solo nel primo ciclo di rilascio di Business Central 2020 e versioni successive.
  
4. A seconda della versione del prodotto, effettua uno dei seguenti:

    * In [!INCLUDE[prod_short](includes/prod_short.md)], cerca **Setup connessione Microsoft Dynamics 365** e quindi scegli il collegamento correlato. 
    * In Dynamics NAV 2018, cerca **Setup connessione Microsoft Dynamics 365 for Sales** e quindi scegli il collegamento correlato.

5. Nel campo **Tipo di autenticazione** scegli l'opzione per OAuth. 
6. Scegli la versione dell'SDK CRM che corrisponde alla versione della soluzione importata nel passaggio 1.

   > [!NOTE]
   > Questo passaggio è rilevante solo per [!INCLUDE[prod_short](includes/prod_short.md)].

7. Immetti l'URL dell'ambiente [!INCLUDE[crm_md](includes/crm_md.md)], quindi immetti il nome utente e la password per l'utente di integrazione. 

   * In [!INCLUDE[prod_short](includes/prod_short.md)], usa il campo **Indirizzo server**.
   * In Dynamics NAV 2018, usa il campo **URL Dynamics 365 Sales**.

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

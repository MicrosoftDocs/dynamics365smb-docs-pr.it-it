---
title: Integrazione con Microsoft Dynamics 365 Field Service
description: Scopri come integrare Business Central con Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>Integrazione con Microsoft Dynamics 365 Field Service

Le organizzazioni di servizi richiedono un'applicazione front-to-back in cui i dati finanziari, l'inventario e l'approvvigionamento siano strettamente collegati alla fornitura dei servizi. Questi generano dati finanziari con ogni transazione. Ogni ordine di lavoro rappresenta costi e ricavi e ogni risorsa genera profitti e perdite. Le interazioni con i clienti aggiungono movimenti nella contabilità generale. L'integrazione tra [!INCLUDE [prod_short](includes/prod_short.md)] e [!INCLUDE [field-service-short](includes/field-service-short.md)] snellisce il processo end-to-end di gestione delle operazioni di servizio e garantisce un flusso regolare di informazioni tra i due sistemi.  

Puoi creare e gestire facilmente ordini di lavoro in [!INCLUDE [field-service-short](includes/field-service-short.md)], monitorare lo stato di avanzamento delle attività di servizio, assegnare risorse e acquisire dettagli sui consumi. Quando completi un ordine di lavoro in [!INCLUDE [field-service-short](includes/field-service-short.md)], l'integrazione consente il trasferimento regolare dei dati a [!INCLUDE [prod_short](includes/prod_short.md)] per un'ulteriore elaborazione.  

L'integrazione facilita inoltre la fatturazione e l'evasione degli ordini di lavoro in [!INCLUDE [prod_short](includes/prod_short.md)]. Puoi generare fatture precise in base alle attività di servizio e ai consumi registrati in [!INCLUDE [field-service-short](includes/field-service-short.md)].  

Grazie all'integrazione di [!INCLUDE [prod_short](includes/prod_short.md)] con [!INCLUDE [field-service-short](includes/field-service-short.md)], non devi inserire i dati manualmente o duplicare gli sforzi. L'integrazione fornisce inoltre una visione completa delle operazioni e dei dati finanziari dei servizi, consentendo un migliore processo decisionale e un'efficienza operativa migliore.

## <a name="prerequisites"></a>Prerequisiti

Poiché [!INCLUDE [field-service-short](includes/field-service-short.md)] è basato su Dynamics 365 Sales, devi [configurare una connessione a Dataverse](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) e [abilitare l'integrazione con Dynamics 365 Sales](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### <a name="permissions-and-security-roles-for-user-accounts"></a>Autorizzazioni e ruoli di sicurezza per account utente

Quando si installa la soluzione di integrazione, le autorizzazioni per l'account utente di integrazione sono configurate. Se tali autorizzazioni cambiano, potrebbe essere necessario ripristinarle. A tale scopo, reinstalla la soluzione di integrazione selezionando **Ridistribuisci soluzione di integrazione** nella pagina **Setup connessione a Dynamics 365**. Le sezioni seguenti elencano le autorizzazioni e i ruoli di sicurezza distribuiti dalla soluzione per ogni app.

#### <a name="sales"></a>Vendita

* Amministratore di integrazione Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]
* Utente di integrazione Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]
* Utente disponibilità prodotto Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]

#### <a name="business-central"></a>Business Central

Gli utenti che pubblicano registrazioni progetti devono disporre del seguente set di autorizzazioni:

* Integrazione Dynamics 365 Sales

#### <a name="field-service"></a>Settore servizi

Per utilizzare i dati integrati, gli utenti devono avere il seguente ruolo di sicurezza:

* Integrazione di Business Central Field Service

Ad esempio, gli utenti devono avere questo ruolo per connettere gli ordini di lavoro a [!INCLUDE [prod_short](includes/prod_short.md)] per l'elaborazione.

> [!NOTE]
> Assicurati che gli utenti siano assegnati ai ruoli e ai profili di sicurezza standard in [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Per ulteriori informazioni sui profili di sicurezza colonne in [!INCLUDE [field-service-short](includes/field-service-short.md)], vai a [Ruoli di sicurezza di Field Service](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Gli amministratori devono aggiungere uno dei profili di sicurezza colonne appropriati agli utenti in Power Platform. Per ulteriori informazioni, vai a [Aggiungere team o utenti a un profilo di sicurezza colonne per controllare l'accesso](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Per utilizzare l'azione **Apri in Business Central** in Vendite, è necessario disporre dei seguenti privilegi per le seguenti tabelle:
>
>* Devi disporre delle autorizzazioni di **lettura** per la tabella **Connessione Dynamics 365 Business Central** (nav_connection).
>* Devi disporre delle autorizzazioni di **lettura**, **scrittura** ed **eliminazione** per la tabella **Connessione Dynamics 365 Business Central predefinita** (nav_defaultconnection).

### <a name="other-settings-in-field-service"></a>Altre impostazioni in Field Service

Nella pagina **Impostazione Field Service**, effettua le seguenti impostazioni:

* Nella scheda **Acquista**, deseleziona il campo **Utilizzo di prodotti esauriti**. In caso contrario, potresti ricevere un avviso "esaurito" quando scegli un prodotto che è esaurito in [!INCLUDE [field-service-short](includes/field-service-short.md)], ma disponibile in [!INCLUDE [prod_short](includes/prod_short.md)].
* Nella scheda **Ordine di lavoro/Prenotazione**, disattiva gli interruttori **Calcola prezzo** e **Calcola costo**. Nel campo **Creazione fattura ordine di lavoro** seleziona **Mai**.

> [!NOTE]
> L'impostazione di una connessione a [!INCLUDE [field-service-short](includes/field-service-short.md)] rimuove l'associazione tra risorse e prodotti. Per rendere gli articoli di [!INCLUDE [prod_short](includes/prod_short.md)] disponibili in [!INCLUDE [field-service-short](includes/field-service-short.md)], aggiorna il campo **Tipo di prodotto Field Service** in modo che corrisponda al campo **Tipo** in [!INCLUDE [prod_short](includes/prod_short.md)]. Per saperne di più, vai a [Creare un prodotto o un servizio](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>Configurare l'integrazione in Business Central

Dopo aver stabilito una connessione a Dataverse e Sales, puoi configurare la tua integrazione con [!INCLUDE [field-service-short](includes/field-service-short.md)]. Nella pagina **Setup assistito** in [!INCLUDE [prod_short](includes/prod_short.md)], scegli **Configura integrazione con Dynamics 365 Field Service** per eseguire la guida al setup assistito. Questa sezione descrive le impostazioni principali nella guida.

Per consentire agli utenti di registrare il consumo di articoli e servizi negli ordini di lavoro di [!INCLUDE [field-service-short](includes/field-service-short.md)], specifica **Modello registrazione progetti** e **Batch registrazioni progetti** da utilizzare per registrere il consumo di prodotti e servizi.

Poiché i servizi sono espressi in durata in [!INCLUDE [field-service-short](includes/field-service-short.md)], specifica l'**Unità di misura ore** da utilizzare per convertire le durate in quantità in [!INCLUDE [prod_short](includes/prod_short.md)].

Puoi anche specificare quando sincronizzare i prodotti e i servizi degli ordini di lavoro con [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, potrebbero sincronizzarsi quando vengono utilizzate righe di ordine di lavoro o quando qualcuno completa un ordine di lavoro. Scegli l'opzione appropriata nel campo **Sincronizza prodotti/servizi per ordine di lavoro**.

Dopo la sincronizzazione dei prodotti e dei servizi dell'ordine di lavoro con le registrazioni progetti in [!INCLUDE [prod_short](includes/prod_short.md)], puoi scegliere se registrare tali registrazioni manualmente. Scegli l'opzione appropriata nel campo **Registra automaticamente righe di registrazione progetto**:

* Quando un ordine di lavoro viene completato.
* Quando vengono utilizzati prodotti o servizi dell'ordine di lavoro.

Dopo aver completato la configurazione, esegui una sincronizzazione completa alla pagina **Impostazione dell'integrazione di Dynamics 365 Field Service**. Questa azione sincronizza il mapping della tabella per cose come:

* Attività di progetto per progetti con **Applica collegamento utilizzo** impostato. Questa sincronizzazione rende i progetti [!INCLUDE [prod_short](includes/prod_short.md)] disponibili per la selezione in [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Le risorse che non sono bloccate, non hanno **Usa foglio presenze** selezionato e hanno **Ore**  specificato come unità di misura nella pagina **Impostazione dell'integrazione di Dynamics 365 Field Service**.
* Articoli di servizio (richiede l'utilizzo dell'esperienza Premium in [!INCLUDE [prod_short](includes/prod_short.md)]).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Mapping delle entità di Field Service standard per la sincronizzazione

La base della sincronizzazione dei dati consiste nel mapping delle tabelle e dei campi in [!INCLUDE [prod_short](includes/prod_short.md)] con tabelle e colonne in Dataverse, di modo che possano scambiarsi i dati. Il mapping avviene tramite tabelle di integrazione. Per ulteriori informazioni sui mapping delle tabelle, vai a [Mapping delle tabelle e dei campi da sincronizzare](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Integrazione con [!INCLUDE [field-service-short](includes/field-service-short.md)]  introduce i seguenti mapping delle tabelle di integrazione standard.

* **PJLINE-WORDERPRODUCT** - Mappa i prodotti dell'ordine di lavoro in [!INCLUDE [field-service-short](includes/field-service-short.md)] alle righe di registrazione progetto in [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE** - Mappa i servizi dell'ordine di lavoro in [!INCLUDE [field-service-short](includes/field-service-short.md)] alle righe delle registrazioni progetti in [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** - Mappa i progetti e le attività di progetto in [!INCLUDE [prod_short](includes/prod_short.md)] ai prodotti in progetti esterni in [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **RESOURCE-BOOKABLERSC** - Mappa le risorse in [!INCLUDE [prod_short](includes/prod_short.md)] alle risorse prenotabili in [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET** - (solo esperienza Premium) Mappa gli articoli di servizio in [!INCLUDE [prod_short](includes/prod_short.md)] alle risorse del cliente in [!INCLUDE [field-service-short](includes/field-service-short.md)].

## <a name="use-data-in-both-applications"></a>Utilizzare i dati in entrambe le applicazioni

Le sezioni seguenti descrivono le funzionalità in cui è possibile utilizzare i dati provenienti da [!INCLUDE [prod_short](includes/prod_short.md)] e [!INCLUDE [field-service-short](includes/field-service-short.md)].

### <a name="field-service-1"></a>Settore servizi

Puoi [creare ordini di lavoro](/dynamics365/field-service/create-work-order) utilizzando **Account di servizio** e **Account di fatturazione** da [!INCLUDE [prod_short](includes/prod_short.md)]. Negli ordini di lavoro, devi selezionare **Attività progetto Business Central** nel campo **Progetto esterno**. La selezione di un progetto consente di sincronizzare i prodotti e i servizi dell'ordine di lavoro con l'attività di progetto appropriata in [!INCLUDE [prod_short](includes/prod_short.md)].

Puoi aggiungere articoli di inventario e non di inventario come **Prodotti ordine di lavoro** in ordini di lavoro e ottenere la giacenza, i costi e i prezzi da [!INCLUDE [prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vai a [Creare un ordine di lavoro dal modulo di ordine di lavoro e dall'elenco di record](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Puoi aggiungere un articolo del tipo servizio come **Servizi per ordini di lavoro** e ottenere costi e prezzi da [!INCLUDE [prod_short](includes/prod_short.md)]. Per saperne di più, vai alla [scheda Prodotti e servizi](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Quando lo stato del prodotto o servizio in un ordine di lavoro passa da **Stimato** a **Usato** in [!INCLUDE [field-service-short](includes/field-service-short.md)], viene sincronizzato con le righe di registrazione progetto in [!INCLUDE [prod_short](includes/prod_short.md)].

Puoi prenotare una risorsa e collegare le **Prenotazioni** ai servizi dell'ordine di lavoro utilizzando una **Risorsa prenotabile** da [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="business-central-1"></a>Business Central

A seconda delle impostazioni nella pagina **Impostazione dell'integrazione di Field Service**, quando gli ordini di lavoro includono prodotti e servizi, le informazioni sul consumo vengono trasferite e registrate utilizzando una **Registrazione progetti** in [!INCLUDE [prod_short](includes/prod_short.md)].

I valori **Quantità da fatturare** e **Durata da fatturare** vengono copiati nel campo **Qtà da trasferire in fattura**. In base a tali valori, puoi creare e registrare fatture di vendita in [!INCLUDE [prod_short](includes/prod_short.md)] per fatturare al cliente. Dopo la registrazione della fattura o l'elaborazione del consumo in [!INCLUDE [prod_short](includes/prod_short.md)], la quantità fatturata e la quantità consumata vengono visualizzate nella scheda [!INCLUDE [prod_short](includes/prod_short.md)] nelle pagine **Prodotto ordine di lavoro** e **Servizio ordini di lavoro**.  

Utilizza la pagina **Righe di pianificazione progetto** per tenere traccia della registrazione e della fatturazione del consumo negli ordini di lavoro. Dalla pagina **Righe di pianificazione progetto** puoi creare e registrare fatture di vendita in [!INCLUDE [prod_short](includes/prod_short.md)]. Successivamente potrai sincronizzarle con [!INCLUDE [field-service-short](includes/field-service-short.md)] e tenere traccia dello stato delle fatture.

> [!NOTE]
> I servizi dell'ordine di lavoro con una prenotazione che utilizza una risorsa prenotabile associata a una risorsa [!INCLUDE [prod_short](includes/prod_short.md)] vengono sincronizzati con due righe di registrazione progetto. Una riga di tipo **Budget** per la risorsa associata e un'altra riga di tipo **Fatturabile** per l'articolo in fase di manutenzione.
>
> Il prodotto scelto nel servizio dell'ordine di lavoro deve essere associato a un articolo di tipo **Servizio** in [!INCLUDE [prod_short](includes/prod_short.md)]. Inoltre, l'unità di misura base per l'articolo deve essere impostata sull'**Unità di misura ore** scelta nella pagina **Impostazione dell'integrazione di Dynamics 365 Field Service**.
>
> Puoi creare una fattura per un articolo di tipo **Servizio** dalla riga di pianificazione del progetto fatturabile e utilizzare la riga di pianificazione del progetto budget per registrare i costi con la risorsa.

## <a name="see-also"></a>Vedere anche

[Integrazione con Microsoft Dataverse tramite la sincronizzazione dei dati](admin-common-data-service.md)  
[Mapping delle tabelle e dei campi da sincronizzare](admin-how-to-modify-table-mappings-for-synchronization.md)

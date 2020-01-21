---
title: Impostazione di account utente per l'integrazione con Dynamics 365 Sales | Microsoft Docs
description: Ottenere informazioni su come impostare account utente che le app utilizzano per scambiare dati e che le persone utilizzano per accedere ai dati nelle app e per sincronizzarli.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 64dd9d1e4645b845c02872a8bc09f0925f4fa33c
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910562"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-sales"></a>Impostazione di account utente per l'integrazione con Dynamics 365 Sales
In questo articolo viene fornita una panoramica su come impostare account utente necessari per integrare [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Impostazione dell'account utente amministratore in Sales
È necessario aggiungere l'account utente amministratore per [!INCLUDE[d365fin](includes/d365fin_md.md)] come utente in [!INCLUDE[crm_md](includes/crm_md.md)] e quindi promuovere l'utente ad amministratore in [!INCLUDE[crm_md](includes/crm_md.md)]. L'account utente amministratore deve anche avere il ruolo Addetto personalizzazione sistema e almeno un altro ruolo utente non amministrativo, ad esempio Manager vendite, in [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Impostazione dell'account utente per l'integrazione
È necessario creare un account utente dedicato nella sottoscrizione di Office 365 che [!INCLUDE[d365fin](includes/d365fin_md.md)] e [!INCLUDE[crm_md](includes/crm_md.md)] possono utilizzare per sincronizzare i dati. Questo account utente deve essere in grado di accedere a [!INCLUDE[crm_md](includes/crm_md.md)], a indicare che tale utente deve avere una licenza per [!INCLUDE[crm_md](includes/crm_md.md)] e almeno un ruolo di sicurezza ad esso assegnato in [!INCLUDE[crm_md](includes/crm_md.md)] come descritto [qui](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Per ulteriori informazioni su come creare utenti in [!INCLUDE[crm_md](includes/crm_md.md)], vedere [Gestire la sicurezza, utenti e team](https://go.microsoft.com/fwlink/?LinkID=616518). Dopo che la connessione è impostata, [!INCLUDE[d365fin](includes/d365fin_md.md)] assegnerà all'account utente i ruoli di sicurezza di cui necessita in [!INCLUDE[d365fin](includes/d365fin_md.md)] e tale account può essere impostato sulla [modalità di accesso non interattiva](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) in [!INCLUDE[crm_md](includes/crm_md.md)]

![Guida al setup assistito che mostra dove immettere le credenziali utente per la sincronizzazione](media/sync-user-setup.png "Visualizzazione della pagina della guida al setup assistito che mostra dove immettere le credenziali utente per la sincronizzazione")

> [!IMPORTANT]  
> Non utilizzare l'account amministratore per [!INCLUDE[crm_md](includes/crm_md.md)] per la sincronizzazione. In caso contrario, la sincronizzazione verrà interrotta.
> Inoltre, per evitare una sincronizzazione costante, le modifiche ai dati eseguite dall'account utente di integrazione non vengono sincronizzate. <!--What changes would this account make?--> Dopo la connessione, si consiglia di impostare la modalità di accesso per l'account utente per l'integrazione sulla modalità non interattiva in [!INCLUDE[crm_md](includes/crm_md.md)]. Per ulteriori informazioni, vedere [Creare un account utente non interattivo](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-salespeople"></a>Impostazione di account per agenti
È necessario creare account utente in [!INCLUDE[crm_md](includes/crm_md.md)] per gli agenti da [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per semplificare tale operazione, l'interfaccia di amministrazione di Microsoft 365 offre un modello di Excel che è possibile utilizzare. Nella pagina **Utenti attivi** scegliere **Altro**, quindi **Importa più utenti**. Scegliere **Scarica un file CSV solo con le intestazioni** e quindi immettere le informazioni per gli agenti. Per visualizzare un esempio, scegliere **Scarica un file CSV con le intestazioni ed esempi di informazioni degli utenti**. Dopo l'immissione delle informazioni relative agli utenti, il passaggio successivo nel processo di importazione consiste nell'assegnare licenze per il piano Dynamics 365 Customer Engagement agli utenti.  

Dopo aver importato gli utenti e assegnato loro le licenze per Dynamics 365 Customer Engagement, è necessario assegnare gli utenti al ruolo **Agente** in [!INCLUDE[crm_md](includes/crm_md.md)].

![Associazione di agenti e utenti in Dynamics 365 Sales](media/couple-salespeople.png "Visualizzazione di agenti e utenti in Dynamics 365 Sales")

## <a name="minimum-permissions-for-user-accounts-in-includecrm_mdincludescrm_mdmd"></a>Autorizzazioni minime per account utente in [!INCLUDE[crm_md](includes/crm_md.md)]
Quando si installa la soluzione di integrazione, le autorizzazioni per l'account utente di integrazione sono configurate in [!INCLUDE[crm_md](includes/crm_md.md)]. Se tali autorizzazioni vengono modificate, potrebbe essere necessario ripristinarle. È possibile farlo reinstallando la soluzione di integrazione o ripristinandole manualmente. Le seguenti tabelle elencano le autorizzazioni minime per gli account utente in [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Amministratore di integrazione
Nella tabella seguente vengono visualizzate le autorizzazioni minime per ogni scheda per ciascun ruolo di sicurezza richiesto per l'utente amministratore.

##### <a name="customization"></a>Personalizzazione
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|App basata su modello|Globale|||Lettura|
|Assembly del plug-in|Globale|Lettura|Lettura|Lettura|
|Tipo di plug-in|Globale|Lettura|Lettura|Lettura|
|Relazione|Globale|||Lettura|
|Messaggio SDK|Globale|Lettura|Lettura|Lettura|
|Passaggio di elaborazione messaggio SDK|Globale|Lettura|Lettura|Lettura|
|Immagine passaggio di elaborazione messaggio SDK|Globale|Lettura|Lettura|Lettura|
|Sistema da|Globale|||Scrittura|

##### <a name="custom-entities"></a>Entità personalizzate
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Statistiche dell'account Business Central|Globale|Lettura|Lettura|Lettura|
|Connessione Business Central|Globale|Creazione, Lettura, Scrittura, Eliminazione|Creazione, Lettura, Scrittura, Eliminazione|Creazione, Lettura, Scrittura, Eliminazione|
|Post-configurazione|Globale|||Scrittura|

#### <a name="integration-user"></a>Utente integrazione
Nella tabella seguente vengono visualizzate le autorizzazioni minime in ogni scheda per ciascun ruolo di sicurezza richiesto per l'utente integrazione.

##### <a name="core-records"></a>Record principali
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Conto|Globale|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a, Assegnazione|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a, Assegnazione|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a, Assegnazione|
|Scheda azione|Globale||Lettura|Lettura|
|Connessione|Globale|Lettura|Lettura|Lettura|
|Contatto|Globale|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|
|Nota|Globale|||Creazione, Lettura, Scrittura, Eliminazione, Aggiunta, Assegnazione|
|Opportunità|Globale||Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|
|Spedizioni postali|Globale|||Creazione, Lettura, Aggiunta a|
|Interfaccia utente entità utente|Utente|Creazione, Lettura, Scrittura|Creazione, Lettura, Scrittura|Creazione, Lettura, Scrittura|

##### <a name="sales"></a>Vendite
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Fattura|Globale|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|
|Ordine|Globale|Lettura, Scrittura, Aggiunta a|Lettura, Scrittura, Aggiunta a|Lettura, Scrittura, Aggiunta, Aggiunta a, Assegnazione|
|Prodotto|Globale|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|
|Proprietà|Globale|Lettura|Lettura|Lettura|
|Associazione proprietà|Globale|Lettura|Lettura|Lettura|
|Elemento Set di opzioni proprietà|Globale|Lettura|Lettura|Lettura|
|Offerta|Globale|Lettura|Lettura|Lettura|

##### <a name="service"></a>Assistenza
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Caso|Globale|Lettura|Lettura|Lettura|

##### <a name="business-management"></a>Gestione aziendale
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Valuta|Globale|Creazione, Lettura, Scrittura|Creazione, Lettura, Scrittura|Creazione, Lettura, Scrittura|
|Organizzazione|Globale|Lettura, Scrittura|Lettura, Scrittura|Lettura, Scrittura|
|Ruolo di sicurezza|Globale|||Lettura|
|Utente|Globale|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta, Aggiunta a|
|Impostazioni utente|Globale|Creazione, Lettura, Scrittura, Eliminazione, Aggiunta a|Creazione, Lettura, Scrittura, Eliminazione, Aggiunta a|Creazione, Lettura, Scrittura, Eliminazione, Aggiunta a|
|Agisce per conto di un altro utente|Globale|Sì|Sì|Sì|

##### <a name="customization"></a>Personalizzazione
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Campo|Globale||Lettura|Lettura|
|Assembly del plug-in|Globale|Lettura|Lettura|Lettura|
|Tipo di plug-in|Globale|Lettura|Lettura|Lettura|
|Messaggio SDK|Globale|Lettura|Lettura|Lettura|
|Passaggio di elaborazione messaggio SDK|Globale|Lettura|Lettura|Lettura|
|Risorsa Web|Globale|Lettura|Lettura|Lettura|

##### <a name="custom-entities"></a>Entità personalizzate
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Statistiche dell'account Dynamics 365 Business Central|Globale|Creazione, Lettura, Scrittura, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta a|
|Connessione di Dynamics 365 Business Central|Globale|Lettura|Lettura|Lettura|

### <a name="product-availability-user"></a>Utente disponibilità prodotto
È possibile consentire agli addetti alle vendite di visualizzare i livelli di magazzino per gli articoli che vendono concedendo agli stessi le autorizzazioni descritte nella tabella seguente.

##### <a name="custom-entities"></a>Entità personalizzate
|Ruolo di sicurezza|Livello di accesso|Dynamics NAV 2018 e versioni precedenti|Business Central <br> Ottobre 2018|Business Central <br> Aprile 2019|
|----|----|-----|----|----|
|Statistiche dell'account Dynamics 365 Business Central|Globale|Creazione, Lettura, Scrittura, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta a|Creazione, Lettura, Scrittura, Aggiunta a|
|Connessione di Dynamics 365 Business Central|Globale|Lettura|Lettura|Lettura|

## <a name="see-also"></a>Vedere anche  
[Integrazione con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

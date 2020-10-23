---
title: Configurazione dei modelli API | Microsoft Docs
description: Descrive i passaggi da seguire per configurare modelli di API per Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: e87809d33fb7fd511912cf6d384db0e488a8ff2d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911607"
---
# <a name="configuring-api-templates"></a>Configurazione di modelli di API
La libreria di API per [!INCLUDE[d365fin_md](includes/d365fin_md.md)] fornisce una rappresentazione semplificata delle entità sottostanti. Tutte le proprietà dell'applicazione non sono esposte tramite l'API associata. La pagina **Setup API** consente di definire modelli utilizzati per popolare le proprietà vuote in un'entità quando si crea un'azione POST tramite l'API. 

Ad esempio, se per l'entità articolo viene definito un modello di configurazione, quando viene creato un nuovo record di articolo tramite l'API articoli, tutte le proprietà per il nuovo articolo che non sono definite nella chiamata API verranno popolate dal modello selezionato. Se, ad esempio, non è definito alcun valore per il campo **Cat. reg. articolo/servizio** tramite l'API, ma un valore è definito nel modello selezionato, al nuovo articolo verrà applicato il valore del gruppo di registrazione definito nel modello. 

## <a name="setting-up-the-entity-template"></a>Impostazione del modello di entità
Per utilizzare i modelli con la libreria di API, è prima necessario definire e impostare le proprietà per i modelli. È possibile impostare questi modelli nella pagina **Modelli di configurazione**. Per ulteriori informazioni, vedere [Preparare la migrazione dei dati dei clienti](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Assegnare il modello a un'API

Per assegnare un modello a un'API, è necessario seguire questi passaggi.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup API** e quindi scegliere il collegamento correlato.
2. Scegliere **Nuovo** e quindi scegliere il valore **Ordine** per importare l'immagine.  
Se è presente più di un modello selezionato per un'API (ID pagina), i modelli vengono applicati nell'ordine definito nella colonna **Order**.   
Quando ciascun modello viene applicato, i valori dei campi definiti nel modello vengono applicati solo ai campi che non hanno ancora definito un valore, esplicitamente nell'API o in un modello precedentemente applicato nell'ordine. 
3. Selezionare un valore **ID pagina**.  
Questa è la pagina per l'API a cui verrà applicato il modello. La ricerca **ID pagina** fornisce un elenco di tutte le API disponibili nella libreria.
4. Selezionare un valore nel campo **Codice modello**.  
Il codice modello è il codice per il modello definito nella pagina **Modelli di configurazione**. I valori del modello definiti vengono applicati all'API. 
5. Nel campo **Condizioni** specificare quale modello deve essere applicato.  
Il modello definito viene applicato a un nuovo record creato tramite l'API se, e solo se, le condizioni definite nel campo **Condizioni** sono soddisfatte dai valori già definiti per la nuova istanza dell'entità.

## <a name="see-also"></a>Vedi anche
[Documentazione API](/dynamics-nav/fin-graph)  
[Sviluppo di app Connect per [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Abilitare le API](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endpoint per le API](/dynamics-nav/endpoints-apis-for-dynamics)  
[Impostazione una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)
---
title: Configurare i modelli di API
description: Descrive i passaggi da seguire per configurare modelli di API per Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'API templates, configuring templates'
ms.search.form: 5469
ms.date: 06/07/2022
ms.author: solsen
---

# <a name="configure-api-templates"></a><a name="configure-api-templates"></a><a name="configure-api-templates"></a>Configurare i modelli di API

La libreria di API per [!INCLUDE[prod_short_md](includes/prod_short.md)] fornisce una rappresentazione semplificata delle entità sottostanti. Tutte le proprietà dell'applicazione non sono esposte tramite l'API associata. La pagina **Setup API** consente di definire modelli utilizzati per popolare le proprietà vuote in un'entità quando si crea un'azione POST tramite l'API. 

Ad esempio, se per l'entità articolo viene definito un modello di configurazione, quando viene creato un nuovo record di articolo tramite l'API articoli, tutte le proprietà per il nuovo articolo che non sono definite nella chiamata API verranno popolate dal modello selezionato. Se, ad esempio, non è definito alcun valore per il campo **Cat. reg. articolo/servizio** tramite l'API, ma un valore è definito nel modello selezionato, al nuovo articolo verrà applicato il valore del gruppo di registrazione definito nel modello. 

## <a name="setting-up-the-entity-template"></a><a name="setting-up-the-entity-template"></a><a name="setting-up-the-entity-template"></a>Impostazione del modello di entità

Per utilizzare i modelli con la libreria di API, è prima necessario definire e impostare le proprietà per i modelli. È possibile impostare questi modelli nella pagina **Modelli di configurazione**. Per ulteriori informazioni, vedi [Migrazione dei dati locali in Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) (solo in inglese) nel contenuto per amministratori.  

## <a name="assign-the-template-to-an-api"></a><a name="assign-the-template-to-an-api"></a><a name="assign-the-template-to-an-api"></a>Assegnare il modello a un'API

Per assegnare un modello a un'API, è necessario seguire questi passaggi.

> [!NOTE]  
> I modelli API possono essere impostati solo con le seguenti pagine API: contatti, countriesRegions, valute, clienti, dipendenti, categorie di articoli, metodi di pagamento, termini di pagamento, metodi di spedizione, unità di misura e fornitori.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup API**, quindi scegli il collegamento correlato.
2. Scegliere **Nuovo** e quindi scegliere il valore **Ordine** per importare l'immagine.  

    Se è presente più di un modello selezionato per un'API (ID pagina), i modelli vengono applicati nell'ordine definito nella colonna **Order**.  

    Quando ciascun modello viene applicato, i valori dei campi definiti nel modello vengono applicati solo ai campi che non hanno ancora definito un valore, esplicitamente nell'API o in un modello precedentemente applicato nell'ordine.  
3. Selezionare un valore **ID pagina**.  

    Questa è la pagina per l'API a cui verrà applicato il modello. La ricerca **ID pagina** fornisce un elenco di tutte le API disponibili nella libreria.
4. Selezionare un valore nel campo **Codice modello**.  

    Il codice modello è il codice per il modello definito nella pagina **Modelli di configurazione**. I valori del modello definiti vengono applicati all'API.  
5. Nel campo **Condizioni** specificare quale modello deve essere applicato.  

    Il modello definito viene applicato a un nuovo record creato tramite l'API se, e solo se, le condizioni definite nel campo **Condizioni** sono soddisfatte dai valori già definiti per la nuova istanza dell'entità.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedi anche

[Documentazione API](/dynamics-nav/fin-graph)  
[Sviluppare Connect Apps per [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Abilitare le API](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endpoint per le API](/dynamics-nav/endpoints-apis-for-dynamics)  
[Amministrazione](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

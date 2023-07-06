---
title: Esplorazione e navigazione delle pagine per ruolo
description: È possibile ottenere una panoramica di tutte le funzionalità aziendali disponibili per il proprio ruolo e per altri ruoli con Esplora ruoli.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
---

# <a name="finding-pages-with-the-role-explorer"></a><a name="finding-pages-with-the-role-explorer"></a><a name="finding-pages-with-the-role-explorer"></a>Ricerca di pagine con Esplora ruoli

È possibile ottenere una panoramica di tutte le funzionalità aziendali disponibili per il proprio ruolo e per altri ruoli. Nella seguente documentazione questa panoramica delle funzionalità viene definita come *Esplora ruoli*.

Ogni elemento in Esplora ruoli è un'azione che apre una pagina. Di conseguenza, è anche possibile utilizzare Esplora ruoli per navigare in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a><a name="open-the-role-explorer"></a><a name="open-the-role-explorer"></a>Aprire l'esploratore di ruoli

È possibile aprire Esplora ruoli da Gestione ruolo utente, da tutte le pagine elenchi e dalla finestra delle **funzionalità delle informazioni**.

- In Gestione ruoli utente o in qualsiasi pagina dell'elenco, scegli il pulsante ![Pulsante Menu.](media/ui_menu_button.png "Pulsante Menu") a destra della barra di spostamento o premi <kbd>Maiusc</kbd>+<kbd>F12</kbd>.
- Nella finestra della **funzionalità delle informazioni**, scegliere l'azione **esplorare** nella parte inferiore.

Quando apri per la prima volta il centro dei ruoli, mostra i collegamenti alla maggior parte delle funzioni disponibili per il tuo ruolo.

## <a name="navigate-features"></a><a name="navigate-features"></a><a name="navigate-features"></a>Navigare le caratteristiche

Le azioni che aprono le pagine sono organizzate in nodi che prendono il nome dalle funzioni o dalle aree di applicazione. È possibile comprimere o espandere ogni nodo singolarmente, così come comprimere/espandere tutti i nodi contemporaneamente.

- Per espandere/collassare un singolo nodo, scegli il nodo. Questa azione viene applicata ai nodi di livello principale e ai nodi secondari.
- Per espandere/collassare tutti i nodi di primo livello della pagina, ma lasciare i sotto-nodi come sono, scegli **...** in alto, poi scegli **Espandi** o **Riduci**.
- Per espandere/collassare tutti i nodi di livello superiore e tutti i sotto nodi sotto di esso, scegli **...** in alto, poi scegli l'azione **Espandi tutto** o **Riduci tutto.** 

## <a name="search-for-features"></a><a name="search-for-features"></a><a name="search-for-features"></a>Cercare le caratteristiche

Per individuare rapidamente le funzioni, seleziona **Trova**, quindi inserisci una parola o una frase per la funzione che stai cercando. Il centro di ruolo evidenzierà qualsiasi testo corrispondente. Se una caratteristica è nascosta alla vista in un nodo collassato, il nodo collassato è segnato con un punto. 

## <a name="explore-other-roles"></a><a name="explore-other-roles"></a><a name="explore-other-roles"></a>Esplora altri ruoli

Per esplorare ruoli diversi dal tuo, seleziona **Esplora altri ruoli**. Il centro dei ruoli visualizza ogni ruolo sotto la propria voce, con collegamenti alle sue caratteristiche. Puoi quindi navigare e trovare le caratteristiche proprio come fai quando esplori il tuo ruolo.

> [!NOTE]
> Vedrai solo i ruoli che sono impostati per essere mostrati nell'esploratore di ruoli. Quindi se non vedete un ruolo che vi aspettavate di vedere, probabilmente non è impostato per questo. Per ulteriori informazioni, vedere [Gestire i profili](admin-users-profiles-roles.md). 

Quando si esplorano altri ruoli, si può anche restringere l'esplorazione utilizzando le azioni **Report e analisi** e **Amministrazione** nella parte superiore del centro dei ruoli.

- **Report e analisi** mostra solo quelle caratteristiche che sono categorizzate come report e caratteristiche di analisi.
- **Amministrazione** mostra solo le caratteristiche che sono categorizzate come caratteristiche di amministrazione.

> [!TIP]
> Per gli sviluppatori, si categorizzano le pagine e i rapporti impostando la [proprietà UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) nel codice AL dell'oggetto.
<!--
 
## <a name="role-explorer-actions"></a><a name="role-explorer-actions"></a><a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a><a name="expand-and-collapse-nodes-on-the-role-explorer"></a><a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Espandere e comprimere i nodi nell'esploratore di ruoli

Le azioni che aprono le pagine sono organizzate in nodi che prendono il nome dalle funzioni o dalle aree di applicazione. È possibile comprimere o espandere ogni nodo singolarmente, così come comprimere/espandere tutti i nodi contemporaneamente.

- Per espandere/comprimere un nodo, selezionare il nodo. Questa azione viene applicata ai nodi di livello principale e ai nodi secondari.
- Per espandere/comprimere tutti i nodi di livello principale nella pagina, selezionare l'azione **Espandi** o **Comprimi** nell'angolo in alto a destra.
- Per espandere/comprimere tutti i nodi di livello superiore e tutti i nodi secondari sottostanti, effettuare uno dei seguenti passaggi:
  - Premi i tasti <kbd>Ctrl</kbd>+<kbd>MAIUSC</kbd> mentre scegli l'azione **Espandi** o **Comprimi** nell'angolo superiore destro.
  - Scegliere **...** nell'angolo superiore destro, quindi scegli l'azione **Espandi tutto** o **Comprimi tutto**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Gestire profili](admin-users-profiles-roles.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

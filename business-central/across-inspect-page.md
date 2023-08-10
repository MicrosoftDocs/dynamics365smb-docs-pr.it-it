---
title: Controllo di pagine in Business Central
description: Utilizzare la funzionalità Controllo pagina per ingrandire i dettagli sulla progettazione della pagina e sull'origine dei dati. Controllo pagina è ideale per la risoluzione dei problemi relativi ai dati.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 04/01/2021
---

# <a name="inspecting-pages-in-business-central"></a>Controllo di pagine in Business Central

La funzionalità Controllo pagina consente di ottenere dettagli su una pagina, fornendo informazioni sulla progettazione della pagina, i differenti elementi della pagina e l'origine dei dati visualizzati. La funzionalità Controllo pagina è specificatamente progettata per amministratori, utenti esperti, personale del supporto e sviluppatori. È ideale per apprendere il modello di dati alla base di una pagina e per la risoluzione di problemi. Ad esempio, in caso di problema con una pagina, si potrebbe utilizzare Controllo pagina per ottenere informazioni da passare all'amministratore di sistema oppure al personale del supporto.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## <a name="work-with-page-inspection"></a>Utilizzare il controllo pagina

L'ispezione della pagina inizia dalla pagina **Guida e supporto**. Scegli il punto interrogativo nell'angolo superiore destro, scegli **Guida e supporto**, quindi scegli **Controllare pagine e dati**. In alternativa, è possibile semplicemente utilizzare i tasti di scelta rapida <kbd>CTRL</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

Il riquadro **Controllo pagina** viene visualizzato sul lato. Quando il riquadro viene aperto per la prima volta, visualizza informazioni relative all'oggetto della pagina principale.

Utilizzare la tastiera o il dispositivo di puntamento per spostare lo stato attivo su elementi differenti nella pagina. Quando si seleziona un riquadro Dettaglio informazioni o una parte nella pagina principale, l'area di delimitazione è evidenziata da un bordo e il riquadro **Controllo pagina** mostra informazioni sull'elemento selezionato. Ad esempio, la figura precedente mostra informazioni su come utilizzare la parte lista nella pagina **Ordine vendita**. Quando ci si sposta ad altre pagine nell'applicazione, il riquadro **Controllo pagina** verrà automaticamente aggiornato con informazioni sulla pagina.

Per ulteriori informazioni relative a quanto visualizzato in Controllo pagina, vedere [Controllo delle pagine e risoluzione dei problemi ad esse relativi](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) nella Guida per sviluppatori e professionisti IT di Business Central.

Se le informazioni previste non sono visualizzate nel riquadro **Controllo pagina**, probabilmente non si dispone delle autorizzazioni necessarie, come descritto nella sezione successiva.

## <a name="controlling-access-to-page-inspection-details"></a>Controllo dell'accesso alle informazioni di controllo pagina

In veste di amministratore, è possibile controllare l'accesso a tutte le informazioni visualizzate nel riquadro **Controllo pagina** configurando le autorizzazioni degli utenti. Per concedere un'autorizzazione per tutte le informazioni a un utente, fornirgli l'autorizzazione **Esegui** per l'oggetto **Sistema** **5330** . È possibile concedere questa autorizzazione utilizzando un set di autorizzazioni (ad esempio **Risoluzione dei problemi di D365**) o un gruppo di utenti (ad esempio **Risoluzione dei problemi di D365**). Per ulteriori informazioni sulle autorizzazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).

Gli utenti a cui non vengono concesse autorizzazioni per l'**Oggetto sistema 5330** possono comunque accedere al riquadro **Controllo pagina**, ma vedranno solo i campi **Pagina** e **Tabella**, che visualizzano dettagli di base che possono passare al team di supporto.

## <a name="see-also"></a>Vedere anche

[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

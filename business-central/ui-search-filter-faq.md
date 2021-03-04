---
title: Informazioni su ricerca e filtro in Business Central
description: Risposte alle domande frequenti relative alla ricerca e al filtro.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 11/16/2020
ms.author: mikebc
ms.openlocfilehash: b993fd047db09b1dc412d9927168aa0233c057a6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756719"
---
# <a name="searching-and-filtering-faq"></a>Domande frequenti su ricerca e filtro
Questo articolo risponde alle domande più frequenti relative alle operazioni di ricerca e filtro.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>C'è differenza tra la ricerca e il filtro?
Sì.
- La ricerca è semplice e ampia: confronta i record che contengono il testo di ricerca in tutti i campi visibili della pagina e non fa distinzione tra maiuscole e minuscole.
- Il filtro è altamente flessibile e può essere applicato a campi specifici, compresi quelli non visibili nella pagina: visualizza i record con corrispondenze esatte, sensibili al maiuscolo/minuscolo, ma può essere regolato con potenti simboli di ricerca, token e formule. Per ulteriori informazioni su come utilizzare tali funzioni, vedere [Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md).

## <a name="exactly-which-fields-are-matched-when-searching"></a>A quali campi vengono applicati i criteri di ricerca?
[!INCLUDE[prod_short](includes/prod_short.md)] applica i criteri di ricerca a tutti i campi visibili nella pagina. Se un campo è stato nascosto, ad esempio utilizzando la personalizzazione, la ricerca non prenderà in considerazione quel campo. I criteri di ricerca vengono applicati ai campi solo se il loro tipo di dati corrisponde a quello dei criteri di ricerca. Ad esempio, se si cerca il termine *oggi*, il valore letterale "oggi" verrà cercato in tutti i campi di testo e codice e anche in qualsiasi campo data dove *oggi* viene valutato come espressione per la data corrente, ma non esegue la ricerca in alcun campo numerico. Per ulteriori informazioni sui criteri di filtro, vedere [Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md#-filter-criteria-and-operators).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Esiste un'esperienza di tastiera per la ricerca e il filtro?
La ricerca e il filtro sono stati notevolmente ottimizzati per gli utenti che preferiscono l'interazione senza mouse per lavorare in modo efficiente con i dati. È disponibile una varietà di tasti di scelta rapida che possono essere utilizzati in sequenza per lavorare ad alta velocità. Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Il riquadro dei filtri è disponibile in tutti gli elenchi?
Il riquadro dei filtri è disponibile nelle pagine in cui l'elenco è il contenuto principale della pagina, come fogli di lavoro e pagine di elenco, inclusi gli elenchi raggiungibili dalla barra di spostamento. Il riquadro filtri non è ancora disponibile per gli elenchi visualizzati come parti, ad esempio Dettaglio informazioni o Gestione ruolo utente o per gli elenchi visualizzati come finestre di dialogo nelle ricerche. Quando un elenco viene incorporato in una pagina, ad esempio delle righe vendita in un ordine di vendita, il riquadro filtri è disponibile quando si sposta lo stato attivo su quell'elenco utilizzando il pulsante modalità stato attivo. Per ulteriori informazioni, vedere [Spostare lo stato attivo su Voci](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Come posso salvare i filtri personali?
I filtri e le modifiche apportate ai filtri predefiniti vengono ricordati durante la sessione (mentre si rimane connessi), anche se si esce dalla pagina. È possibile salvare in modo permanente i filtri come vista con nome dell'elenco selezionando l'icona ![Salva visualizzazione](media/save_view_icon.png "Salva visualizzazione") nel riquadro filtri. Per ulteriori informazioni, vedere [Domande frequenti sulle visualizzazioni elenco](ui-views-faq.md). Si noti che, a differenza dei filtri, il testo di ricerca non viene memorizzato quando si esce da una pagina e non viene salvato quando si salva una visualizzazione.

Nelle pagine di richiesta del report, è anche possibile salvare i filtri o utilizzare filtri predefiniti. Per ulteriori informazioni, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Questa funzionalità è uguale a Filtri avanzati e Limita totali di Microsoft Dynamics NAV?
[!INCLUDE[prod_short](includes/prod_short.md)] si basa su queste note funzionalità e offre un'esperienza moderna e altamente utilizzabile per la ricerca e l'analisi dei dati. Con più tasti di scelta rapida e l'introduzione della ricerca, [!INCLUDE[prod_short](includes/prod_short.md)] supera la funzionalità fornite da Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-add-ins-for-microsoft-365"></a>Posso cercare e filtrare utilizzando le app complementari e i componenti aggiuntivi per Microsoft 365?
Su diverse destinazioni di visualizzazione come i dispositivi mobili o in Outlook, è possibile cercare negli elenchi, ma nella maggior parte dei casi non è possibile filtrare nei singoli campi. Nell'app [!INCLUDE[prod_short](includes/prod_short.md)] per Microsoft Teams, sia la ricerca che il filtro sono disponibili negli elenchi.

## <a name="how-do-i-view-how-my-search-terms-have-been-applied-to-fields-in-the-list"></a>Come visualizzo il modo in cui i termini di ricerca sono stati applicati ai campi nell'elenco?
Dopo aver immesso i termini di ricerca nella casella di ricerca, è possibile visualizzare i criteri di ricerca esatti e i campi a cui sono stati applicati aprendo il riquadro di ispezione della pagina (**CTRL + ALT + F1**) e scegliendo la scheda **Filtri di pagina**.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Quali azioni posso intraprendere per il messaggio "La ricerca delle righe richiede troppo tempo"?

Esiste un limite di tempo su quanto può durare un'operazione di ricerca. Innanzitutto, provare a cambiare i criteri di ricerca e cercare di nuovo. Se si utilizza [!INCLUDE[prod_short](includes/prod_short.md)] in locale, contattare l'amministratore di sistema, poiché un amministratore può aumentare il limite di tempo per le ricerche.

In qualità di amministratore locale, è possibile aumentare il limite di tempo per le ricerche modificando l' impostazione **Timeout ricerca** del server [!INCLUDE[prod_short](includes/prod_short.md)]. Per ulteriori informazioni, vedere [Configurazione di Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) nella Guida di Business Central per sviluppatori e professionisti IT.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Microsoft estenderà l'esperienza del riquadro dei filtri?
In Microsoft, i feedback della nostra variegata comunità di utenti vengono costantemente monitorati e si agisce in base ai migliori suggerimenti della community. Se si è interessati a estendere il riquadro dei filtri a più fattori di forma e più tipi di elenchi o si hanno suggerimenti utili per migliorarlo, è possibile aggiungere un'idea o votare le idee esistenti su [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="see-also"></a>Vedere anche
[Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Ricerca di pagine con Esplora ruoli](ui-role-explorer.md)  
[Introduzione](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
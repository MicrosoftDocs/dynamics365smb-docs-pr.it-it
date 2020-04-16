---
title: Informazioni su ricerca e filtro in Business Central
description: Risposte alle domande frequenti relative alla ricerca e al filtro.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 04/01/2020
ms.author: mikebc
ms.openlocfilehash: 3021cd73ad3f737596c542aaa4989aa9741a7ef8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195777"
---
# <a name="searching-and-filtering-faq"></a>Domande frequenti su ricerca e filtro
Questo articolo risponde alle domande più frequenti relative alle operazioni di ricerca e filtro.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>C'è differenza tra la ricerca e il filtro?
Sì.
- La ricerca è semplice e ampia: confronta i record che contengono il testo di ricerca in tutti i campi visibili della pagina e non fa distinzione tra maiuscole e minuscole.
- Il filtro è altamente flessibile e può essere applicato a campi specifici, compresi quelli non visibili nella pagina: visualizza i record con corrispondenze esatte, sensibili al maiuscolo/minuscolo, ma può essere regolato con potenti simboli di ricerca, token e formule. Per ulteriori informazioni su come utilizzare tali funzioni, vedere [Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Esiste un'esperienza di tastiera per la ricerca e il filtro?
La ricerca e il filtro sono stati notevolmente ottimizzati per gli utenti che preferiscono l'interazione senza mouse per lavorare in modo efficiente con i dati. È disponibile una varietà di tasti di scelta rapida che possono essere utilizzati in sequenza per lavorare ad alta velocità. Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Il riquadro dei filtri è disponibile in tutti gli elenchi?
Il riquadro dei filtri è disponibile nelle pagine in cui l'elenco è il contenuto principale della pagina, come fogli di lavoro e pagine di elenco, inclusi gli elenchi raggiungibili dalla barra di spostamento. Il riquadro filtri non è ancora disponibile per gli elenchi visualizzati come parti, ad esempio Dettaglio informazioni o Gestione ruolo utente. Quando un elenco viene incorporato in una pagina, ad esempio delle righe vendita in un ordine di vendita, il riquadro filtri è disponibile quando si sposta lo stato attivo su quell'elenco utilizzando il pulsante modalità stato attivo. Per ulteriori informazioni, vedere [Spostare lo stato attivo su Voci](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Come posso salvare i filtri personali?
I filtri e le modifiche apportate ai filtri predefiniti vengono ricordati durante la sessione (mentre si rimane connessi), anche se si esce dalla pagina. È possibile salvare in modo permanente i filtri come vista con nome dell'elenco selezionando l'icona ![Salva visualizzazione](media/save_view_icon.png "Salva visualizzazione") nel riquadro filtri. Per ulteriori informazioni, vedere [Domande frequenti sulle visualizzazioni elenco](ui-views-faq.md). Si noti che, a differenza dei filtri, il testo di ricerca non viene memorizzato quando si esce da una pagina e non viene salvato quando si salva una visualizzazione.

Nelle pagine di richiesta del report, è anche possibile salvare i filtri o utilizzare filtri predefiniti. Per ulteriori informazioni, vedere [Uso delle impostazioni salvate](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Questa funzionalità è uguale a Filtri avanzati e Limita totali di Microsoft Dynamics NAV?
[!INCLUDE[d365fin](includes/d365fin_md.md)] si basa su queste note funzionalità e offre un'esperienza moderna e altamente utilizzabile per la ricerca e l'analisi dei dati. Con più tasti di scelta rapida e l'introduzione della ricerca, [!INCLUDE[d365fin](includes/d365fin_md.md)] supera la funzionalità fornite da Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Posso cercare e filtrare utilizzando le app complementari e il componente aggiuntivo di Outlook?
Su diverse destinazioni di visualizzazione come i dispositivi mobili o in Outlook, è possibile cercare negli elenchi, ma nella maggior parte dei casi non è possibile filtrare nei singoli campi.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Microsoft estenderà l'esperienza del riquadro dei filtri?
In Microsoft, i feedback della nostra variegata comunità di utenti vengono costantemente monitorati e si agisce in base ai migliori suggerimenti della community. Se si è interessati a estendere il riquadro dei filtri a più fattori di forma e più tipi di elenchi o si hanno suggerimenti utili per migliorarlo, è possibile aggiungere un'idea o votare le idee esistenti su [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Quali azioni posso intraprendere per il messaggio "La ricerca delle righe richiede troppo tempo"?

Esiste un limite di tempo su quanto può durare un'operazione di ricerca. Innanzitutto, provare a cambiare i criteri di ricerca e cercare di nuovo. Se si utilizza [!INCLUDE[prodshort](includes/prodshort.md)] in locale, contattare l'amministratore di sistema, poiché un amministratore può aumentare il limite di tempo per le ricerche.

In qualità di amministratore locale, è possibile aumentare il limite di tempo per le ricerche modificando l' impostazione **Timeout ricerca** del server [!INCLUDE[prodshort](includes/prodshort.md)]. Per ulteriori informazioni, vedere [Configurazione di Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) nella Guida di Business Central per sviluppatori e professionisti IT.

## <a name="see-also"></a>Vedere anche
[Ricerca, filtro e ordinamento](ui-enter-criteria-filters.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Ricerca di pagine con Esplora ruoli](ui-role-explorer.md)  
[Introduzione](product-get-started.md)  

---
title: Informazioni su ricerca e filtro in Business Central
description: Risposte alle domande frequenti relative alla ricerca e al filtro.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 06/03/2019
ms.author: mikebc
ms.openlocfilehash: a4e33c2f1598f4e3ff659302f046b32656edb81a
ms.sourcegitcommit: 0854c074b500c3031eaf86fde9d452f93f238081
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2019
ms.locfileid: "1701177"
---
# <a name="searching-and-filtering-faq"></a>Domande frequenti su ricerca e filtro
Questo articolo risponde alle domande più frequenti relative alle operazioni di ricerca e filtro.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>C'è differenza tra la ricerca e il filtro?
Sì.
- La ricerca è semplice e ampia: confronta i record che contengono il testo di ricerca in tutti i campi visibili della pagina e non fa distinzione tra maiuscole e minuscole.
- Il filtro è altamente flessibile e può essere applicato a campi specifici, compresi quelli non visibili nella pagina: visualizza i record con corrispondenze esatte, sensibili al maiuscolo/minuscolo, ma può essere regolato con potenti simboli di ricerca, token e formule. Per ulteriori informazioni su come utilizzare tali funzioni, vedere [Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Esiste un'esperienza di tastiera per la ricerca e il filtro?
La ricerca e il filtro sono stati notevolmente ottimizzati per gli utenti che preferiscono l'interazione senza mouse per lavorare in modo efficiente con i dati. È disponibile una varietà di tasti di scelta rapida che possono essere utilizzati in sequenza per lavorare ad alta velocità. Per ulteriori informazioni, vedere [Tasti di scelta rapida](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Il riquadro dei filtri è disponibile in tutti gli elenchi?
Il riquadro dei filtri è disponibile nelle pagine in cui l'elenco è il contenuto principale della pagina, come fogli di lavoro e pagine di elenco, inclusi gli elenchi raggiungibili dalla barra di spostamento. Il riquadro filtri non è ancora disponibile per gli elenchi visualizzati come parti, ad esempio Dettaglio informazioni o Gestione ruolo utente. Quando un elenco viene incorporato in una pagina, ad esempio delle righe vendita in un ordine di vendita, il riquadro filtri è disponibile quando si sposta lo stato attivo su quell'elenco utilizzando il pulsante modalità stato attivo. Per ulteriori informazioni, vedere [Spostare lo stato attivo su Voci](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Come posso salvare i filtri personali?

I filtri e le modifiche apportate ai filtri predefiniti vengono ricordati durante la sessione (mentre si rimane connessi), anche se si esce dalla pagina. Al momento non è possibile salvare i filtri in modo permanente. A differenza dei filtri, il testo di ricerca non viene memorizzato quando si esce da una pagina.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Questa funzionalità è uguale a Filtri avanzati e Limita totali di Microsoft Dynamics NAV?

[!INCLUDE[d365fin](includes/d365fin_md.md)] si basa su queste note funzionalità e offre un'esperienza moderna e altamente utilizzabile per la ricerca e l'analisi dei dati. Con più tasti di scelta rapida e l'introduzione della ricerca, [!INCLUDE[d365fin](includes/d365fin_md.md)] supera la funzionalità fornite da Dynamics NAV.  

Vedere anche [Il riquadro dei filtri è disponibile per filtrare i report?](#is-the-filter-pane-available-for-filtering-reports).  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Posso cercare e filtrare utilizzando le app complementari e il componente aggiuntivo di Outlook?
Su diverse destinazioni di visualizzazione come i dispositivi mobili o in Outlook, è possibile cercare negli elenchi, ma nella maggior parte dei casi non è possibile filtrare nei singoli campi.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Il riquadro dei filtri è disponibile per filtrare i report?
No. La finestra di dialogo del filtro dei report, comunemente denominata pagina di richiesta, utilizza attualmente un'esperienza diversa che fornisce alcune, ma non tutte, le funzionalità del riquadro dei filtri.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Microsoft estenderà l'esperienza del riquadro dei filtri?
In Microsoft, i feedback della nostra variegata comunità di utenti vengono costantemente monitorati e si agisce in base ai migliori suggerimenti della community. Se si è interessati a estendere il riquadro dei filtri a più fattori di forma, a più tipi di elenchi e report o se ci sono utili suggerimenti di miglioramento, è possibile aggiungere un'idea o votare le idee esistenti su [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Quali azioni posso intraprendere per il messaggio "La ricerca delle righe richiede troppo tempo"?

Esiste un limite di tempo su quanto può durare un'operazione di ricerca. Innanzitutto, provare a cambiare i criteri di ricerca e cercare di nuovo. Se si utilizza [!INCLUDE[prodshort](includes/prodshort.md)] in locale, contattare l'amministratore di sistema, poiché un amministratore può aumentare il limite di tempo per le ricerche.

In qualità di amministratore locale, è possibile aumentare il limite di tempo per le ricerche modificando l' impostazione **Timeout ricerca** del server [!INCLUDE[prodshort](includes/prodshort.md)]. Per ulteriori informazioni, vedere [Configurazione di Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) nella Guida di Business Central per sviluppatori e professionisti IT.

## <a name="see-also"></a>Vedere anche

[Introduzione](product-get-started.md)  
[Ricerca, filtro e ordinamento di elenchi](ui-enter-criteria-filters.md)  

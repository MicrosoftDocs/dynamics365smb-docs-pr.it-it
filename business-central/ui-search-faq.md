---
title: Domande frequenti relative alle informazioni | Documenti Microsoft
description: Questo articolo risponde alle domande che i partner e i clienti spesso chiedono sulla nuova funzione delle informazioni.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d04f78b31b9fb0403201cb9e5cb1f98f1ef935e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248015"
---
# <a name="tell-me-faq"></a>Domande frequenti relative alle informazioni
Questo argomento risponde alle domande che gli utenti avanzati spesso pongono sulla nuova funzionalità delle informazioni, che ha sostituito la precedente funzionalità di ricerca della pagina nota come **Trova pagine e report**.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Tutte le azioni della pagina corrente sono individuabili nelle informazioni?
No. Le azioni in parti, come la parte relativa alle righe di vendita o riquadri Dettaglio informazioni, non vengono visualizzate nelle informazioni.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>I risultati vengono filtrati in base alle autorizzazioni?
Se l'utente non dispone di AccessByPermissions, le azioni non vengono visualizzate. Tuttavia, le pagine e i report vengono visualizzati nei risultati ma richiedono che l'utente disponga dell'autorizzazione per accedervi. Un messaggio verrà visualizzato se l'utente non dispone dell'autorizzazione per visualizzare l'oggetto.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Le informazioni mostrano i contenuti delle personalizzazioni o delle estensioni di terze parti installate?
Le azioni, le pagine e i report che provengono da estensioni vengono acquisiti dalle informazioni, ma non la documentazione della guida personalizzata. Per informazioni tecniche su come rendere visibili le pagine e i report personalizzati, vedere [Aggiunta di pagine e report alla ricerca](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Quali sono le differenze dalla funzionalità precedente di ricerca della pagina?
La ricerca della pagina si è evoluta nelle informazione per aiutare a svolgere rapidamente il lavoro. La ricerca della pagina potrebbe essere utile per passare a pagine o report. A livello tecnico, le informazioni non si basano più sul concetto di MenuSuite precedente.

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a>Utilizzo [!INCLUDE[d365fin](includes/d365fin_md.md)] in locale. La funzionalità delle informazioni è inclusa.
È possibile utilizzare le informazioni nel client Web locale per trovare azioni, pagine e report, ma non documentazione oppure app e servizi di consulenza su AppSource. Gli utenti che si connettono a [!INCLUDE[d365fin](includes/d365fin_md.md)] dal client Dynamics NAV continuano a utilizzare la ricerca della pagina.

### <a name="is-tell-me-available-for-all-form-factors"></a>Le informazioni sono disponibili per tutti i fattori di forma?
Le informazioni sono disponibili solo nel client Web o nell'app desktop di Windows.

### <a name="are-the-documentation-results-available-in-any-language"></a>I risultati della documentazione sono disponibili in tutte le lingue?
Gli articoli della guida vengono visualizzati nella lingua specificata in **Impostazioni personali**, se la guida è disponibile in tale lingua.

## <a name="see-also"></a>Vedi anche  
[Individuazione di funzionalità e informazioni](ui-search.md)

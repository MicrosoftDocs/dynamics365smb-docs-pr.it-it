---
title: Domande frequenti relative alla funzionalità delle informazioni | Documenti Microsoft
description: Questo articolo risponde alle domande che i partner e i clienti spesso chiedono sulla nuova funzionalità delle informazioni.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 88a1e6cc711888a3cf68744d0ea6bbfdee41aea3
ms.sourcegitcommit: 49309bdff9b680a35032b355fe97c565845dba15
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2695097"
---
# <a name="tell-me-faq"></a>Domande frequenti relative alla funzionalità delle informazioni
Questo argomento risponde alle domande poste spesso dai nostri utenti esperti sulla funzionalità delle informazioni.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Tutte le azioni della pagina corrente sono individuabili nella funzionalità delle informazioni?
No. Le azioni in parti, come la parte relativa alle righe di vendita o riquadri Dettaglio informazioni, non vengono visualizzate nella funzionalità delle informazioni.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>I risultati nella funzionalità delle informazioni vengono filtrati in base alle autorizzazioni?
Se l'utente non dispone di AccessByPermissions, le azioni non vengono visualizzate. Tuttavia, le pagine e i report vengono visualizzati nei risultati ma richiedono che l'utente disponga dell'autorizzazione per accedervi. Un messaggio verrà visualizzato se l'utente non dispone dell'autorizzazione per visualizzare l'oggetto.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>La funzionalità delle informazioni visualizza i contenuti delle personalizzazioni o delle estensioni di terze parti installate?
Le azioni, le pagine e i report che provengono da estensioni vengono acquisiti tramite la funzionalità delle informazioni, ma non la documentazione della guida personalizzata. Per informazioni tecniche su come rendere visibili le pagine e i report personalizzati, vedere [Aggiunta di pagine e report alla ricerca](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Quali sono le differenze dalla funzionalità precedente di ricerca della pagina?
La ricerca della pagina si è evoluta nella funzionalità delle informazioni per aiutare a svolgere rapidamente il lavoro. La ricerca della pagina potrebbe essere utile per passare a pagine o report. A livello tecnico, la funzionalità delle informazioni non si basa più sul concetto di MenuSuite precedente.

### <a name="i-use-on-premises-included365finincludesd365fin_mdmd-does-that-include-tell-me"></a>Utilizzo [!INCLUDE[d365fin](includes/d365fin_md.md)] in locale. La funzionalità delle informazioni è inclusa.
È possibile utilizzare la funzionalità delle informazioni nel client Web locale per trovare azioni, pagine e report, ma non documentazione oppure app e servizi di consulenza su AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>La funzionalità delle informazioni è disponibile per tutti i fattori di forma?
La funzionalità delle informazioni è disponibile solo nel client Web o nell'app desktop di Windows.

### <a name="are-the-documentation-results-available-in-any-language"></a>I risultati della documentazione sono disponibili in tutte le lingue?
Gli articoli della guida vengono visualizzati nella lingua specificata in **Impostazioni personali**, se la guida è disponibile in tale lingua.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Perché l'icona segnalibro non è visibile per i risultati della ricerca?
L'icona segnalibro non viene visualizzata nella finestra della funzionalità delle informazioni quando la personalizzazione è disabilitata per un ruolo utente.

### <a name="is-the-bookmark-icon-available-for-reports"></a>L'icona segnalibro è disponibile per i report?
No. È possibile aggiungere un segnalibro solo a un collegamento a una pagina o a qualsiasi risultato di ricerca visualizzato nella sezione **Pagine e task** della finestra della funzionalità delle informazioni.


## <a name="see-also"></a>Vedere anche  
[Salvare e personalizzare visualizzazioni elenco](ui-views.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Ricerca di pagine con Esplora ruoli](ui-role-explorer.md)

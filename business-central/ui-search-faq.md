---
title: Domande frequenti relative alla funzionalità delle informazioni
description: Questo articolo risponde alle domande che i partner e i clienti spesso chiedono sulla funzionalità delle informazioni.
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 03/20/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# <a name="tell-me-faq"></a>Domande frequenti relative alla funzionalità delle informazioni

Questo articolo risponde alle domande poste spesso dai nostri utenti esperti sulla funzionalità Informazioni sull'operazione che si desidera eseguire.

## <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Tutte le azioni della pagina corrente sono individuabili nella funzionalità delle informazioni?

No. Le azioni in parti, come la parte relativa alle righe di vendita o riquadri Dettaglio informazioni, non vengono visualizzate nella funzionalità delle informazioni.

## <a name="can-i-search-for-a-specific-record"></a>Posso cercare un record specifico?

Sì. Ad esempio, se desideri trovare rapidamente un ordine di vendita, immetti il relativo identificatore, quindi scegli l'azione **Ricerca nei dati della società**. Se conosci solo il nome del cliente, immettilo. La funzionalità delle informazioni organizza i risultati per tipo, in modo da poter trovare l'ordine nella categoria Ordini di vendita.

## <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>I risultati nella funzionalità delle informazioni vengono filtrati in base alle autorizzazioni?

Se l'utente non dispone di AccessByPermissions, le azioni non vengono visualizzate. Tuttavia, le pagine e i report vengono visualizzati nei risultati ma richiedono che l'utente disponga dell'autorizzazione per accedervi. Un messaggio viene visualizzato se l'utente non dispone dell'autorizzazione per visualizzare l'oggetto.

## <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>La funzionalità delle informazioni visualizza i contenuti delle personalizzazioni o delle estensioni di terze parti installate?

Le azioni, le pagine e i report che provengono da estensioni vengono acquisiti tramite la funzionalità delle informazioni. Per informazioni tecniche su come rendere visibili le pagine e i report personalizzati, vedere [Aggiunta di pagine e report alla ricerca](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Quali sono le differenze dalla funzionalità precedente di ricerca della pagina?

La ricerca della pagina si è evoluta nella funzionalità delle informazioni per aiutare a svolgere rapidamente il lavoro. La ricerca della pagina potrebbe essere utile per passare a pagine o report. A livello tecnico, la funzionalità delle informazioni non si basa più sul concetto di MenuSuite precedente.

## <a name="i-use-on-premises--does-that-include-tell-me"></a>Utilizzo [!INCLUDE[prod_short](includes/prod_short.md)] in locale. La funzionalità delle informazioni è inclusa.

È possibile utilizzare la funzionalità delle informazioni nel client Web locale per trovare azioni, pagine e report, ma non app e servizi di consulenza su AppSource.

## <a name="is-tell-me-available-for-all-form-factors"></a>La funzionalità delle informazioni è disponibile per tutti i fattori di forma?

Sì. È stata introdotta in telefoni e tablet nel secondo ciclo di rilascio di Business Central 2023. Nel secondo ciclo di rilascio del 2023, deve essere abilitata in [Gestione funzionalità](/dynamics365/business-central/dev-itpro/administration/feature-management) usando l'interruttore **Funzionalità: ricerca di pagine e dati nell'app per dispositivi mobili**. Nel primo ciclo di rilascio del 2024 e successivi, è sempre abilitata.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language"></a>Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>La funzionalità delle informazioni mi fornisce aiuto su come utilizzare pagine, report e altre cose?

No, ma puoi facilmente ottenere queste informazioni dal riquadro della Guida. Basta selezionare l'azione **Cercare nella Guida** nella pagina **Informazioni sull'operazione che si desidera eseguire** o selezionare <kbd>CTRL</kbd>+<kbd>F1</kbd> sulla tastiera. Per saperne di più sul riquadro della Guida, vedi [Riquadro della Guida](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Perché l'icona segnalibro non è visibile per i risultati della ricerca?

L'icona segnalibro non viene visualizzata nella finestra della funzionalità delle informazioni quando la personalizzazione è disabilitata per un ruolo utente.

## <a name="see-also"></a>Vedere anche

[Salvare e personalizzare visualizzazioni elenco](ui-views.md)  
[Individuare pagine e informazioni con la funzionalità delle informazioni](ui-search.md)  
[Ricerca di pagine con Esplora ruoli](ui-role-explorer.md)  
[Aggiungere un segnalibro a una pagina o un report in Gestione ruolo utente](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

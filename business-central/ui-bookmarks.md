---
title: Aggiungi ai preferiti collegare alla pagina o al report sul centro ruoli
description: 'Utilizzando l''icona del segnalibro, puoi aggiungere un''azione che apre una pagina o un report dal menu di navigazione del tuo centro gestione ruoli.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Aggiungi ai preferiti una pagina o un report sul tuo centro ruoli

Utilizzando l'icona del segnalibro, puoi aggiungere un'azione che apre una pagina o un report dal menu di navigazione del tuo centro gestione ruoli. I segnalibri consentono di raggiungere rapidamente i contenuti o le attività aziendali preferiti. Aggiungi il segnalibro dalla pagina o dal report di destinazione, ovvero dalla schermata che vuoi che collegare apra nel centro gestione ruolo.

L'icona segnalibro è visualizzata nell'angolo in alto a destra di una pagina e anche nella finestra della **funzionalità delle informazioni** in cui puoi contrassegnare correttamente più pagine o report. Se un segnalibro esiste per la pagina, l'icona è scura e la descrizione comandi indica "Con segnalibro".

## <a name="bookmark-the-target-page"></a>Aggiungi ai preferiti la pagina di destinazione

1. Apri una pagina qualsiasi per cui desideri un collegare nel tuo centro gestione ruolo.
2. Scegli l'icona ![Segnalibro.](media/ui_bookmark_icon.png "Segnalibro") .

Un'azione denominata come la pagina è ora aggiunta al menu di navigazione nel tuo centro gestione ruolo.

## <a name="bookmark-the-target-report"></a>Aggiungi ai preferiti il report di destinazione

1. Apri una pagina di richiesta report per la quale desideri un collegare nel tuo centro gestione ruolo.
2. Scegli l'icona ![Segnalibro.](media/ui_bookmark_icon.png "Segnalibro") .

Un'azione denominata in base al report è ora aggiunta al menu di navigazione nel tuo centro gestione ruolo.

## <a name="bookmark-a-page-or-report-from-the-tell-me-window"></a>Aggiungi ai preferiti una pagina o un report dalla finestra Dimmi

1. Aprire la finestra della **funzionalità delle informazioni** e immettere, ad esempio, **Ordini vendita**.
2. Passa il mouse sopra il risultato della ricerca per la pagina o il report **Ordini vendita**, quindi scegli l'icona ![Segnalibro.](media/ui_bookmark_icon.png "Segnalibro") .

Un'azione denominata in base alla pagina o al report viene ora aggiunta al menu di navigazione nel tuo centro gestione ruolo.

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="can-i-reorganize-my-bookmarks"></a>Posso riorganizzare i miei segnalibri?

Sì. Puoi personalizzare il tuo centro ruoli e spostare le azioni in una sequenza più ottimale oppure spostarle in gruppi o sottogruppi esistenti.  
Informazioni su come [personalizzare l'area di lavoro](ui-personalization-user.md).

### <a name="how-do-i-remove-a-bookmark"></a>Come faccio a rimuovere un segnalibro?

Nella pagina o nel report di destinazione, seleziona nuovamente l'icona del segnalibro per rimuovere l'azione interessata dal tuo centro gestione ruolo. Puoi anche personalizzare il tuo centro ruoli e nascondere temporaneamente le azioni senza rimuoverle completamente.

### <a name="where-do-i-find-my-bookmarks"></a>Dove trovo i miei segnalibri?

Quando aggiungi un segnalibro a una pagina o a un report, la nuova azione viene aggiunta al menu di navigazione in alto nella schermata iniziale corrente (Centro gestione ruoli). Se sono presenti molte azioni, potrebbe essere necessario attivare il pulsante **Altro** per visualizzarle tutte perché la nuova azione viene sempre aggiunta alla fine dell'elenco.
<!-- Should we add a screenshot here? -->

### <a name="i-dont-have-a-bookmark-icon-is-something-wrong"></a>Non è presente un'icona segnalibro. Si è verificato un errore?

La possibilità di aggiungere un segnalibro a una pagina o un report è una delle molte funzionalità di personalizzazione per gli utenti in Business Central. Se l'icona del segnalibro non viene visualizzata, è probabile che l'amministratore abbia disabilitato la personalizzazione.

### <a name="why-cant-i-bookmark-certain-pages-or-reports"></a>Perché non riesco a aggiungere ai preferiti determinate pagine o report?

Non a tutte le pagine e i report possono essere aggiunti i segnalibri. Quando una pagina o un report viene eseguito in un contesto speciale regolato dall'applicazione aziendale, l'icona del segnalibro non viene visualizzata. Ad esempio, nelle pagine che non sono presenti nella finestra della **funzionalità delle informazioni** ma vengono avviate altrove non è visualizzata l'icona del segnalibro. Allo stesso modo, le pagine di richiesta report che vengono utilizzate solo per raccogliere i filtri senza eseguire il report non includono l'icona del segnalibro.

  Vedere i dettagli tecnici su [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) e [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

### <a name="when-clearing-my-personalization-will-my-bookmarks-also-be-cleared"></a>Quando elimino la mia personalizzazione, verranno cancellati anche i miei segnalibri?

Sì. I segnalibri si trovano nel menu di navigazione. Se cancelli le modifiche al menu di navigazione da una pagina qualsiasi o cancelli tutte le personalizzazioni nel centro gestione ruolo, tutte le nuove azioni verranno rimosse definitivamente.

### <a name="why-does-the-bookmark-icon-continue-to-indicate-its-still-not-bookmarked"></a>Perché l'icona del segnalibro continua a indicare che il segnalibro non è ancora stato aggiunto?

Quando aggiungi un segnalibro, la nuova azione viene aggiunta al menu di navigazione nel centro gestione ruoli e le visite successive alla pagina o al report mostrano un'icona di segnalibro scura. Se personalizzi il tuo centro ruoli e riorganizzi le tue azioni spostandole in gruppi, l'icona del segnalibro non sarà più scura e potrai aggiungere un altro segnalibro alla stessa pagina o report. Ciò consente di aggiungere più azioni alla stessa pagina o report e classificarle in gruppi diversi.

### <a name="why-does-my-link-to-a-report-display-a-different-report"></a>Perché il mio collegare in un report visualizza un report diverso?

Alcuni report possono essere sostituiti da altri report dopo aver applicato un'estensione a Business Central. Quando si verifica la sostituzione, il testo della nuova azione non viene aggiornato e continua a visualizzare il nome del report originale, ma passa al report più recente. Per correggere il testo della nuova azione, è possibile rimuovere la nuova azione e aggiungerla di nuovo.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

### <a name="is-bookmarking-available-for-xmlports"></a>È disponibile la funzione bookmarking per XMLports?

No. Al momento, non è possibile aggiungere azioni per aprire XMLports dall'interfaccia utente.

### <a name="will-my-bookmarks-be-translated-when-i-change-my-language-in-business-central"></a>I miei segnalibri verranno tradotti quando cambio la lingua in Business Central?

Quando viene aggiunta una nuova azione, qualsiasi testo tradotto disponibile in quel momento viene contrassegnato con un segnalibro. Se il nuovo testo tradotto viene aggiunto in un secondo momento, la nuova azione non includerà le traduzioni più recenti.

### <a name="why-cant-i-add-text-in-a-page-right-after-opening-it-with-the-bookmark"></a>Perché non posso aggiungere testo direttamente in una pagina dopo averla aperta con il segnalibro?

Quando una pagina è aggiunta ai segnalibri, la pagina si aprirà sempre in modalità di visualizzazione dal segnalibro, anche se era in modalità di modifica quando è stata aggiunta ai segnalibri. Selezionando l'icona **Apportare le modifiche nella pagina** ![Mostra l'icona della matita per modificare la pagina.](media/edit-pencil.png) ti consentirà di aggiungere testo nei campi modificabili.

## <a name="see-also"></a>Vedere anche

[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modificare le funzionalità visualizzate](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

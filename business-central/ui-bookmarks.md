---
title: Aggiungere un collegamento a segnalibro a una pagina o un report in Gestione ruolo utente
description: 'Utilizzando la nuova icona segnalibro, è possibile aggiungere un''azione che apre una pagina o un report dal menu di navigazione di Gestione ruolo utente.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="bookmark-a-page-or-report-on-your-role-center"></a><a name="bookmark-a-page-or-report-on-your-role-center"></a>Aggiungere un segnalibro a una pagina o un report in Gestione ruolo utente
Utilizzando la nuova icona segnalibro, è possibile aggiungere un'azione che apre una pagina o un report dal menu di navigazione di Gestione ruolo utente. I segnalibri consentono di raggiungere rapidamente i contenuti o le attività aziendali preferiti. Si aggiunge il segnalibro dalla pagina o dal report di destinazione, ovvero la schermata che deve essere aperta con il collegamento in Gestione ruolo utente.

L'icona segnalibro è visualizzata nell'angolo in alto a destra di una pagina e anche nella finestra della **funzionalità delle informazioni** in cui puoi contrassegnare correttamente più pagine o report. Se un segnalibro esiste per la pagina, l'icona è scura e la descrizione comandi indica "Con segnalibro".

## <a name="to-bookmark-the-target-page"></a><a name="to-bookmark-the-target-page"></a>Per aggiungere un segnalibro alla pagina di destinazione
1. Aprire qualsiasi pagina per la quale si desidera un collegamento in Gestione ruolo utente.
2. Scegli l'icona ![Segnalibro.](media/ui_bookmark_icon.png "Segnalibro") .

Un'azione denominata come la pagina viene aggiunta al menu di navigazione in Gestione ruolo utente.

## <a name="to-bookmark-the-target-report"></a><a name="to-bookmark-the-target-report"></a>Per aggiungere un segnalibro al report di destinazione
1. Aprire qualsiasi pagina di richiesta report per la quale si desidera un collegamento in Gestione ruolo utente.
2. Scegli l'icona ![Segnalibro.](media/ui_bookmark_icon.png "Segnalibro") .

Un'azione denominata come il report viene aggiunta al menu di navigazione in Gestione ruolo utente.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a><a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>Per aggiungere un segnalibro a una pagina o un report dalla finestra della funzionalità delle informazioni
1. Aprire la finestra della **funzionalità delle informazioni** e immettere, ad esempio, **Ordini vendita**.
2. Passa il mouse sopra il risultato della ricerca per la pagina o il report **Ordini vendita**, quindi scegli l'icona ![Segnalibro.](media/ui_bookmark_icon.png "Segnalibro") .

Un'azione denominata come la pagina o il report viene aggiunta al menu di navigazione in Gestione ruolo utente.


## <a name="frequently-asked-questions"></a><a name="frequently-asked-questions"></a>Domande frequenti

- **È possibile riorganizzare i segnalibri?**  
Sì. È possibile personalizzare Gestione ruolo utente e spostare le azioni in una sequenza più ottimale o in gruppi e sottogruppi esistenti.  
Informazioni su come [personalizzare l'area di lavoro](ui-personalization-user.md).

- **Come si rimuove un segnalibro?**  
Nella pagina o nel report di destinazione, selezionare nuovamente l'icona del segnalibro per rimuovere l'azione in questione da Gestione ruolo utente. È anche possibile personalizzare Gestione ruolo utente e nascondere temporaneamente le azioni senza rimuoverle completamente.

- **Dove si trovano i segnalibri?**  
Quando si aggiunge un segnalibro a una pagina o a un report, la nuova azione viene aggiunta al menu di navigazione in alto nella schermata iniziale corrente (Gestione ruolo utente). Se sono presenti molte azioni, potrebbe essere necessario attivare il pulsante **Altro** per visualizzarle tutte perché la nuova azione viene sempre aggiunta alla fine dell'elenco.
<!-- Should we add a screenshot here? -->

- **Non è presente un'icona segnalibro. Si è verificato un errore?**  
La possibilità di aggiungere un segnalibro a una pagina o un report è una delle molte funzionalità di personalizzazione per gli utenti in Business Central. Se l'icona del segnalibro non viene visualizzata, è probabile che l'amministratore abbia disabilitato la personalizzazione.

- **Perché non è possibile aggiungere segnalibri a determinate pagine o report?**  
Non a tutte le pagine e i report possono essere aggiunti i segnalibri. Quando una pagina o un report viene eseguito in un contesto speciale regolato dall'applicazione aziendale, l'icona del segnalibro non viene visualizzata. Ad esempio, nelle pagine che non sono presenti nella finestra della **funzionalità delle informazioni** ma vengono avviate altrove non è visualizzata l'icona del segnalibro. Allo stesso modo, le pagine di richiesta report che vengono utilizzate solo per raccogliere i filtri senza eseguire il report non includono l'icona del segnalibro.

  Vedere i dettagli tecnici su [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) e [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Quando si cancella la personalizzazione, verranno cancellati anche i segnalibri?**  
Sì. I segnalibri si trovano nel menu di navigazione. Se si cancellano le modifiche al menu di navigazione da qualsiasi pagina o si cancella tutta la personalizzazione in Gestione ruolo utente, tutte le nuove azioni verranno rimosse in modo permanente.

- **Perché l'icona del segnalibro continua a indicare che non ha applicato il segnalibro?**  
Quando si aggiunge un segnalibro, la nuova azione viene aggiunta al menu di navigazione in Gestione ruolo utente e le successive visite alla pagina o al report mostrano un'icona di segnalibro scura. Se si personalizza Gestione ruolo utente e si riorganizzano le azioni spostandole in gruppi, l'icona del segnalibro non sarà più scura e si potrà aggiungere un altro segnalibro alla stessa pagina o report. Ciò consente di aggiungere più azioni alla stessa pagina o report e classificarle in gruppi diversi.

- **Perché il collegamento a un report visualizza un report diverso?**  
Alcuni report possono essere sostituiti da altri report dopo aver applicato un'estensione a Business Central. Quando si verifica la sostituzione, il testo della nuova azione non viene aggiornato e continua a visualizzare il nome del report originale, ma passa al report più recente. Per correggere il testo della nuova azione, è possibile rimuovere la nuova azione e aggiungerla di nuovo.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **I segnalibri sono disponibili per XMLports?**  
No. Al momento, non è possibile aggiungere azioni per aprire XMLports dall'interfaccia utente.

- **I segnalibri verranno tradotti quando si cambia lingua in Business Central?**  
Quando viene aggiunta una nuova azione, qualsiasi testo tradotto disponibile in quel momento viene contrassegnato con un segnalibro. Se il nuovo testo tradotto viene aggiunto in un secondo momento, la nuova azione non includerà le traduzioni più recenti.

- **Perché non posso aggiungere del testo in una pagina direttamente dopo averla aperta con il segnalibro?**<br> Quando una pagina è aggiunta ai segnalibri, la pagina si aprirà sempre in modalità di visualizzazione dal segnalibro, anche se era in modalità di modifica quando è stata aggiunta ai segnalibri. Selezionando l'icona **Apportare le modifiche nella pagina** ![Mostra l'icona della matita per modificare la pagina.](media/edit-pencil.png) ti consentirà di aggiungere testo nei campi modificabili.


## <a name="see-also"></a><a name="see-also"></a>Vedere anche
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

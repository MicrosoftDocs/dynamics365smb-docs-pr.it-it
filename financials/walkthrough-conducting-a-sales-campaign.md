---
title: 'Procedura dettagliata: Conduzione di una campagna di vendita | Documenti Microsoft'
description: "Una campagna è ogni tipo di attività che coinvolga diversi contatti. Una parte importante dell'impostazione di una campagna è la selezione del target. A questo scopo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] si crea un segmento, o gruppo di contatti, utilizzando dei filtri."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e9eb96fb0f9669a9ddac5e4ea6e973fd64388b87
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Procedura dettagliata: Conduzione di una campagna di vendita
Una campagna è ogni tipo di attività che coinvolga diversi contatti. Una parte importante dell'impostazione di una campagna è la selezione del target. A questo scopo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] si crea un segmento, o gruppo di contatti, utilizzando dei filtri.  

 Utilizzare queste funzionalità di Vendite e marketing per pianificare attentamente le attività di marketing e gestire le interazioni con i contatti e i clienti. È possibile creare campagne e impostare segmenti di contatti per il mailing e altri tipi di interazioni con contatti e clienti potenziali.  

 Le funzioni di Campagna e Segmento con i loro processi automatizzati consentono di pianificare, organizzare e tenere traccia delle attività di marketing. Ciò incrementa le possibilità di acquisire nuovi clienti e mantenere quelli esistenti.  

## <a name="about-this-walkthrough"></a>Informazioni sulla procedura dettagliata  
 In questa procedura dettagliata viene illustrato come fare seguito a una fiera di settore rivolgendosi ai potenziali clienti (contatti) con una campagna mirata.  

 Verranno descritte le funzioni di gestione delle campagne e dei segmenti del reparto Vendite e marketing. In questa procedura dettagliata sono illustrati i task seguenti:  

-   Impostazione della campagna  
-   Selezione del target  
-   Data mining  
-   Invio di lettere ai contatti  
-   Registrazione delle risposte alla campagna  

## <a name="roles"></a>Ruoli  
 Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

-   Manager marketing o manager vendite  
-   Impiegato di marketing  

## <a name="prerequisites"></a>Prerequisiti  
 Prima di svolgere le attività di questa procedura dettagliata, è necessario installare [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="story"></a>Scenario  
 Il manager marketing del reparto vendite di CRONUS ha il compito di pianificare le campagne e di attuarle. Decide anche a quali fiere di settore partecipare e valuta il progresso della campagna.  

 L'impiegato di marketing si occupa della produzione, della distribuzione e della collocazione del materiale di marketing.  

 La società ha appena lanciato un nuovo prodotto chiamato Millennium Server. Il prodotto è stato presentato a una fiera di settore, Computer Futurus. Molti clienti hanno espresso grande interesse nel prodotto e, come parte di un'iniziativa promozionale, è stato offerto un prezzo speciale a chi decide di acquistare Millenium Server durante il periodo di promozione.  

 Uno dei task dell'impiegato di marketing dopo la fiera è di inserire tutti i potenziali clienti come contatti.  

 Il manager marketing imposta una campagna, crea un segmento comprendente tutti i nuovi contatti e quindi estrae ed esamina i dati dei contatti per selezionare i destinatari della campagna.  

 L'impiegato di marketing aiuta ad inviare lettere di ringraziamento a tutti i contatti che hanno lasciato il loro biglietto da visita allo stand e, infine, il responsabile registra tutte le risposte ricevute dai potenziali clienti.  

## <a name="setting-up-a-campaign"></a>Impostazione della campagna  
 Non appena l'impiegato ha terminato di inserire i dati dei biglietti da visita raccolti alla fiera, il manager imposta una scheda per gestire le attività necessarie per la campagna.  

### <a name="to-set-up-a-campaign"></a>Per impostare una campagna  

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Campagne**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo** per creare una nuova campagna. Nella scheda campagna, premere INVIO per inserire automaticamente un numero campagna.  
3.  Nel campo **Descrizione** immettere una descrizione per la campagna, ad esempio **Fiera FUTURUS**.  
4.  Scegliere il campo **Cod. Stato** e selezionare un codice di stato nell'elenco visualizzato nella finestra **Stato campagna**.  
5.  Compilare i campi **Data inizio** e **Data fine** della campagna.  

## <a name="selecting-the-target-audience"></a>Selezione del target  
 Il manager marketing crea un segmento per selezionare i contatti con i quali vuole interagire.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Per creare un segmento con i contatti scelti  

1.  Scegliere l'azione **Segmenti**.  
2.  Scegliere l'azione **Nuovo** per creare un nuovo segmento. Nella scheda segmento, premere INVIO per inserire automaticamente un numero segmento.  
3.  Nel campo **Descrizione** della Scheda dettaglio **Generale**, immettere, ad esempio, **Visitatori della fiera FUTURUS**.  

     Dopo aver inserito informazioni generali sul segmento, selezionare i contatti da includervi.  

     Sono disponibili diversi criteri per selezionare i contatti, ad esempio le persone di contatto che lavorano presso la sede di un cliente o responsabili degli acquisti presso un potenziale cliente.  

     I filtri servono per aggiungere contatti in base ai criteri più rispondenti ai propri scopi. Ad esempio, è possibile scegliere di impostare un filtro in base al ruolo professionale del contatto o alla relazione d'affari o al settore della società contatto. In questa procedura dettagliata verrà impiegato il filtro **Ruolo professionale** per selezionare i contatti.  

4.  Nella finestra **Segmento** selezionare l'azione **Agg. contatti** per aprire il filtro **Agg. contatti**.  
5.  Nella Scheda dettaglio **Ruolo professionale**, selezionare il filtro **Acquisto** come **Cod. ruolo professionale** e fare clic su **OK**.  

     La finestra **Segmento** ora contiene una lista dei contatti in base al filtro immesso. Nella Scheda dettaglio **Generale**, nel campo **Nr. di righe** , è possibile visualizzare immediatamente il numero dei contatti che rispondono ai criteri.  

    > [!NOTE]  
    >  È possibile salvare i criteri per riutilizzarli in futuro.

    1.  Nella finestra **Segmento** scegliere l'azione **Segmento** e quindi l'azione **Salva criteri**.  
    2.  Nella finestra **Salva criteri segmento** , immettere un codice per il segmento. Nel campo **Descrizione** inserire una descrizione dei criteri segmento.
    3.  Scegliere il pulsante **OK**.  

## <a name="mining-the-data"></a>Data mining  
 Il manager marketing esamina più attentamente l'elenco dei contatti nel segmento e si rende conto che è troppo corposa. Decide quindi di ridurre il numero dei contatti a quelli dei clienti potenziali effettivi, in modo da concentrarsi sul target giusto. Questo processo di affinamento e riduzione dei dati è anche detto data mining.  

### <a name="to-remove-contacts-from-the-segment"></a>Per rimuovere contatti dal segmento  

1.  Nella finestra **Segmento**, scegliere l'azione **Contatti** e quindi l'azione **Riduci contatti** per aprire la finestra **Eliminaz. contatti - Riduzione**.  
2.  Nella Scheda dettaglio **Relazione d'affari**, selezionare il filtro **POTENZ** come **Codice relazione d'affari** e fare clic su **OK**.  

     Nella finestra **Segmento** l'elenco è ora ridotto ai contatti che soddisfano questi nuovi criteri e così il numero riportato nel campo **Nr. di righe**.  

    > [!NOTE]  
    >  Per annullare quest'ultima operazione, utilizzare la funzione **Vai a precedente**. Ciò significa che è possibile annullare l'ultima segmentazione.  
    >   
    >  Nella finestra **Segmento** scegliere l'azione **Segmento** e quindi l'azione **Vai a precedente**.  
    >   
    >  I contatti appena rimossi vengono reinseriti nell'elenco dei contatti.  

## <a name="linking-a-segment-to-a-campaign"></a>Collegamento di un segmento a una campagna  
 Il manager marketing decide che l'elenco ridotto è quello finale dei contatti da coinvolgere nella campagna. Quindi collega questo segmento alla campagna della fiera FUTURUS.  

### <a name="to-link-a-segment-to-the-campaign"></a>Per collegare un segmento a una campagna  

1.  Nella finestra **Segmento**, nella Scheda dettaglio **Campagna**, selezionare il campo **Nr. campagna** per selezionare la campagna alla quale si desidera collegare il segmento, ad esempio, **CP0001**.  
2.  Poiché questo segmento è il target della campagna, selezionare la casella di controllo **Target campagna**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Invio di lettere e messaggi di posta elettronica ai contatti  
 L'impiegato di marketing aiuta il manager a inviare una comunicazione ai potenziali clienti, ringraziandoli di aver visitato lo stand alla fiera.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Per utilizzare un segmento per l'invio di una lettera a un contatto  

1.  Aprire la scheda **Segmento** di **Visitatori della fiera FUTURUS**.  
2.  Nel campo **Codice modello interazione** della Scheda dettaglio **Interazione** selezionare il modello Lettera Business con codice **BUS**.  
3.  Nel campo **Oggetto (Default)** immettere il seguente testo di esempio: **Grazie di aver visitato la fiera**.  

    > [!NOTE]  
    >  Il modello consiste di più documenti allegati in lingue diverse. Le lingue di esempio includono inglese e danese.  

4.  Scegliere il campo **Codice lingua (default)** per aprire la finestra **Lingue interazione segmento**. Selezionare un codice della lingua e scegliere il pulsante **OK**.  
5.  È possibile visualizzare il documento nella lingua selezionata. Scegliere l'azione **Allegato** e quindi l'azione **Apri**.  

     Quando viene visualizzato il messaggio che richiede l'autorizzazione per l'avvio di Word, selezionare l'opzione **Consenti per questa sessione client**.  

     Verrà aperto il documento di Word allegato per poterlo controllare. È inoltre possibile sfruttare questa opportunità per rielaborare e modificare la lettera. Al termine dell'operazione, chiudere Word.  

6.  Inserire l'oggetto della lettera nel campo **Oggetto**, nella lingua scelta per il modello.  
7.  Scegliere l'azione **Log**.
8.  Selezionare la casella di controllo **Invia allegati** per stampare l'allegato.  

    1. Selezionare la casella di controllo **Crea segmento di follow-up**.  
    2. Scegliere **OK** per avviare il processo batch **Log segmento**.  

9. Gli allegati vengono inviati. Al termine del processo, fare clic sul pulsante **OK** all'interno del messaggio che indica che il segmento è stato registrato.  

     Le lettere vengono stampate automaticamente e il segmento registrato. Dal momento che il segmento è stato registrato, non è più contenuto nella lista dei segmenti, ma è stato spostato nella lista dei segmenti registrati. Per visualizzare l'elenco, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Segmenti registrati**, quindi scegliere il collegamento correlato.  

10. Dopo che il segmento è stato registrato, ogni lettera inviata viene registrata come un'interazione, che è possibile visualizzare nel log.  

     Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Movimenti log interazione**, quindi scegliere il collegamento correlato. È presente un movimento per ciascuna lettera inviata.  

### <a name="to-send-an-email-message-to-a-contact"></a>Per inviare un messaggio di posta elettronica a un contatto  

1.  Nel campo **Codice modello interazione** della Scheda dettaglio **Interazione** selezionare il modello Lettera Business con codice **BUS**.  
2.  Nel campo **Oggetto (Default)** immettere il seguente testo di esempio: **Grazie di aver visitato la fiera**.  
3.  Nel campo **Tipo di corrispondenza**, selezionare **E-mail**.  
4.  Specificare le impostazioni relative alla lingua, come indicato nella procedura precedente.  
5.  Scegliere l'azione **Log**. Verrà visualizzata la finestra **Log segmento**.  
6.  Selezionare la casella di controllo **Invia allegati** per inviare gli allegati tramite posta elettronica.  
7.  Selezionare la casella di controllo **Crea segmento di follow-up**.  
8.  Scegliere il pulsante **OK**.  

     Le lettere vengono inviate automaticamente tramite posta elettronica e il segmento registrato. Dal momento che il segmento è stato registrato, non è più contenuto nella lista dei segmenti, ma è stato salvato nella lista dei segmenti registrati. Per visualizzare l'elenco, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Segmenti registrati**, quindi scegliere il collegamento correlato.  

## <a name="registering-campaign-responses"></a>Registrazione delle risposte alla campagna  
 Nel corso delle due settimane seguenti, i potenziali clienti rispondono alla lettera. Il responsabile del marketing desidera tenere traccia delle risposte e registrare le interazioni.  

 A tal scopo, impostare un segmento dei contatti che hanno risposto alla lettera  

### <a name="to-register-campaign-responses"></a>Per registrare le risposte alla campagna  

1.  Espandere la Scheda dettaglio **Interazione** nella finestra **Segmento**.  
2.  Selezionare il campo **Codice modello interazione** .  

     Non esiste un modello per registrare le risposte alla campagna. Pertanto, creare un nuovo modello.  

3.  Nella finestra **Modelli interazione** scegliere l'azione **Nuovo**.  
4.  Immettere **RISP** nel campo **Codice** e **Risposte su campagna** nel campo **Descrizione**.  
5.  Scegliere il pulsante **OK**.  
6.  Selezionare questo modello nel campo **Codice modello interazione** e rispondere affermativamente al messaggio che chiede se si desidera aggiornare le righe di segmento con lo stesso codice di modello interazione.  

     Specificare ora i contatti che hanno risposto alla campagna.  
7.  Nel campo **Nr. campagna** della Scheda dettaglio **Campagna** selezionare la campagna.  
8.  Lasciare il campo **Nr. campagna** e rispondere affermativamente al messaggio che chiede se si desidera aggiornare le righe di segmento con lo stesso codice di modello interazione.  
9. Selezionare il campo **Risposta su campagna** e confermare il messaggio successivo.  

     Registrare il segmento per garantire che le interazioni siano registrate.  
10. Nella finestra **Segmento**, scegliere l'azione **Log**.  
11. Nella finestra **Log segmento** deselezionare la casella di controllo **Invia allegati**, fare clic su **OK** e confermare il messaggio visualizzato.  

     Dopo la registrazione del segmento, viene automaticamente creato un movimento per la campagna per registrare questa azione nella finestra **Movimenti campagna**.  

## <a name="see-also"></a>Vedi anche  
[Relationship Management](marketing-relationship-management.md)  
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


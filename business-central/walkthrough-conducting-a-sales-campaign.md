---
title: 'Procedura dettagliata: Conduzione di una campagna di vendita'
description: Questa procedura dettagliata offre una panoramica dettagliata di tutte le attività coinvolte nella conduzione di una campagna di vendita in Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# Procedura dettagliata: Conduzione di una campagna di vendita

Una campagna è ogni tipo di attività che coinvolga diversi contatti. Una parte importante dell'impostazione di una campagna è la selezione del target. A questo scopo, in [!INCLUDE[prod_short](includes/prod_short.md)] si crea un segmento, o gruppo di contatti, utilizzando dei filtri.  

 Utilizzare queste funzionalità di Vendite e marketing per pianificare attentamente le attività di marketing e gestire le interazioni con i contatti e i clienti. È possibile creare campagne e impostare segmenti di contatti per il mailing e altri tipi di interazioni con contatti e clienti potenziali.  

 Le funzioni di Campagna e Segmento con i loro processi automatizzati consentono di pianificare, organizzare e tenere traccia delle attività di marketing. Ciò incrementa le possibilità di acquisire nuovi clienti e mantenere quelli esistenti.  

## Informazioni sulla procedura dettagliata

 In questa procedura dettagliata viene illustrato come fare seguito a una fiera di settore rivolgendosi ai potenziali clienti (contatti) con una campagna mirata.  

 Verranno descritte le funzioni di gestione delle campagne e dei segmenti del reparto Vendite e marketing. In questa procedura dettagliata sono illustrati i task seguenti:  

- Preparazione dei dati.
- Impostazione della campagna  
- Selezione del target  
- Data mining  
- Invio di lettere ai contatti  
- Registrazione delle risposte alla campagna  

## Ruoli

 Questa procedura dettagliata comprende task svolti dai ruoli utente seguenti:  

- Manager marketing o manager vendite  
- Impiegato di marketing  

## Prerequisiti

 Prima di svolgere le attività di questa procedura dettagliata, è necessario installare [!INCLUDE[prod_short](includes/prod_short.md)].  

## Scenario

 Il manager marketing del reparto vendite di CRONUS ha il compito di pianificare le campagne e di attuarle. Decide anche a quali fiere di settore partecipare e valuta il progresso della campagna.  

 L'impiegato di marketing si occupa della produzione, della distribuzione e della collocazione del materiale di marketing.  

 La società ha appena lanciato un nuovo prodotto chiamato Sedia ospiti ROMA. Il prodotto è stato presentato a una fiera di settore, Ufficio Futurus. Molti clienti hanno espresso grande interesse nel prodotto e, come parte di un'iniziativa promozionale, è stato offerto un prezzo speciale a chi decide di acquistare Sedia ospiti Roma durante il periodo di promozione.  

 Uno dei task dell'impiegato di marketing dopo la fiera è di inserire tutti i potenziali clienti come contatti.  

 Il manager marketing imposta una campagna, crea un segmento comprendente tutti i nuovi contatti e quindi estrae ed esamina i dati dei contatti per selezionare i destinatari della campagna.  

 L'impiegato di marketing aiuta ad inviare lettere di ringraziamento a tutti i contatti che hanno lasciato il loro biglietto da visita allo stand e, infine, il responsabile registra tutte le risposte ricevute dai potenziali clienti.  

## Impostazione della campagna

 Non appena l'impiegato ha terminato di inserire i dati dei biglietti da visita raccolti alla fiera, il manager imposta una scheda per gestire le attività necessarie per la campagna.  

### Per impostare una campagna  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Campagne**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** per creare una nuova campagna. Nella scheda campagna, seleziona <kbd>Invio</kbd> per inserire automaticamente un numero campagna.  
3. Nel campo **Descrizione** immettere una descrizione per la campagna, ad esempio **Fiera Ufficio Futurus**.  
4. Scegliere il campo **Codice di stato** e selezionare il codice di stato "1-PLAN". 
5. Compilare i campi **Data inizio** e **Data fine** della campagna.  

## Selezione del target

 Il manager marketing crea un segmento per selezionare i contatti con i quali vuole interagire.  
 
 Quando crei un segmento, puoi utilizzare una serie di criteri per selezionare i contatti che devono essere target per il segmento. Ad esempio, puoi selezionare le persone di contatto che lavorano presso la sede di un cliente o responsabili degli acquisti presso un potenziale cliente. I filtri servono per aggiungere contatti in base ai criteri più rispondenti ai propri scopi. Ad esempio, è possibile scegliere di impostare un filtro in base al ruolo professionale del contatto o alla relazione d'affari o al settore della società contatto. In questa procedura dettagliata verrà impiegato il filtro **Ruolo professionale** per selezionare i contatti.

### Per creare un segmento con i contatti scelti  

1. Scegliere l'azione **Naviga**, quindi scegliere **Segmenti**.  
2. Scegliere l'azione **Nuovo** per creare un nuovo segmento. Nella scheda segmento, premere **Invio** per inserire automaticamente un numero segmento.  
3. Nel campo **Descrizione** della Scheda dettaglio **Generale**, immettere, ad esempio, *Visitatori della fiera Ufficio Futurus*.
4. Selezionare l'azione **Agg. contatti** per aprire il filtro **Agg. contatti**.  
5. Scorrere fino alla Scheda dettaglio **Ruolo professionale contatto**, selezionare il filtro **Acquisto** come **Cod. ruolo professionale** e fare clic su **OK**.  

La pagina **Segmento** ora contiene una lista dei contatti in base al filtro immesso. Nella Scheda dettaglio **Generale**, nel campo **Nr. di righe** , è possibile visualizzare immediatamente il numero dei contatti che rispondono ai criteri.  

> [!NOTE]  
> È possibile salvare i criteri per riutilizzarli in futuro.

### Per salvare i criteri di segmentazione

1. Nella pagina **Segmento**, scegliere **Azioni**.
2. Scegliere **Funzioni**, quindi **Segmento**, quindi scegliere l'azione **Salva criteri**.  
3. Nella pagina **Salva criteri segmento** , immettere un codice per il segmento. Nel campo **Descrizione** inserire una descrizione dei criteri segmento.
4. Scegliere il pulsante **OK**.  

## Data mining

 Il manager marketing esamina più attentamente l'elenco dei contatti nel segmento e si rende conto che è troppo corposa. Decide quindi di ridurre il numero dei contatti a quelli dei clienti potenziali effettivi, in modo da concentrarsi sul target giusto. Questo processo di affinamento e riduzione dei dati è anche detto data mining.  

### Per rimuovere contatti dal segmento  

1. Nella pagina **Segmento**, scegliere **Azioni**.
2. Nella barra dei menu in basso, scegli **Funzioni**, **Contatti** e **Riduci contatti**.  

  Verrà aperta la finestra di dialogo **Eliminaz. contatti - Riduzione**.  
4. Nella Scheda dettaglio **Contatto relazione d'affari**, selezionare il filtro **POTENZ** come **Codice relazione d'affari** e fare clic su **OK**.

 Nella pagina **Segmento** l'elenco è ora ridotto ai contatti che soddisfano questi nuovi criteri e così il numero riportato nel campo **Nr. di righe**.  

 > [!NOTE]  
 > Per annullare quest'ultima operazione, utilizzare la funzione **Vai a precedente**. Ciò significa che è possibile annullare l'ultima segmentazione.  

### Per riportare i contatti rimossi

1. Nella pagina **Segmento**, scegliere l'azione **Segmento**.
2. Scegliere l'azione **Indietro**.

I contatti appena rimossi vengono reinseriti nell'elenco dei contatti.

## Collegamento di un segmento a una campagna

Il manager marketing decide che l'elenco ridotto è quello finale dei contatti da coinvolgere nella campagna. Quindi collega questo segmento alla campagna della fiera FUTURUS.  

### Per collegare un segmento a una campagna  

1. Nella pagina **Segmento**, nella Scheda dettaglio **Campagna**, selezionare il campo **Nr. campagna** per selezionare la campagna alla quale si desidera collegare il segmento, ad esempio, **CP0001**.
2. Seleziona **Sì**.  
3. Poiché questo segmento è il target della campagna, selezionare la casella di controllo **Target campagna** e poi **Sì**.  

## Invio di lettere e messaggi di posta elettronica ai contatti

 L'impiegato di marketing aiuta il manager a inviare una comunicazione ai potenziali clienti, ringraziandoli di aver visitato lo stand alla fiera.

### Per utilizzare un segmento per l'invio di una lettera a un contatto  

> [!NOTE]  
> In questa procedura devi allegare un documento Word. Puoi aggiungere allegati in qualsiasi lingua.

> [!NOTE]  
> Se necessario fai clic sull'icona **Matita per modifica** per aprire la pagina in modalità di modifica.

1. Aprire la scheda **Segmento** di **Visitatori della fiera FUTURUS**.  
2. Nel campo **Codice modello interazione** della Scheda dettaglio **Interazione** selezionare il modello Lettera Business con codice **BUS** e selezionare **Sì**.
3. Scegliere il campo **Codice lingua (default)** per aprire la pagina **Lingue interazione segmento**. Selezionare un **Codice lingua** e scegliere il pulsante **OK**.
4. Assicurati che il **Tipo di corrispondenza (predefinito)** è impostato su **Stampa**.
5. Nel campo **Allegato** selezionare la casella **Puntini di sospensione**. In questo modo viene aperta la finestra di dialogo Importa allegato.
    1. Selezionare il pulsante **Scegli** per scegliere il file.
    1. Trova il file e seleziona il pulsante **Apri** per allegarlo.
6. Nel campo **Oggetto (Default)** immettere il seguente testo di esempio: **Grazie di aver visitato la fiera**. Seleziona il tasto <kbd>Tab</kbd> per uscire dal campo e seleziona il pulsante **Sì**.
7. Attivare **Invia documenti Word come all.** e selezionare il pulsante **Sì**.
8. Scegliere l'azione **Log**. Nella finestra pop-up Segmento log abilitare: **Crea segmento di follow-up**
9. Scegliere **OK** per avviare il **Processo bastch log segmento**.  

Gli allegati vengono inviati. Al termine del processo, fare clic sul pulsante **OK** all'interno del messaggio che indica che il segmento è stato registrato.  

 Le lettere vengono stampate automaticamente e il segmento registrato. Dal momento che il segmento è stato registrato, non è più contenuto nella lista dei segmenti, ma è stato spostato nella lista dei segmenti registrati. Per vedere l'elenco, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Segmenti registrati**, quindi scegli il collegamento correlato.  

Dopo che il segmento è stato registrato, ogni lettera inviata viene registrata come un'interazione, che è possibile visualizzare nel log.  

Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Movimenti log interazione**, quindi scegli il collegamento correlato. È presente un movimento per ciascuna lettera inviata.  

### Per inviare un messaggio di posta elettronica a un contatto  

1. Nel campo **Codice modello interazione** della Scheda dettaglio **Interazione** selezionare il modello Lettera Business con codice **BUS**.  
2. Nel campo **Oggetto (Default)** immettere il seguente testo di esempio: **Grazie di aver visitato la fiera**.  
3. Nel campo **Tipo di corrispondenza**, selezionare **E-mail**.  
4. Specificare le impostazioni della lingua e allegare un documento Word, come nella procedura precedente.  
5. Scegliere l'azione **Log**. Verrà visualizzata la pagina **Log segmento**.  
6. Selezionare la casella di controllo **Invia allegati** per inviare gli allegati tramite posta elettronica.  
7. Selezionare la casella di controllo **Crea segmento di follow-up**.  
8. Scegliere il pulsante **OK**.  

 Le lettere vengono inviate automaticamente tramite posta elettronica e il segmento registrato. Dal momento che il segmento è stato registrato, non è più contenuto nella lista dei segmenti, ma è stato salvato nella lista dei segmenti registrati. Per vedere l'elenco, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Segmenti registrati**, quindi scegli il collegamento correlato.  

## Registrazione delle risposte alla campagna

 Nel corso delle due settimane seguenti, i potenziali clienti rispondono alla lettera. Il responsabile del marketing desidera tenere traccia delle risposte e registrare le interazioni.  

 A tal scopo, impostare un segmento dei contatti che hanno risposto alla lettera  

### Per registrare le risposte alla campagna  

1. Nella scheda dettaglio **Interazione** della pagina **Segmento**, scegli il **Codice modello interazione**.  

 Non esiste un modello per registrare le risposte alla campagna. Pertanto, creare un nuovo modello.  

2. Nell'elenco a discesa **Modelli interazione** scegliere l'azione **Nuovo**.  
3. Immettere **RISP** nel campo **Codice** e **Risposte su campagna** nel campo **Descrizione**.  
4. Scegliere il pulsante **OK**.
5. Scegliere **Sì** per confermare che si desidera applicare questo codice modello interazione a tutte le linee di segmento.
6. Nella Scheda dettaglio **Campagna** selezionare il campo **Risposta campagna**. Scegliere **Sì** per confermare il messaggio *Hai modificato la risposta alla campagna*.  
7. Nella pagina **Segmento**, scegliere l'azione **Log**.  
8. Nella pagina **Segmento di registro**, cancellare la casella di controllo **Invia allegati**. Quindi selezionare **OK** per confermare il messaggio che il segmento è stato registrato.  
  
## Vedere anche  
[Gestione delle relazioni](marketing-relationship-management.md)  
 [Procedure dettagliate per i processi aziendali](walkthrough-business-process-walkthroughs.md)  
 [Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Rateizzare le entrate e le uscite
description: 'Per riconoscere un''entrata o una spesa in un periodo diverso dal periodo in cui è stata registrata la transazione, puoi differire o posporre automaticamente le entrate e le uscite per una pianificazione specificata.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="defer-revenues-and-expenses" />Rateizzare le entrate e le uscite

Per riconoscere un'entrata o una spesa in un periodo diverso dal periodo in cui è stata registrata la transazione, utilizzare la funzionalità per differire automaticamente le entrate e le uscite per una pianificazione specificata.

Per ripartire le entrate o le spese sui periodi contabili implicati, impostare un modello di differimento per risorsa, articolo o conto C/G per il quale verrà registrata l'entrata o la spesa. Quando si registra il documento relativo alla vendita o all'acquisto, l'entrata o la spesa è differita ai periodi contabili implicati, in base a una pianificazione di differimento che è governata dalle impostazioni nel modello di differimento e dalla data di registrazione.

## <a name="to-set-up-a-gl-account-for-deferral" />Per impostare un conto C/G per il differimento

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Piano dei conti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare tutti i campi in modo da creare un conto C/G per le entrate differite. Per ulteriori informazioni, vedere [Contabilità generale e piano dei conti](finance-general-ledger.md).
4. Ripetere i passaggi 2 e 3 per creare un nuovo conto C/G per le spese differite.

Per entrambi i tipi di differimenti, selezionare **Conto patrimoniale** nel campo **Tipo** e chiamare i conti in modo appropriato, ad esempio "Rendita" per le entrate differite e "Spese non pagate" per le spese differite.

## <a name="to-set-up-a-deferral-template" />Per impostare un modello di differimento

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Modelli di differimento**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario.
4. Nel campo **Metodo calcolo** specificare come viene calcolato il campo **Importo** per ciascun periodo della pagina **Programmazione differimento**. È possibile scegliere tra le seguenti opzioni:

   * **Quote costanti**: gli importi di differimento periodici vengono calcolati in base al numero di periodi, distribuiti in base alla durata del periodo.
   * **Uguale per periodo**: gli importi di differimento periodici vengono calcolati in base al numero di periodi, distribuiti equamente sui periodi.
   * **Giorni per periodo**: gli importi di differimento periodici vengono calcolati in base al numero di giorni di tale periodo.
   * **Personalizzato**: gli importi di differimento periodici non vengono calcolati. È necessario compilare manualmente il campo **Importo** per ogni periodo nella pagina Programmazione differimento. Per ulteriori informazioni, vedere la sezione “Per modificare un programma di differimento da una fattura di vendita”.
5. Nel campo **Descrizione periodo** specificare una descrizione che sarà mostrata sui movimenti per la registrazione del differimento. È possibile immettere i seguenti codici di segnaposto per i valori tipici che verranno immessi automaticamente quando verrà visualizzata la descrizione del periodo.

   * %1 = Il numero del giorno della data di registrazione del periodo
   * %2 = Il numero della settimana della data di registrazione del periodo
   * %3 = Il numero del mese della data di registrazione del periodo
   * %4 = Il nome del mese della data di registrazione del periodo
   * %5 = Il nome del periodo contabile della data di registrazione del periodo
   * %6 = L'anno fiscale della data di registrazione del periodo

Esempio: la data di registrazione è 06/02/2016. Se si immette “Spese differite per %4 %6, la descrizione visualizzata sarà “Spese differite per febbraio 2016”.

## <a name="to-assign-a-deferral-template-to-an-item" />Per assegnare un modello di differimento a un articolo

> [!NOTE]  
> I passaggi di questa procedura sono gli stessi di quando si assegna un modello di rateo a un conto C/G o una risorsa.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Articolo**, quindi scegli il collegamento correlato.
2. Aprire la scheda dell'articolo per il quale devono essere differite le entrate o le spese ai periodi contabili in cui l'articolo è stato venduto o acquistato.
3. Nel campo **Modello di differimento di default** selezionare il modello di differimento pertinente.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice" />Per modificare un programma di differimento da una fattura di vendita

> [!NOTE]  
> I passaggi di questa procedura sono identici a quelli seguiti quando si modifica una programmazione di differimento da una fattura di acquisto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.
2. Creare una fattura di vendita per un articolo che ha un modello di differimento assegnato. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md).

    Non appena si immette l'articolo (o risorsa o conto C/G) nella riga della fattura, il campo **Codice differimento** viene compilato con il codice del modello di differimento assegnato.
3. Scegliere l'azione **Programmazione differimento**.
4. Nella pagina **Programmazione differimento** modificare le impostazioni nella testata o nei valori delle righe, ad esempio per differire l'importo a un periodo contabile addizionale.
5. Scegliere l'azione **Calcola programmazione**.
6. Scegliere il pulsante **OK**. La programmazione differimento viene aggiornata per la fattura di vendita. Il modello di differimento correlato è invariato.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger" />Per visualizzare in anteprima come le entrate o le spese differite verranno registrate nella contabilità generale

> [!NOTE]  
> I passaggi di questa procedura sono identici a quelli di quando si visualizza in anteprima come vengono registrati i differimenti spesa.

1. Nella pagina **Fattura di vendita** scegliere l'azione **Anteprima registrazione**.
2. Nella pagina **Anteprima registrazione** scegliere l'azione **Movimento C/G**, quindi l'azione **Mostra movimenti correlati**.

I movimenti C/G da registrare nel conto specificato di differimento, ad esempio, Rendita, sono denotati dalla descrizione inserita nel campo **Descrizione periodo** nel modello di differimento, ad esempio, “Spese differite per febbraio 2016”.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report" />Per rivedere i differimenti registrati nel report Riepilogo differimento vendite

> [!NOTE]  
> I passaggi di questa procedura sono identici a quelli di quando si rivede il report Riepilogo differimento acquisto.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Riepilogo differimento vendite**, quindi scegli il collegamento correlato.
2. Nel campo **Saldo a partire dal** della pagina **Riepilogo differimento vendite** immettere la data fino alla quale si intende visualizzare le entrate differite.
3. Fare clic sul pulsante **Anteprima**.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting" />Per specificare un periodo in cui consentire la registrazione differita

È possibile specificare un periodo in cui le persone possono registrare le transazioni inserendo le date nei campi **Consenti registrazione da** e **Consenti registrazione a** come segue:

* Per tutti gli utenti, nella pagina **Setup contabilità generale**
* Per utenti specifici, nella pagina **Setup utente**

Se lo hai fatto, devi creare un'eccezione per i differimenti per consentirne la registrazione al di fuori del periodo. Per definire il periodo, attieniti a questa procedura.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità generale** o **Setup utente**, quindi scegli il collegamento correlato.
2. Nei campi **Consenti registrazione differita da** e **Consenti registrazione differita a**, inserisci una data di inizio e di fine per il periodo.

## <a name="see-related-microsoft-trainingtrainingmodulesprocessing-invoices-dynamics-365-business-central" />Vedi il relativo [training Microsoft](/training/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also" />Vedere anche

[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

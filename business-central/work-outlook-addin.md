---
title: Utilizzo di Business Central con Outlook
description: Questo servizio è completamene integrato con Microsoft 365 e consente di gestire tutte le interazioni aziendali e le e-mail con clienti e fornitori direttamente in Outlook.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365'
ms.date: 04/21/2022
ms.author: jswymer
---
# <a name="use-business-central-as-your-business-inbox-in-outlook"></a>Utilizzare Business Central come Posta in arrivo aziendale di Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] offre un add-in che permette di gestire le interazioni commerciali con i vostri clienti e fornitori, direttamente in Microsoft Outlook. Con l'add-in [!INCLUDE[prod_short](includes/prod_short.md)] per Outlook, è possibile vedere i dati finanziari relativi a clienti e fornitori, e creare e inviare documenti finanziari, come preventivi e fatture.

[!INCLUDE[prod_short](includes/prod_short.md)] è composto da due add-in separati che forniscono le seguenti capacità:

- Approfondimenti di contatto

   Questo add-in permette di cercare [!INCLUDE[prod_short](includes/prod_short.md)] informazioni su clienti o fornitori nelle e-mail di Outlook e negli appuntamenti del calendario. Permette anche di creare e inviare [!INCLUDE[prod_short](includes/prod_short.md)] documenti aziendali, come un preventivo di vendita o una fattura a un contatto.

- Vista del documento

   Quando un documento aziendale viene inviato in una e-mail, l'add-in fornisce un collegamento diretto dall'e-mail al documento aziendale effettivo in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Inizia

1. La prima cosa da fare è installare l'add-in [!INCLUDE[prod_short](includes/prod_short.md)] in Outlook. Il tuo amministratore potrebbe aver già installato l'add-in per te. Quindi, se non sei sicuro, controlla con il tuo amministratore o vedi il prossimo passo per verificare se è installato.

    Se l'add-in non è stato installato per te, vedi [Installare l'add-in per uso personale](admin-outlook.md#install). 

2. Con il componente aggiuntivo installato, è possibile accedere all’add-in **[!INCLUDE[prod_short](includes/prod_short.md)]** da qualsiasi messaggio di posta elettronica nuovo o esistente o appuntamento del calendario in Outlook.

    Inizia accedendo a Outlook e aprendo un messaggio di posta elettronica. Poi, se stai usando l'applicazione Outlook, vai alla barra multifunzione e cerca **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Oppure, se stai usando Outlook sul web, nella parte superiore o inferiore del messaggio e-mail, cerca l'icona dell'add-in di ![Business Central in Outlook.](media/outlook-business-central-icon.png) o vai a più azioni ![Mostra più azioni per un'email in Outlook.](media/outlook-more-actions-button.png) .

    ![Accedi ai componenti aggiuntivi di Business Central in Outlook.](media/outlook-business-central-addin.png)

   Se hai installato l'add-in per conto tuo e hai scelto di ricevere un'email di esempio, controlla la tua casella di posta per l'email di benvenuto. Questa e-mail fornisce informazioni per aiutarti a iniziare.

La prima volta che usi l'add-in [!INCLUDE[prod_short](includes/prod_short.md)], nel riquadro Add-in, ti potrebbe essere chiesto di accedere. In questo caso, sceglie **Accedi ora** e seguite le istruzioni sullo schermo per accedere a Business Central usando il tuo account.

> [!TIP]
> Se usi il nuovo Outlook sul web, puoi appuntare **[!INCLUDE[prod_short](includes/prod_short.md)]** in modo che sia sempre immediatamente visibile, invece di dover andare al pulsante più azioni, rendendo conveniente visualizzare gli approfondimenti dei contatti mentre si sfogliano diverse e-mail.

Per ulteriori informazioni, vedi [Utilizzare componenti aggiuntivi in Outlook sul Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Lavorare con contatti e documenti usando l'add-in Informazioni contatto

Supponiamo che si riceva un'email da un cliente che vuole un preventivo per alcuni articoli. Direttamente in Outlook, puoi aprire il componente aggiuntivo di [!INCLUDE[prod_short](includes/prod_short.md)] in cui il mittente viene riconosciuto come cliente e verrà aperta la scheda cliente relativa alla società. Da questo dashboard, vedi le informazioni generali per il cliente e puoi scendere in maggiori dettagli su documenti specifici. È inoltre possibile approfondire le informazioni cronologiche di vendita per il cliente. Se si tratta di un nuovo contatto, è possibile crearlo come nuovo cliente in [!INCLUDE[prod_short](includes/prod_short.md)] senza uscire da Outlook.  

Nel componente aggiuntivo, è possibile creare un'offerta di vendita e inviarla di nuovo al cliente senza uscire da Outlook. Tutte le informazioni necessarie per inviare l'offerta di vendita sono disponibili nella Posta in arrivo aziendale in Outlook. Una volta inseriti i dati, si pubblica il preventivo e lo si invia per e-mail. [!INCLUDE[prod_short](includes/prod_short.md)] genera un file PDF all'offerta di vendita e lo allega al messaggio e-mail definito nel componente aggiuntivo.  

Analogamente, se si riceve un messaggio e-mail a un fornitore, è possibile utilizzare il componente aggiuntivo per lavorare con i fornitori e le fatture di acquisto.  

Talvolta si desidera visualizzare più campi rispetto a quelli che è possibile visualizzare nel componente aggiuntivo, ad esempio se si desidera compilare le righe di una fattura. Per ottenere maggiore spazio, è possibile visualizzare il componente aggiuntivo in una pagina separata. Fa parte ancora di Outlook, ma offre più spazio per il lavoro. Se si digitano i dati per il documento nella nuova finestra, le modifiche vengono salvate automaticamente. Le sezioni seguenti ti guidano attraverso alcuni compiti di base per darti una comprensione generale su come usarlo.

> [!TIP]
> I compiti spiegano come utilizzare l'add-in da un messaggio di posta elettronica. Ma si può fare lo stesso da un appuntamento del calendario in Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Cercare un contatto commerciale quando si compone un'e-mail

1. Crea un nuovo messaggio e-mail.
2. Nella barra multifunzione, vai su **[!INCLUDE[prod_short](includes/prod_short.md)]** e scegli **Informazioni contatto**. O se stai usando Outlook sul web, vai in fondo al messaggio, scegli ![l’icona dell’add-in Business Central in Outlook.](media/outlook-business-central-icon.png) > **Contatto Approfondimenti**.
3. Nel **[!INCLUDE[prod_short](includes/prod_short.md)]** che si apre, cerca e scegli il contatto che vuoi.

    Una panoramica del contatto viene visualizzata nel riquadro e il contatto viene aggiunto nella riga **A** dell'e-mail.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Visualizzare e modificare i dettagli di contatto o cambiare azienda

La barra delle azioni nella parte superiore del pannello dell'add-in [!INCLUDE[prod_short](includes/prod_short.md)] include diverse azioni che ti permettono di scavare più a fondo nei dettagli del contatto e di cambiare le cose.

![Barra delle azioni di Business Central add-in in Outlook.](media/outlook-addin-action-bar.png)

Per esempio, puoi aprire i dettagli completi del contatto come li vedresti in [!INCLUDE[prod_short](includes/prod_short.md)]. Se lavorate con più di una compagnia [!INCLUDE[prod_short](includes/prod_short.md)], potete facilmente passare da una compagnia all'altra.

### <a name="track-incoming-documents"></a>Tracciare i documenti in arrivo

Forse usi la lista **Documenti in entrata** in [!INCLUDE[prod_short](includes/prod_short.md)] per tenere traccia dei documenti da elaborare che i fornitori ti inviano, come una fattura di acquisto che deve essere pagata. Se lo fai, puoi facilmente creare record di Documenti in entrata dall'add-in di Outlook e includere gli allegati di posta elettronica.

1. Quando ricevi un'e-mail da un fornitore che ha un allegato, scegli l'icona dell’add-in ![Business Central in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Informazioni contatto**.  

2. Nella barra delle azioni dell'add-in, scegli **Mostra altre azioni**, poi scegli **Invia a documenti in entrata...** .  

### <a name="create-and-send-new-document-to-a-contact"></a>Creare e inviare un nuovo documento a un contatto

1. Nella barra multifunzione o nella parte inferiore del messaggio di posta elettronica, scegli l'icona del componente aggiuntivo ![ Business Central in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nuovo**, poi scegli il tipo di documento che vuoi creare, ad esempio **Preventivo di vendita**.
2. Apportare modifiche al documento nel pannello add-in **[!INCLUDE[prod_short](includes/prod_short.md)]**.
3. Quando il documento è pronto per l'invio al contatto, nella barra delle azioni, scegli **Mostra altre azioni**, quindi scegli l'azione **Invia tramite posta elettronica** .

### <a name="attach-files-to-records"></a>Allegare file ai record

La tua casella di posta elettronica spesso funge da origine di file in arrivo che avviano o sbloccano flussi di lavoro. I file possono includere elementi come pagamenti di fatture PDF, foto di merci o requisiti in un documento Word. Quando si lavora in Outlook con record di Business Central come fornitori, clienti, fatture di acquisto o ordini di vendita, è possibile allegare questi file ai record.

Ci sono un paio di modi per allegare i file. Un modo è caricare i file dal tuo dispositivo. L'altro modo è caricare i file allegati a un'e-mail. Ad esempio, supponiamo di ricevere un'e-mail con i file da un contatto. Il componente aggiuntivo visualizzerà automaticamente il record del contatto che corrisponde al mittente dell'e-mail. Da lì, puoi passare a un documento per il contatto, come l'ultimo ordine cliente. Una volta identificato l'ordine a cui si riferisce l'e-mail, carichi rapidamente i file dall'e-mail a quell'ordine.

![Mostra come aggiungere allegati da un'e-mail ai record in Business Central.](media/outlook-attach-files.png)

Dopo aver allegato un file, i colleghi possono scaricare e visualizzare immediatamente il file dalla scheda dettaglio **Allegati** in uno qualsiasi dei client Business Central. Oppure possono aprire il file in OneDrive per condividere e collaborare con il reparto.

#### <a name="how-to-attach-a-file"></a>Come allegare un file

1. Apri l'e-mail, scegli ![Icona del componente aggiuntivo Business Central in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Informazioni contatto**.
2. Nella barra delle azioni del componente aggiuntivo, scegli **Mostra altre azioni** > **Allegati**.

    Si apre la pagina **Documenti allegati** per elencare tutti i documenti già allegati al record.
3. Scegli **File allegati...**, quindi scegli una delle seguenti opzioni:

   - Scegli **Allega da e-mail** per caricare tutti o alcuni file allegati all'e-mail.
   - Scegli **Carica da file** per caricare uno o più file dal tuo dispositivo.

> [!NOTE]
> Non puoi allegare file a tutti i record. Questa funzione è disponibile per i record che utilizzano la scheda dettaglio **Allegati** ad esempio un fornitore, un cliente, una fattura di acquisto o un ordine cliente.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Visualizzare un documento da un'e-mail usando l'add-in Vista documento

Che si tratti di un'e-mail inviata o ricevuta, è possibile far emergere qualsiasi documento [!INCLUDE[prod_short](includes/prod_short.md)], come il preventivo di vendita, direttamente in Outlook. Da lì, puoi apportare modifiche e navigare verso le informazioni correlate&mdash;proprio come faresti dall'interno di [!INCLUDE[prod_short](includes/prod_short.md)].

Se stai usando l'applicazione Outlook, basta scegliere **Collegamento a documento** nella parte superiore del messaggio di posta elettronica. Per Outlook sul web, cerca il link di riferimento del documento nel messaggio e-mail. Il testo del link di riferimento includerà il numero del documento, che è basato sulla serie di numeri usata in [!INCLUDE[prod_short](includes/prod_short.md)]. Per esempio, il link per un preventivo di vendita sarebbe qualcosa come **Preventivo di vendita S-QUO1000**.  

> [!TIP]
> A partire dal primo ciclo di rilascio del 2022, i documenti si aprono in una nuova finestra del browser con tutte le funzionalità che conosci di [!INCLUDE [prod_short](includes/prod_short.md)]. Puoi passare da un documento a un elenco e tornare indietro, aprire elenchi in Excel, inviare documenti da stampare ed eseguire o visualizzare in anteprima i report correlati. Hai anche tutte le scelte rapide da tastiera familiari proprio lì quando apri i documenti da Outlook.  

## <a name="see-also"></a>Vedi anche

[Prepararsi a fare affari](ui-get-ready-business.md)  
[Scaricare Business Central sul dispositivo mobile](install-mobile-app.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Finanze](finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Requisiti minimi per Outlook](product-requirements.md#outlook)  
[Utilizzare i componenti aggiuntivi in Outlook sul Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Utilizzo di Dynamics 365 for Financials come posta in arrivo aziendale in Outlook | Documenti Microsoft
description: Utilizzo di Dynamics 365 for Financials come posta in arrivo aziendale in Outlook
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a872c8817c412953a64cb1adb8f8234f2801e8fa
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-your-business-inbox-in-outlook"></a>Utilizzo di Dynamics 365 for Financials come posta in arrivo aziendale in Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] offre la possibilità di gestire le interazioni d'affari con i clienti e fornitori, direttamente in Microsoft Outlook. Con i componenti aggiuntivi Outlook di [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile visualizzare i dati finanziari relativi a clienti e fornitori e creare e inviare documenti finanziari, quali offerte o fatture.  

## <a name="get-the-add-in"></a>Ottenere il componente aggiuntivo
In [!INCLUDE[d365fin](includes/d365fin_md.md)] uno dei passaggi del setup assistito dell'Introduzione nella finestra **Esegui attività in Office 365**. Nella finestra, quando si sceglie il pulsante **Imposta in Outlook**, è necessario specificare il proprio nome utente e password di Office 365. I componenti aggiuntivi di [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente aggiunti ad Outlook.  

Quindi, quando si apre Outlook, si vedranno i messaggi e-mail dell'amministratore Financials. Il nuovo componente aggiuntivo viene aggiunto alla barra multifunzione di Outlook e in Outlook Web Access nella barra multifunzione del componente aggiuntivo, immediatamente sopra il corpo del messaggio e-mail. Il componente aggiuntivo stesso verrà aggiornato periodicamente e verrà visualizzata una notifica che una nuova versione è pronta per la società in Outlook.  

Alcune società che utilizzano Office 365 limitano i permessi degli utenti alla distribuzione dei componenti aggiuntivi. Pertanto è necessario assicurarsi di disporre di una sottoscrizione di Office 365 che include la posta elettronica e consente di distribuire i componenti aggiuntivi. Se si desidera provare comunque il componente aggiuntivo, è possibile [provare Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Se si utilizza il componente aggiuntivo Informazioni contatto
Supponiamo che si riceva un'email da un cliente che vuole un preventivo per alcuni articoli. Direttamente in Outlook, è possibile aprire il componente di Financials in cui il mittente viene riconosciuto come cliente e verrà aperta la scheda cliente relativa alla società. Dal dashboard, è possibile visualizzare le informazioni generali per il cliente ed eseguire il drill-down per ulteriori dettagli sui documenti specifici. È inoltre possibile approfondire le informazioni cronologiche di vendita per il cliente. Se si tratta di un nuovo cliente, è possibile crearlo come nuovo cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)] senza uscire da Outlook.  

Nel componente aggiuntivo, è possibile creare un'offerta di vendita e inviarla di nuovo al cliente senza uscire da Outlook. Tutte le informazioni necessarie per inviare l'offerta di vendita sono disponibili nella Posta in arrivo aziendale in Outlook.  
Una volta che si inseriscono i dati, è possibile registrare l'offerta. È possibile inviarla tramite posta elettronica. [!INCLUDE[d365fin](includes/d365fin_md.md)] genera un file PDF all'offerta di vendita e lo allega al messaggio e-mail definito nel componente aggiuntivo.  

Analogamente, se si riceve un messaggio e-mail a un fornitore, è possibile utilizzare il componente aggiuntivo per lavorare con i fornitori e le fatture di acquisto.  

Talvolta si desidera visualizzare più campi rispetto a quelli che è possibile visualizzare nel componente aggiuntivo, ad esempio se si desidera compilare le righe di una fattura. Per ottenere maggiore spazio, è possibile visualizzare il componente aggiuntivo in una finestra separata. Fa parte ancora di Outlook, ma offre più spazio per il lavoro. Se si digitano i dati per il documento nella nuova finestra, le modifiche vengono salvate automaticamente. Al termine dell'immissione dei dati per il documento, è possibile scegliere il pulsante **OK**. Scegliendo il frame del componente aggiuntivo in Outlook, il documento viene aggiornato automaticamente con le modifiche apportate nella visualizzazione apposita.  

## <a name="create-invoices-from-your-meeting-appointments"></a>Creare fatture da appuntamenti per riunioni
Alcune aziende registrano tutti gli appuntamenti fatturabili nel calendario di Outlook. In [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile creare la fattura relativa per il cliente direttamente dall'elemento: aprire l'appuntamento quindi aprire il componente aggiuntivo di [!INCLUDE[d365fin](includes/d365fin_md.md)], qui è possibile cercare informazioni esistenti oppure creare una fattura o un'altra destra del documento di vendita direttamente.  

## <a name="quick-document-lookup"></a>Ricerca rapida del documento
Il Componente aggiuntivo dei Collegamenti del documento di [!INCLUDE[d365fin](includes/d365fin_md.md)] offre accesso rapido ai documenti citati nei messaggi di posta elettronica. Il componente aggiuntivo è disponibile per un messaggio e-mail se un numero di documento viene riconosciuto nel corpo del messaggio. Aprire il componente aggiuntivo consente l'accesso rapido al documento.  

Ad esempio, se si riceve un messaggio e-mail che cita il testo *S-QUO100*, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo identifica come un'offerta di vendita e consente di aprire il documento in Outlook. In Outlook, selezionare il pulsante **Collegamenti documento** immediatamente sopra il corpo del messaggio e-mail. In the Outlook Web App, selezionare il testo *V-OFFER1001* nel corpo del messaggio e-mail.  

Nel componente aggiuntivo Collegamenti documento, è possibile modificare ed effettuare azioni relative il documento, come in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Aggiunta dei componenti aggiuntivi manualmente
In alcuni casi, i componenti aggiuntivi non vengono aggiunti automaticamente a Outlook. Anche se la società oppure un collega ha eseguito la Guida di setup assistito per conto della società, [!INCLUDE[d365fin](includes/d365fin_md.md)] potrebbe non venire visualizzato in Outlook. In questi casi, è possibile aggiungere manualmente i componente aggiuntivi [!INCLUDE[d365fin](includes/d365fin_md.md)].  

In primo luogo, è necessario verificare che non sia possibile accedere ai componenti aggiuntivi nell'account di Office 365. Semplicemente aprire la finestra Outlook Web Access in un browser quindi aggiungere `/owa/#path=/options/manageapps` all'URL sulla barra degli indirizzi. Verrà visualizzata la pagina **Gestione componenti aggiuntivi** in cui è possibile abilitare Financials per Outlook. Quindi tornare a Outlook, [!INCLUDE[d365fin](includes/d365fin_md.md)] dovrebbe essere disponibile.  

Analogamente nel client desktop di Outlook, è possibile verificare se [!INCLUDE[d365fin](includes/d365fin_md.md)] è visualizzato nella finestra **Gestione componenti aggiuntivi**.  

In entrambi i casi, se [!INCLUDE[d365fin](includes/d365fin_md.md)] non è ancora disponibile, è necessario ottenere i file add-in manifest. Per ulteriori informazioni, contattare l'amministratore di sistema Office 365.

## <a name="see-also"></a>Vedi anche
[[!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Finanza](finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  


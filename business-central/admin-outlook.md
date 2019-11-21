---
title: Utilizzo di Business Central con Outlook | Documenti di Microsoft
description: Questo servizio è completamene integrato con Office 365 e consente di gestire tutte le interazioni aziendali e la posta elettronica con clienti e fornitori direttamente in Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 10/17/2019
ms.author: edupont
ms.openlocfilehash: 6c1ec2e61b1a6d61b9662abe70e3177747b73a12
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649718"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Utilizzo di Business Central come Posta in arrivo aziendale di Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] offre la possibilità di gestire le interazioni d'affari con i clienti e fornitori, direttamente in Microsoft Outlook. Con i componenti aggiuntivi Outlook di [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile visualizzare i dati finanziari relativi a clienti e fornitori e creare e inviare documenti finanziari, quali offerte o fatture.  

## <a name="getting-the-add-in"></a>Come ottenere il componente aggiuntivo
È semplice iniziare a utilizzare il componente aggiuntivo [!INCLUDE[d365fin](includes/d365fin_md.md)] per Outlook. Nella guida al setup assistito **Imposta Posta in arrivo aziendale in Outlook**, è possibile impostare la connessione per uso personale o per la propria organizzazione se l'organizzazione utilizza Office 365. Specificare semplicemente il nome utente e la password Office 365, se richiesto, e indicare se si intende ricevere un messaggio di posta elettronica di esempio. I componenti aggiuntivi di [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente aggiunti ad Outlook. Per ulteriori informazioni, vedere [Requisiti minimi per Outlook ](product-requirements.md#outlook).  

Quindi, quando si apre Outlook, si vedrà il messaggio e-mail dell'*amministratore Dynamics 365 Business Central*. I nuovi componenti aggiuntivi sono aggiunti alla barra multifunzione di Outlook e nel browser è possibile vedere i componenti aggiuntivi di [!INCLUDE[prodshort](includes/prodshort.md)] immediatamente sopra o sotto il corpo del messaggio e-mail. I componenti aggiuntivi sono aggiornati periodicamente e verrà visualizzata una notifica che una nuova versione è pronta per la società in Outlook.  

> [!TIP]
> Se si utilizza il nuovo Outlook in un browser, i componenti aggiuntivi di [!INCLUDE [prodshort](includes/prodshort.md)] possono essere nascosti sotto **Altre azioni**.

Qualora si collabori con più società [!INCLUDE [prodshort](includes/prodshort.md)], è possibile passare con facilità tra le varie società in Outlook.

Alcune società che utilizzano Office 365 limitano i permessi degli utenti alla distribuzione dei componenti aggiuntivi. Pertanto è necessario assicurarsi di disporre di una sottoscrizione di Office 365 che include la posta elettronica e consente di distribuire i componenti aggiuntivi. Se si desidera provare comunque il componente aggiuntivo, è possibile [provare Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Utilizzo del componente aggiuntivo Informazioni contatto
Supponiamo che si riceva un'email da un cliente che vuole un preventivo per alcuni articoli. Direttamente in Outlook, è possibile aprire il componente aggiuntivo di [!INCLUDE[d365fin](includes/d365fin_md.md)] in cui il mittente viene riconosciuto come cliente e verrà aperta la scheda cliente relativa alla società. Dal dashboard, è possibile visualizzare le informazioni generali per il cliente ed eseguire il drill-down per ulteriori dettagli sui documenti specifici. È inoltre possibile approfondire le informazioni cronologiche di vendita per il cliente. Se si tratta di un nuovo contatto, è possibile crearlo come nuovo cliente in [!INCLUDE[d365fin](includes/d365fin_md.md)] senza uscire da Outlook.  

Nel componente aggiuntivo, è possibile creare un'offerta di vendita e inviarla di nuovo al cliente senza uscire da Outlook. Tutte le informazioni necessarie per inviare l'offerta di vendita sono disponibili nella Posta in arrivo aziendale in Outlook.  
Una volta che si inseriscono i dati, è possibile registrare l'offerta. È possibile inviarla tramite posta elettronica. [!INCLUDE[d365fin](includes/d365fin_md.md)] genera un file PDF all'offerta di vendita e lo allega al messaggio e-mail definito nel componente aggiuntivo.  

Analogamente, se si riceve un messaggio e-mail a un fornitore, è possibile utilizzare il componente aggiuntivo per lavorare con i fornitori e le fatture di acquisto.  

Talvolta si desidera visualizzare più campi rispetto a quelli che è possibile visualizzare nel componente aggiuntivo, ad esempio se si desidera compilare le righe di una fattura. Per ottenere maggiore spazio, è possibile visualizzare il componente aggiuntivo in una pagina separata. Fa parte ancora di Outlook, ma offre più spazio per il lavoro. Se si digitano i dati per il documento nella nuova finestra, le modifiche vengono salvate automaticamente. Al termine dell'immissione dei dati per il documento, è possibile scegliere il pulsante **OK**. Scegliendo il frame del componente aggiuntivo in Outlook, il documento viene aggiornato automaticamente con le modifiche apportate nella visualizzazione apposita.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Creazione di fatture da appuntamenti per riunioni
Alcune aziende registrano tutti gli appuntamenti fatturabili nel calendario di Outlook. In [!INCLUDE[d365fin](includes/d365fin_md.md)], è possibile creare la fattura relativa per il cliente direttamente dall'elemento: aprire l'appuntamento quindi aprire il componente aggiuntivo di [!INCLUDE[d365fin](includes/d365fin_md.md)], qui è possibile cercare informazioni esistenti oppure creare una fattura o un'altra destra del documento di vendita direttamente.  

## <a name="doing-quick-document-lookup"></a>Come effettuare la ricerca rapida del documento
Il Componente aggiuntivo dei Collegamenti del documento di [!INCLUDE[d365fin](includes/d365fin_md.md)] offre accesso rapido ai documenti citati nei messaggi di posta elettronica. Il componente aggiuntivo è disponibile per un messaggio e-mail se un numero di documento viene riconosciuto nel corpo del messaggio. Aprire il componente aggiuntivo consente l'accesso rapido al documento.  

Ad esempio, se si riceve un messaggio e-mail che cita il testo *S-QUO100*, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo identifica come un'offerta di vendita e consente di aprire il documento in Outlook. In Outlook, selezionare il pulsante **Collegamenti documento** immediatamente sopra il corpo del messaggio e-mail. In the Outlook Web App, selezionare il testo *V-OFFER1001* nel corpo del messaggio e-mail.  

Nel componente aggiuntivo Collegamenti documento, è possibile modificare ed effettuare azioni relative il documento, come in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Aggiunta manuale dei componenti aggiuntivi
In alcuni casi, i componenti aggiuntivi non vengono aggiunti automaticamente a Outlook. Anche se la società oppure un collega ha eseguito la Guida di setup assistito per conto della società, [!INCLUDE[d365fin](includes/d365fin_md.md)] potrebbe non venire visualizzato in Outlook. In questi casi, è possibile aggiungere manualmente i componente aggiuntivi [!INCLUDE[d365fin](includes/d365fin_md.md)].  

In primo luogo, è necessario verificare che non sia possibile accedere ai componenti aggiuntivi nell'account di Office 365. Basta semplicemente aprire Outlook in un browser, aprire un messaggio, selezionare **Più azioni** (...) nella parte superiore del messaggio, quindi, in fondo all'elenco, scegliere **Ottieni componenti aggiuntivi** . Viene visualizzata la pagina **Componenti aggiuntivi per Outlook** dove è possibile abilitare [!INCLUDE[prodshort](includes/prodshort.md)] per Outlook. Quindi tornare a Outlook, [!INCLUDE[prodshort](includes/prodshort.md)] dovrebbe essere disponibile.  

Analogamente nel client desktop di Outlook, è possibile verificare se [!INCLUDE[d365fin](includes/d365fin_md.md)] è visualizzato nella pagina **Scarica componenti aggiuntivi**.  

In entrambi i casi, se [!INCLUDE[d365fin](includes/d365fin_md.md)] non è ancora disponibile, è necessario ottenere i file add-in manifest. Per ulteriori informazioni, contattare l'amministratore di Office 365.

## <a name="using-other-email-accounts"></a>Utilizzo di altri account e-mail

I componenti aggiuntivi sono progettati per l'uso con Office 365. Se si utilizza [!INCLUDE [prodshort](includes/prodshort.md)] in locale, l'amministratore saprà se è possibile utilizzare i componenti aggiuntivi di [!INCLUDE [prodshort](includes/prodshort.md)] in Outlook. Per ulteriori informazioni, vedere [Quale indirizzo e-mail posso utilizzare con [!INCLUDE[prodshort](includes/prodshort.md)] ? ](across-faq.md#what-email-address-can-i-use-with-) e [Funzionalità che richiedono specifiche circostanze](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).  

## <a name="see-also"></a>Vedere anche

[Introduzione](product-get-started.md)  
[Scaricare Business Central sul dispositivo mobile](install-mobile-app.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Finanze](finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Requisiti minimi per Outlook](product-requirements.md#outlook)  
[Utilizzo di componenti aggiuntivi in Outlook sul Web](https://support.office.com/en-us/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  

---
title: Impostazione di posta elettronica in Business Central | Microsoft Docs
description: Descrive come utilizzare il server SMTP della società per inviare e ricevere messaggi e-mail all'interno di Business Central o, in alternativa, come utilizzare le impostazioni del server di posta elettronica create con la sottoscrizione di Office 365.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 07/12/2019
ms.author: edupont
ms.openlocfilehash: 5f1afacec447e645136321b73b6dd3fab8b36fe0
ms.sourcegitcommit: f5050fd209b8d66722c81abe48c4c0a6f749a1f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/12/2019
ms.locfileid: "1740481"
---
# <a name="set-up-email-manually-or-using-the-assisted-setup"></a>Impostare la posta elettronica manualmente o tramite il setup assistito
Per registrare e ricevere messaggi e-mail da [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario compilare i campi nella pagina **Setup posta elettronica SMTP**.

> [!NOTE]  
>   Anziché inserire i dettagli del server SMTP, è possibile utilizzare una funzione che consenta di immetterli con informazioni dalla sottoscrizione di Office 365.

È possibile impostare il messaggio e-mail manualmente oppure ottenere informazioni della Guida utilizzando la guida al setup assistito **Setup e-mail**. Per ulteriori informazioni, vedere [Preparazione al business](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Per impostare la posta elettronica
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup posta elettronica SMTP** e quindi scegliere il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. In alternativa, scegliere l'azione **Applica impostazioni server Office 365** per inserire tutte le informazioni che sono già state definite per la propria sottoscrizione di Office 365.
4. Quando tutti i campi vengono compilati correttamente, scegliere l'azione **Setup e-mail di verifica**.
5. Quando il test riesce, chiudere la pagina.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Utilizzo di un indirizzo mittente sostitutivo nei messaggi di posta elettronica in uscita
Tutti i messaggi di posta elettronica in uscita da [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzeranno l'indirizzo predefinito per l'account specificato nella pagina Setup e-mail SMTP, come descritto sopra. È tuttavia possibile utilizzare le funzionalità **Invia come** o **Invio per conto di** sul server Exchange per modificare l'indirizzo del mittente nei messaggi in uscita. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzerà l'account predefinito per l'autenticazione su Exchange, ma sostituirà l'indirizzo del mittente con quello specificato o lo modificherà con "per conto di". 

Di seguito vengono riportati esempi di utilizzo di Invia come e Invia per conto di in [!INCLUDE[d365fin](includes/d365fin_md.md)]:

 * Quando si inviano documenti come ordini di acquisto o di vendita a fornitori e clienti, è possibile che debbano essere visualizzati da un indirizzo _noreply@yourcompanyname.com_. 
 * Quando il flusso di lavoro invia una richiesta di approvazione tramite e-mail utilizzando l'indirizzo e-mail del richiedente.

> [!Note]
> È possibile utilizzare un solo account per sostituire gli indirizzi del mittente. Cioè, non è possibile avere un indirizzo sostitutivo per i processi di acquisto e un altro per i processi di vendita.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Per impostare l'indirizzo mittente sostitutivo per i messaggi di posta elettronica in uscita
1. Nell'**Interfaccia di amministrazione di Exchange** per l'account Office 365, trovare la casella di posta da utilizzare come indirizzo sostitutivo, quindi copiare o annotare l'indirizzo. Se è necessario un nuovo indirizzo, andare all'interfaccia di amministrazione di Microsoft 365 per creare un nuovo utente e configurare la relativa casella di posta. 
2. In [!INCLUDE[d365fin](includes/d365fin_md.md)] scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup posta elettronica SMTP** e quindi scegliere il collegamento correlato.
3. Nel campo **Invia come**, immettere l'indirizzo sostitutivo.
4. Copiare o prendere nota dell'indirizzo nel campo **ID utente**.
5. Nell'**Interfaccia di amministrazione di Exchange**, trovare la casella di posta da utilizzare come indirizzo sostitutivo, quindi immettere l'indirizzo nel campo **ID utente** nel campo **Invia come**. Per ulteriori informazioni, vedere [Gestire autorizzazioni per destinatari](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Per utilizzare l'indirizzo sostitutivo nei workflow di approvazione
1. In [!INCLUDE[d365fin](includes/d365fin_md.md)] scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup posta elettronica SMTP** e quindi scegliere il collegamento correlato.
2. Copiare o prendere nota dell'indirizzo nel campo **ID utente**.
3. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup utente approvazione** e quindi scegliere il collegamento correlato.
4. Nell'**Interfaccia di amministrazione di Exchange**, trovare le caselle di posta per ogni utente elencato nella pagina **Setup utente approvazione** e nel campo **Invia come** immettere l'indirizzo dal campo **ID utente** della pagina **Setup e-mail SMTP** pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per ulteriori informazioni, vedere [Gestire autorizzazioni per destinatari](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. In [!INCLUDE[d365fin](includes/d365fin_md.md)] scegliere l'icona ![a forma di lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup posta elettronica SMTP** e quindi scegliere il collegamento correlato.
6. Per abilitare la sostituzione, attivare l'interruttore **Consenti sostituzione mittente**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] determinerà quale indirizzo visualizzare nel seguente ordine: <br><br> 1. L'indirizzo specificato nel campo **Posta elettronica** della pagina **Setup utente approvazione** per i messaggi in un workflow. <br> 2. L'indirizzo specificato nel campo **Invia come** della pagina **Setup e-mail SMTP**. <br> 3. L'indirizzo specificato nel campo **ID utente** della pagina **Setup e-mail SMTP**.


## <a name="see-also"></a>Vedere anche  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Impostazione di [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)] come Posta in arrivo aziendale in Outlook](admin-outlook.md)  
[Scaricare [!INCLUDE[d365fin](includes/d365fin_md.md)] sul dispositivo mobile](install-mobile-app.md)

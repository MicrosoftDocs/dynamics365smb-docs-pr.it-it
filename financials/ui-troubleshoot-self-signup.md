---
title: Risoluzione dei problemi o soluzioni alternative relative all'iscrizione self-service | Documenti Microsoft
description: "Informazioni sui motivi più comuni per cui non è possibile accedere a Dynamics 365 for Financials e soluzioni per risolvere gli errori di accesso."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1bc036d4e57403d903c292a07a8985dfe939b20d
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="troubleshooting-self-service-sign-up"></a>Risoluzione dei problemi relativi all'iscrizione self-service
L'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)] è facile e può essere effettuata molto rapidamente. È possibile creare un account gratuito anche se si è un'organizzazione esistente. Questo articolo illustra i problemi che è possibile incontrare durante l'iscrizione.

## <a name="what-email-address-can-i-use-with-financials"></a>Quale indirizzo e-mail posso utilizzare con Financials?
[!INCLUDE[d365fin](includes/d365fin_md.md)] richiede l'utilizzo di un indirizzo e-mail di lavoro o della scuola. [!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Questo include indirizzi di outlook.com, hotmail.com, gmail.com e altri simili.

Se si prova a effettuare l'iscrizione con un indirizzo e-mail personale, si riceve un messaggio che richiede di utilizzare un indirizzo e-mail un lavoro o di scuola.

## <a name="troubleshooting"></a>Troubleshooting
In molti casi, la registrazione a [!INCLUDE[d365fin](includes/d365fin_md.md)] si ottiene seguendo il processo di iscrizione. Tuttavia, esistono diverse motivi per i quali non è possibile completare l'iscrizione self service. La tabella sottostante riepiloga alcuni dei motivi più comuni per cui non è possibile completare l'iscrizione e i modi in cui è possibile ovviare ai problemi.

| Sintomo/Messaggio di errore | Causa e soluzione alternativa |
| --- | --- |
| Per gli indirizzi e-mail Office 365 che non sono registrati negli Stati Uniti, durante l'iscrizione si riceve un messaggio simile al seguente:<br /><br />**Impossibile eseguire l'iscrizione. Il paese non è ancora supportato.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] attualmente supporta solo gli account e-mail di Office 365 registrati negli Stati Uniti. |
| Gli indirizzi e-mail personali come nancy@gmail.com non sono supportati. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**È stato immesso un indirizzo e-mail personale. Immettere l'indirizzo e-mail di lavoro per consentirci di archiviare in modo sicuro i dati della società.**<br> oppure <br> **È possibile che sia stato utilizzato un indirizzo di posta elettronica personale. Immettere l'indirizzo di lavoro per connettersi agli altri utenti nella società. Nessuna preoccupazione. L'indirizzo immesso non verrà condiviso con nessuno.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Per completare l'iscrizione, provare a utilizzare un indirizzo e-mail assegnato dall'organizzazione o dalla scuola. Se non è ancora possibile effettuare l'iscrizione e si desidera completare un processo di setup più avanzato, è possibile registrare una nuova sottoscrizione di prova di Office 365 e utilizzare tale indirizzo e-mail per effettuare l'iscrizione. |
| Indirizzi e-mail .gov o .mil. Durante l'iscrizione è possibile ricevere un messaggio simile al seguente:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] non disponibile. Al momento [!INCLUDE[d365fin](includes/d365fin_md.md)] non è disponibile per gli utenti con .gov o gli indirizzi e-mail di .mil attualmente. Utilizzare un altro indirizzo e-mail di lavoro o riprovare più tardi.** <br>oppure <br>**Impossibile completare l'iscrizione. [!INCLUDE[d365fin](includes/d365fin_md.md)] non risulta disponibile per l'organizzazione o la scuola indicata.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta indirizzi e-mail .gov o .mil. |
| L'iscrizione self-service non è abilitata. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile completare l'iscrizione. Il reparto IT ha disattivato l'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Contattare il proprio reparto IT per completare l'iscrizione.** <br>oppure <br> **È possibile che sia stato utilizzato un indirizzo di posta elettronica personale. Immettere l'indirizzo di lavoro per connettersi agli altri utenti nella società. Nessuna preoccupazione. L'indirizzo immesso non verrà condiviso con nessuno.** |L'amministratore IT dell'organizzazione ha disabilitato l'iscrizione self service a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per completare l'iscrizione, contattare l'amministratore IT e chiedergli di seguire le istruzioni indicate nella pagina sottostante per consentire agli utenti esistenti di iscriversi a [!INCLUDE[d365fin](includes/d365fin_md.md)] e consentire a nuovi utenti di accedere al tenant esistente. Questo problema può verificarsi anche se è stato sottoscritto Office 365 tramite un partner. |
| L'indirizzo e-mail non è un ID di Office 365. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile individuare l'utente su contoso.com. Probabilmente utilizza un ID diverso al lavoro o a scuola. Provare ad accedere con quell'account e se non funziona contattare il proprio reparto IT.** |Per accedere a Office 365 e altri servizi Microsoft, l'organizzazione utilizza degli ID che sono diversi dall'indirizzo e-mail. Ad esempio, l'indirizzo e-mail potrebbe essere Nancy.Smith@contoso.com mentre l'ID è nancys@contoso.com. Per completare l'iscrizione, utilizzare l'ID assegnato dall'organizzazione per accedere a Office 365 o altri servizi Microsoft. Per ulteriori informazioni sull'ID, contattare l'amministratore IT. Se non è ancora possibile effettuare l'iscrizione e si è in grado di completare un processo di setup più avanzato, è possibile registrare una nuova sottoscrizione di prova di Office 365 e utilizzare tale indirizzo e-mail per effettuare l'iscrizione. |

## <a name="see-also"></a>Vedi anche
[Benvenuto in [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)



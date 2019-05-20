---
title: Risoluzione dei problemi relativi all'iscrizione self-service | Documenti Microsoft
description: Informazioni sui motivi più comuni per cui non è possibile accedere a Business Central e soluzioni per risolvere gli errori di accesso.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 07b32664ac93d7772ecc245361cc6b96440857b5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249401"
---
# <a name="troubleshooting-self-service-sign-up"></a>Risoluzione dei problemi relativi all'iscrizione self-service
L'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)] è facile e può essere effettuata molto rapidamente. È possibile creare un account gratuito anche se si è un'organizzazione esistente. Questo articolo illustra i problemi che è possibile incontrare durante l'iscrizione.

## <a name="what-email-address-can-i-use-with-business-central"></a>Quale indirizzo e-mail posso utilizzare con Business Central?
[!INCLUDE[d365fin](includes/d365fin_md.md)] richiede l'utilizzo di un indirizzo e-mail di lavoro o della scuola. [!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Questo include indirizzi di outlook.com, hotmail.com, gmail.com e altri simili.

Se si prova a effettuare l'iscrizione con un indirizzo e-mail personale, si riceve un messaggio che richiede di utilizzare un indirizzo e-mail un lavoro o di scuola.

## <a name="troubleshooting"></a>Troubleshooting
In molti casi, la registrazione a [!INCLUDE[d365fin](includes/d365fin_md.md)] si ottiene seguendo il processo di iscrizione. Tuttavia, esistono diverse motivi per i quali non è possibile completare l'iscrizione self service. La tabella sottostante riepiloga alcuni dei motivi più comuni per cui non è possibile completare l'iscrizione e i modi in cui è possibile ovviare ai problemi.

| Sintomo/Messaggio di errore | Causa e soluzione alternativa |
| --- | --- |
| Per gli indirizzi e-mail di Office 365 che non sono registrati in un paese supportato, durante l'iscrizione si riceve un messaggio simile al seguente:<br /><br />**Impossibile eseguire l'iscrizione. Il paese non è ancora supportato.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] supporta attualmente solo account di posta elettronica di Office 365 registrati in un numero limitato di mercati. Per ulteriori informazioni, vedere [Disponibilità regionale](#regional-availability). |
| Gli indirizzi e-mail personali ad esempio nancy@gmail.com non sono supportati. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**È stato immesso un indirizzo e-mail personale. Immettere l'indirizzo e-mail di lavoro per consentirci di archiviare in modo sicuro i dati della società.**<br> oppure <br> **È possibile che sia stato utilizzato un indirizzo di posta elettronica personale. Immettere l'indirizzo di lavoro per connettersi agli altri utenti nella società. Nessuna preoccupazione. L'indirizzo immesso non verrà condiviso con nessuno.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Per completare l'iscrizione, provare a utilizzare un indirizzo e-mail assegnato dall'organizzazione o dalla scuola. Se non è ancora possibile effettuare l'iscrizione e si desidera completare un processo di setup più avanzato, è possibile registrare una nuova sottoscrizione di prova di Office 365 e utilizzare tale indirizzo e-mail per effettuare l'iscrizione. |
| Indirizzi e-mail .gov o .mil. Durante l'iscrizione è possibile ricevere un messaggio simile al seguente:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] non disponibile. Al momento [!INCLUDE[d365fin](includes/d365fin_md.md)] non è disponibile per gli utenti con .gov o gli indirizzi e-mail di .mil attualmente. Utilizzare un altro indirizzo e-mail di lavoro o riprovare più tardi.** <br>oppure <br>**Impossibile completare l'iscrizione. [!INCLUDE[d365fin](includes/d365fin_md.md)] non risulta disponibile per l'organizzazione o la scuola indicata.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] non supporta indirizzi e-mail .gov o .mil. |
| L'iscrizione self-service non è abilitata. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile completare l'iscrizione. Il reparto IT ha disattivato l'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Contattare il proprio reparto IT per completare l'iscrizione.** <br>oppure <br> **È possibile che sia stato utilizzato un indirizzo di posta elettronica personale. Immettere l'indirizzo di lavoro per connettersi agli altri utenti nella società. Nessuna preoccupazione. L'indirizzo immesso non verrà condiviso con nessuno.** |L'amministratore IT dell'organizzazione ha disabilitato l'iscrizione self service a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Per completare l'iscrizione, contattare l'amministratore IT e chiedergli di seguire le istruzioni indicate nella pagina sottostante per consentire agli utenti esistenti di iscriversi a [!INCLUDE[d365fin](includes/d365fin_md.md)] e consentire a nuovi utenti di accedere al tenant esistente. Questo problema può verificarsi anche se è stato sottoscritto Office 365 tramite un partner. |
| L'indirizzo e-mail non è un ID di Office 365. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile individuare l'utente su contoso.com. Probabilmente utilizza un ID diverso al lavoro o a scuola. Provare ad accedere con quell'account e se non funziona contattare il proprio reparto IT.** |Per accedere a Office 365 e altri servizi Microsoft, l'organizzazione utilizza degli ID che sono diversi dall'indirizzo e-mail. Ad esempio, se l'indirizzo e-mail è Nancy.Smith@contoso.com, l'ID potrebbe essere nancys@contoso.com. Per completare l'iscrizione, utilizzare l'ID assegnato dall'organizzazione per accedere a Office 365 o ad altri servizi Microsoft. Per ulteriori informazioni sull'ID, contattare l'amministratore IT. Se non è ancora possibile effettuare l'iscrizione e si è in grado di completare un processo di setup più avanzato, è possibile registrare una nuova sottoscrizione di prova di Office 365 e utilizzare tale indirizzo e-mail per effettuare l'iscrizione. |
| Se l'account di Office 365 è registrato in un paese supportato e si sta eseguendo la registrazione per [!INCLUDE[d365fin](includes/d365fin_md.md)] in un altro paese, durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile eseguire l'iscrizione. Il paese non è ancora supportato.**| La sottoscrizione di Office 365 dell'organizzazione è registrata in uno specifico paese nel portale di amministrazione di Office 365. Per l'iscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)] vengono utilizzate la lingua e le impostazioni locali del browser corrente e di conseguenza, è possibile ottenere il messaggio di errore anche se si è in un paese supportato. Chiedere all'amministratore IT di verificare il paese specificato nel profilo dell'organizzazione nel portale di amministrazione di [Office 365](https://portal.office.com/adminportal/home#/companyprofile). È possibile che sia necessario utilizzare un account differente per [!INCLUDE[d365fin](includes/d365fin_md.md)].|

## <a name="regional-availability"></a>Disponibilità regionale
Per un elenco dei mercati attualmente supportati, vedere la presentazione [Disponibilità internazionale di Microsoft Dynamics 365](https://docs.microsoft.com/en-us/dynamics365/get-started/availability) e la pagina di destinazione [Funzionalità locale](about-localization.md).

<!-- [!INCLUDE[d365fin](includes/d365fin_md.md)] is currently available in the following markets:

| Europe | North America |
| --- | --- |
| Australia | Canada |
| Austria | |
| Belgium | United States |
| Denmark | |
| Germany | |
| Finland | |
| France | |
| Italy | |
| Netherlands | |
| New Zealand | |
| Spain | |
| Sweden | |
| Switzerland | |
| United Kingdom | |
-->

## <a name="see-also"></a>Vedi anche
[Benvenuto in [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funzionalità locale](about-localization.md)  

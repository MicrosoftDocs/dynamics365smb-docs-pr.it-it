---
title: Risoluzione dei problemi relativi all'iscrizione self-service | Documenti Microsoft
description: Informazioni sui motivi più comuni per cui non è possibile completare l'iscrizione a Business Central e soluzioni al problema.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="troubleshooting-self-service-sign-up"></a>Risoluzione dei problemi relativi all'iscrizione self-service
L'iscrizione a [!INCLUDE[prod_short](includes/prod_short.md)] è facile e può essere effettuata molto rapidamente. È possibile creare un account gratuito anche se si è un'organizzazione esistente. Questo articolo illustra i problemi che è possibile incontrare durante l'iscrizione.

## <a name="what-email-address-can-i-use-with-business-central"></a>Quale indirizzo e-mail posso utilizzare con Business Central?
[!INCLUDE[prod_short](includes/prod_short.md)] richiede l'utilizzo di un indirizzo e-mail di lavoro o della scuola. [!INCLUDE[prod_short](includes/prod_short.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Questo include indirizzi di outlook.com, hotmail.com, gmail.com e altri simili.

Se si prova a effettuare l'iscrizione con un indirizzo e-mail personale, si riceve un messaggio che richiede di utilizzare un indirizzo e-mail un lavoro o di scuola.

## <a name="troubleshooting"></a>Troubleshooting
In molti casi, la registrazione a [!INCLUDE[prod_short](includes/prod_short.md)] si ottiene seguendo il processo di iscrizione. Tuttavia, esistono diverse motivi per i quali non è possibile completare l'iscrizione self service. La tabella sottostante riepiloga alcuni dei motivi più comuni per cui non è possibile completare l'iscrizione e i modi in cui è possibile ovviare ai problemi.

| Sintomo/Messaggio di errore | Causa e soluzione alternativa |
| --------------------- | -------------------- |
| Per gli indirizzi e-mail di Microsoft 365 che non sono registrati in un paese supportato, durante l'iscrizione si riceve un messaggio simile al seguente:<br /><br />**Impossibile eseguire l'iscrizione. Il paese non è ancora supportato.** |[!INCLUDE[prod_short](includes/prod_short.md)] supporta attualmente solo account e-mail di Microsoft 365 registrati in un numero limitato di mercati. Per ulteriori informazioni, vedere [Disponibilità regionale](#regional-availability). |
| Gli indirizzi e-mail personali come nancy@gmail.com non sono supportati. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**È stato immesso un indirizzo e-mail personale. Immettere l'indirizzo e-mail di lavoro per consentirci di archiviare in modo sicuro i dati della società.**<br> oppure <br> **È possibile che sia stato utilizzato un indirizzo di posta elettronica personale. Immettere l'indirizzo di lavoro per connettersi agli altri utenti nella società. Nessuna preoccupazione. L'indirizzo immesso non verrà condiviso con nessuno.** |[!INCLUDE[prod_short](includes/prod_short.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Per completare l'iscrizione, provare a utilizzare un indirizzo e-mail assegnato dall'organizzazione o dalla scuola. Se non è ancora possibile effettuare l'iscrizione e si desidera completare un processo di setup più avanzato, è possibile registrare un nuovo abbonamento di prova di Microsoft 365 e utilizzare tale indirizzo e-mail per effettuare l'iscrizione. |
| Indirizzi e-mail .gov o .mil. Durante l'iscrizione è possibile ricevere un messaggio simile al seguente:<br /><br />**[!INCLUDE[prod_short](includes/prod_short.md)] non disponibile. Al momento [!INCLUDE[prod_short](includes/prod_short.md)] non è disponibile per gli utenti con .gov o gli indirizzi e-mail di .mil attualmente. Utilizzare un altro indirizzo e-mail di lavoro o riprovare più tardi.** <br>oppure <br>**Impossibile completare l'iscrizione. [!INCLUDE[prod_short](includes/prod_short.md)] non risulta disponibile per l'organizzazione o la scuola indicata.** |[!INCLUDE[prod_short](includes/prod_short.md)] non supporta indirizzi e-mail .gov o .mil. |
| L'iscrizione self-service non è abilitata. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile completare l'iscrizione. Il reparto IT ha disattivato l'iscrizione a [!INCLUDE[prod_short](includes/prod_short.md)]. Contattare il proprio reparto IT per completare l'iscrizione.** <br>oppure <br> **È possibile che sia stato utilizzato un indirizzo di posta elettronica personale. Immettere l'indirizzo di lavoro per connettersi agli altri utenti nella società. Nessuna preoccupazione. L'indirizzo immesso non verrà condiviso con nessuno.** |L'amministratore IT dell'organizzazione ha disabilitato l'iscrizione self service a [!INCLUDE[prod_short](includes/prod_short.md)]. Per completare l'iscrizione, contattare l'amministratore IT e chiedergli di seguire le istruzioni indicate [in questa pagina](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups) per consentire agli utenti esistenti di iscriversi a [!INCLUDE[prod_short](includes/prod_short.md)] e consentire a nuovi utenti di accedere al tenant esistente. Questo problema può verificarsi anche se è stato eseguito l'abbonamento a Microsoft 365 tramite un partner. |
| L'indirizzo e-mail non è un ID di Microsoft 365. Durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile individuare l'utente su contoso.com. Probabilmente utilizza un ID diverso al lavoro o a scuola. Provare ad accedere con quell'account e se non funziona contattare il proprio reparto IT.** |Per accedere a Microsoft 365 e altri servizi Microsoft, l'organizzazione utilizza degli ID che sono diversi dall'indirizzo e-mail. Ad esempio, se l'indirizzo e-mail è Nancy.Smith@contoso.com, l'ID potrebbe essere  nancys@contoso.com. Per completare l'iscrizione, utilizzare l'ID assegnato dall'organizzazione per accedere a Microsoft 365 o ad altri servizi Microsoft. Per ulteriori informazioni sull'ID, contattare l'amministratore IT. Se non è ancora possibile effettuare l'iscrizione e si è in grado di completare un processo di setup più avanzato, è possibile registrare un nuovo abbonamento di prova di Microsoft 365 e utilizzare tale indirizzo e-mail per effettuare l'iscrizione. |
| Se l'account di Microsoft 365 è registrato in un paese supportato e si sta eseguendo la registrazione per [!INCLUDE[prod_short](includes/prod_short.md)] in un altro paese, durante l'iscrizione viene visualizzato un messaggio simile al seguente:<br /><br />**Impossibile eseguire l'iscrizione. Il paese non è ancora supportato.**| L'abbonamento a Microsoft 365 dell'organizzazione è registrato in uno specifico paese nel portale di amministrazione di Microsoft 365. Per l'iscrizione a [!INCLUDE[prod_short](includes/prod_short.md)] vengono utilizzate la lingua e le impostazioni locali del browser corrente e di conseguenza, è possibile ottenere il messaggio di errore anche se si è in un paese supportato. Chiedere all'amministratore IT di verificare il paese specificato nel profilo dell'organizzazione nel portale di amministrazione di [Microsoft 365](https://portal.office.com/adminportal/home#/companyprofile). È possibile che sia necessario utilizzare un account differente per [!INCLUDE[prod_short](includes/prod_short.md)].|

## <a name="regional-availability"></a>Disponibilità regionale

[!INCLUDE[prod_short](includes/prod_short.md)] è disponibile in vari paesi con la localizzazione fornita da Microsoft o da un partner di localizzazione approvato. Per un elenco completo dei paesi supportati, vedere [Disponibilità nazionale/regionale e traduzioni supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  

Per una panoramica dei mercati attualmente supportati in Dynamics 365, vedere la presentazione [Disponibilità internazionale di Microsoft Dynamics 365](/dynamics365/get-started/availability). Per una panoramica della funzionalità locale in [!INCLUDE[prod_short](includes/prod_short.md)], vedere la pagina di destinazione [Funzionalità locale](about-localization.md).  

## <a name="see-also"></a>Vedere anche

[Iscrizione per una versione di valutazione gratuita di Dynamics 365 Business Central](trial-signup.md)  
[Domande frequenti sulla versione di valutazione di Dynamics 365 Business Central](trial-faq.md)  
[Benvenuto in [!INCLUDE[prod_short](includes/prod_long.md)]](welcome.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funzionalità locale](about-localization.md)  
[Disponibilità nazionale/regionale e traduzioni supportate](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[Disponibilità internazionale di Microsoft Dynamics 365](/dynamics365/get-started/availability)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

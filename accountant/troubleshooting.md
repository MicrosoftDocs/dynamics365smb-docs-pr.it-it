---
title: Risoluzione dei problemi o soluzioni alternative | Documenti Microsoft
description: Informazioni sulle soluzioni alternative per problemi di Accountant Hub per Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a>Risoluzione dei problemi [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

L'iscrizione a [!INCLUDE[d365acc](includes/d365acc_md.md)] è facile e può essere effettuata molto rapidamente. Anche aggiungere i clienti al dashboard è facile, ma in questo articolo vengono tratti i problemi che potrebbero verificarsi.

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a>Quale indirizzo e-mail posso utilizzare con [!INCLUDE[d365acc](includes/d365acc_md.md)]?
[!INCLUDE[d365acc](includes/d365acc_md.md)] richiede l'utilizzo di un indirizzo e-mail di lavoro o della scuola. [!INCLUDE[d365acc](includes/d365acc_md.md)] non supporta gli indirizzi e-mail forniti dai servizi di posta elettronica di tipo consumer o dai provider di telecomunicazione. Questo include indirizzi di outlook.com, hotmail.com, gmail.com e altri simili.  

Se si prova a effettuare l'iscrizione con un indirizzo e-mail personale, si riceve un messaggio che richiede di utilizzare un indirizzo e-mail un lavoro o di scuola.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Perché non posso collegarmi ai dati del cliente?
Questo potrebbe verificarsi per diversi motivi, tra cui i seguenti:

- L'URL nel campo **URL cliente** non è valido.  

  Vai a **Gestisci clienti**, apri il cliente a cui non è possibile connettersi e quindi scegli **Esegui test URL cliente**.  
- La società del cliente è attualmente non in linea, ad esempio se è in corso un aggiornamento

  Nel dashboard, scegli la voce di menu **Strumenti** e quindi **Controlla errori**. Verrà visualizzato un elenco con dettagli tecnici, in modo che sia possibile contattare l'amministratore se sono presenti errori. Ad esempio, il messaggio di errore simile al seguente: "Il server ha rifiutato le credenziali del cliente" suggerisce che l'utente non dispone delle autorizzazioni di accesso.  
- Non è stato ricevuto un messaggio e-mail del cliente con invito per [!INCLUDE[d365fin](includes/d365fin_md.md)] oppure non è stata aperto il collegamento nell'e-mail o non è stato accettato l'invito

  È necessario aprire il collegamento in questione e seguire i passaggi che consentono di aggiungersi al [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente. Sino a quel momento, non è possibile accedere ai dati.  
- Non è possibile accedere a tutte le società presenti [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente.

  Il cliente dispone di più business unit o società in [!INCLUDE[d365fin](includes/d365fin_md.md)] e l'invito non include sempre tutte le società. Collaborare con il cliente in modo che non sia possibile accedere alle società con cui il cliente desidera che tu lavori.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Perché i dati non vengono aggiornati nel dashboard?
Quando si aggiunge un cliente o si richiede un aggiornamento dei dati, [!INCLUDE[d365acc](includes/d365acc_md.md)] recupera i dati. Tuttavia è necessario aggiornare la finestra manualmente, ad esempio con l'azione Rivisualizza tutte le società, aggiornando la finestra del browser, uscendo e quindi rientrando nel dashboard o in altri modi simili. Si tratta di un problema noto su cui stiamo lavorando per la risoluzione in un aggiornamento successivo.  

## <a name="see-also"></a>Vedi anche
[Introduzione a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Aggiungere clienti al dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  


---
title: Risoluzione dei problemi nell'hub aziendale
description: Informazioni su come risolvere i problemi relativi all'hub aziendale in Dynamics 365 Business Central per gestire il lavoro in più società.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accountant, accounting, troubleshoot'
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Risoluzione dei problemi dell'hub aziendale

Anche aggiungere le società al dashboard dell'hub aziendale è facile, ma in questo articolo vengono tratti i problemi che potrebbero verificarsi.  

## Controlla errori

Usare l'azione **Controlla errori** per visualizzare un elenco di errori recenti. È possibile visualizzare ulteriori dettagli per ogni errore e pulire il log eliminando le voci precedenti.  

## Connessione non riuscita

Ci possono essere un paio di motivi per cui non è possibile connettersi a una società, inclusi i seguenti:

- L'URL nel campo **Collegamento ambiente** non è valido.  

  Andare alla pagina **Collegamenti ambiente**, aprire l'ambiente a cui non è possibile connettersi, quindi scegliere l'azione **Test della connessione**.  
- La società del cliente è attualmente non in linea, ad esempio se è in corso un aggiornamento

  Nel dashboard, scegli la voce di menu **Strumenti** e quindi **Controlla errori**. Verrà visualizzato un elenco con dettagli tecnici, in modo che sia possibile contattare l'amministratore se sono presenti errori. Ad esempio, il messaggio di errore simile al seguente: "*Il server ha rifiutato le credenziali del cliente*" suggerisce che l'utente non dispone delle autorizzazioni di accesso.  
- Non si dispone dell'accesso a tutte le società nell'ambiente a cui si sta tentando di connettersi

  In [!INCLUDE [prod_short](includes/prod_short.md)], un'organizzazione può avere più business unit denominate società ed è possibile che non si disponga dell'accesso a tutte le società. Collaborare con l'amministratore o il cliente in modo che sia possibile accedere alle società con si desidera lavorare.  

## I dati non vengono aggiornati

Quando si aggiunge una società o si richiede un aggiornamento dei dati, [!INCLUDE [prod_short](includes/prod_short.md)] recupera i dati. Tuttavia è necessario aggiornare la pagina manualmente, ad esempio con l'azione **Ricarica tutte le società**, aggiornando la pagina del browser, uscendo e quindi rientrando nel dashboard o in altri modi simili.  

Se è stata aggiunta una società, ma non viene visualizzata nell'elenco, è anche possibile utilizzare l'azione **Ricarica tutte le società** per aggiornare l'elenco.

## Vedere anche

[Gestire il lavoro tra più aziende nell'hub aziendale](company-hub.md)  
[Aggiungere società all'hub aziendale](company-hub-add-company.md)  
[Esperienze contabile in Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
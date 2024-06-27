---
title: Impostare le condizioni di pagamento
description: Usare le condizioni di pagamento per gestire delle date di scadenza e degli sconti pagamento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Impostare le condizioni di pagamento

Le condizioni di pagamento determinano la modalità di gestione delle date di scadenza e degli sconti pagamento. È possibile utilizzare formule di data per definire le condizioni di pagamento. Quando ti iscrivi per la prima volta a [!INCLUDE [prod_short](includes/prod_short.md)], la società demo fornisce alcuni metodi di pagamento che le aziende utilizzano spesso. Puoi tuttavia aggiungere tutti quelli desiderati.  

Se assegni condizioni di pagamento a clienti e fornitori, le stesse condizioni siano sempre utilizzate per i documenti vendita e acquisto create per gli stessi. Per calcolare le date di scadenza dei pagamenti vengono utilizzate le date dei documenti di vendita e di acquisto, non le relative date di registrazione. Se necessario, è possibile modificare i termini nel documento di vendita o di acquisto. Ad esempio, se desideri che un determinato cliente ti paghi entro sette giorni anziché i 14 giorni predefiniti. La modifica dei termini sul documento non modifica la condizione di pagamento predefinito assegnato al cliente. Le stesse condizioni di pagamento sono disponibili per documenti vendita e acquisto.

Quando registri una fattura, [!INCLUDE [prod_short](includes/prod_short.md)] calcola gli sconti pagamento in base alle condizioni di pagamento. La data di sconto sul pagamento è la data più recente in cui il cliente riceve uno sconto. La data viene calcolata anche quando si registra una fattura.  

Analogamente, quando registri una nota credito, [!INCLUDE [prod_short](includes/prod_short.md)] calcola gli sconti pagamento in base alle condizioni di pagamento. Calcola lo sconto sulle note credito in base agli stessi principi degli sconti sulle fatture. Quando si applica una nota di credito a una fattura, [!INCLUDE [prod_short](includes/prod_short.md)] riduce l'importo dello sconto per la fattura dell'importo dello sconto della nota di credito.  

Se si desidera inviare ai clienti solleciti per pagamenti in ritardo, è necessario impostare i livelli e i termini di sollecito. Per ulteriori informazioni sui solleciti, vai a [Impostare i termini e i livelli di sollecito](finance-setup-reminders.md).  

## Impostare le condizioni di pagamento

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Condizioni pagamento**, quindi scegli il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Dopo avere impostato le condizioni di pagamento, è possibile assegnarle ai clienti e ai fornitori. Facoltativamente, assegna condizioni di pagamento ai metodi di pagamento.  

> [!TIP]
> Nella versione base di [!INCLUDE [prod_short](includes/prod_short.md)], le condizioni di pagamento con pagamenti parziali non sono supportate. È invece necessario utilizzare la funzionalità di pagamento anticipato. Per ulteriori informazioni sui pagamenti anticipati, vai a [Impostare i pagamenti anticipati](finance-set-up-prepayments.md).
>
> In alcuni paesi/aree geografiche, *puoi* impostare le condizioni di pagamento con pagamenti parziali. Per sapere se questa funzionalità è supportata nel tuo paese/area geografica, vai alla sezione **Funzionalità locale** nel sommario sul lato sinistro di un articolo [Microsoft Learn](about-localization.md).

## Vedere anche

[Impostare i metodi di pagamento](finance-payment-methods.md)  
[Impostare i pagamenti anticipati](finance-set-up-prepayments.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

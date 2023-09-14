---
title: Impostare le condizioni pagamento
description: 'Nella versione base di Business Central, utilizza i termini di pagamento per gestire le date di scadenza e gli sconti pagamento.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: 4
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-payment-terms"></a>Impostare le condizioni pagamento

I termini di pagamento determinano la modalità di gestione delle date di scadenza e degli sconti pagamento. È possibile impostare un numero indefinito di codici di condizioni pagamento e utilizzare le formule data per definire le condizioni pagamento. Quando ti iscrivi per la prima volta a [!INCLUDE [prod_short](includes/prod_short.md)], la società demo fornisce alcuni metodi di pagamento che le aziende utilizzano spesso. È tuttavia possibile aggiungere tutti quelli desiderati.  

È possibile assegnare condizioni pagamento a clienti e fornitori di modo che le stesse condizioni siano sempre utilizzate per i documenti vendita e acquisto create per gli stessi. Se necessario, puoi modificare le condizioni sul documento vendita o acquisto, ad esempio se desideri che un determinato cliente ti paghi entro 7 giorni anziché i 14 giorni predefiniti. Ciò non modifica le condizioni pagamento predefinite assegnate al cliente. Le stesse condizioni pagamento sono disponibili per documenti vendita e acquisto.

Quindi, quando registri una fattura, [!INCLUDE [prod_short](includes/prod_short.md)] calcola gli sconti pagamento in base alle condizioni pagamento. Nello stesso momento verrà calcolata anche la data dello sconto pagamento, ovvero l'ultima data utile per il pagamento che consenta al cliente di ricevere uno sconto sul pagamento.  

Analogamente, quando registri una nota credito, [!INCLUDE [prod_short](includes/prod_short.md)] calcola gli sconti pagamento possibili in base alle condizioni pagamento. Lo sconto sulle note credito viene calcolato in base agli stessi principi degli sconti pagamento sulle fatture. Quando si applica una nota credito a una fattura, l'importo dell'eventuale sconto pagamento per la fattura verrà ridotto dall'importo dello sconto pagamento per la nota credito.  

Se si desidera inviare ai clienti solleciti per pagamenti in ritardo, è necessario impostare i livelli e i termini di sollecito. Per ulteriori informazioni, vedere [Impostare i termini e i livelli di sollecito](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Impostare le condizioni pagamento

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Condizioni pagamento**, quindi scegli il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Dopo avere impostato le condizioni pagamento, è possibile assegnarle ai clienti e ai fornitori. Facoltativamente, assegna condizioni pagamento ai metodi di pagamento.  

> [!TIP]
> Nella versione base di [!INCLUDE [prod_short](includes/prod_short.md)], le condizioni pagamento con pagamenti parziali non sono supportate. È invece necessario utilizzare la funzionalità di pagamento anticipato. Per ulteriori informazioni, vedere [Impostare i pagamenti anticipati](finance-set-up-prepayments.md).
>
> In alcuni paesi/aree geografiche, *puoi* impostare le condizioni pagamento con pagamenti parziali. Per sapere se questa funzionalità è supportata nel tuo paese/area geografica, consulta la sezione **Funzionalità locale** nel riquadro di navigazione sul lato sinistro di un articolo [Microsoft Learn](about-localization.md).

## <a name="see-also"></a>Vedi anche

[Impostare i metodi di pagamento](finance-payment-methods.md)  
[Impostare i pagamenti anticipati](finance-set-up-prepayments.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

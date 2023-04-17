---
title: Impostare le condizioni pagamento
description: 'Nella versione italiana di Business Central, per ogni condizione pagamento, è possibile specificare se il pagamento può essere rateizzato.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '12170, 12171, 12172, 12173, 12174'
ms.date: 04/01/2021
ms.author: edupont
---
# Impostare le condizioni pagamento nella versione italiana

I termini di pagamento determinano la modalità di gestione delle date di scadenza e degli sconti pagamento. Per ogni condizione di pagamento, è possibile specificare se il pagamento può essere rateale. Ad esempio, è possibile definire che un pagamento può essere eseguito in tre rate dello stesso importo dopo 30, 60 e 90 giorni.  

Se una condizione di pagamento deve prevedere un unico pagamento, è necessario specificare come verrà calcolata la data di scadenza.  

Quando ti iscrivi per la prima volta a [!INCLUDE [prod_short](../../includes/prod_short.md)], la società demo fornisce alcuni metodi di pagamento che le aziende utilizzano spesso. Puoi tuttavia aggiungere tutti quelli desiderati.

## Impostare le condizioni pagamento

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Condizioni pagamento**, quindi scegli il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Calcola**.  
4. Nella pagina **Righe condizioni pagamento**, compilare i campi come indicato nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**% pagamento**|Specificare la percentuale del pagamento totale a cui si riferisce il pagamento rateale.<br /><br /> Ad esempio, se il pagamento deve essere effettuato in una rata, immettere **100**.|  
    |**Calcolo Data di Scadenza**|Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato.<br /><br /> Ad esempio, se il pagamento deve essere effettuato in una rata dopo due settimane, immettere **14D**. Per ulteriori informazioni, vedi [Utilizzare le formule per le date](../../ui-enter-date-ranges.md#use-date-formulas)|  
    |**Calcolo Sconto per Data**|Specificare la formula che viene utilizzata per calcolare la data in cui il pagamento deve essere effettuato per ottenere uno sconto.|  
    |**Sconto %**|Specificare la percentuale di sconto che viene applicata per il pagamento anticipato di un importo fattura.|  

5. Scegliere il pulsante **OK**.  

Il campo **Nr. di pagamenti** nella pagina **Condizioni pagamento** viene aggiornato. Le condizioni di pagamento impostate qui saranno un riferimento per il calcolo automatico della data di scadenza dei documenti registrati per clienti e fornitori.  

Dopo avere impostato le condizioni pagamento, è possibile assegnarle ai clienti e ai fornitori. Facoltativamente, assegna condizioni pagamento ai metodi di pagamento.  

## Vedere anche

[Impostare le condizioni pagamento nella versione italiana](../../finance-payment-terms.md)  
[Definizione dei metodi di pagamento](../../finance-payment-methods.md)  
[Impostazione di dati finanziari](../../finance-setup-finance.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
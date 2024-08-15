---
title: Utilizzo della funzione di trasferimento della differenza sul conto per riconciliare i pagamenti
description: 'Descrive come elaborare i pagamenti che non possono essere applicati a un documento, ad esempio quando un tasso di cambio determina una differenza negli importi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="reconcile-payments-that-cant-be-applied-automatically"></a>Riconciliare i pagamenti che non possono essere applicati automaticamente
A volte potrebbe essere necessario gestire pagamenti sul tuo conto bancario che non possono essere applicati a una voce contabile aperta correlata a un cliente, a un fornitore o a un conto bancario. I motivi potrebbero essere che non esiste alcun documento a cui applicare il pagamento oppure che il documento correlato ha un importo diverso da quello della transazione, ad esempio a causa del cambio valuta. [!INCLUDE[prod_short](includes/prod_short.md)]  [!INCLUDE[prod_short](includes/prod_short.md)]  Nella pagina  **Giornale di riconciliazione dei pagamenti**, tutti gli importi delle transazioni per i pagamenti che non sono ancora stati applicati vengono visualizzati nel campo  **Differenza**, inclusi gli importi che non possono essere applicati per motivi come quelli sopra indicati.

I metodi per risolvere questi tipi di pagamento non collegati:
* Collegare manualmente
* Utilizzare la mappatura testo a conto
* Trasferire un importo in eccesso a una riga di registrazione per creare e registrare il movimento richiesto, ad esempio un rimborso di un sovrapagamento.

I pagamenti che non possono essere applicati possono comparire nelle righe del giornale di riconciliazione dei pagamenti nei seguenti modi diversi:

* Il valore nel campo **Differenza** è uguale al valore del campo **Importo transazioni**, pertanto nessuna parte del pagamento può essere collegata a un movimento contabile del conto corrente bancario, fornitore o cliente aperto.
* Il valore nel campo **Differenza** è inferiore al valore del campo **Importo transazioni**, pertanto una parte del pagamento può essere collegata a un movimento contabile del conto corrente bancario, fornitore o cliente aperto. La parte rimanente del pagamento non può essere utilizzata e deve essere riconciliata manualmente o registrandola direttamente su un conto.

Per riconciliare questi pagamenti, è possibile scegliere l'azione **Trasferisci differenza a conto** quindi specificare su quale conto registrare l'importo del campo **Differenza** quando si effettua la registrazione riconciliazione pagamenti. È possibile farlo dalla pagina **Registrazione riconciliazione pagamenti** o **Revisione collegamento del pagamento** aperta scegliendo il valore nel campo **Affidabilità corrispondenza** o scegliendo il campo **Differenza**.

> [!TIP]  
>   Tale funzionalità consente di impostare la riconciliazione automatica dei pagamenti ricorrenti che non possono essere collegati ai relativi movimenti contabili del conto corrente bancario, fornitore o cliente aperto. Per ulteriori informazioni, vedere [Mappare il testo nei pagamenti ricorrenti a conti per la riconciliazione automatica](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cant-be-applied-automatically"></a>Per riconciliare i pagamenti che non possono essere applicati automaticamente
1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni riconciliazione pagamenti**, quindi scegli il collegamento correlato.
2. Aprire una registrazione della riconciliazione di pagamento. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).
3. Scegliere **Trasferisci differenza a conto**. Si apre la pagina **Trasferisci differenza a conto**.
4. Nel campo **Tipo conto** specificare il tipo di conto in cui sarà registrato l'importo di pagamento.
5. Nel campo **Nr. conto** specificare il conto in cui sarà registrato l'importo di pagamento.
6. Nel campo **Descrizione** specificare il testo che descrive questa registrazione di pagamento diretto. Per impostazione predefinita, viene inserito il testo nel campo **Testo transazione** nella riga di registrazione riconciliazione pagamenti.
7. Scegliere il pulsante **OK**.

Se il valore nel campo **Differenza** è uguale al valore del campo **Importo transazioni** quando si registra la riconciliazione pagamenti, l'intero pagamento nella riga di registrazione sarà registrato direttamente nel conto di contropartita specificato.

Se il valore nel campo **Differenza** è inferiore al valore del campo **Importo transazioni**, verrà creata una nuova riga di registrazione aggiuntiva con lo stesso testo e la stessa data e con la differenza inserita nel campo **Importo transazioni**. Nella riga di registrazione originale, la differenza verrà dedotta dal valore nel campo **Importo transazioni** e il pagamento rimarrà collegato al relativo movimento contabile del conto corrente bancario, fornitore o cliente. Quando si contabilizza la registrazione riconciliazione pagamenti, una parte del pagamento verrà registrata come pagamento collegato. L'altra parte del pagamento verrà registrata direttamente nel conto specificato.

## <a name="see-also"></a>Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Registrare pagamenti e resi nelle registrazioni pagamenti
description: Informazioni su come registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti nella pagina Registrazioni pagamenti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrare pagamenti e resi nella registrazione pagamenti

Nella pagina  **Giornali di pagamento**, puoi registrare i pagamenti effettuati ai fornitori e i rimborsi effettuati ai clienti. Quando si registra una riga di registrazione pagamenti, l'importo pagato viene registrato nel conto corrente bancario specificato. È quindi necessario intraprendere le azioni necessarie per eseguire il trasferimento effettivo del denaro dal relativo conto bancario.  

Le registrazioni pagamenti sono registrazioni generali ottimizzate per eseguire i pagamenti. È possibile aggiungere rapidamente le righe manualmente, si può consentire a [!INCLUDE[prod_short](includes/prod_short.md)] di suggerire i pagamenti dei fornitori e collegare il pagamento ai documenti registrati. Sebbene si stiano eseguendo i pagamenti, si immette un importo positivo nel campo **Importo documento**. In base al tipo di documento per la riga delle registrazioni, questo importo viene quindi convertito in un importo negativo nelle transazioni sottostanti. In questo modo, è più veloce aggiungere le righe nelle registrazioni manualmente. Se si preferisce immettere importi negativi, è possibile personalizzare le registrazioni pagamenti per mostrare invece il campo **Importo**. Per ulteriori informazioni sulla personalizzazione di pagine, vedi [Iniziare a personalizzare utilizzando la modalità di personalizzazione](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).  

- Collegare i pagamenti a fatture o note di credito

    Se si compila il campo **Collega-a nr. doc.** con la fattura o la nota di credito da pagare o rimborsare, il documento viene impostato su **Pagato** quando la registrazione viene contabilizzata. Questa impostazione viene definita "applicata". In alternativa al collegamento durante la registrazione di un pagamento, è possibile utilizzare le pagine **Collega movimenti fornitori** e **Collega movimenti clienti** dopo aver effettuato la registrazione dei pagamenti. Per ulteriori informazioni, vedi, ad esempio, [Riconciliare i pagamenti ai fornitori con la registrazione pagamenti o dai movimenti contabili fornitori](payables-how-apply-purchase-transactions-manually.md).  

- Ricevere pagamenti suggeriti per fornitori o dipendenti

    Le azioni **Sugg. pagamenti fornitore** e **Suggerisci pagamenti dipendente** possono essere utili per compilare automaticamente le righe delle registrazioni pagamenti in base alle priorità e alle data di scadenza del fornitore. Per saperne di più, vedi [Suggerire pagamenti fornitore](payables-how-suggest-vendor-payments.md). Con questa funzione, il campo **Collega-a nr. doc.** viene sempre compilato.  

- Stampare assegni e inviare elettronicamente i pagamenti alla banca

    Oltre alla registrazione che il pagamento è stato effettuato, è possibile utilizzare la pagina **Registrazioni pagamenti** per emettere il pagamento per l'ulteriore elaborazione da parte della banca. Per ulteriori informazioni, vedi [Effettuare pagamenti tramite assegno](payables-how-work-checks.md) e [Effettuare pagamenti elettronici](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Per eseguire i pagamenti nelle registrazioni pagamenti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Apri il batch registrazioni che usi per i pagamenti.
3. Se conosci i clienti da pagare, compila i campi manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per applicare il pagamento anche alla fattura o nota di accredito correlata, selezionare il campo  **Applica a n. doc.** nella pagina  **Applica voci fornitore**, Seleziona la fattura o nota di accredito pertinente, quindi selezionare il pulsante  **OK** .

    Molti campi, ad esempio i campi **Importo documento** e **Data scadenza** ora contengono informazioni tratte dal documento selezionato.
5. In alternativa, utilizza l'azione **Sugg. pagamenti fornitore**. Tutte le informazioni applicabili e gli importi vengono quindi inseriti anche nelle righe di registrazione. Per saperne di più, vedi [Suggerire pagamenti fornitore](payables-how-suggest-vendor-payments.md).
6. Una volta completate tutte le righe di registrazione pagamenti, scegliere l'azione **Registra**.

## <a name="to-issue-a-refund-check"></a>Per emettere un assegno di rimborso

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.
2. Nel campo **Tipo di documento** seleziona **Rimborso**.  
3. Nel campo **Nr. documento esterno**, immetti un riferimento per l'assegno di rimborso (ad esempio, il numero di ordine di reso).  
4. Nel campo **Tipo conto** selezionare **Cliente**.  
5. Nel campo **Nr. conto**, seleziona il numero di conto del cliente per cui viene emesso l'assegno di rimborso.  
6. Immetti l'importo da rimborsare nel campo **Importo**.  
7. Nel campo **Tipo contropartita** selezionare **Conti C/C bancari**.  
8. Nel campo  **Numero conto saldo**, Seleziona indica il conto bancario da cui proviene l'assegno.  
9. Nel campo **Collega-a nr. doc.** seleziona i documenti che richiedono un rimborso.  
10. Quando tutte le righe di registrazione pagamenti sono state completate, scegli l'azione **Registra/Stampa** quindi scegli **Registra e stampa** e infine **Sì**.  
  
## <a name="see-also"></a>Vedere anche

[Effettuare pagamenti tramite assegno](payables-how-work-checks.md)  
[Effettuare pagamenti elettronici](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

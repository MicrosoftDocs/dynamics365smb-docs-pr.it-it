---
title: Registrare pagamenti e resi nelle Registrazioni pagamenti
description: Informazioni su come registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti nella pagina Registrazioni pagamenti.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/09/2021
ms.author: edupont
---
# <a name="record-payments-and-refunds-in-the-payment-journal" />Registrare pagamenti e resi nelle Registrazioni pagamenti

Nella pagina **Registrazioni pagamenti** è possibile registrare i pagamenti corrisposti ai fornitori e i rimborsi corrisposti ai clienti. Quando si registra una riga di registrazioni dei pagamenti, l'importo pagato viene registrato sul conto bancario di sistema specificato. È quindi necessario intraprendere le azioni necessarie per eseguire il trasferimento effettivo del denaro dal relativo conto bancario.  

Le registrazioni pagamenti sono registrazioni generali ottimizzate per eseguire i pagamenti. È possibile aggiungere rapidamente le righe manualmente, si può consentire a [!INCLUDE[prod_short](includes/prod_short.md)] di suggerire i pagamenti dei fornitori ed applicare il pagamento ai documenti registrati. Anche se si sta eseguendo i pagamenti, si immette un importo positivo nel campo **Importo documento**. In base al tipo di documento per la riga delle registrazioni, questo importo viene quindi convertito in un importo negativo nelle transazioni sottostanti. In questo modo, è più veloce aggiungere le righe nelle registrazioni manualmente. Se si preferisce immettere importi negativi, è possibile personalizzare le registrazioni pagamenti per mostrare invece il campo **Importo**.  

- Applicare i pagamenti alle fatture o note di credito

    Se si compila il campo **Collega-a nr. doc.** con la fattura o la nota di credito che deve essere pagata o rimborsata, il documento in questione viene impostato su pagato quando tale registrazione viene contabilizzata. Questa procedura viene definita "collegamento". In alternativa all'applicazione durante la registrazione dei pagamenti, è possibile utilizzare le pagine **Collega movimenti fornitori** e **Collega movimenti clienti** dopo aver effettuato la registrazione dei pagamenti. Per ulteriori informazioni, vedere, ad esempio, [Riconciliare manualmente i pagamenti ai fornitori con la registrazioni pagamenti o dai movimenti contabili fornitori](payables-how-apply-purchase-transactions-manually.md).  

- Ricevere pagamenti suggeriti per fornitori o dipendenti

    Le funzioni **Suggerisci pagamenti fornitore** e **Suggerisci pagamenti dipendente** possono essere utili per compilare automaticamente le righe delle registrazioni pagamenti in base alle priorità e alle data di scadenza. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md). Con questa funzione, il campo **Collega-a nr. doc.** viene sempre compilato.  

- Stampare assegni e inviare elettronicamente i pagamenti alla banca

    Oltre alla registrazione che il pagamento è stato effettuato, è possibile utilizzare la pagina **Registrazioni pagamenti** per emettere il pagamento per l'ulteriore elaborazione da parte della banca. Per ulteriori informazioni, vedere [Effettuare pagamenti tramite assegno](payables-how-work-checks.md) e [Effettuare pagamenti elettronici](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal" />Per eseguire i pagamenti nelle registrazioni pagamenti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Aprire il batch contabile che verrà dedicato ai pagamenti.
3. Se conosci i clienti da pagare, compila i campi manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Per collegare anche il pagamento alla relativa fattura o nota di credito, selezionare il campo **Collega-a nr. doc.** nella pagina **Collega movimenti fornitori**, selezionare la relativa fattura o nota di credito, quindi selezionare il pulsante **OK**.

    Molti campi, ad esempio i campi **Importo documento** e **Data scadenza** vengono compilati con le informazioni tratte dal documento selezionato.
5. In alternativa, utilizzare la funzione **Sugg. pagamenti fornitore**. Tutte le informazioni applicabili e gli importi vengono quindi inseriti anche nelle righe del giornale di registrazione. Per ulteriori informazioni, vedere [Suggerire i pagamenti ai fornitori](payables-how-suggest-vendor-payments.md).

    I messaggi guideranno la compilazione corretta dei campi richiesti.
6. Una volta completate tutte le righe di registrazione pagamento, scegliere l'azione **Registra**.


## <a name="to-issue-a-refund-check" />Per emettere un assegno di rimborso

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immettere **Registrazioni pagamenti** e quindi scegliere il collegamento correlato.
2. Nel campo **Tipo di documento** seleziona **Rimborso**.  
3. Nel campo **Nr. documento esterno**, utilizzalo come riferimento per l'assegno di rimborso (ad esempio, numero di ordine di reso).  
4. Nel campo **Tipo conto** selezionare **Cliente**.  
5. Nel campo **Nr. conto**, seleziona il numero di conto del cliente per cui viene emesso l'assegno di rimborso.  
6. Immetti l'importo da rimborsare nel campo **Importo**.  
7. Nel campo **Tipo contropartita** seleziona **Conti C/C bancari**.  
8. Nel campo **Nr. contropartita**, seleziona il conto bancario da cui uscirà l'assegno.  
9. Nel campo **Collega-a nr. doc.** seleziona i documenti che richiedono un rimborso.  
10. Quando tutte le righe di registrazione pagamenti sono state completate, scegli l'azione **Registra/Stampa** quindi scegli **Registra e stampa** e seleziona **Sì**.  
  

## <a name="see-also" />Vedere anche
[Effettuare pagamenti tramite assegno](payables-how-work-checks.md)  
[Effettuare pagamenti elettronici](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Impostazione delle attività bancarie](bank-setup-banking.md)  
[Esportare un file Positive Pay](finance-how-positive-pay.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Personalizzare l'area di lavoro](ui-personalization-user.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

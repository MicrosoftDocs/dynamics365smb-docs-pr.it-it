---
title: Rivedere o collegare i pagamenti manualmente in seguito al collegamento automatico
description: 'Dopo che i pagamenti sono stati collegati automaticamente, è possibile verificare tutti i movimenti relativi a un pagamento e ricollegare manualmente i movimenti che sono stati collegati erroneamente.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="review-and-apply-payments-manually-after-automatic-application" />Rivedere o collegare i pagamenti manualmente in seguito al collegamento automatico
Per ogni riga di registrazione che rappresenta un pagamento nella pagina **Registrazione riconciliazione pagamenti** è possibile aprire la pagina **Collegamento pagamenti** per vedere tutti i movimenti aperti candidati per il pagamento e visualizzare, per ciascun movimento, informazioni dettagliate sulla corrispondenza dei dati su cui si basa un collegamento di pagamento. Qui è possibile collegare manualmente i pagamenti o applicare nuovamente i pagamenti che sono stati collegati automaticamente a un movimento aperto scorretto. Per ulteriori informazioni sul collegamento automatico, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Quando il conto corrente bancario per il quale si stanno riconciliando i pagamenti è impostato sulla valuta locale, nella pagina **Collegamento pagamenti** vengono mostrati tutti i movimenti aperti nella valuta locale, inclusi i movimenti aperti per i documenti originariamente fatturati in valute estere. I pagamenti collegati ai movimenti con valute convertite possono quindi essere registrati con importi diversi rispetto al documento originale per via dei tassi di cambio potenzialmente diversi utilizzati dalla banca e da [!INCLUDE[prod_short](includes/prod_short.md)] rispettivamente.

Di conseguenza, consigliamo di guardare i codici valuta estera nel campo **Codice valuta** della pagina **Collegamento pagamenti** per controllare se i collegamenti sono basati su valute convertite. Per verificare l'imposto del documento originale in valuta estera e visualizzare il tasso di cambio utilizzato, selezionare il campo **Collega-a Nr. mov.** quindi, nel menu di scelta rapida, selezionare il pulsante DrillDown per aprire la pagina **Movimenti contabili clienti** o **Movimenti contabili fornitori**.

Ogni rettifica di guadagno-e-perdite obbligatoria a causa delle conversioni di valuta non viene gestita automaticamente da [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]  
>   Non è possibile collegare movimenti con un segno diverso dal segno sul pagamento. Ad esempio, per chiudere sia una nota di credito di segno negativo che la relativa fattura relativa di segno positivo, è necessario innanzitutto collegare la nota di credito alla fattura, quindi collegare il pagamento alla fattura con l'importo residuo ridotto.

> [!WARNING]  
>   Se si utilizzano sconti sul pagamento e se la data di pagamento è anteriore alla data di scadenza del pagamento, verrà utilizzato per la corrispondenza il campo **Importo residuo incluso sconto** della pagina **Collegamento pagamenti**. In alternativa, verrà utilizzato il valore del campo **Importo residuo**. Se il pagamento è stato eseguito con un importo scontato dopo la data di scadenza del pagamento, o l'importo completo è stato pagato ma è stato concesso uno sconto, non sarà possibile far corrispondere l'importo.

> [!NOTE]  
>   È possibile collegare un pagamento solo a un conto. Se si desidera suddividere il collegamento su più movimenti aperti, ad esempio per collegare un pagamento forfettario, i movimenti aperti devono essere per lo stesso conto. Per ulteriori informazioni, vedere passaggi 7 e 8 della procedura in questo argomento.

## <a name="to-review-or-apply-payments-after-automatic-application" />Per esaminare o collegare i pagamenti in seguito al collegamento automatico
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni riconciliazione pagamenti**, quindi scegli il collegamento correlato.
2. Aprire la registrazione della riconciliazione di pagamento di un conto corrente bancario per cui si desidera riconciliare i pagamenti. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).
3. Nella pagina **Registrazione riconciliazione pagamenti**, selezionare un pagamento che si desidera esaminare o collegare manualmente a uno o più movimenti aperti, quindi scegliere l'azione **Collega manualmente**.
4. Selezionare la casella di controllo **Collegato** nella riga del movimento aperto al quale si vuole collegare il pagamento.
5. L'importo del pagamento, che viene mostrato anche nel campo **Importo transazioni** della pagina **Collegamento pagamenti**, viene inserito nel campo **Importo collegato**. Il campo può tuttavia essere modificato, ad esempio se si desidera collegare l'importo a numerosi movimenti aperti.
6. Per collegare una parte dell'importo pagato a un altro movimento aperto per il conto, ad esempio per collegare un pagamento forfettario, selezionare la casella di controllo **Collegato** per la riga. L'importo collegato viene automaticamente dedotto dall'importo della transazione per riflettere la distribuzione dei due movimenti aperti.
7. Per collegare una parte di un pagamento a uno o più movimenti aperti inesistenti nel database, creare una nuova riga sotto la riga per lo stesso conto. Nel campo **Importo collegato** immettere l'importo da collegare nella nuova riga, quindi rettificare il campo **Importo collegato** nella riga esistente.
8. Ripetere i passaggi 5, 6 o 7 per gli altri movimenti aperti a cui si desidera collegare una parte o il totale dell'importo di pagamento.
9. Una volta esaminato un collegamento di pagamento o collegato manualmente a uno o più movimenti aperti, scegliere l'azione **Accetta collegamento**.

Viene chiusa la pagina **Collegamento pagamenti** e nella pagina **Registrazione riconciliazione pagamenti** il valore del campo **Affidabilità corrispondenza** viene modificato in **Accettato** a indicare che il pagamento è stato esaminato o collegato manualmente.

## <a name="see-also" />Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Riconciliare le ricevute di pagamento o i rimborsi del fornitore nelle registrazioni pagamenti
description: 'Per elaborare, associare, riconciliare manualmente i pagamenti o i rimborsi dei fornitori, è possibile collegare l''importo a uno o più movimenti contabili aperti del fornitore.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment application, payment processing, match payments'
ms.search.form: '62, 233, 522, 623'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Riconciliare manualmente i pagamenti ai fornitori con la registrazioni pagamenti o dai movimenti contabili fornitori.
Quando si invia un pagamento o si riceve un rimborso da un fornitore, è necessario decidere se collegare il pagamento o il rimborso a uno o più movimenti aperti. È possibile specificare l'importo esatto che si desidera collegare alla ricevuta di pagamento o al rimborso, quindi collegare solo parzialmente i movimenti contabili fornitori. È necessario collegare tutti i movimenti contabili fornitori per ottenere statistiche e report corretti degli estratti conto e degli interessi attivi.

> [!NOTE]  
>   Talvolta i fornitori concedono un rimborso anziché una nota di credito per compensare le fatture successive, in particolare nei casi in cui si rendono articoli già pagati o si è corrisposto un prezzo maggiore della fattura.

È possibile collegare i movimenti contabili fornitori in tre modi diversi:

* Immettendo informazioni nelle finestre dedicate, ad esempio nella pagina **Registrazioni pagamenti** e nella pagina **Registrazione riconciliazione pagamenti**.
* Dai documenti di nota di credito di acquisto.
* Dai movimenti contabili fornitori dopo che i documenti di acquisto sono stati registrati ma non collegati.

> [!NOTE]  
>   Se il campo **Metodo collegamento** nella scheda fornitore è impostato su **Collega al più Vecchio**, i pagamenti saranno automaticamente collegati al movimento di credito meno recente, a meno che non si specifichi manualmente a quale movimento collegarli. Se il metodo di collegamento per un cliente è impostato su **Manuale**, i movimenti dovranno essere collegati manualmente.

È possibile collegare i pagamenti fornitori manualmente ai documenti di acquisto correlati quando si registrano i pagamenti nella pagina **Registrazioni pagamenti**. Per informazioni sulla compilazione delle registrazioni pagamenti, vedere [Effettuare i pagamenti](payables-make-payments.md).

È inoltre possibile collegare i pagamenti fornitori e i pagamenti clienti dopo che i pagamenti risultano come transazioni bancarie negative in banca. Nella pagina **Registrazione riconciliazione pagamenti** è possibile utilizzare le funzioni per l'importazione del rendiconto bancario, il collegamento automatico e la riconciliazione bancaria. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Per collegare un pagamento a uno o più movimenti contabili fornitori
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Nella pagina **Registrazioni pagamenti**, immettere nella prima riga di registrazione le informazioni rilevanti sul movimento di pagamento.
3. Per collegare un singolo movimento contabile fornitore:
   1. Nel campo **Collega-a nr. doc.** scegliere il campo da aprire nella pagina **Collega movimenti fornitori**.
   2. Nella pagina **Collega movimenti fornitori** selezionare il movimento a cui collegare il pagamento.
   3. Nella riga del campo **Importo da collegare** immettere l'importo da collegare al movimento.
4. In alternativa, per collegare più movimenti contabili fornitori:

   1. Scegliere l'azione **Collega movimenti**.
   2. Nella pagina **Partite fornitori** selezionare le righe con i movimenti ai quali collegare il pagamento.
   3. Scegliere l'azione **Collega a ID**.  
   4. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento.

      Se non si immette alcun importo, verrà applicato automaticamente l'importo massimo. Nella parte inferiore della pagina **Collega movimenti fornitori** è possibile vedere l'importo nel campo Importo collegato e verificare se il saldo del collegamento è corretto.
5. Scegliere il pulsante **OK**.
6. Scegliere l'azione **Registra** per contabilizzare le registrazioni di pagamento.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Per collegare una nota di credito a uno o più movimenti contabili fornitori
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Nota credito acquisto**, quindi scegli il collegamento correlato.
2. Aprire la nota di credito da collegare.
3. Immettere le informazioni appropriate nella testata.
4. Per collegare un singolo movimento contabile fornitore, nella Scheda dettaglio **Collegamento**, nel campo **Collega-a nr. doc.**, selezionare il movimento a cui collegare il credito, quindi nel campo **Importo da collegare**, immettere l'importo da collegare al movimento.
5. In alternativa, per collegare più movimenti contabili fornitori:

   1. Scegliere l'azione **Collega movimenti**.
   2. Selezionare le righe con i movimenti a cui collegare la nota di credito.
   3. Scegliere l'azione **Collega a ID**.  
   4. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento.

       Se non si immette alcun importo, verrà applicato automaticamente l'importo massimo. Nella parte inferiore della pagina **Collega movimenti fornitori** è possibile vedere l'importo nel campo **Importo collegato** e verificare se il saldo del collegamento è corretto.
6. Scegliere il pulsante **OK**.  
   Nella pagina **Nota credito acquisto** viene mostrato il movimento precedentemente selezionato nel campo **Collega-a tipo doc.** e nel campo **Collega-a nr. doc.**. Nella pagina verrà inoltre visualizzato l'importo della nota di credito da registrare, rettificato per eventuali sconti di pagamenti.
7. Scegliere il pulsante **Registra** per contabilizzare la nota di credito di acquisto.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Per collegare i movimenti contabili fornitori registrati
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Aprire la scheda fornitore con movimenti già registrati.
3. Scegliere l'azione **Movimenti contabili**, quindi l'azione **Collega movimenti**.
4. Nella pagina **Collega movimenti fornitori** è possibile vedere i movimenti aperti per il fornitore.
5. Selezionare la riga con il movimento da collegare.
6. Scegliere l'azione **Collega a ID**.

    Nel campo **Collega-a ID** vengono visualizzati tre asterischi se si lavora in un sistema a utente singolo oppure l'ID utente se si lavora in un sistema multiutente.  
7. Per ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento.

    Se non si immette alcun importo, verrà applicato automaticamente l'importo massimo. L'importo nel campo **Importo collegato** è visibile nella parte inferiore della pagina **Collega movimenti fornitori**.
8. Scegliere l'azione **Registra collegamento**.  

    Viene visualizzata la pagina **Registra collegamento** con il numero di documento del movimento di collegamento e la data di registrazione del movimento con la data di registrazione più recente.
9. Scegliere **OK** per registrare il collegamento.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Per collegare movimenti contabili fornitori in valute diverse
Se si acquista da un fornitore con una valuta e si paga con un'altra valuta, è possibile collegare la fattura al pagamento.

Se si collega un movimento (Movimento 1) espresso in una determinata valuta a un movimento (Movimento 2) con valuta diversa, verrà utilizzata la data di registrazione del Movimento 1 per trovare il tasso di cambio appropriato per la conversione degli importi nel Movimento 2. Il tasso di cambio rilevante è disponibile nella pagina **Tassi di cambio valuta**. In tal caso, è necessario abilitare il collegamento dei movimenti contabili fornitore in valute diverse. Per ulteriori informazioni, vedere [Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.
2. Aprire la registrazione desiderata e compilare la prima riga delle registrazioni vuota con un codice valuta.
3. Scegliere l'azione **Collega movimenti**.
4. Selezionare la riga con il movimento a cui si intende collegare il movimento nelle registrazioni pagamenti. Scegliere l'azione **Collega a ID**, quindi selezionare il movimento che si desidera collegare.
5. Fare clic su **OK** per tornare alle registrazioni pagamenti.
6. Contabilizzare le registrazioni di pagamento.

> [!IMPORTANT]  
>   Quando si collegano movimenti in valute diverse, i movimenti vengono convertiti nella valuta USD. Sebbene i tassi di cambio per le due valute siano fissi, ad esempio tra USD ed EUR, è possibile che durante la conversione di tali valute estere nella valuta locale vengano prodotti importi residui di piccola entità. Gli importi residui vengono registrati come utili e perdite sul conto specificato nel campo **Conto utili realizzati** o **Conto perdite realizzate** della pagina **Valute**. Viene rettificato anche il campo **Importo (USD)** nei movimenti contabili fornitori rilevanti.

## <a name="to-unapply-an-application-of-vendor-entries"></a>Per scollegare un collegamento di movimenti fornitori
Quando si scollega un collegamento errato, vengono creati e registrati movimenti di rettifica identici a quelli originali ma con segno opposto nel campo relativo all'importo, per tutti i movimenti, incluse le registrazioni di contabilità generale derivanti dal collegamento, quali ad esempio sconto pagamento e profitti e perdite legati alla valuta. Vengono inoltre riaperti i movimenti chiusi dal collegamento.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fornitori**, quindi scegli il collegamento correlato.
2. Aprire la scheda fornitore pertinente.
3. Scegliere l'azione **Movimenti contabili**.
4. Selezionare il movimento contabile rilevante e scegliere l'azione **Scollega movimenti**.
5. In alternativa, scegliere l'azione **Movimenti contabili dettagliati**.
6. Selezionare il movimento di collegamento e scegliere l'azione **Scollega movimenti**.
7. Compilare i campi della testata, quindi scegliere l'azione **Scollega**.

> [!IMPORTANT]  
>   Se un movimento è stato collegato da più di un movimento di collegamento, è necessario prima scollegare il movimento di collegamento più recente.

## <a name="see-also"></a>Vedere anche
[Contabilità fornitori](payables-manage-payables.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

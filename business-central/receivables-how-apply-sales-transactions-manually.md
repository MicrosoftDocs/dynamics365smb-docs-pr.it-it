---
title: Riconciliare i pagamenti dei clienti con il giornale di registrazione delle ricevute di cassa o dai movimenti contabili dei clienti
description: Collegare le ricevute di cassa o i rimborsi dei clienti a uno o più movimenti contabili clienti aperti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Riconciliare i pagamenti dei clienti con un giornale di registrazione delle ricevute di cassa o dai movimenti contabili dei clienti

Quando ricevi un pagamento in contanti da un cliente o effettui un rimborso in contanti, puoi applicare il pagamento o il rimborso per chiudere i debiti o i crediti aperti. Puoi specificare l'importo esatto da collegare. Ad esempio, è possibile collegare pagamenti parziali ai movimenti contabili clienti. La chiusura dei movimenti contabili dei clienti mantiene aggiornate le statistiche dei clienti, gli estratti conto, gli oneri finanziari e così via.

> [!TIP]  
> Nella pagina **Movimenti contabili clienti** il carattere rosso indica che il pagamento correlato ha luogo dopo la data di scadenza. Se i pagamenti in ritardo stanno diventando un problema, è possibile ridurne la frequenza. È possibile abilitare l'estensione **Previsioni pagamenti ritardati**, che utilizza un modello predittivo creato in Azure Machine Learning per prevedere i tempi dei pagamenti. Le previsioni aiutano a ridurre i crediti in sospeso e ad affinare la strategia di riscossione. Ad esempio, se si prevede che un pagamento sia in ritardo, è possibile adeguare i termini di pagamento o il metodo di pagamento per il cliente. Per ulteriori informazioni, vedere [Previsioni pagamenti ritardati](ui-extensions-late-payment-prediction.md).  

È possibile collegare i movimenti contabili clienti in modi diversi:

* Inserisci le informazioni nelle seguenti pagine:
   * La pagina **Registrazione riconciliazione pagamenti**. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).
   * La pagina **Registrazione pagamenti**. Per ulteriori informazioni, vedere [Riconciliare i pagamenti dei clienti da un elenco di documenti di vendita non pagati](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
   * La pagina **Registro incassi** . Per ulteriori informazioni, vedere [Per compilare e registrare un giornale di registrazione entrate di cassa](#to-fill-and-post-a-cash-receipt-journal).
* La compilazione del campo **Collega-a nr. doc.** nei documenti nota di credito di vendita. Per ulteriori informazioni, vedere [Per applicare una nota di credito a un singolo movimento contabile cliente](#to-apply-a-credit-memo-to-a-single-customer-ledger-entry).
* Utilizzando l'azione **Imposta Collega a ID** in un movimento registro clienti. Per ulteriori informazioni, vedere [Per collegare un pagamento a un singolo movimento contabile cliente](#to-apply-a-payment-to-a-single-customer-ledger-entry).
* Utilizzando l'azione **Collega movimenti** della pagina **Deposito bancario** e immettendo il numero di fattura nel campo **Collega a ID**. Per ulteriori informazioni, vedi [Creare depositi bancari](bank-create-bank-deposits.md).

> [!NOTE]  
> Se il campo **Metodo Collegamento PA** nella scheda cliente è impostato su **Collega al più Vecchio**, i pagamenti vengono automaticamente collegati al movimento di credito meno recente, a meno che non si specifichi manualmente un movimento. Se il metodo di collegamento è impostato su **Manuale**, i movimenti vengono collegati sempre manualmente.

## Per compilare e contabilizzare una registrazione incasso

Una registrazione incasso è un tipo di registrazione COGE. Puoi usarla per registrare transazioni nei conti C/G, conti correnti bancari, conti clienti, conti fornitori e conti cespite. È possibile collegare il pagamento a uno o più movimenti Dare quando si registra il pagamento. Puoi anche collegare dai movimenti registrati in un secondo momento.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni incassi**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Selezionare il batch appropriato nel campo **Nome batch**.
4. Compilare il campo **Data di Registrazione**.  
5. Nel campo **Tipo di documento** selezionare **Pagamento**.

    Il campo **Nr. documento** viene compilato utilizzando il numero di serie assegnato al batch.  
6. Utilizzare il campo **Nr. documento esterno** per archiviare un identificatore come il numero dell'assegno del cliente.

   > [!NOTE]
   > Per impostazione predefinita, il campo N. documento esterno è nascosto. Se lo è e desideri utilizzarlo, puoi utilizzare la personalizzazione per aggiungerlo. Per ulteriori informazioni, vedere [Personalizzare l'area di lavoro](ui-personalization-user.md).

7. Nel campo **Tipo conto** selezionare **Cliente**.
8. Nel campo **N. conto**, seleziona il cliente.
9. Per pubblicare la domanda contestualmente alla pubblicazione del giornale, compilare i seguenti campi:
   1. Nel campo **Tipo contropartita** selezionare **Conto C/G** per i pagamenti in contanti e **Conto C/C bancario** per gli altri pagamenti.
   2. Nel campo **Conto profitti/perdite** selezionare il conto cassa per i pagamenti in contanti o il conto bancario appropriato per gli altri pagamenti.
10. Effettuare la registrazione.

## Per collegare un pagamento a un singolo movimento contabile cliente

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , immettere **Registro incassi** e scegliere il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Nella prima riga delle registrazioni immettere le informazioni relative al movimento da collegare.
4. Nel campo **Tipo di documento** immettere **Pagamento**.
5. Nel campo **Tipo conto** immettere **Cliente**.
6. Nel campo **Tipo contropartita** immettere **Conto bancario**.
7. Nel campo **Collega-a nr. doc.** scegliere il campo da aprire nella pagina **Collega movimenti clienti**.
8. Nella pagina **Collega movimenti clienti** selezionare il movimento a cui collegare il pagamento.
9. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare al movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
10. Scegli il pulsante **OK**. Nella pagina **Registrazioni incassi** viene a questo punto visualizzato il movimento nel campo **Collega-a tipo doc.** e nel campo **Collega-a nr. doc.**.
11. Effettuare la registrazione dell'incasso.

## Per collegare un pagamento a più movimenti contabili clienti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni incassi**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Nella prima riga delle registrazioni immettere le informazioni relative al movimento da collegare.
4. Nel campo **Tipo di documento** immettere **Pagamento**.
5. Nel campo **Tipo conto** immettere **Cliente**.
6. Nel campo **Tipo contropartita** immettere **Conto bancario**.
7. Nel campo **Importo** immettere il pagamento completo come importo negativo.
8. Per collegare il pagamento a più movimenti contabili clienti durante la registrazione, scegliere l'azione **Collega movimenti**.  
9. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID**.  
10. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
11. Scegliere il pulsante **OK**.
12. Effettuare la registrazione dell'incasso.

## Per collegare una nota di credito a un singolo movimento contabile cliente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note credito vendita**, quindi scegli il collegamento correlato.
2. Aprire la nota di credito di vendita desiderata.
3. Per applicare la nota di credito a un singolo movimento contabile cliente durante la registrazione, nella Scheda dettaglio Collegamento, nel campo **Collega-a nr. doc.** selezionare il movimento che si desidera collegare il pagamento.
4. Nella riga del campo **Importo da collegare** immettere l'importo da collegare al movimento.  

    Se non si immette alcun importo, verrà applicato automaticamente l'importo massimo. Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
5. Scegli il pulsante **OK**. La pagina  **Nota credito vendita** mostra ora la voce selezionata nella sezione **Applica-a doc. Digita** e **Applica-a doc. N.** campi. e l'importo della nota di credito da registrare, rettificato per eventuali sconti di pagamenti.
6. Registrare la nota di credito.

## Per collegare una nota di credito a più movimenti contabili clienti

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note credito vendita**, quindi scegli il collegamento correlato.
2. Aprire la nota di credito di vendita desiderata.
3. Per collegare la nota di credito a più movimenti contabili clienti durante la registrazione, scegliere l'azione **Collega movimenti**.
4. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID**.
5. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.  

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
6. Scegliere il pulsante **OK**. Nella pagina **Nota credito vendita** viene a questo punto visualizzato l'importo della nota di credito da registrare, rettificato di ogni possibile sconto.
7. Registrare la nota di credito.

## Per collegare i movimenti contabili clienti registrati

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Aprire la scheda cliente relativa al cliente per il quale sono disponibili i movimenti da collegare.
3. Scegliere l'azione **Movimenti contabili**, quindi selezionare la riga con il movimento da applicare.
4. Scegliere l'azione **Collega movimenti**. Verrà visualizzata la pagina **Collega movimenti clienti** nella quale saranno indicati i movimenti aperti per il cliente.
5. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID** .
6. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.  

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato**.  
7. Scegliere l'azione **Registra collegamento**. Viene visualizzata la pagina **Registra collegamento** con il numero di documento del movimento di collegamento e la data di registrazione del movimento con la data di registrazione più recente.  
8. Scegliere **OK** per registrare il collegamento.

    Se la domanda registrata ha prodotto movimenti contabili clienti chiusi, il campo **Aperto** viene cancellato per questi movimenti contabili.  
9. Per vedere i movimenti contabili, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato. Spostarsi sulla scheda del cliente per visualizzare i movimenti contabili.  

Nella lista dei movimenti contabili, nella riga che contiene il movimento contabile che era stato interamente collegato, è possibile vedere che la casella di controllo **Aperto** non è selezionata.  

> [!NOTE]  
> Dopo aver selezionato un movimento nella pagina **Collega movimenti clienti** o numerosi movimenti impostando **Collega-a ID**, il campo **Importo collegato** nella riga di registrazione conterrà la somma dei restanti importi per i movimenti registrati selezionati, a meno che il campo non contenga un'impostazione differente. Se si seleziona **Collega al più Vecchio** nel campo **Metodo collegamento** della scheda cliente, il collegamento viene stabilito automaticamente.

## Per collegare movimenti contabili clienti nelle varie valute

Se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile ancora collegare la fattura al pagamento.  

Ecco un esempio. Si applica la Voce A in una valuta alla Voce B in un'altra valuta. La data di registrazione nella voce A viene utilizzata per trovare il tasso di cambio da utilizzare per convertire gli importi nella voce B. Il tasso di cambio si trova nella pagina  **Tassi di cambio** .  

È necessario abilitare il collegamento dei movimenti contabili clienti in differenti valute. Per ulteriori informazioni, vedere [Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazione incassi**, quindi scegli il collegamento correlato.
2. Aprire la registrazione desiderata e compilare la prima riga delle registrazioni vuota con un codice valuta.
3. Scegliere l'azione **Collega movimenti**.
4. Selezionare la riga con il movimento a cui si intende collegare il movimento nelle registrazioni incassi. Scegliere l'azione **Collega a ID**, quindi selezionare il movimento che si desidera collegare.
5. Scegliere **OK** per tornare alle registrazioni incassi.
6. Registrare la registrazione vendite.  

> [!IMPORTANT]  
>   Quando si collegano movimenti in valute diverse, i movimenti vengono convertiti nella valuta locale. Sebbene i tassi di cambio per le due valute siano fissi, ad esempio tra USD ed EUR, è possibile che durante la conversione nella valuta locale vengano prodotti importi residui di piccola entità. Gli importi residui vengono registrati come utili e perdite sul conto specificato nel campo **Conto utili realizzati** o **Conto perdite realizzate** della pagina **Valute**. Viene rettificato anche il campo **Importo (USD)** nei movimenti contabili fornitori.  

## Per correggere un collegamento di movimenti clienti
Quando correggi un'applicazione, i movimenti di correzione vengono creati e registrati per tutti i movimenti. I movimenti di correzione sono uguali agli originali ma hanno un segno opposto nel campo **Importo**. I movimenti di correzione includono tutti i movimenti di contabilità generale derivati dall'applicazione. Ad esempio, lo sconto sul pagamento e utili/perdite valutari. Le voci chiuse dall'applicazione vengono riaperte.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Aprire la scheda cliente desiderata.
3. Scegliere l'azione **Movimenti contabili**.
4. Selezionare il movimento contabile rilevante e scegliere l'azione **Scollega movimenti**.
5. In alternativa, scegliere l'azione **Movimenti contabili dettagliati**.
6. Selezionare il movimento di collegamento e scegliere l'azione **Scollega movimenti**.
7. Compilare i campi della testata, quindi scegliere l'azione **Scollega**.  

> [!IMPORTANT]  
>   Se un movimento è stato collegato da più di un movimento di collegamento, è necessario prima scollegare il movimento di collegamento più recente.  

## Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
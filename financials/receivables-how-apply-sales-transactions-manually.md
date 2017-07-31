---
title: Collegare i movimenti contabili clienti per riconciliare manualmente i pagamenti dei clienti | Documenti Microsoft
description: "Descrive come collegare gli incassi o i rimborsi del cliente a uno o più movimenti contabili aperti del cliente e riconciliare i pagamenti del cliente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 568bd66c201764cae45ea12a900ea12eabbf0546
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017

---
# <a name="how-to-reconcile-customer-payments-manually"></a>Procedura: Riconciliare manualmente i pagamenti dei clienti
Quando si riceve un incasso da un cliente o si effettua un rimborso in contanti, è necessario stabilire se collegare il pagamento o il rimborso per chiudere uno o più movimenti contabili aperti. È possibile specificare l'importo esatto che si desidera collegare. Ad esempio, è possibile collegare pagamenti parziali ai movimenti contabili clienti. Chiudere i movimenti contabili clienti garantisce che informazioni, quali statistiche dei clienti, estratti conto e addebiti interessi siano corretti.

> [!NOTE]  
>   Nella finestra **Movimenti contabili clienti** il carattere rosso indica che il pagamento correlato ha luogo dopo la data di scadenza.

È possibile collegare i movimenti contabili clienti in modi diversi:

* Immettendo informazioni nelle finestre dedicate, ad esempio nella finestra **Registrazioni incassi** e nella finestra **Registrazione riconciliazione pagamenti**.
* Dai documenti nota di credito di vendita.
* Dai movimenti contabili clienti dopo che i documenti di vendita sono stati registrati ma non collegati.

> [!NOTE]  
>   Se il campo **Metodo Collegamento PA** nella scheda cliente è impostato su **Collega al più Vecchio**, i pagamenti vengono automaticamente collegati al movimento di credito meno recente, a meno che non si specifichi manualmente un movimento. Se il metodo di collegamento è impostato su **Manuale**, i movimenti vengono collegati sempre manualmente.

È possibile collegare i pagamenti dei clienti manualmente nella finestra **Registrazioni incassi**. Una registrazione incassi è un tipo di registrazione generale che può essere utilizzata per registrare transazioni in conti di contabilità generale, bancari, cliente, fornitori e cespiti. È possibile collegare il pagamento a uno o più movimenti Dare quando si registra il pagamento oppure collegare dai movimenti registrati in un momento successivo.

È inoltre possibile collegare i pagamenti dei clienti e dei fornitori nella finestra **Registrazione riconciliazione pagamenti** utilizzando le funzioni per l'importazione del rendiconto bancario, il collegamento automatico e la riconciliazione del conto corrente bancario. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md). In alternativa, è possibile riconciliare i pagamenti dei clienti in base a un elenco di documenti di vendita non pagati nella finestra **Registrazione pagamenti**. Per ulteriori informazioni, vedere [Procedura: Riconciliare i pagamenti dei clienti da un elenco di documenti di vendita non pagati](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Per compilare e contabilizzare una registrazione incasso
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni incassi**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Selezionare il batch appropriato nel campo **Nome batch**.
4. Compilare il campo **Data di Registrazione**.  
5. Nel campo **Tipo di documento** selezionare **Pagamento**.

    Il campo **Nr. documento** viene compilato dalla numerazione assegnata al batch.  
6. Utilizzare il campo **Nr. documento esterno** per archiviare un identificatore, quale il numero di assegno del cliente.
7. Nel campo **Tipo conto** selezionare **Cliente**.
8. Nel campo **Nr. conto** selezionare il conto C/G desiderato.
9. Se si desidera registrare il collegamento contemporaneamente alle registrazioni, effettuare una delle operazioni seguenti.
10. Nel campo **Tipo contropartita** selezionare **Conto C/G** per i pagamenti in contanti e **Conto C/C bancario** per gli altri pagamenti.
11. Nel campo **Nr. conto profitti/perdite** selezionare il conto cassa per i pagamenti in contanti o il conto bancario appropriato per gli altri pagamenti.
12. Effettuare la registrazione.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Per collegare un pagamento a un singolo movimento contabile cliente
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni incassi** e scegliere il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Nella prima riga delle registrazioni immettere le informazioni relative al movimento da collegare.
4. Nel campo **Tipo di documento** immettere **Pagamento**.
5. Nel campo **Tipo conto** immettere **Cliente**.
6. Nel campo **Tipo contropartita** immettere **Conto bancario**.
7. Nel campo **Collega-a nr. doc.** scegliere il campo da aprire nella finestra **Collega movimenti clienti**.
8. Nella finestra **Collega movimenti clienti** selezionare il movimento a cui collegare il pagamento.
9. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare al movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.

    Nella parte inferiore della finestra **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
10. Scegliere il pulsante **OK**. Nella finestra **Registrazioni incassi** viene a questo punto visualizzato nel campo **Collega-a tipo doc.** e nel campo **Collega-a nr. doc.** il movimento selezionato. .
11. Effettuare la registrazione dell'incasso.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Per collegare un pagamento a più movimenti contabili clienti
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni incassi**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Nella prima riga delle registrazioni immettere le informazioni relative al movimento da collegare.
4. Nel campo **Tipo di documento** immettere **Pagamento**.
5. Nel campo **Tipo conto** immettere **Cliente**.
6. Nel campo **Tipo contropartita** immettere **Conto bancario**.
7. Nel campo **Importo** immettere il pagamento completo come importo negativo.
8. Per collegare il pagamento a più movimenti contabili clienti durante la registrazione, scegliere l'azione **Collega movimenti**.
9. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID**.
10. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.

    Nella parte inferiore della finestra **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
11. Scegliere il pulsante **OK**.
12. Effettuare la registrazione dell'incasso.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Per collegare una nota di credito a un singolo movimento contabile cliente
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Note credito vendita**, quindi scegliere il collegamento correlato.
2. Aprire la nota di credito di vendita desiderata.
3. Per collegare la nota di credito a un singolo movimento contabile cliente durante la registrazione, nel campo **Collega-a nr. doc.**, selezionare il movimento al quale si desidera collegare il pagamento.
4. Nella riga del campo **Importo da collegare** immettere l'importo da collegare al movimento.  

    Se non si immette alcun importo, verrà applicato automaticamente l'importo massimo. Nella parte inferiore della finestra **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.    
5. Scegliere il pulsante **OK**. Nella finestra **Note credito vendita** viene a questo punto visualizzato nel campo **Collega-a tipo doc.** e nel campo **Collega-a nr. doc.** il movimento selezionato. . e l'importo della nota di credito da registrare, rettificato per eventuali sconti di pagamenti.
6. Registrare la nota di credito.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Per collegare una nota di credito a più movimenti contabili clienti
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Note credito vendita**, quindi scegliere il collegamento correlato.
2. Aprire la nota di credito di vendita desiderata.
3. Per collegare la nota di credito a più movimenti contabili clienti durante la registrazione, scegliere l'azione **Collega movimenti**.
4. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID**.
5. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.  

    Nella parte inferiore della finestra **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
6. Scegliere il pulsante **OK**. Nella finestra **Nota credito vendita** viene a questo punto visualizzato l'importo della nota di credito da registrare, rettificato di ogni possibile sconto.
7. Registrare la nota di credito.

## <a name="to-apply-posted-customer-ledger-entries"></a>Per collegare i movimenti contabili clienti registrati
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente relativa al cliente per il quale sono disponibili i movimenti da collegare.
3. Scegliere l'azione **Mov. contabili** e selezionare la riga con il movimento che sarà il movimento di collegamento.
4. Scegliere l'azione **Collega movimenti**. Verrà visualizzata la finestra **Collega movimenti clienti** nella quale saranno indicati i movimenti aperti per il cliente.
5. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID** .
6. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.  

    Nella parte inferiore della finestra **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato**.  
7. Scegliere l'azione **Registra collegamento**. Viene visualizzata la finestra **Registra collegamento** con il numero di documento del movimento di collegamento e la data di registrazione del movimento con la data di registrazione più recente.  
8. Scegliere **OK** per registrare il collegamento.

    Se il collegamento registrato ha comportato la creazione di movimenti contabili clienti chiusi, per tali movimenti contabili verrà deselezionato il campo **Aperto**.    
9. Per visualizzare i movimenti contabili, scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato. Spostarsi sulla scheda del cliente per visualizzare i movimenti contabili.  

Nella lista dei movimenti contabili, nella riga che contiene il movimento contabile che era stato interamente collegato, è possibile vedere che la casella di controllo **Aperto** non è selezionata.  

> [!NOTE]  
>   Dopo aver selezionato un movimento nella finestra **Collega movimenti clienti** o numerosi movimenti impostando **Collega-a ID**, il campo **Importo collegato** nella riga di registrazione conterrà la somma dei restanti importi per i movimenti registrati selezionati, a meno che il campo non contenga un'impostazione differente. Se si seleziona **Collega al più Vecchio** nel campo **Metodo collegamento** della scheda cliente, il collegamento viene stabilito automaticamente.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Per collegare movimenti contabili clienti nelle varie valute
Se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile ancora collegare la fattura al pagamento.  

Se si collega un movimento (Movimento 1) espresso in una determinata valuta a un movimento (Movimento 2) con valuta diversa, verrà utilizzata la data di registrazione del Movimento 1 per trovare il tasso di cambio appropriato per la conversione degli importi nel Movimento 2. Il tasso di cambio rilevante è disponibile nella finestra **Tassi di cambio valuta**.  

È necessario abilitare il collegamento dei movimenti contabili clienti in differenti valute. Per ulteriori informazioni, vedere [Procedura: Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni incassi**, quindi scegliere il collegamento correlato.
2. Aprire la registrazione desiderata e compilare la prima riga delle registrazioni vuota con un codice valuta.
3. Scegliere l'azione **Collega movimenti**.
4. Selezionare la riga con il movimento a cui si intende collegare il movimento nelle registrazioni incassi. Scegliere l'azione **Collega a ID**, quindi selezionare il movimento che si desidera collegare.
5. Scegliere **OK** per tornare alle registrazioni incassi.
6. Registrare la registrazione vendite.  

> [!IMPORTANT]  
>   Quando si collegano movimenti in valute diverse, i movimenti vengono convertiti nella valuta locale. Sebbene i tassi di cambio per le due valute siano fissi, ad esempio tra USD ed EUR, è possibile che durante la conversione nella valuta locale vengano prodotti importi residui di piccola entità. Gli importi residui vengono registrati come utili e perdite sul conto specificato nel campo **Conto utili realizzati** o **Conto perdite realizzate** della finestra **Valute**. Viene rettificato anche il campo **Importo (USD)** nei movimenti contabili fornitori.  

## <a name="to-correct-an-application-of-customer-entries"></a>Per correggere un collegamento di movimenti clienti
Quando si corregge un collegamento, vengono creati e registrati movimenti di rettifica identici a quelli originali ma con segno opposto nel campo relativo all'importo, per tutti i movimenti, incluse le registrazioni di contabilità generale derivanti dal collegamento, quali ad esempio sconto pagamento e profitti e perdite legati alla valuta. Vengono inoltre riaperti i movimenti chiusi dal collegamento.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente desiderata.
3. Scegliere l'azione **Movimenti contabili**.
4. Selezionare il movimento contabile rilevante e scegliere l'azione **Scollega movimenti**.
5. In alternativa, scegliere l'azione **Movimenti contabili dettagliati**.
6. Selezionare il movimento di collegamento e scegliere l'azione **Scollega movimenti**.
7. Compilare i campi della testata, quindi scegliere l'azione **Scollega**.  

> [!IMPORTANT]  
>   Se un movimento è stato collegato da più di un movimento di collegamento, è necessario prima scollegare il movimento di collegamento più recente.  

## <a name="see-also"></a>Vedi anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


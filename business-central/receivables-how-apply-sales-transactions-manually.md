---
title: Collegare i movimenti contabili clienti per riconciliare i pagamenti | Documenti Microsoft
description: Descrive come collegare gli incassi o i rimborsi del cliente a uno o più movimenti contabili aperti del cliente e riconciliare i pagamenti del cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d32f614ce86f6ad1b3f846631d3b4062788b755a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312342"
---
# <a name="reconcile-customer-payments-with-the-cash-receipt-journal-or-from-customer-ledger-entries"></a>Riconciliare i pagamenti clienti con la registrazione incassi o da movimenti contabili clienti
Quando si riceve un incasso da un cliente o si effettua un rimborso in contanti, è necessario stabilire se collegare il pagamento o il rimborso per chiudere uno o più movimenti contabili aperti. È possibile specificare l'importo esatto che si desidera collegare. Ad esempio, è possibile collegare pagamenti parziali ai movimenti contabili clienti. Chiudere i movimenti contabili clienti garantisce che informazioni, quali statistiche dei clienti, estratti conto e addebiti interessi siano corretti.

> [!TIP]  
>   Nella pagina **Movimenti contabili clienti** il carattere rosso indica che il pagamento correlato ha luogo dopo la data di scadenza. Se i pagamenti in ritardo stanno diventando un problema, è possibile ridurne la frequenza. È possibile abilitare l'estensione **Previsioni pagamenti ritardati**, che utilizza un modello predittivo creato in Azure Machine Learning per prevedere i tempi dei pagamenti. Le previsioni aiutano a ridurre i crediti in sospeso e ad affinare la strategia di riscossione. Ad esempio, se si prevede che un pagamento sia in ritardo, è possibile adeguare i termini di pagamento o il metodo di pagamento per il cliente. Per ulteriori informazioni, vedere [Previsioni pagamenti ritardati](ui-extensions-late-payment-prediction.md).  

È possibile collegare i movimenti contabili clienti in modi diversi:

* Immettendo le informazioni nelle pagine dedicate:
    * La pagina **Registrazione riconciliazione pagamenti**. Per ulteriori informazioni, vedere [Collegare i pagamenti automaticamente e riconciliare i conti correnti bancari](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * La pagina **Registrazione pagamenti**. Per ulteriori informazioni, vedere [Riconciliare i pagamenti dei clienti da un elenco di documenti di vendita non pagati](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
    * La finestra **Registrazioni incassi**. Questa finestra è descritta di seguito.
* La compilazione del campo **Collega-a nr. doc.** nei documenti nota di credito di vendita. Questa finestra è descritta di seguito.
* Utilizzando l'azione **Imposta Collega a ID** in un movimento registro clienti. Questa finestra è descritta di seguito.

> [!NOTE]  
>   Se il campo **Metodo Collegamento PA** nella scheda cliente è impostato su **Collega al più Vecchio**, i pagamenti vengono automaticamente collegati al movimento di credito meno recente, a meno che non si specifichi manualmente un movimento. Se il metodo di collegamento è impostato su **Manuale**, i movimenti vengono collegati sempre manualmente.

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Per compilare e contabilizzare una registrazione incasso
Una registrazione incassi è un tipo di registrazione generale che può essere utilizzata per registrare transazioni in conti di contabilità generale, bancari, cliente, fornitori e cespiti. È possibile collegare il pagamento a uno o più movimenti Dare quando si registra il pagamento oppure collegare dai movimenti registrati in un momento successivo.
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni incassi** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Selezionare il batch appropriato nel campo **Nome batch**.
4. Compilare il campo **Data di Registrazione**.  
5. Nel campo **Tipo di documento** selezionare **Pagamento**.

    Il campo **Nr. documento** viene compilato utilizzando il numero di serie assegnato al batch.  
6. Utilizzare il campo **Nr. documento esterno** per archiviare un identificatore come il numero dell'assegno del cliente.
7. Nel campo **Tipo conto** selezionare **Cliente**.
8. Nel campo **Nr. conto corrente** selezionare il conto C/G pertinente.
9. Se si desidera registrare il collegamento contemporaneamente alle registrazioni, effettuare una delle operazioni seguenti.
10. Nel campo **Tipo contropartita** selezionare **Conto C/G** per i pagamenti in contanti e **Conto C/C bancario** per gli altri pagamenti.
11. Nel campo **Conto profitti/perdite** selezionare il conto cassa per i pagamenti in contanti o il conto bancario appropriato per gli altri pagamenti.
12. Effettuare la registrazione.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Per collegare un pagamento a un singolo movimento contabile cliente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni incassi** e scegliere il collegamento correlato.
2. Scegliere l'azione **Modifica registrazione**.
3. Nella prima riga delle registrazioni immettere le informazioni relative al movimento da collegare.
4. Nel campo **Tipo di documento** immettere **Pagamento**.
5. Nel campo **Tipo conto** immettere **Cliente**.
6. Nel campo **Tipo contropartita** immettere **Conto bancario**.
7. Nel campo **Collega-a nr. doc.** scegliere il campo da aprire nella pagina **Collega movimenti clienti**.
8. Nella pagina **Collega movimenti clienti** selezionare il movimento a cui collegare il pagamento.
9. Nel campo **Importo da collegare** immettere l'importo che si desidera collegare al movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
10. Scegliere il pulsante **OK**. Nella pagina **Registrazioni incassi** viene a questo punto visualizzato il movimento selezionato nel campo **Collega-a tipo doc.** e nel campo **Collega-a nr. doc.**.
11. Effettuare la registrazione dell'incasso.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Per collegare un pagamento a più movimenti contabili clienti
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni incassi** e quindi scegliere il collegamento correlato.
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

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Per collegare una nota di credito a un singolo movimento contabile cliente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note credito vendita** e quindi scegliere il collegamento correlato.
2. Aprire la nota di credito di vendita desiderata.
3. Per applicare la nota di credito a un singolo movimento contabile cliente durante la registrazione, nella Scheda dettaglio Collegamento, nel campo **Collega-a nr. doc.** selezionare il movimento che si desidera collegare il pagamento.
4. Nella riga del campo **Importo da collegare** immettere l'importo da collegare al movimento.  

    Se non si immette alcun importo, verrà applicato automaticamente l'importo massimo. Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.    
5. Scegliere il pulsante **OK**. Nella pagina **Note credito vendita** viene a questo punto visualizzato il movimento selezionato nel campo **Collega-a tipo doc.** e nel campo **Collega-a nr. doc.**. e l'importo della nota di credito da registrare, rettificato per eventuali sconti di pagamenti.
6. Registrare la nota di credito.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Per collegare una nota di credito a più movimenti contabili clienti
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Note credito vendita** e quindi scegliere il collegamento correlato.
2. Aprire la nota di credito di vendita desiderata.
3. Per collegare la nota di credito a più movimenti contabili clienti durante la registrazione, scegliere l'azione **Collega movimenti**.
4. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID**.
5. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.  

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato** e anche se il saldo del collegamento è corretto.  
6. Scegliere il pulsante **OK**. Nella pagina **Nota credito vendita** viene a questo punto visualizzato l'importo della nota di credito da registrare, rettificato di ogni possibile sconto.
7. Registrare la nota di credito.

## <a name="to-apply-posted-customer-ledger-entries"></a>Per collegare i movimenti contabili clienti registrati
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente relativa al cliente per il quale sono disponibili i movimenti da collegare.
3. Scegliere l'azione **Mov. contabili** e selezionare la riga con il movimento che sarà il movimento di collegamento.
4. Scegliere l'azione **Collega movimenti**. Verrà visualizzata la pagina **Collega movimenti clienti** nella quale saranno indicati i movimenti aperti per il cliente.
5. Selezionare le righe con i movimenti a cui si desidera collegare il movimento, quindi scegliere l'azione **Collega a ID** .
6. In ciascuna riga del campo **Importo da collegare** immettere l'importo da collegare al singolo movimento. Se non si immette alcun importo, verrà collegato l'importo massimo.  

    Nella parte inferiore della pagina **Collega movimenti clienti** è possibile vedere l'importo specifico nel campo **Importo collegato**.  
7. Scegliere l'azione **Registra collegamento**. Viene visualizzata la pagina **Registra collegamento** con il numero di documento del movimento di collegamento e la data di registrazione del movimento con la data di registrazione più recente.  
8. Scegliere **OK** per registrare il collegamento.

    Se il collegamento registrato ha comportato la creazione di movimenti contabili clienti chiusi, per tali movimenti contabili verrà deselezionato il campo **Aperto**.    
9. Per visualizzare i movimenti contabili, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato. Spostarsi sulla scheda del cliente per visualizzare i movimenti contabili.  

Nella lista dei movimenti contabili, nella riga che contiene il movimento contabile che era stato interamente collegato, è possibile vedere che la casella di controllo **Aperto** non è selezionata.  

> [!NOTE]  
>   Dopo aver selezionato un movimento nella pagina **Collega movimenti clienti** o numerosi movimenti impostando **Collega-a ID**, il campo **Importo collegato** nella riga di registrazione conterrà la somma dei restanti importi per i movimenti registrati selezionati, a meno che il campo non contenga un'impostazione differente. Se si seleziona **Collega al più Vecchio** nel campo **Metodo collegamento** della scheda cliente, il collegamento viene stabilito automaticamente.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Per collegare movimenti contabili clienti nelle varie valute
Se si effettua una vendita a un cliente in una valuta e si riceve il pagamento in un'altra, è possibile ancora collegare la fattura al pagamento.  

Se si collega un movimento (Movimento 1) espresso in una determinata valuta a un movimento (Movimento 2) con valuta diversa, verrà utilizzata la data di registrazione del Movimento 1 per trovare il tasso di cambio appropriato per la conversione degli importi nel Movimento 2. Il tasso di cambio rilevante è disponibile nella pagina **Tassi di cambio valuta**.  

È necessario abilitare il collegamento dei movimenti contabili clienti in differenti valute. Per ulteriori informazioni, vedere [Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni incassi** e quindi scegliere il collegamento correlato.
2. Aprire la registrazione desiderata e compilare la prima riga delle registrazioni vuota con un codice valuta.
3. Scegliere l'azione **Collega movimenti**.
4. Selezionare la riga con il movimento a cui si intende collegare il movimento nelle registrazioni incassi. Scegliere l'azione **Collega a ID**, quindi selezionare il movimento che si desidera collegare.
5. Scegliere **OK** per tornare alle registrazioni incassi.
6. Registrare la registrazione vendite.  

> [!IMPORTANT]  
>   Quando si collegano movimenti in valute diverse, i movimenti vengono convertiti nella valuta locale. Sebbene i tassi di cambio per le due valute siano fissi, ad esempio tra USD ed EUR, è possibile che durante la conversione nella valuta locale vengano prodotti importi residui di piccola entità. Gli importi residui vengono registrati come utili e perdite sul conto specificato nel campo **Conto utili realizzati** o **Conto perdite realizzate** della pagina **Valute**. Viene rettificato anche il campo **Importo (USD)** nei movimenti contabili fornitori.  

## <a name="to-correct-an-application-of-customer-entries"></a>Per correggere un collegamento di movimenti clienti
Quando si corregge un collegamento, vengono creati e registrati movimenti di rettifica identici a quelli originali ma con segno opposto nel campo relativo all'importo, per tutti i movimenti, incluse le registrazioni di contabilità generale derivanti dal collegamento, quali ad esempio sconto pagamento e profitti e perdite legati alla valuta. Vengono inoltre riaperti i movimenti chiusi dal collegamento.  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
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

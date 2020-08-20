---
title: Impostare le regole per il collegamento automatico dei pagamenti
description: Nella pagina Regole di collegamento pagamenti, si impostano le regole per stabilire in che modo i pagamenti e le transazioni bancarie devono essere collegati automaticamente ai relativi movimenti contabili aperti quando si utilizza la funzione Collega automaticamente nella pagina Registrazione riconciliazione pagamenti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 07/23/2020
ms.author: sgroespe
ms.openlocfilehash: b655032a17aa617ccbaba2ac3dfd5413d4ca4326
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617575"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Impostare le regole per il collegamento automatico dei pagamenti

Nella pagina **Regole di collegamento pagamenti**, si impostano le regole per stabilire il modo in cui il testo del pagamento (in una transazione bancaria) viene automaticamente abbinato al testo dei movimenti aperti nei seguenti due processi:

- Collegare automaticamente i pagamenti a fatture aperte (non pagate), note di credito o altre voci correlate quando si usa la funzione **Collega automaticamente** nella pagina **Registrazione riconciliazione pagamenti**. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

- Corrispondere automaticamente le transazioni bancarie con i relativi movimenti contabili interni del conto bancario quando si sceglie l'opzione **Corrispondenza automatica** nella pagina **Riconciliazioni C/C bancari**. Per ulteriori informazioni, vedere [Riconciliare i conti correnti bancari](bank-how-reconcile-bank-accounts-separately.md).

Impostare una nuova regola di collegamento dei pagamenti scegliendo quali tipi di dati presenti in una riga di registrazione riconciliazione pagamenti devono corrispondere ai dati di uno o più movimenti aperti prima che il pagamento correlato venga collegato automaticamente ai movimenti aperti. La qualità di ogni collegamento automatico in base alle regole di collegamento viene visualizzata come valore da **Basso** ad **Alto** nel campo **Affidabilità corrispondenza** della pagina **Registrazione riconciliazione pagamenti** in base alla regola di collegamento del pagamento utilizzata.

Ogni riga della pagina **Regole di collegamento pagamenti** rappresenta una regola per il collegamento del pagamento. Le regole si collegano nell'ordine specificato dal campo **Ordinamento**. Se vengono utilizzate più regole contemporaneamente, viene utilizzata la regola con affidabilità di corrispondenza più alta.

La funzione di collegamento automatico è basata sui criteri di corrispondenza prioritaria. In primo luogo la funzione prova, seguendo un ordine di priorità, ad associare il testo nei cinque campi **Parte correlata** in una riga di registrazione con testo in conto corrente bancario, nome o indirizzo dei clienti o fornitori con i documenti non pagati che rappresentano movimenti aperti. Quindi, la funzione tenta di far corrispondere il testo nei campi **Testo transazione** e **Informazioni transazione aggiuntive** in una riga di registrazione con il testo nei campi **Nr. documento esterno** e **Nr. documento** di movimenti aperti. Infine, la funzione prova ad associare l'importo presente nel campo **Importo estratto conto** di una riga di registrazione con l'importo nei movimenti aperti.

> [!NOTE]
> La corrispondenza del testo è possibile solo per il testo più lungo di quattro caratteri.

Oltre ai criteri di corrispondenza, il segno dell'importo del pagamento dipende da quanto riportato di seguito:

- Per gli importi negativi, viene creata una corrispondenza innanzitutto con i movimenti aperti che rappresentano le fatture cliente e poi con le note di credito fornitore.
- Per gli importi positivi, viene creata una corrispondenza innanzitutto con i movimenti aperti che rappresentano le fatture fornitore e poi con le note di credito cliente.

## <a name="to-set-up-a-payment-application-rule"></a>Per impostare una regola di collegamento del pagamento
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Regole di collegamento pagamenti** e quindi scegliere il collegamento correlato.
2. Definire una regola dell'applicazione di pagamento nuova o modificata compilando i campi di una riga come descritto nella tabella.

|Campo|Descrizione|
|-|-|
|**Affidabilità corrispondenza**|Specifica l'affidabilità della regola di applicazione definita nella riga. <br /></br>Un valore specificato in questo campo viene visualizzato nel campo **Affidabilità corrispondenza** nella pagina **Registrazione riconciliazione pagamenti** in base alla qualità del collegamento automatico di pagamento nella riga di registrazione.|
|**Priorità**|Specifica la priorità della regola di collegamento relativa alle altre regole di collegamento definite come righe nella pagina **Regole di collegamento pagamenti**. 1 rappresenta la priorità più alta.|
|**Parte correlata corrispondente**|Specifica quante informazioni sul cliente o fornitore, ad esempio indirizzo, città e il numero di conto corrente bancario, nella riga di registrazione della riconciliazione di pagamento devono corrispondere alle informazioni sul movimento aperto prima che la regola di collegamento venga utilizzata per collegare automaticamente il pagamento al movimento aperto.|
|**Nr. doc./nr. doc. est. corrispondente**|Specifica se il testo nella riga di registrazione riconciliazione pagamenti deve corrispondere al valore nel campo **Nr. documento** o nel campo **Nr. documento esterno** nel movimento aperto prima che venga utilizzata la regola di collegamento per collegare automaticamente il pagamento al movimento aperto.|
|**Importo incl. tolleranza corrispondente**|Specifica quanti movimenti per un cliente o fornitore devono corrispondere all'importo, compresa la tolleranza pagamento, prima che la regola di collegamento sia utilizzata per collegare automaticamente un pagamento al movimento aperto.|

La seguente tabella mostra quali regole di collegamento del pagamento vengono impostate nella versione generica di [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Important]
> Le regole di collegamento dei pagamenti possono essere diverse nella propria installazione di [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Affidabilità corrispondenza | Priorità | Parte correlata corrispondente | Nr. doc./nr. doc. est. Corrispondente | Importo incl. tolleranza corrispondente |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Alto             | 1        | Completamente                 | Sì - Multiplo                 | Una corrispondenza                      |
| Alto             | 2        | Completamente                 | Sì - Multiplo                 | Più corrispondenze               |
| Alto             | 3        | Completamente                 | Sì                            | Una corrispondenza                      |
| Alto             | 4        | Completamente                 | Sì                            | Più corrispondenze               |
| Alto             | 5        | Parzialmente             | Sì - Multiplo                 | Una corrispondenza                      |
| Alto             | 6        | Parzialmente             | Sì - Multiplo                 | Più corrispondenze               |
| Alto             | 7        | Parzialmente             | Sì                            | Una corrispondenza                      |
| Alto             | 8        | Completamente                 | No                             | Una corrispondenza                      |
| Alto             | 9        | No                    | Sì - Multiplo                 | Una corrispondenza                      |
| Alto             | 10       | No                    | Sì - Multiplo                 | Più corrispondenze               |
| Medio           | 1        | Completamente                 | Sì - Multiplo                 | Non considerato                 |
| Medio           | 2        | Completamente                 | Sì                            | Non considerato                 |
| Medio           | 3        | Completamente                 | No                             | Più corrispondenze               |
| Medio           | 4        | Parzialmente             | Sì - Multiplo                 | Non considerato                 |
| Medio           | 5        | Parzialmente             | Sì                            | Non considerato                 |
| Medio           | 6        | No                    | Sì                            | Una corrispondenza                      |
| Medio           | 7        | No                    | Sì-Multiplo                   | Non considerato                 |
| Medio           | 8        | Parzialmente             | No                             | Una corrispondenza                      |
| Medio           | 9        | No                    | Sì                            | Non considerato                 |
| Basso              | 1        | Completamente                 | No                             | Nessuna corrispondenza                     |
| Basso              | 2        | Parzialmente             | No                             | Più corrispondenze               |
| Basso              | 3        | Parzialmente             | No                             | Nessuna corrispondenza                     |
| Basso              | 4        | No                    | No                             | Una corrispondenza                      |
| Basso              | 5        | No                    | No                             | Più corrispondenze               |

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

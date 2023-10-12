---
title: Regole per il collegamento automatico dei pagamenti
description: Leggi come impostare le regole per il collegamento automatico dei pagamenti nella pagina Regole di collegamento pagamenti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/25/2021
ms.author: bholtorf
---
# Impostare le regole per il collegamento automatico dei pagamenti

Nella pagina **Regole di collegamento pagamenti**, si impostano le regole per stabilire in che modo il testo del pagamento (in una transazione bancaria) viene collegato automaticamente al testo sulle relative fatture aperte (non pagate), note di credito o altre voci quando viene utilizzata la funzione **Applica automaticamente** nella pagina **Registrazione riconciliazione pagamenti**. Per ulteriori informazioni, vedere [Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md).

Impostare una nuova regola di collegamento dei pagamenti scegliendo quali tipi di dati presenti in una riga di registrazione riconciliazione pagamenti devono corrispondere ai dati di uno o più movimenti aperti prima che il pagamento correlato venga collegato automaticamente ai movimenti aperti. La qualità di ogni collegamento automatico in base alle regole di collegamento viene visualizzata come valore da **Basso** ad **Alto** nel campo **Affidabilità corrispondenza** della pagina **Registrazione riconciliazione pagamenti** in base alla regola di collegamento del pagamento utilizzata.

Ogni riga della pagina **Regole di collegamento pagamenti** rappresenta una regola per il collegamento del pagamento. Le regole si collegano nell'ordine specificato dal campo **Ordinamento**. Se vengono utilizzate più regole contemporaneamente, viene utilizzata la regola con affidabilità di corrispondenza più alta.

La funzione di collegamento automatico è basata sui criteri di corrispondenza prioritaria. In primo luogo la funzione prova, seguendo un ordine di priorità, ad associare il testo nei cinque campi **Parte correlata** in una riga di registrazione con testo in conto corrente bancario, nome o indirizzo dei clienti o fornitori con i documenti non pagati che rappresentano movimenti aperti. Quindi, la funzione tenta di far corrispondere il testo nei campi **Testo transazione** e **Informazioni transazione aggiuntive** in una riga di registrazione con il testo nei campi **Nr. documento esterno** e **Nr. documento** di movimenti aperti. Infine, la funzione prova ad associare l'importo presente nel campo **Importo estratto conto** di una riga di registrazione con l'importo nei movimenti aperti.

> [!NOTE]
> La corrispondenza del testo è possibile solo per il testo più lungo di quattro caratteri.

Oltre ai criteri di corrispondenza, il segno dell'importo del pagamento dipende da quanto riportato di seguito:

- Per gli importi negativi, viene creata una corrispondenza innanzitutto con i movimenti aperti che rappresentano le fatture cliente e poi con le note di credito fornitore.
- Per gli importi positivi, viene creata una corrispondenza innanzitutto con i movimenti aperti che rappresentano le fatture fornitore e poi con le note di credito cliente.

## Per impostare una regola di collegamento del pagamento
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Regole di collegamento pagamenti**, quindi seleziona il collegamento correlato.
2. Definire una regola dell'applicazione di pagamento nuova o modificata compilando i campi di una riga come descritto nella tabella.

|Campo|Descrizione|
|-|-|
|**Affidabilità corrispondenza**|Specifica l'affidabilità della regola di applicazione definita nella riga. <br /></br>Un valore specificato in questo campo viene visualizzato nel campo **Affidabilità corrispondenza** nella pagina **Registrazione riconciliazione pagamenti** in base alla qualità del collegamento automatico di pagamento nella riga di registrazione.|
|**Priorità**|Specifica la priorità della regola di collegamento relativa alle altre regole di collegamento definite come righe nella pagina **Regole di collegamento pagamenti**. 1 rappresenta la priorità più alta.|
|**Parte correlata corrispondente**|Specifica quante informazioni sul cliente o fornitore, ad esempio indirizzo, città e il numero di conto corrente bancario, nella riga di registrazione della riconciliazione di pagamento devono corrispondere alle informazioni sul movimento aperto prima che la regola di collegamento venga utilizzata per collegare automaticamente il pagamento al movimento aperto.|
|**Nr. doc./nr. doc. est. corrispondente**|Specifica se il testo nella riga di registrazione riconciliazione pagamenti deve corrispondere al valore nel campo **Nr. documento** o nel campo **Nr. documento esterno** nel movimento aperto prima che venga utilizzata la regola di collegamento per collegare automaticamente il pagamento al movimento aperto.|
|**Importo incl. tolleranza corrispondente**|Specifica quanti movimenti per un cliente o fornitore devono corrispondere all'importo, compresa la tolleranza pagamento, prima che la regola di collegamento sia utilizzata per collegare automaticamente un pagamento al movimento aperto.|
|**Revisione necessaria**|Specifica se il collegamento dei pagamenti automatico è consigliato per la revisione manuale da parte dell'utente prima della registrazione. Scegliendo il campo **Righe per la revisione** nella pagina **Registrazione collegamenti pagamenti**, viene avviata un'esperienza guidata durante la quale è possibile rivedere con facilità più collegamenti in sequenza nella pagina **Revisione collegamento del pagamento**.|

La tabella seguente descrive le regole di collegamento dei pagamenti standard in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Important]
> Le regole di collegamento dei pagamenti possono essere diverse nella propria installazione di [!INCLUDE[prod_short](includes/prod_short.md)].

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
| Bassa              | 4        | Nr.                    | Nr.                             | Una corrispondenza                      |
| Bassa              | 5        | Nr.                    | Nr.                             | Più corrispondenze               |

## Vedi anche
[Riconciliare i pagamenti utilizzando il collegamento automatico](receivables-how-reconcile-payments-auto-application.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

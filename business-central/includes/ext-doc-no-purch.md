---
author: edupont04
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
---

Nei documenti acquisto e nelle registrazioni è possibile specificare un numero documento che fa riferimento al sistema di numerazione del fornitore. Utilizzare questo campo per registrare il numero assegnato dal fornitore all'ordine, alla fattura o alla nota di credito. Il numero potrà essere utilizzato per cercare la riga dopo che questa sia stata contabilizzata.

Il campo **Nr. doc. esterno obblig.** nella pagina **Setup contabilità fornitori** specifica se è obbligatorio inserire un numero di documento esterno nelle seguenti situazioni:

* Nel campo **Nr. fattura fornitore**, **Nr. ordine fornitore** o **Nr. nota credito for.** in una testata acquisto

* Nel campo **Nr. documento esterno** in una riga registrazioni COGE, dove il campo **Tipo di Documento** è impostato su *Fattura*, *Nota Credito* o *Nota addebito interessi* e il campo **Tipo conto** è impostato su *Fornitore*.

Selezionando questo campo con un segno di spunta, non sarà possibile registrare alcuna fattura, nota di credito o riga delle registrazioni generali del tipo descritto sopra senza un numero di documento esterno.

Il numero del documento esterno è incluso nei documenti registrati in cui è possibile eseguire la ricerca in base al numero pertinente. È inoltre possibile eseguire la ricerca utilizzando il numero di documento esterno durante la navigazione nei movimenti contabili fornitori.

Un modo diverso di gestire i numeri dei documenti esterni consiste nell'utilizzare il campo **Vs. riferimento**. Se viene utilizzato il campo **Vs. riferimento**, il numero verrà incluso nei documenti registrati e puoi cercarlo come per i valori dei campi **Nr. documento esterno** . Ma il campo non è disponibile nelle righe di registrazione.

---
title: Utilizzo delle registrazioni COGE per registrare direttamente in contabilità generale| Documenti Microsoft
description: Informazioni su come è possibile utilizzare le registrazioni per la contabilizzazione nei conti C/G e in altri conti delle transazioni finanziarie, ad esempio i conti correnti bancari e i conti fornitori.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9ba3873284f5e40e46eeee8615974dd6053d4991
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249953"
---
# <a name="working-with-general-journals"></a>Utilizzo delle registrazioni COGE

La maggior parte delle transazioni finanziarie vengono registrate nella contabilità generale attraverso i documenti aziendali dedicati quali fatture di acquisto e ordini di vendita. Ma è anche possibile elaborare attività commerciali come l'acquisto, il pagamento o il rimborso delle spese dei dipendenti registrando le righe di registrazione nelle varie registrazioni in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

La maggior parte delle registrazioni sono basate *Contabilità generale* ed è possibile elaborare tutte le operazioni nella pagina **Contabilità generale**. Per ulteriori informazioni, vedere [Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md).  

Ad esempio, è possibile usare la spesa del dipendente nelle spese correlate all'azienda per un risarcimento successivo. Per altre informazioni, vedere [Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md).

In molti casi, tuttavia, si desidera utilizzare le registrazioni ottimizzate per specifici tipi di transazioni, ad esempio le **Registrazioni pagamenti** per la registrazione dei pagamenti. Per ulteriori informazioni, vedere [Registrare pagamenti e resi nelle Registrazioni pagamenti](payables-how-post-payments-refunds.md)  

Le registrazioni generali vengono utilizzate per la contabilizzazione diretta nei conti C/G e in altri conti delle transazioni finanziarie, ad esempio i conti correnti bancari, i conti clienti, fornitori e dipendenti. La contabilizzazione mediante una registrazione generale crea sempre movimenti nei conti di contabilità generale. Ciò è vero anche quando, ad esempio, viene contabilizzata una riga di registrazione in un conto cliente, in quanto tramite una categoria di registrazione viene registrata una riga in un conto crediti nella contabilità generale.

Le informazioni immesse in una registrazione sono temporanee e possono essere modificate mentre si trovano nella registrazione. Quando si contabilizza la registrazione, le informazioni vengono trasferite a movimenti in singoli conti, dove non possono essere modificate. È tuttavia possibile scollegare i movimenti registrati e stornare o correggere i movimenti. Per ulteriori informazioni, vedere [Stornare le registrazioni](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Utilizzo di batch e definizioni di registrazioni

Esistono numerose definizioni registrazioni COGE. Ogni definizione registrazioni è rappresentata da una pagina dedicata con funzioni specifiche e campi necessari per supportare tali funzioni, ad esempio la pagina **Registrazione riconciliazione pagamenti** per elaborare i pagamenti bancari e la pagina **Registrazioni pagamenti** per pagare i fornitori o rimborsare i dipendenti. Per ulteriori informazioni, vedere [Effettuare i pagamenti](receivables-how-apply-sales-transactions-manually.md) e [Riconciliare i pagamenti clienti con la registrazione incassi o da movimenti contabili clienti](payables-make-payments.md).

Per ogni definizione registrazioni è possibile impostare le proprie registrazioni personali come batch registrazioni. Ad esempio, è possibile definire dei batch registrazioni personali per le registrazioni pagamenti che abbiano delle impostazioni e un layout personali. Di seguito viene fornito un suggerimento come esempio per personalizzare una registrazione.

> [!TIP]  
> Se si seleziona la casella di controllo **Suggerisci importo contropartita** nella riga per il proprio batch nella pagina **Batch registrazioni COGE**, il campo **Importo** ad esempio nelle righe di registrazione COGE per lo stesso numero di documento viene precompilato automaticamente con il valore richiesto per saldare il documento. Per ulteriori informazioni, vedere [Suggerimento automatico dei valori in [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Informazioni su conti principali e contropartita
Se sono stati impostati conti di contropartita di default per i batch di registrazioni nella pagina **Registrazioni COGE**, il conto di contropartita verrà compilato automaticamente quando si inserisce un valore nel campo **Nr. conto**. In caso contrario, compilare manualmente sia il campo **Nr. conto** che il campo **Contropartita**. Un importo positivo nel campo **Importo** viene addebitato sul conto principale e accreditato nella contropartita. Un importo negativo viene accreditato sul conto principale e addebitato nella contropartita.

> [!NOTE]  
>   L'IVA viene calcolata separatamente per il conto principale e il conto di contropartita, quindi possono essere utilizzate percentuali IVA diverse.

## <a name="working-with-recurring-journals"></a>Utilizzo delle registrazioni periodiche
Una registrazione periodica è una registrazione generale con campi specifici per la gestione di transazioni registrate frequentemente con poche o nessuna modifica, come affitto, sottoscrizioni, elettricità, riscaldamento. Se si utilizzano questi campi per le transazioni ricorrenti, è possibile registrare sia gli importi fissi sia quelli variabili. È inoltre possibile specificare movimenti di storno automatico per il giorno successivo alla data di registrazione. È anche possibile utilizzare chiavi di assegnazione per suddividere i movimenti ricorrenti tra vari conti. Per ulteriori informazioni, vedere [Allocare importi di registrazioni periodiche a vari conti](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Utilizzando registrazioni periodiche, è sufficiente immettere una sola volta i movimenti registrati regolarmente. Ciò significa che i conti, le dimensioni, i valori dimensioni e così via, immessi nei campi rimarranno nelle registrazioni dopo la contabilizzazione. Se sono necessarie rettifiche, è possibile eseguirle a ogni registrazione.

### <a name="recurring-method-field"></a>Campo Metodo ricorrenza
Questo campo consente di determinare in che modo verrà considerato l'importo specificato nella riga delle registrazioni dopo la contabilizzazione. Se ad esempio si utilizza il medesimo importo per ogni registrazione, l'importo risulta invariato. Se nella riga vengono utilizzati i medesimi conti e testo e l'importo varia a ogni registrazione, sarà possibile eliminare l'importo dopo la registrazione.

| A | Vedere |
| --- | --- |
|Fisso|l'importo specificato nella riga delle registrazioni rimarrà invariato dopo la contabilizzazione.|
|Variabile|l'importo specificato nella riga delle registrazioni verrà eliminato dopo la contabilizzazione.|
|Saldo|L'importo registrato nel conto specificato nella riga verrà allocato tra i conti specificati relativi alla riga nella tabella Allocazioni registrazioni gen. il saldo nel conto risulterà così uguale a zero. Compilare il campo **Allocazione %** nella pagina **Allocazioni**. Per ulteriori informazioni, vedere [Allocare importi di registrazioni periodiche a vari conti](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Storno Costante|l'importo specificato nella riga delle registrazioni rimarrà invariato dopo la contabilizzazione e un movimento di quadratura verrà registrato il giorno seguente.|
|Storno Variabile|l'importo specificato nella riga delle registrazioni verrà eliminato dopo la contabilizzazione e un movimento di quadratura verrà registrato il giorno seguente.|
|Storno Saldo|L'importo registrato nel conto specificato nella riga verrà allocato tra i conti specificati relativi alla riga nella pagina **Allocazioni**. Il saldo nel conto verrà impostato su zero e un movimento di contropartita viene registrato il giorno seguente.|

> [!NOTE]  
>  È possibile immettere informazioni nei campi relativi all'IVA nella riga delle registrazioni periodiche o di allocazione ma non in entrambe. È possibile completarli nella pagina **Allocazioni** soltanto se le righe corrispondenti delle registrazioni periodiche non sono completate.

### <a name="recurring-frequency-field"></a>Campo Frequenza ricorrenza
Questo campo determina la frequenza con cui il movimento contenuto nella riga delle registrazioni verrà contabilizzato. Si tratta di un campo di formula per le date e deve essere riempito per le righe delle registrazioni periodiche. Per ulteriori informazioni, vedere [Utilizzo di formule per le date](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Esempi
Se è necessario contabilizzare ogni mese la riga delle registrazioni, immettere "1M". Dopo ogni registrazione, la data indicata nel campo **Data di registrazione** verrà aggiornata alla stessa data del mese successivo.

Se si desidera registrare un movimento l'ultimo giorno di ogni mese, è possibile operare in uno dei modi descritti di seguito:

- Registrare il primo movimento l'ultimo giorno di un mese immettendo la formula 1G + 1M - 1G (1 giorno + 1 mese - 1 giorno). Con questa formula, la data di registrazione viene calcolata correttamente indipendentemente dalla lunghezza del mese.

- Registrare il primo movimento in qualsiasi giorno del mese immettendo la formula: 1M+CM. Con questa formula, la data di registrazione sarà dopo un mese intero + i giorni rimanenti del mese corrente.

### <a name="expiration-date-field"></a>Campo Data di scadenza
Questo campo determina la data in cui la riga sarà registrata per l’ultima volta. Oltre tale data, la riga non verrà più registrata.

L'utilizzo di questo campo risulta vantaggioso poiché la riga non viene eliminata dalle registrazioni immediatamente. Sarà possibile sostituire la data di termine già stabilita con una data successiva e utilizzare quindi la riga più a lungo.

Se il campo rimane vuoto, la riga viene contabilizzata ogni volta che si effettuerà una registrazione fino a quando non verrà eliminata dalle registrazioni.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Allocare importi di registrazioni periodiche a vari conti
Nella pagina **Reg. periodiche generali**, è possibile scegliere l'azione **Allocazioni** per visualizzare o gestire il modo in cui gli importi nella riga delle registrazioni ricorrenti sono allocati a vari conti e dimensioni. Da notare che un'allocazione è una riga delle registrazioni periodiche nella riga di contropartita.

È sufficiente immettere un'allocazione una sola volta, esattamente come nelle registrazioni periodiche. Poiché dopo la contabilizzazione l'allocazione verrà conservata nelle registrazioni di allocazione, non è necessario immettere gli importi e le allocazioni a ogni contabilizzazione della riga delle registrazioni periodiche.

Se il metodo ricorrente nelle registrazioni periodiche viene impostato su **Saldo** o **Saldo a pareggio**, qualsiasi codice valore dimensioni nelle registrazioni periodiche viene ignorato quando il conto risulta uguale a zero. Quindi, se viene allocata una riga ricorrente in diversi valori dimensioni nella pagina **Allocazioni**, sarà creato un solo movimento di pareggio. Se pertanto viene allocata una riga delle registrazioni periodiche contenente un codice valore dimensioni, è necessario non immettere il medesimo codice nella pagina **Allocazioni**. In caso contrario, i valori dimensioni non risulteranno corretti.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Esempio: Allocare pagamenti di affitti a diversi reparti
l'importo dell'affitto mensile è stato immesso nel conto cassa specificato in una riga delle registrazioni periodiche. Nelle pagina **Allocazioni**, è possibile suddividere la spesa tra più reparti (dimensione Reparto) in base ai metri quadrati occupati da ciascuno. Il calcolo si basa sulla percentuale di allocazione relativa a ogni riga. È possibile immettere diversi conti in differenti righe di allocazione (se anche l'affitto verrà diviso tra più conti) oppure immettere lo stesso conto, ma con diversi codici valore dimensioni per la dimensione Reparto in ogni riga.

## <a name="working-with-standard-journals"></a>Utilizzo delle registrazioni standard
Quando si creano righe di registrazione che verranno probabilmente create di nuovo successivamente, è possibile scegliere di salvarle come registrazioni standard prima di contabilizzare la registrazione. Questa funzionalità si applica alle registrazioni di magazzino e alle registrazioni COGE.

> [!NOTE]  
>   la seguente procedura si riferisce alle registrazioni magazzino, ma le informazioni sono valide anche per le registrazioni COGE.

### <a name="to-save-a-standard-journal"></a>Per salvare una registrazione standard
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni magazzino** e quindi scegliere il collegamento correlato.
2. Immettere una o più righe di registrazione.
3. Selezionare le righe di registrazione che si desidera riutilizzare.
4. Scegliere l'azione **Salva come registrazioni standard**.
5. Nella pagina di richiesta **Salva come Registrazioni Magazzino Standard**, definire una registrazione di magazzino standard nuova o esistente in cui devono essere salvate le righe:

    Se sono già state create una o più registrazioni magazzino standard e si desidera sostituirne una con il nuovo insieme di righe di registrazione magazzino, selezionare il codice desiderato nel campo Codice.
6. Scegliere **OK** per verificare l'intenzione di sovrascrivere la registrazione magazzino standard esistente e sostituirne tutto il contenuto.
7. Selezionare il campo **Salva importo unitario** se si desidera salvare i valori nel campo **Importo unitario** delle registrazioni magazzino standard.
8. Selezionare il campo **Salva quantità** se si desidera che vengano salvati i valori nel campo **Quantità** .
9. Scegliere **OK** per salvare le registrazioni magazzino standard.

Al termine del salvataggio della registrazione magazzino standard, viene visualizzata la pagina Registrazioni Magazzino ed è possibile procedere alla contabilizzazione della registrazione, che potrà essere facilmente ricreata nel caso in cui sia nuovamente necessario contabilizzare righe identiche o simili.

### <a name="to-reuse-a-standard-journal"></a>Per riutilizzare registrazioni standard
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni magazzino** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Ottieni registrazioni standard**.

    Verrà visualizzata la pagina Registrazioni magazzino standard, contenente i codici e le descrizioni per tutte le registrazioni di magazzino standard esistenti.
3. Per rivedere una registrazione di magazzino standard prima della relativa selezione a scopo di riutilizzo, scegliere l'azione **Mostra registrazioni**.

    Qualsiasi modifica apportata in una registrazione di magazzino standard viene immediatamente implementata. Sarà presente alla successiva apertura o al successivo riutilizzo della registrazione di magazzino standard in questione. È pertanto opportuno assicurarsi che la modifica sia sufficientemente importante da essere applicata a livello generale. In caso contrario, apportare la modifica specifica nella registrazione di magazzino dopo l'inserimento delle righe della registrazione di magazzino standard. Vedere il passaggio 4 di seguito.
4. Nella pagina **Registrazioni magazzino standard** selezionare la registrazione di magazzino standard che si desidera riutilizzare e quindi scegliere **OK**.

    La registrazione di magazzino sarà ora completata con le righe salvate come registrazione di magazzino standard. Se nella registrazione di magazzino erano già presenti righe di registrazione, le righe inserite verranno posizionate sotto le righe di registrazione esistenti.

    Se non si è selezionato il campo **Salva importo unitario** quando si è utilizzato il processo della funzione **Salva come registrazioni magazzino standard**, il campo **Importo unitario** delle righe inserite dalle registrazioni standard viene automaticamente completato con il valore corrente dell'articolo, copiato dal campo **Costo unitario** della scheda articolo.

    > [!NOTE]  
    >   in caso di selezione dei campi **Salva Importo Unitario** o **Salva Quantità**, è opportuno assicurarsi che i valori inseriti siano corretti per la rettifica di magazzino specifica prima di contabilizzare la registrazione di magazzino.

    Se le righe di registrazione di magazzino inserite contengono importi unitari salvati che non si desidera contabilizzare, è possibile eseguire rapidamente la rettifica al valore corrente dell'articolo come indicato di seguito.

6. Selezionare e righe di registrazioni magazzino che si desidera rettificare e scegliere l'azione **Ricalcola importo unitario**. Il campo Importo unitario verrà così aggiornato con il costo unitario corrente dell'articolo.
7. Scegliere l'azione **Registra**.

## <a name="to-renumber-document-numbers-in-journals"></a>Rinumerare i documenti nei giornali di registrazione
Per evitare errori di registrazione dovuti all'ordine dei numeri di documento, è possibile utilizzare la funzione **Rinumera documenti** prima di effettuare una registrazione.

In tutte le registrazioni basate sulle registrazioni COGE, il campo **Nr. documento** può essere modificato per poter specificare numeri di documento diversi in base alle diverse righe registrazioni o lo stesso numero di documento per le righe registrazioni correlate.

Se il campo **Nr. serie** nel batch registrazioni è compilato, la funzione di registrazione nelle registrazioni COGE richiede che il numero di documento nelle righe registrazioni singole o raggruppate segua un ordine sequenziale. Per evitare errori di registrazione dovuti all'ordine dei numeri di documento, è possibile utilizzare la funzione **Rinumera documenti** prima di effettuare registrazioni. Se le righe registrazioni correlate sono state raggruppate in base al numero del documento prima dell'utilizzo della funzione, rimarranno raggruppate, anche se potrebbero essere assegnate a un numero di documento diverso.

Questa funzione può anche essere utilizzata sulle viste filtrate.

La rinumerazione dei documenti rispetterà i collegamenti correlati, ad esempio il collegamento di un pagamento tra il documento nella riga registrazioni e un conto fornitore. Di conseguenza, è possibile aggiornare i campi **Collega-a ID** e **Collega-a nr. doc.** nei movimenti contabili interessati.

La procedura riportata di seguito è basata sulla pagina **Registrazione COGE**, ma si applica a tutte le altre registrazioni basate sulle registrazioni COGE, ad esempio la pagina **Registraz. pagamenti**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.
2. Quando si è pronti per contabilizzare la registrazione, scegliere l'azione **Rinumera documenti**.

I valori nel campo **Nr. documento** vengono modificati, se necessario, in modo che il numero del documento nelle righe registrazioni singole o raggruppate seguano un ordine sequenziale. Dopo la rinumerazione dei documenti, è possibile procedere con la contabilizzazione delle registrazioni.

## <a name="see-also"></a>Vedi anche
[Registrare le transazioni direttamente nella contabilità generale](finance-how-post-transactions-directly.md)  
[Stornare le registrazioni](finance-how-reverse-journal-posting.md)  
[Allocazione di costi e ricavi](year-allocate-costs-income.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

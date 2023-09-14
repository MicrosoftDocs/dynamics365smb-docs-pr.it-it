---
title: 'Impostare capacità, prezzi, costi delle risorse del progetto'
description: 'Per utilizzare le risorse e semplificare la gestione dei progetti, specificare i costi e i prezzi per le singole risorse o i gruppi di risorse e impostare la capacità della risorsa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Impostazione delle risorse per i progetti

Per gestire correttamente le attività delle risorse, è necessario impostare le risorse, nonché i costi e i prezzi correlati. I prezzi, gli sconti e le regole dei fattori di costi correlati a una commessa vengono impostati nella scheda commessa. È possibile specificare i costi e i prezzi per singole risorse, gruppi di risorse oppure per tutte le risorse disponibili della società.

Quando le risorse vengono utilizzate o vendute nell'ambito di una commessa, i prezzi e i costi ad esse associati vengono recuperati dalle informazioni impostate.

L'importo orario di default viene specificato durante la creazione della risorsa. Se, ad esempio, si utilizza per cinque ore un macchinario per l'esecuzione di una commessa, quest'ultima verrà calcolata sulla base dell'importo orario.

> [!NOTE]
> Puoi acquistare risorse esterne, ad esempio, per fatturare a un fornitore per il lavoro eseguito. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).<br /><br />
> Per le risorse esterne, ti consigliamo di nominare o raggruppare tali risorse in modo che non vengano confuse con le risorse interne.
>  
> Se registri transazioni intercompany, sebbene sia possibile una risorsa in una riga di un ordine cliente, se si converte l'ordine cliente in un ordine fornitore sul lato ricevente, la risorsa non verrà inclusa. Per utilizzare le risorse nelle transazioni intercompany, utilizza il campo **Nr. conto C/G acq. partner IC** della scheda risorsa per specificare il conto su cui registrare le spese.

## Per impostare una risorsa

Creare una scheda per ogni risorsa che si desidera utilizzare nei progetti.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Risorse**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Per impostare un gruppo di risorse

È possibile unire diverse risorse in uno stesso gruppo di risorse. Le capacità e i budget di un gruppo di risorse sono il risultato della somma delle capacità e dei budget delle singole risorse. È possibile immettere le capacità dei gruppi di risorse indipendentemente dai valori accumulati oppure in aggiunta a questi.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Gruppi di risorse**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Compilare i campi, se necessario.

## Per impostare la capacità per una risorsa

Per calcolare quanto tempo una risorsa può dedicare alle commesse, la relativa capacità deve essere prima impostata come tempo disponibile per periodo nel calendario di produzione. Questa impostazione è utilizzata quando si compilano le righe di pianificazione commessa che contengono la risorsa. Per ulteriori informazioni, vedere [Creare le commesse](projects-how-create-jobs.md).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Risorse**, quindi scegli il collegamento correlato.
2. Aprire la scheda risorsa interessata e scegliere l'azione **Capacità risorsa**.
3. Nella pagina **Capacità risorsa** nel campo **Visualizza per** specificare la durata del periodo, ad esempio **giorno**, che viene visualizzato nelle colonne della Scheda dettaglio **Matrice capacità risorse**.
4. Per ogni risorsa di una riga, specificare per ogni periodo nelle colonne il numero di ore per cui la risorsa è disponibile.
5. In alternativa, per dettagliare la capacità settimanale della risorsa con una data di inizio e una data di fine, scegliere l'azione **Imposta capacità**.
6. Nella pagina **Impostazioni capacità risorse** compilare i campi in una riga in base alle esigenze.
7. Scegliere l'azione **Aggiorna capacità**. La pagina **Capacità risorsa** viene aggiornata con la capacità immessa.
8. Chiudere la pagina.

## Per impostare costi di risorsa alternativi

Oltre al costo specificato nella scheda risorsa, è possibile impostare dei costi alternativi per ogni risorsa. Se ad esempio un lavoratore percepisce una paga oraria maggiore per il lavoro straordinario, si può impostare un costo risorsa per lo straordinario. Il costo alternativo impostato per la risorsa sovrascriverà il costo nella scheda della risorsa, quando si utilizzerà la risorsa nelle registrazioni risorse.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Risorse**, quindi scegli il collegamento correlato.  
2. Selezionare la risorsa per la quale si desidera impostare uno o più costi alternativi, quindi scegliere l'azione **Costi**.  
3. Nella pagina **Costi risorse** compilare i campi in una riga in base alle esigenze.  
4. Ripetere il passaggio 3 per ogni costo di risorsa alternativo che si desidera impostare.

**Nota**. Per impostare i costi risorse da applicare a tutte le risorse e ai gruppi di risorse, aprire la pagina **Costi risorse** e compilare i campi.

## Per impostare prezzi di risorsa alternativi

Oltre al prezzo specificato nella scheda risorsa, è possibile impostare dei prezzi alternativi per ogni risorsa. Questi prezzi alternativi possono essere condizionali. Possono dipendere dal fatto che la risorsa sia utilizzata con un tipo di lavoro o una commessa specifica.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Risorse**, quindi scegli il collegamento correlato.
2. Selezionare la risorsa per la quale si desidera impostare uno o più prezzi alternativi, quindi scegliere l'azione **Prezzi**.
3. Nella pagina **Prezzi risorse** compilare i campi in una riga in base alle esigenze.
4. Ripetere il passaggio 3 per ogni prezzo di risorsa alternativo che si desidera impostare.

## Vedi il relativo [training Microsoft](/training/paths/set-up-jobs-resources/)

## Vedere anche

[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

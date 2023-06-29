---
title: Creare cicli
description: 'Questo argomento fornisce una panoramica dei diversi modi per creare i ciclil, inclusi i prerequisiti richiesti e come creare i collegamenti di ciclo.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="create-routings"></a><a name="create-routings"></a>Creare cicli

Le aziende manifatturiere utilizzano i cicli per visualizzare e gestire il processo di produzione.

Il ciclo è la base della programmazione del processo e delle capacità, delle assegnazioni programmate delle necessità di materiali e dei documenti relativi alla produzione.  

Per quanto riguarda la DB di produzione, i cicli di produzione vengono assegnati all'articolo finale di produzione. Un ciclo contiene i dati master per l'acquisizione dei requisiti di processo di un determinato articolo prodotto. Dopo la creazione di un ordine di produzione per l'articolo, il ciclo relativo determinerà la pianificazione delle operazioni come rappresentato nella pagina **Cicli ordini produzione** nell'ordine di produzione.  

Prima di poter configurare un ciclo, è necessario verificare quanto segue:  

- Aver creato schede articolo per gli articoli padre inclusi nella produzione. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).
- Sono state impostate le risorse di produzione. Per ulteriori informazioni, vedere [Impostare aree di produzione e centri di lavoro](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a><a name="to-create-a-routing"></a>Per creare un ciclo

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cicli**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.  
3. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nel campo **Tipo** selezionare **Seriale** per calcolare il ciclo di produzione in base al valore del campo **Nr. operazione** .  
    Selezionare **Parallelo** per calcolare le operazioni in base al valore nel campo **Nr. operazione successivo** .  
5. Per modificare il ciclo, impostare il campo **Stato** su **Nuovo** o **In sviluppo**. Per attivarlo, impostare lo **Stato** su **Certificato**.  

    Riempire le righe del ciclo.
6. Nel campo **Nr. operazione** immettere il numero della prima operazione, ad esempio **10**.  
7. Specificare nel campo **Tipo** il tipo di risorsa utilizzata, ad esempio **Area di produzione**.  
8. Nel campo **Nr.** selezionare la risorsa da utilizzare oppure immetterla nel campo.  
9. Nel campo **Cod. legame ciclo-DB**, immettere un codice per connettere il componente a un'operazione specifica. Per ulteriori informazioni, vedere [Per creare collegamenti ciclo](production-how-to-create-routings.md#to-create-routing-links).
10. Nei campi **Tempo Lavorazione** e **Tempo di Setup** specificare i tempi di processo necessari per l'esecuzione dell'operazione.

     > [!NOTE]
     > il tempo di setup viene calcolato per ordine di produzione, mentre il tempo di lavorazione viene calcolato per articolo prodotto.  

11. Nel campo **Capacità simultanee** , specificare il numero di unità della risorsa selezionata da utilizzare per eseguire l'operazione. Ad esempio, se si assegnano due persone a un'operazione di imballaggio si dimezzerà il tempo di lavorazione.  
12. Continuare a compilare le righe relative a tutte le operazioni previste per la produzione dell'articolo specificato.  
13. Per copiare righe da un ciclo esistente, scegliere l'azione **Copia ciclo** per selezionarle.  
14. Certificare il ciclo.  
15. È ora possibile allegare il nuovo ciclo alla scheda dell'articolo padre desiderato, compilando il campo **Nr. ciclo**. Per ulteriori informazioni, vedere [Registrare nuovi articoli](inventory-how-register-new-items.md).  

> [!NOTE]  
> Ricordare inoltre di ricalcolare il costo standard dell'articolo dalla scheda **Articolo**: scegliere l'azione **Produzione**, quindi selezionare l'azione **Calc. costo standard** e poi l'azione **Tutti i livelli**.  

## <a name="to-create-routing-links"></a><a name="to-create-routing-links"></a>Per creare collegamenti ciclo

È possibile creare collegamenti ciclo per connettere componenti a operazioni specifiche, in modo da conservarne le relazioni anche in caso di modifica della distinta base di produzione o del ciclo. Questa soluzione facilita inoltre la consuntivazione dei componenti in tempo reale, che avviene infatti all'avvio dell'operazione specifica collegata, anziché al rilascio dell'ordine di produzione completo. Per ulteriori informazioni vedere [Componenti ordine produzione a livello in base all'output dell'operazione](production-how-to-flush-components-according-to-operation-output.md).  

Un altro vantaggio importante consiste nel fatto che le operazioni e i componenti collegati vengono visualizzati in una struttura di processo logica quando si utilizza la pagina **Registrazioni di produzione** per la registrazione di output e consumo.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cicli**, quindi scegli il collegamento correlato.  
2. Aprire il ciclo che contiene le operazioni da collegare.  

    Assicurarsi che lo stato del ciclo sia impostato su **In sviluppo**.  

3. Nella riga del ciclo di produzione pertinente, nel campo **Cod. legame ciclo-DB** , selezionare un codice.  
4. Aggiungere diversi codici legame ciclo-DB a altre operazioni, nel ciclo, se necessario.  

    > [!NOTE]  
    > Non utilizzare lo stesso codice di legame ciclo-DB in diverse operazioni su un ciclo, per evitare di collegare erroneamente un componente a due operazioni diverse e, quindi, di utilizzarlo due volte.  
    >
    > Si consiglia di assegnare un nome al codice di legame tra il ciclo e la distinta base dopo l'operazione, per assicurare la creazione di collegamenti ciclo specifici per ogni operazione.

5. Impostare lo stato del ciclo su **Certificato**.  

    I codice legame tra ciclo e distinta base vengono assegnati alle operazioni. A questo punto, è necessario creare il collegamento effettivo assegnando gli stessi codici ai componenti specifici nella distinta base di produzione.  

6. Aprire la **DB produzione** contenente i componenti da collegare alle operazioni precedenti. Per ulteriori informazioni, vedere [Creare distinte base di produzione](production-how-to-create-production-boms.md).
7. Assicurarsi che lo stato della DB sia impostato su **In sviluppo**.  
8. Nella riga della distinta base di produzione, nel campo **Cod. legame ciclo-DB** , selezionare il codice appena assegnato all'operazione specificata.  
9. Continuare aggiungendo i codici di legame agli altri componenti, in base alle operazioni univoche in cui vengono utilizzati.  
10. Impostare lo stato della distinta base di produzione su **Certificato**.  

    > [!NOTE]  
    > Per abilitare i collegamenti ciclo in un ordine di produzione esistente, è necessario aggiornare l'ordine di produzione. Per ulteriori informazioni, vedere [Creare ordini di produzione](production-how-to-create-production-orders.md).  

I componenti selezionati risultano collegati alle operazioni specificate quando si crea o si aggiorna un ordine di produzione mediante la distinta base di produzione e il ciclo interessati. Ciò è visibile nella pagina **Componenti ordine produzione** nell'ordine di produzione, dove è inoltre possibile rimuovere e aggiungere i codici di collegamento ciclo codici definiti in qualsiasi momento.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a><a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Per assegnare personale, strumenti e controlli di qualità alle operazioni di ciclo

Se occorre personale con speciali qualifiche, particolari conoscenze o una speciale autorizzazione per un'operazione, è possibile assegnarlo all'operazione. Inoltre, è possibile assegnare strumenti e requisiti di qualità all'operazione. Questa procedura descrive come assegnare personale. I passaggi sono simili per altri tipi di informazioni sull'operazione.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cicli**, quindi scegli il collegamento correlato.  
2. Apri il ciclo pertinente.  
3. Nella Scheda dettaglio **Righe**, selezionare la riga da elaborare, quindi scegliere l'azione **Operazioni** e **Personale**.  
4. Compilare i campi della pagina **Personale ciclo**.  
5. Scegliere il pulsante **OK** per chiudere la pagina. I valori immessi vengono copiati e assegnati all'operazione.  

## <a name="to-create-a-new-versions-of-a-routing"></a><a name="to-create-a-new-versions-of-a-routing"></a>Per creare nuove versioni di un ciclo

La funzionalità di versione consente di gestire più versioni dei cicli. La struttura della versione del ciclo corrisponde a quella del ciclo ed è costituita da una testata e da righe. La differenza principale è costituita dalla data iniziale del ciclo.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cicli**, quindi scegli il collegamento correlato.  
2. Selezionare il ciclo da copiare quindi scegliere l'azione **Versioni**.  
3. Nella pagina **Versioni ciclo**, scegliere l'azione **Nuovo**.
4. Compilare i campi come necessario.
5. Nel campo **Cod. versione** immettere il codice identificativo univoco della versione. Nel campo è possibile inserire qualsiasi combinazione di numeri o di lettere.  

    Alla versione appena creata viene assegnato automaticamente lo stato **Nuovo**.  
6. Per creare righe dell'operazione, selezionare la prima riga vuota e riempire il campo **Nr. operazione**. in base alla sequenza di operazioni.

    Le righe delle operazioni sono ordinate in ordine crescente in base ai numeri di operazione. Per poter apportare modifiche seguito, è consigliabile distanziare adeguatamente le varie fasi. Il campo **Nr. operazione successivo** si riferisce all'operazione che segue. È possibile immettere direttamente il numero dell'operazione.

7. Quando la versione del ciclo è completata, scegliere **Certificata** nel campo **Stato**.

La validità temporale della versione viene specificata nel campo **Data di Inizio**.  

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Creare le distinte base di produzione](production-how-to-create-production-boms.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Pianif.](production-planning.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

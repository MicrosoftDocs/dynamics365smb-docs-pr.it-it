---
title: Combinare la consuntivazione automatica e manuale
description: 'Procedura dettagliata per un pianificatore di produzione di Contoso Coffee, che desidera combinare la consuntivazione automatica e manuale.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Procedura dettagliata: Combinare la consuntivazione automatica e manuale

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee nella consuntivazione.  

## Scenario

Sei l'addetto alla pianificazione della produzione di Contoso Coffee. È necessario creare un nuovo ordine di produzione per dieci unità dell'articolo SP-SCM1004, AutoDrip. Alcuni componenti e operazioni verranno consuntivati in avanti, altri all'indietro in base a condizioni diverse.

## Passaggi

> [Nota!] Ricordati di rettificare l'inventario registrando il giornale di registrazione articolo con i saldi di apertura.

1. Crea un ordine di produzione pianificato confermato per cinque unità dell'articolo **SP-SCM1004, AutoDrip** nell'ubicazione *PRINCIPALE*. Per informazioni, vedi [Procedura dettagliata: Creare un ordine di produzione confermato e modificarlo](create-firm-planned-production-order-change.md).  

2. Rilascia l'ordine di produzione.

    1. Scegli l'azione **Cambia stato**.  

    2. Nella pagina che appare, imposta il campo **Nuovo stato** su *Rilasciato*, quindi scegli il pulsante **Sì**.  

        Viene visualizzato un messaggio con una barra di stato che fa riferimento al consumo automatico. Questo è seguito da un messaggio di conferma che l'ordine è stato modificato per avere lo stato *Rilasciato*.  

    3. Scegli il pulsante **OK** per chiudere il messaggio di conferma.

3. Esamina i movimenti contabili dell'articolo e della capacità per l'ordine di produzione.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordine di produzione rilasciato**, quindi scegli il collegamento correlato.  

    2. Apri l'ordine di produzione con le 5 unità della macchina da caffè AutoDrip.  

    3. Scegli l'azione **Movimenti contabili articoli**.  

        L'articolo **SP-BOM1305 Screw Hex M3 Zink** viene consuntivato immediatamente con l'intera quantità prevista. Chiudi la pagina **Movimenti contabili articoli**.  

    4. Scegli l'azione **Movimenti contabili capacità**.  Nota che una voce di operazioni di assemblaggio corpo è stata completata nel momento in cui è stato rilasciato l'ordine. Chiudi la finestra **Movimenti contabili capacità**.

    È possibile eseguire la consuntivazione manualmente degli articoli componenti utilizzando il giornale di registrazione consumo o produzione. La consuntivazione manuale consente di regolare la quantità prima della registrazione. Ad esempio, se è necessaria una quantità aggiuntiva per coprire le materie prime di bassa qualità.
4. Esegui la consuntivazione dei componenti manualmente.  
    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni consumi**, quindi scegli il collegamento correlato.  

    2. Sceglie l'azione **Calcola consumo**.  

    3. Nella pagina della richiesta **Calcola consumo** nella Scheda dettaglio **Ordine di produzione** definisci un filtro per l'ordine specifico nel campo **Numero ordine** e scegli il pulsante **OK**. Dopo la chiusura della pagina della richiesta di processo batch, nota che la pagina **Registrazioni consumi** viene popolata con i componenti che richiedono il consumo manuale.

    4. Scegli l'azione **Registra**. Chiudi le registrazioni consumi.

5. Registra manualmente l'output per il cablaggio elettrico.  

    Devi compilare manualmente i campi **Tempo di setup** e **Tempo lavorazione**. È inoltre possibile specificare la quantità effettivamente prodotta e lo scarto. Immetti *3* come quantità di output e registra l'output.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni output**, quindi scegli il collegamento correlato.  

    2. Nella pagina **Registrazioni output**, crea una nuova riga di registrazione.  

    3. Nel campo **Nr. ordine** specifica l'ordine.  

    4. Scegli l'azione **Esplodi ciclo**.  

        La pagina **Registrazioni output** viene popolata con la riga operativa solo per il cablaggio elettrico.

    5. Imposta il campo **Tempo lavorazione** su *10*.  

    6. Cambia il campo **Quantità** da *5* a *3*.

    7. Scegli **Registra**.  
    8. Chiudi le registrazioni output.

6. Esamina i movimenti contabili dell'articolo per l'ordine di produzione.

    1. Nella pagina dell'ordine di produzione, scegli l'azione **Movimenti contabili articoli**.  

    L'articolo **SP-BOM1302, Display del pannello di controllo** viene registrato con una quantità di *3*, in base all'output effettivo, mentre **SP-BOM1303, pulsante** viene registrato con l'intera quantità prevista. Chiudi la pagina **Movimenti contabili articoli**.

7. Finalizza l'ordine di produzione.  

    1. Scegli l'azione **Cambia stato**.
    2. Nella pagina che appare, imposta il campo **Nuovo stato** su *Completato*, quindi scegli il pulsante **Sì**.  

        Viene visualizzato un messaggio con una barra di stato che riflette il consumo automatico. Questo è seguito da un messaggio di conferma che l'ordine è stato modificato per avere lo stato *Completato*. L'ordine di produzione finito ha lo stesso numero che aveva quando lo stato era *Rilasciato*.
    3. Scegli il pulsante **OK** per chiudere il messaggio di conferma.

8. Esamina di nuovo i movimenti contabili dell'articolo e della capacità per l'ordine di produzione.

    1. Scegli l'azione **Movimenti contabili capacità**.  

        Il movimento delle operazioni di imballaggio è stato completato nel momento in cui l'ordine è stato rilasciato. La quantità prodotta (output) è *5*, indipendentemente dall'output del passaggio precedente. Chiudi la pagina **Movimenti contabili capacità**.

    2. Scegli l'azione **Movimenti contabili articoli**.  

        La quantità nel movimento contabile articolo di tipo *Output* è uguale alla quantità di output nel movimento contabile della capacità. La quantità consumata di **SP-BOM1301, Alloggiamento AutoDrip**, e **SP-BOM1304, Caraffa termica acciaio inox** è 5 per entrambi perché l'output previsto e l'output effettivo sono uguali. 

    3. Chiudi la pagina **Movimenti contabili articoli**.  

Questo è tutto per la consuntivazione manuale e automatica dei componenti.

## Vedere anche

[Eseguire la consuntivazione dei componenti in base all'output dell'operazione](../../production-how-to-flush-components-according-to-operation-output.md)  
[Introduzione ai dati demo Contoso Coffee](contoso-coffee-manufacturing-intro.md)  

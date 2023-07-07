---
title: Impostare una nuova capacità
description: Procedura dettagliata per apprendere come impostare una nuova area di produzione con un calendario di capacità per un singolo turno in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-set-up-new-capacity"></a>Procedura dettagliata: Impostare una nuova capacità

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee per gestire la capacità.  

## <a name="scenario"></a>Scenario

Sei l'addetto alla pianificazione della produzione di Contoso Coffee. In risposta ai cambiamenti della produzione, è necessario impostare una nuova area di produzione, il Reparto test. La nuova area di produzione dispone di un centro di lavoro, Test. Le nuove aree devono avere un calendario di capienza per un unico turno dalle 08:00:00 alle 16:00:00, dal lunedì al venerdì.  

## <a name="steps"></a>Passaggi

1. Imposta l'area di produzione.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **aree di produzione**, quindi scegli il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Nr.** |700|
        |**Nome** |Reparto test|
        |**Cod. gruppo aree prod.** |1, Reparto produzione|
        |**Costo Diretto Unitario**|3,25|
        |**Calcolo costo unitario**|Ora|
        |**Metodo Consuntivazione Produz.**|Manuale|
        |**Cat. Reg. Articolo/Servizio**|NO IVA</br></br>Tieni presente che questa selezione dipende dall'impostazione della tua contabilità e dal tuo paese.|
        |**Cod. Unità di Misura** |MINUTI|
        |**Capacità** |1|
        |**Efficienza** |90|
        |**Cod. calendario reparto prod.** |1|

        Nel campo **Cod. calendario reparto prod.**, l'impostazione 1 indica un turno dal lunedì al venerdì.

    3. Chiudi la scheda dell'area di produzione.

2. Imposta il centro di lavoro.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **centri di lavoro**, quindi scegli il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Nr.** |760|
        |**Nome** |Test|
        |**Nr. area produzione** |700, Reparto test|
        |**Costo Diretto Unitario**|3,25|
        |**Metodo Consuntivazione Produz.**|Manuale|
        |**Cat. Reg. Articolo/Servizio**|NO IVA</br></br>Tieni presente che questa selezione dipende dall'impostazione della tua contabilità e dal tuo paese.|
        |**Capacità** |1|
        |**Efficienza** |90|
    3. Espandi la scheda dettaglio **Setup cicli** e quindi, nel campo **Tempo di setup** immetti *10*.  

3. Calcola il calendario della capacità del centro di lavoro.  

    1. Scegliere l'azione **Calendario**.  

    2. Nella pagina **Calendario centri lavoro** nella scheda dettaglio **Opzioni matrice** imposta il campo **Visualizza per** su *Mese*.  

    3. Scegliere l'azione **Mostra matrice**.  

    4. Nella pagina **Matrice calendario centri lavoro**, scegli l'azione **Calcola**.  

    5. Nella pagina **Calc. calendario centro lavoro** nella scheda dettaglio **Opzioni** imposta il campo **Data inizio** su *1° gennaio*.  

    6. Imposta il campo **Data fine** su 31 dicembre.  

    7. Nella Scheda dettaglio **Centro di lavoro** nel campo di filtro **Nr.** seleziona *760, Test*.  

    8. Scegli il pulsante **OK**. Al termine del processo batch, torna alla pagina **Matrice calendario centri lavoro**.  

    9. Scegliere l'azione **Aggiorna**.  

    10. Nella riga per il centro lavori 760, Test, esegui il drill-down del valore nella colonna di gennaio.  

Nella pagina **Movimenti calendario**, i movimenti di capacità giornaliera nel campo **Capacità (totale)** sono per 480 minuti. Ciò riflette un turno di otto ore per ogni giorno lavorativo. Inoltre il campo **Capacità (effettiva)** mostra 432 minuti. Ciò riflette il tasso di efficienza del 90% assegnato al centro di lavoro.  

## <a name="see-also"></a>Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  

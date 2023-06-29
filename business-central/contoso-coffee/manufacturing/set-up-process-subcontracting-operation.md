---
title: Impostare ed elaborare un'operazione di subappalto
description: Procedura dettagliata per apprendere come impostare ed elaborare un'operazione di subappalto in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="set-up-and-process-a-subcontracting-operation"></a><a name="set-up-and-process-a-subcontracting-operation"></a>Impostare ed elaborare un'operazione di subappalto

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee nel conto lavoro.

## <a name="scenario"></a><a name="scenario"></a>Scenario

Sei l'addetto alla pianificazione della produzione di Contoso Coffee. A causa di limiti di capacità, prevedi di utilizzare un subappaltatore per produrre l'articolo **SP-SCM1009, Airpot**.

Crei un nuovo ordine di produzione rilasciato per 12 unità dell'articolo SP-SCM1009, Airpot, utilizzando Routing - SP-SCM1009-SUB-2. Utilizza il foglio di lavoro conto lavoro per generare un ordine d'acquisto per la produzione, quindi completa l'operazione ricevendo e fatturando l'ordine d'acquisto.

## <a name="steps"></a><a name="steps"></a>Passaggi

1. Crea un nuovo ordine di produzione rilasciato per 12 unità dell'articolo SP-SCM1009, Airpot.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordine di produzione rilasciato**, quindi scegli il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Tipo Origine** |Articolo|
        |**Nr. Origine** |SP-SCM1009|
        |**Quantità** |100|
    3. Scegli l'azione **Aggiorna ordine produzione**.  

2. Sostituisci il ciclo in SP-SCM1009-SUB-2 nella riga dell'ordine di produzione, quindi aggiorna l'ordine di produzione ma solo per il ciclo.  

    1. Aggiungi il campo N. ciclo di produzione alle righe nell'ordine di produzione rilasciato.<!--in code, this is marked as visible=false-->

    2. Cambia il campo **Nr. ciclo** da *SP-SCM1009-SERIAL* a *SP-SCM1009-SUB-2*.  

    3. Scegli l'azione **Aggiorna ordine produzione**.  

    4. Nella pagina di richiesta **Aggiorna ordine di produzione** cancella i campi **Righe** e **Necessità componenti** in modo che l'attività venga eseguita solo per il ciclo quindi scegli il pulsante **Ok**.

3. Utilizza il foglio di lavoro conto lavoro per generare un ordine d'acquisto per l'operazione in conto lavoro nell'ordine di produzione creato nel passaggio 2.  

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **prospetto conto lavoro**, quindi scegli il collegamento correlato.  

    2. Scegli l'azione **Calcolo conto lavoro**.

    3. Seleziona il campo **Accetta messaggio azione** per la nuova riga.

    4. Scegliere l'azione **Esegui messaggi di azione**.  

    5. Nella pagina di richiesta **Approv. - Esegui mess. azioni**, accetta tutti i valori predefiniti, quindi scegli il pulsante **OK**.

    6. Al termine del lavoro batch, scegli il pulsante **ok** per chiudere il foglio di lavoro conto lavoro.  

4. Ricevi e fattura l'ordine di acquisto.  

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **ordini acquisto**, quindi scegli il collegamento correlato.  

    2. Nell'elenco **Ordini di acquisto** trova l'ordine di acquisto dal fornitore 82000 Subappaltatore.

    3. Nel campo **Nr. fatt. fornitore** immetti *542349*.

    4. Nella scheda dettaglio **Righe** seleziona la riga, quindi imposta il campo **Costo diretto** su *18*.

    5. Scegli l'azione **Registra**.  

    6. Nel messaggio di richiesta, scegli l'opzione **Ricevi e fattura**.  

L'output dell'articolo SP-SCM1009 Airpot è ora registrato.

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  

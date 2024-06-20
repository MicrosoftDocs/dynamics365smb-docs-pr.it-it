---
title: Utilizzare la pianificazione degli ordini per creare e prenotare la fornitura
description: Procedura dettagliata per apprendere come utilizzare la pianificazione degli ordini per creare l'ordine di produzione richiesto per la fornitura in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Procedura dettagliata: Utilizzare la pianificazione degli ordini per creare e prenotare la fornitura

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee nella pianificazione ordini.

## Scenario

Sei l'addetto alla pianificazione della produzione di Contoso Coffee. Hai creato un ordine di produzione per 100 unità dell'articolo **SP-SCM1009, Airpot** e vuoi pianificare i sottoassiemi per questo ordine. Utilizza la pianificazione degli ordini per creare l'ordine di produzione richiesto per la fornitura. Poiché si sta creando l'ordine di produzione per soddisfare i requisiti di un ordine specifico, decidi di prenotare l'output dell'ordine di produzione.  

## Passaggi

1. Crea il nuovo ordine di produzione rilasciato per 100 unità dell'articolo **SP-SCM1009, Airpot**.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordine di produzione rilasciato**, quindi scegli il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Tipo Origine** |Articolo|
        |**Nr. Origine** |SP-SCM1009|
        |**Quantità** |100|
    3. Scegli l'azione **Aggiorna ordine produzione**.  

    Nota il numero dell'ordine di produzione rilasciato.

2. Apri la pagina **Pianificazione ordini** e calcola un nuovo piano.

    1. Scegliere l'azione **Pianifica**.  

    2. Nella pagina **Pianificazione ordini** scegliere l'azione **Calcola piano**.  

    3. Scorri verso il basso fino alla riga della domanda che rappresenta l'ordine di produzione rilasciato che hai creato in precedenza.  

    4. Espandi le righe per visualizzare i dettagli della riga della domanda. Conferma che si tratta di un suggerimento per un ordine di produzione di 100 unità dell'articolo 1001.  

3. Crea un nuovo ordine di produzione per 100 unità di articolo **SP-BOM2000, Gruppo serbatoio** e prenota l'output di questo ordine di produzione per conto dell'ordine padre correlato.  

    1. Seleziona la casella di controllo nel campo **Prenota** nella riga della domanda per le 100 unità dell'articolo SP-BOM2000.

    2. Scegliere l'azione **Crea ordini**.  

    3. Imposta il campo **Effettua ordini per** su *La riga attiva*.  

    4. Imposta il campo **Crea ordine di produzione** su *Confermato*.

    5. Seleziona il pulsante **OK** per creare l'ordine di produzione.

    6. Nellapagina **Pianificazione ordini** verifica che la riga della domanda per le 100 unità dell'articolo 1001 sia stata rimossa.

Questo è tutto per la pianificazione degli ordini in [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  
[Informazioni sugli ordini di produzione](../../production-about-production-orders.md)  

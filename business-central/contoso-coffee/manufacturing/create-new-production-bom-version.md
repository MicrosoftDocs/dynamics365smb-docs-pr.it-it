---
title: Creare una nuova DBA di produzione e la versione DBA
description: Procedura dettagliata per aggiungere un'altra macchina per il caffè alla linea di prodotti di Contoso Coffee in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---
# Procedura dettagliata: Creare una nuova DBA di produzione e la versione DBA

In questo articolo vengono illustrati i passaggi per utilizzare i dati demo di Contoso Coffee per lavorare con le distinte base (DBA) nei processi di produzione.  

## Scenario

Contoso Coffee ha deciso di aggiungere un'altra caffettiera alla propria linea di prodotti: **SP-SCM1008 Airpot Lite**. Questa caffettiera è identica all'articolo esistente **SP-SCM1009 Airpot**, tranne per il fatto che non include la piastra riscaldante, **SP-BOM1104**. In un passaggio separato, la spia di accensione/spegnimento, **SP-BOM1106** viene rimossa per una versione della distinta base di Airpot Lite.

Oscar, l'ingegnere di processo di Contoso Coffee, deve impostare una nuova distinta base di produzione per definire i requisiti dei componenti iniziali per Airpot Lite. Oscar deve quindi impostare una nuova versione della distinta base, con una data di inizio del 01 luglio, per allinearsi a ulteriori piani sul rilascio di un'altra edizione.

## Passaggi

1. Crea una nuova distinta base di produzione per Airpot Lite.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **DB produzione**, quindi seleziona il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Nr.** |SP-SCM1008|
        |**descrizione** |Airpot Lite|
        |**Cod. Unità di Misura**|PZ  |

2. Copia i componenti dalla distinta base di produzione **SP-SCM1009**.

    1. Scegli l'azione **Copia distinta base**.

    2. Nella pagina **DBA di produzione** scegli la riga **SP-SCM1009, Airpot**, e quindi seleziona il pulsante **OK**.

3. Modifica i componenti per la nuova distinta base di produzione come descritto nello scenario.

    1. Nella Scheda dettaglio **Righe**, scegli la riga per l'articolo **SP-BOM1104** quindi scegli l'azione **Elimina riga**.  

4. Certifica la nuova distinta base.  

    1. Nel campo **Stato** seleziona *Certificato*.  

5. Crea una versione della distinta base di produzione per Airpot Lite.

    1. Scegli l'azione **Versioni**.

    2. Nella pagina **Lista versioni DB prod.** scegli l'azione **Nuovo** quindi compila i campi dei conti come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Cod. versione** |02|
        |**descrizione** |Airpot Lite, v2|
        |**Cod. Unità di Misura**|PZ  |  
        |**Data Inizio**|1 luglio  |  

6. Copia le righe componenti dalla distinta base di produzione nella nuova versione della distinta base.

    1. Scegli l'azione **Copia distinta base** quindi scegli il pulsante **sì** per copiare i componenti dalla distinta base di produzione originale.

7. Rimuovi l'articolo **SP-BOM1106, Luce accesa/spenta** dai componenti della versione.

8. Certifica la nuova versione della distinta base.

    1. Nel campo **Stato** seleziona *Certificato*.  

    2. Chiudere la versione della distinta base

La nuova caffettiera è ora configurata come distinta base di produzione con una versione.  

## Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  

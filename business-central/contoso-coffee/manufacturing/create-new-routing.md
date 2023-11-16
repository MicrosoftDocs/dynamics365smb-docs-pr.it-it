---
title: Creare un nuovo ciclo
description: Procedura dettagliata per informazioni su come immettere manualmente tutte le informazioni per un nuovo ciclo in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---
# <a name="walkthrough-create-a-new-routing"></a>Procedura dettagliata: Creare un nuovo ciclo

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee per configurare manualmente un nuovo ciclo di produzione in [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="scenario"></a>Scenario

Oscar, l'ingegnere di processo presso Contoso Coffee, decide di creare un nuovo ciclo con il nome *Nuovo percorso*. Poiché questo ciclo è diverso da qualsiasi altro ciclo in Contoso Coffee, Oscar deve immettere manualmente tutte le informazioni per il ciclo.  

## <a name="steps"></a>Passaggi

1. Crea l'intestazione del ciclo.  

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **cicli**, quindi scegli il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Nr.** |1099|
        |**descrizione** |Nuovo percorso|
2. Crea le righe ciclo.

    1. Nella Scheda dettaglio **Righe** aggiungi una nuova riga e compila i campi come descritto nella tabella riportata di seguito.  

        |Campo  |Valore  |
        |---------|---------|
        |**Nr. operazione** |10|
        |**Tipo** |Area di produzione|
        |**Nr.** |100|
        |**Tempo di setup** |20|
        |**Tempo lavorazione** |15|

    2. Aggiungi una nuova riga e compila i campi come descritto nella tabella riportata di seguito.  

        |Campo  |Valore  |
        |---------|---------|
        |**Nr. operazione** |20|
        |**Tipo** |Area di produzione|
        |**Nr.** |200|
        |**Tempo di setup** |30|
        |**Tempo lavorazione** |5|
3. Certificare il ciclo.

    1. Nel campo **Stato** seleziona *Certificato*.  

Il nuovo ciclo è ora impostato.  

## <a name="see-also"></a>Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  

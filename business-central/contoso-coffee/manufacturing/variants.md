---
title: Varianti
description: Procedura dettagliata per apprendere come aggiornare la previsione della domanda per ciascuna variante di un prodotto in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-variants"></a>Procedura dettagliata: varianti

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee per apprendere le varianti.

## <a name="scenario"></a>Scenario

Sei l'addetto alla pianificazione della produzione di Contoso Coffee. È necessario aggiornare la previsione della domanda per ciascuna variante dell'articolo SP-SCM1006, AutoDripLite. Poiché ha colori diversi, è necessario garantire che venga utilizzata la distinta base (DB) corretta per ciascuna variante. Esegui il prospetto pianificazione per calcolare l'offerta.  

## <a name="steps"></a>Passaggi

1. Imposta le unità di stockkeeping per l'articolo SP-SCM1006, AutoDripLite. Assegna una distinta base per SKU con le varianti ROSSO e BIANCO.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci *Articoli* e scegli il collegamento relativo.  

    2. Apri l'articolo **SP-SCM1006, AutoDripLite**.

    3. Scegliere l'azione **Crea unità di stockkeeping**.  

    4. Imposta il campo **Crea per** su *Ubicazione e variante*.

    5. Imposta un filtro per l'ubicazione su *PRINCIPALE*, quindi scegli il pulsante **OK**.

    6. Scegli l'azione **Unità di stockkeeping**.  

    7. Aggiorna le distinte base di produzione per le seguenti unità di stockkeeping:

        1. ROSSO su PRINCIPALE, imposta SP-SCM1006-ROSSO  

        2. BIANCO su PRINCIPALE, imposta SP-SCM1006-BIANCO  

        3. Mantieni il numero DB di produzione vuoto per NERO su PRINCIPALE  

2. Aggiorna il setup di produzione e rispetta le previsioni della domanda per ubicazioni e varianti.  

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti *setup manufacturing*, quindi scegli il collegamento correlato.  

    2. Attiva il campo **Usa previsioni per le ubicazioni**.

    3. Attiva il campo **Usa previsioni per le varianti**.

    4. Chiudi la finestra **Setup manufacturing**.

3. Crea una nuova previsione mensile della domanda, *AUTODRIP*. Filtra per articolo SP-SCM1006 e ubicazione PRINCIPALE. Imposta la domanda per maggio per ogni variante. 

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti *Previsione della domanda*, quindi seleziona il collegamento correlato.

    2. Crea una nuova previsione della domanda con il nome *AUTODRIP*.

    3. Scegli l'azione **Modifica previsione della domanda**.

    4. Nel campo **Visualizza per** seleziona *Mese*.

    5. Nel campo **Filtro articolo** scegli *SP-SCM1006*

    6. Attiva il campo **Usa previsioni per le ubicazioni**.

    7. Nel campo **Filtro ubicazione** seleziona *PRINCIPALE*

    8. Attiva il campo **Usa previsioni per le varianti**.

    9. Per ogni riga i valori aggiornati nella colonna di maggio

        1. ROSSO su PRINCIPALE, imposta 100

        2. BIANCO su PRINCIPALE, imposta 200

        3. NERO su PRINCIPALE, imposta 300

    10. Chiudere le finestre di previsione della domanda

4. Esegui il piano MPS a maggio per le previsioni della domanda creata. Esamina i componenti per vedere che la vernice dell'articolo è correlata alla variante.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti *prospetto pianificazione*, quindi scegli il collegamento correlato.

    2. Scegliere l'azione **Calcola piano - Rigenerativo**.

    3. Attiva il campo **MPS**.

    4. Disattiva il campo **MPS**.

    5. Nel campo **Data di inizio** seleziona *1 maggio*

    6. Nel campo **Data di fine** seleziona *31 maggio*

    7. Nel campo **Usa previsione** seleziona *AUTODRIP*

    8. Scegli l'azione **OK**.

    9. Per ogni riga creata, scegli l'azione **Componenti** e rivedi quale vernice viene utilizzata.  

## <a name="see-also"></a>Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  

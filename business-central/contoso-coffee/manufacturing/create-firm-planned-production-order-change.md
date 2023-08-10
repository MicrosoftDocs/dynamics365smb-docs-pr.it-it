---
title: Creare un ordine di produzione confermato e modificarlo
description: Procedura dettagliata per un addetto alla pianificazione di produzione presso Contoso Coffee che desidera creare un ordine di produzione pianificato fisso e quindi modificarlo.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Procedura dettagliata: Creare un ordine di produzione confermato e modificarlo

In questo articolo, ti guideremo attraverso i passaggi per utilizzare i dati demo di Contoso Coffee per utilizzare gli ordini di produzione.  

## <a name="scenario"></a>Scenario

Eduardo, l'addetto alla pianificazione di produzione di Contoso Coffee, deve creare un nuovo ordine di produzione per 10 unità dell'articolo **SP-SCM1009, Airpot** che deve essere pronto per il 28 aprile. Eduardo lo programma a ritroso e conferma che può iniziare l'ordine il 27 aprile.  

Poco dopo aver terminato questa attività, a Eduardo viene chiesto di aumentare l'ordine a 50 unità. Quando esegue questa operazione, la funzionalità di pianificazione a ritroso sposta la data di inizio dell'ordine troppo presto. Quindi Eduardo anticipa l'ordine dal 23 aprile al fine di determinare una data di fine più realistica.  

## <a name="steps"></a>Passaggi

1. Crea l'ordine di produzione iniziale per 10 unità dell'articolo **SP-SCM1009, Airpot**.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ord. produzione confermati**, quindi seleziona il collegamento correlato.  

    2. Scegliere l'azione **Nuovo**, quindi compilare i campi come descritto nella tabella che segue.  

        |Campo  |Valore  |
        |---------|---------|
        |**Tipo Origine** |Articolo|
        |**Nr. Origine** |SP-SCM1009|
        |**Quantità** |10|
        |**Data di scadenza**|Aprile 28  |

    3. Scegli l'azione **Aggiorna ordine produzione**.  

    4. Nella pagina **Aggiorna ordine di produzione**, accetta tutte le impostazioni predefinite, quindi scegli il pulsante **OK** per avviare il processo.  

        Nella configurazione corrente, questo processo utilizza la pianificazione a ritroso. Nella nuova riga dell'ordine di produzione, la data di inizio è il 26 aprile.  

2. Modifica la quantità dell'ordine di produzione su 50 unità e pianifica l'ordine.  

    1. Nella scheda dettaglio **Righe** della **Distinta base di produzione**, seleziona la riga aggiunta di recente, quindi, nel campo **Quantità** immetti *50*.  

3. Scegli l'azione **Aggiorna ordine produzione**.  

    La data di inizio è stata ora posticipata al 20 aprile. Questa non è una data accettabile per Eduardo.

4. Attiva una pianificazione anticipata dell'ordine di produzione.

    1. Nella scheda dettaglio **Programma** imposta il campo **Data di inizio** su *23 aprile*.

    L'inizio dell'ordine è ora il 25 aprile e la data di fine è il 2 maggio. La data di scadenza dell'ordine è fissata un giorno dopo, il 3 maggio. Eduardo ora sa che ci vorrà fino al 3 maggio per consegnare l'ordine aumentato.

> [!NOTE]
> La pianificazione di un ordine modificandone la data di inizio o fine non richiede il processo batch **Aggiorna ordine di produzione** perché tutte le date vengono ricalcolate automaticamente.

Il nuovo ordine di produzione è ora impostato e le esigenze di Eduardo sono soddisfatte.  

## <a name="see-also"></a>Vedere anche

[Introduzione ai dati demo Contoso Coffee](../contoso-coffee-intro.md)  

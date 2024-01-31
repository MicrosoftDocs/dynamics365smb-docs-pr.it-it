---
title: Ripianificare o aggiornare direttamente gli ordini di produzione
description: Questo argomento descrive le procedure per ripianificare gli ordini di produzione e aggiornare direttamente gli ordini di produzione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000842, 99000843, 99000861, 99000862, 99000863'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Ripianificare o aggiornare direttamente gli ordini di produzione

La funzione **Ripianifica** viene solitamente utilizzata negli ordini di produzione dopo l'aggiunta o la modifica di componenti che costituiscono ordini di produzione sottostanti. La funzione consente di calcolare le modifiche apportate alle righe componente e ciclo e include articoli disponibili nei livelli inferiori della distinta base di produzione per i quali potrebbero essere generati nuovi ordini di produzione.  

In base alle modifiche apportate alle righe componente e ciclo, la funzione Ripianifica consente di calcolare e di pianificare l'eventuale nuova domanda per l'ordine di produzione.  

La funzione **Aggiorna** viene in genere utilizzata negli ordini di produzione dopo aver eseguito una delle operazioni elencate di seguito:

- Creazione manuale di una testata dell'ordine di produzione, per calcolare e creare i dati della riga per la prima volta.
- Modifica della testata dell'ordine di produzione, per ricalcolare tutti i dati delle righe.

La funzione Aggiorna consente di calcolare le modifiche apportate alla testata di un ordine di produzione e non influisce sui livelli della distinta base di produzione. La funzione calcola e inizializza i valori delle righe componenti e delle righe ciclo sulla base dell'anagrafica definita nella distinta base di produzione e nel ciclo e in base alla quantità dell'ordine e alla data di scadenza specificata nella testata dell'ordine di produzione.

Le righe dell'ordine di produzione possono essere inserite manualmente oppure con la funzione che le calcola dalla testata.  

> [!NOTE]
> Utilizzando la funzione Aggiorna per ricalcolare le righe dell'ordine di produzione, le righe vecchie vengono eliminate e vengono calcolate le nuove righe.  

## Per ripianificare un ordine di produzione

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Ord. produzione confermati**, quindi seleziona il collegamento correlato.  
2. Aprire l'ordine di produzione da ripianificare.  
3. Nella Scheda dettaglio **Righe**, scegliere l'azione **Righe** e quindi l'azione **Componenti**.  
4. Aggiungere un componente che corrisponda a un articolo prodotto, ovvero un sottoassemblato.  
5. Nell'ordine di produzione scegliere l'azione **Ripianifica**.  

    Nella pagina **Ripianifica ordine produzione** specificare la modalità desiderata per la ripianificazione e gli elementi da ripianificare.  
6. Nel campo **Direzione programmazione** selezionare una delle seguenti opzioni.  

    | Opzione | Description |
    |--|--|
    | **Indietro** | Calcola la sequenza di operazioni a ritroso dalla prima data di fine disponibile, definita dalla data di scadenza e/o da altri ordini programmati, fino all'ultima data di inizio disponibile. **Nota:** questa opzione di default è appropriata per la maggior parte delle situazioni. |
    | **Da inizio ordine** | Calcola la sequenza di operazioni in avanti a partire dall'ultima data di inizio disponibile, definita dalla data di scadenza e/o da altri ordini programmati, fino alla prima data di fine disponibile. **Nota:** questa opzione è appropriata solo per ordini urgenti. |

7. Nel campo **Pianifica** specificare se calcolare i requisiti di produzione per gli articoli prodotti nella distinta base di produzione, nel modo seguente:  

    |Opzione|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nessun Livello**|Non prendere in considerazione la produzione nei livelli inferiori. Questa opzione consente di aggiornare solo la programmazione dell'articolo, in modo analogo all'aggiornamento.|  
    |**Un Livello**|Pianificare la domanda di produzione di primo livello. È possibile che vengano creati ordini di produzione di primo livello.|  
    |**Tutti i Livelli**|Pianificare la domanda di produzione di tutti i livelli. È possibile che vengano creati ordini di produzione di tutti i livelli.|  

8. Selezionare **Un livello** e fare clic su **OK** per ripianificare l'ordine di produzione e calcolare e creare un nuovo ordine di produzione sottostante per il sottoassemblato aggiunto, nel caso in cui non sia completamente disponibile.  

> [!NOTE]  
> Le modifiche apportate con la funzione **Ripianifica** comportano una variazione nella capacità necessaria per l'ordine di produzione e occorre quindi riprogrammare le operazioni dopo l'aggiornamento.  

## Per aggiornare un ordine di produzione

Se righe ciclo, componente o dell'ordine di produzione sono state corrette, è necessario procedere anche all'aggiornamento delle informazioni nell'ordine di produzione. Nella procedura che segue i componenti vengono calcolati per un ordine produzione confermato. I passaggi sono simili per le righe ciclo.

1. Scegli la ![lampadina che apre la funzione Dimmi 2](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Ord. produzione confermato**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Per ulteriori informazioni, vedere [Creare ordini di produzione](production-how-to-create-production-orders.md).  
3. Scegliere l'azione **Aggiorna**.
4. Nella pagina **Aggiorna ordine produzione**, selezionare una delle seguenti opzioni:

    |Campo|Opzione|Descrizione|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Direzione Programmazione**|**Da inizio ordine**|La programmazione inizia con la data di inizio e continua fino alla data di fine. È necessario compilare la data iniziale per utilizzare questa opzione.|  
    ||**Aut. fine**|La programmazione inizia con la data di fine e continua all'indietro fino alla data di inizio.|  
    |**Calcola**|**Righe**|Selezionare questo campo per calcolare le righe dell'ordine di produzione.|  
    ||**Cicli**|Il contenuto di questo campo non influenza il calcolo delle righe di produzione.|  
    ||**Componente Necessario**|Il contenuto di questo campo non influenza il calcolo delle righe di produzione.|  
    |**Warehouse**|**Crea Richiesta in Entrata**|Il contenuto di questo campo non influenza il calcolo delle righe di produzione.|  

5. Fare clic sul pulsante **OK** per confermare la selezione. Le righe dell'ordine di produzione vengono calcolate.

> [!NOTE]  
> Con il calcolo dei componenti dell'ordine di produzione vengono annullate le precedenti modifiche ai componenti.

## Vedi anche

[Pianif.](production-planning.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)   
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
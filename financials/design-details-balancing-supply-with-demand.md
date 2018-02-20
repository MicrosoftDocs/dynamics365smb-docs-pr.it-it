---
title: 'Dettagli di progettazione: Bilanciamento approvvigionamento con domanda | Microsoft Docs'
description: Il cuore del sistema di pianificazione implica il bilanciamento tra domanda e approvvigionamento per mezzo di azioni suggerite all'utente per riesaminare gli ordini di approvvigionamento nel caso di sbilanciamento. Questa operazione viene eseguita per combinazione di variante e ubicazione.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5020c048373f10e72e40f0c9b1e5a11fc45eedb5
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-balancing-supply-with-demand"></a>Dettagli di progettazione: Bilanciamento approvvigionamento con domanda
Il cuore del sistema di pianificazione implica il bilanciamento tra domanda e approvvigionamento per mezzo di azioni suggerite all'utente per riesaminare gli ordini di approvvigionamento nel caso di sbilanciamento. Questa operazione viene eseguita per combinazione di variante e ubicazione.  
  
Si immagini che ogni profilo di magazzino contenga una serie di eventi di domanda (ordinati per data e per priorità) e un numero corrispondente di eventi di approvvigionamento. Ogni evento si riferisce al suo tipo e identificativo di origine. Le regole per controbilanciare l'articolo sono chiare. Quattro istanze di domanda corrispondente e di approvvigionamento possono verificarsi in qualsiasi momento nel processo:  
  
1. Non esiste alcuna domanda o approvvigionamento per l'articolo => la pianificazione è terminata (o non deve iniziare).  
2. La domanda esiste ma non esiste un approvvigionamento => suggerire approvvigionamento.  
3. L'approvvigionamento esiste ma non esiste una domanda => approvvigionamento da annullare.  
4. Esistono sia la domanda che l'approvvigionamento => è necessario fare domande e fornire risposte affinché il sistema possa garantire che tale domanda venga soddisfatta e l'approvvigionamento sia sufficiente.  
  
     Se l'intervallo di approvvigionamento non è appropriato, è possibile riprogrammare l'approvvigionamento come segue:  
  
    1.  Se l'approvvigionamento viene inserito prima della domanda, è possibile riprogrammarlo in modo che il magazzino sia più basso possibile.  
    2.  Se l'approvvigionamento viene inserito successivamente alla domanda, è possibile riprogrammarlo. Altrimenti, il sistema suggerirà un nuovo approvvigionamento.  
    3.  Se l'approvvigionamento soddisfa la domanda alla data, il sistema di pianificazione può procedere a verificare se la quantità di approvvigionamento può coprire la domanda.  
  
     Una volta impostati i tempi, la quantità appropriata da fornire può essere calcolata come segue:  
  
    1.  Se la quantità di approvvigionamento è minore della domanda, è possibile che la quantità di approvvigionamento possa essere aumentata (o non aumentata se limitata da un metodo di quantità massima).  
    2.  Se la quantità di approvvigionamento è maggiore della domanda, è possibile che la quantità di approvvigionamento possa essere diminuita (o non diminuita se limitata da un metodo di quantità minima).  
  
     A questo punto, esiste una di queste due situazioni:  
  
    1.  La domanda corrente può essere coperta, nel qual caso può essere chiusa e si può procedere con la pianificazione della domanda successiva.  
    2.  L'approvvigionamento ha raggiunto il massimo, lasciando una certa quantità di domanda scoperta. In questo caso, il sistema di pianificazione può chiudere l'approvvigionamento corrente e procedere a quello successivo.  
  
 La procedura inizia dappertutto con la domanda successiva e l'approvvigionamento corrente o viceversa. L'approvvigionamento corrente potrebbe essere in grado di soddisfare anche la domanda successiva o la domanda corrente se non è stata ancora interamente coperta.  
  
## <a name="rules-concerning-actions-for-supply-events"></a>Regole concernenti azioni per gli eventi di approvvigionamento  
Quando il sistema di pianificazione esegue un calcolo dall'alto verso il basso in cui l'approvvigionamento deve soddisfare la domanda, la domanda viene considerata come un dato di fatto, vale a dire che rimane fuori dal controllo del sistema di pianificazione. Tuttavia, il lato dell'approvvigionamento può essere gestito. Di conseguenza, il sistema di pianificazione suggerirà la creazione di nuovi ordini di approvvigionamento, la ripianificazione di quelli esistenti e/o la modifica della quantità dell'ordine. Se un ordine di approvvigionamento esistente diventa superfluo, il sistema di pianificazione ne suggerirà l'annullamento all'utente.  
  
Se l'utente desidera escludere un ordine di approvvigionamento esistente dai suggerimenti di pianificazione, può dichiarare di non disporre di flessibilità di pianificazione (flessibilità pianificazione = nessuna). Quindi, l'approvvigionamento in eccesso da tale ordine verrà utilizzato per soddisfare la domanda, ma non verrà suggerita alcuna azione.  
  
In genere, tutti gli approvvigionamenti hanno una flessibilità di pianificazione che è limitata dalle condizioni di ciascuna delle azioni suggerite.  
  
-   **Riprogramma all'esterno**: la data di un ordine di approvvigionamento esistente può essere programmata per soddisfare la data di scadenza della domanda a meno che:  
  
    -   Rappresenta il magazzino (sempre nel giorno zero).  
    -   Contiene un metodo da ordine a ordine collegato a un'altra domanda.  
    -   Risiede al di fuori della finestra di ripianificazione definita dall'intervallo di tempo.  
    -   Esiste un approvvigionamento più recente che potrebbe essere utilizzato.  
    -   D'altro canto, l'utente potrebbe scegliere di non ripianificare per i seguenti motivi:  
    -   L'ordine di approvvigionamento è già stato associato a un'altra domanda in una data precedente.  
    -   La riprogrammazione necessaria è talmente minima che l'utente la trova trascurabile.  
  
-   **Riprogramma all'interno**: la data di un ordine di approvvigionamento esistente può essere programmata nel periodo, ad eccezione delle seguenti condizioni:  
  
    -   È collegata direttamente a un'altra domanda.  
    -   Risiede al di fuori della finestra di ripianificazione definita dall'intervallo di tempo.  
  
> [!NOTE]  
>  Nella pianificazione di un articolo tramite un punto di riordino, l'ordine di approvvigionamento può sempre essere riprogrammato all'interno, se necessario. Ciò è comune negli ordini di approvvigionamento programmati in avanti attivati da un punto di riordino.  
  
-   **Aumentare la quantità**: la quantità di un ordine di approvvigionamento esistente può essere aumentata per soddisfare la domanda a meno che l'ordine di approvvigionamento sia collegato direttamente a una domanda da un collegamento ordine a ordine.  
  
> [!NOTE]  
>  Anche se è possibile aumentare l'ordine di approvvigionamento, potrebbe essere limitato a causa di quantità massima ordine definita.  
  
-   **Riduci quantità**: un ordine di approvvigionamento esistente con un surplus rispetto a una domanda esistente può essere ridotto per soddisfare la domanda.  
  
> [!NOTE]  
>  Anche se la quantità può essere diminuita, può ancora esservi un certo surplus rispetto alla domanda a causa di una quantità minima di ordine definita o molteplicità ordine.  
  
-   **Annulla**: come incidente speciale dell'azione di riduzione quantità, l'ordine di approvvigionamento potrebbe essere annullato se è stato diminuito a zero.  
-   **Nuovo**: se non è presente alcun ordine di approvvigionamento già esistente o un ordine esistente non può essere modificato per soddisfare la quantità necessaria alla data di scadenza richiesta, verrà proposto un nuovo ordine di approvvigionamento.  
  
## <a name="determining-the-supply-quantity"></a>Determinazione della quantità di approvvigionamento  
I parametri di pianificazione definiti dall'utente controllano la quantità suggerita di ogni ordine di approvvigionamento.  
  
Quando il sistema di pianificazione calcola la quantità di nuovo ordine di approvvigionamento o la modifica della quantità in un ordine esistente, la quantità suggerita può essere diversa dalla quantità effettivamente richiesta.  
  
Se è selezionata una quantità massima di magazzino o una quantità di ordine fissa, la quantità suggerita può essere aumentata per soddisfare la quantità fissa o la giacenza massima. Se un metodo di riordino utilizza un punto di riordino, la quantità può essere aumentata almeno per soddisfare il punto di riordino.  
  
 La quantità suggerita può essere modificata nella sequenza:  
  
1. Eseguire il drill-down alla quantità di ordine massima (se esistente).  
2. Fino alla quantità minima ordine.  
3. Fino a soddisfare la molteplicità di ordini più vicina. (Nel caso di impostazioni errate, questo potrebbe violare le quantità di ordine massima).  
  
## <a name="order-tracking-links-during-planning"></a>Collegamenti della tracciabilità ordini durante la pianificazione  
Nel caso di tracciabilità dell'ordine durante la pianificazione, è importante ricordare che il sistema di pianificazione ridispone i collegamenti di tracciabilità ordine creati in modo dinamico per le combinazioni articolo/variante/ubicazione.  
  
Questo avviene per due motivi:  
  
-   Il sistema di pianificazione deve essere in grado di giustificare i suggerimenti che fornisce; che tutta la domanda sia stata coperta e che non esistano ordini di approvvigionamento superflui.  
-   I collegamenti di tracciabilità ordine creati in modo dinamico devono essere ribilanciati regolarmente.  
  
Nel tempo, i collegamenti di tracciabilità ordini dinamici finiscono per non quadrare poiché l'intera rete di tracciabilità ordini non viene ridisposta fino a quando un evento di approvvigionamento o di domanda non viene effettivamente chiuso.  
  
Prima di bilanciare l'approvvigionamento con la domanda, il programma elimina tutti i collegamenti di tracciabilità ordine esistenti. Quindi durante la procedura di bilanciamento, quando viene chiuso un evento di approvvigionamento o di domanda, il programma stabilisce nuovi collegamenti di tracciabilità ordine tra la domanda e l'approvvigionamento.  
  
> [!NOTE]  
>  Anche se l'articolo non è impostato per la tracciabilità dinamica dell'ordine, il sistema pianificato creerà collegamenti di tracciabilità ordine come di seguito illustrato.  
  
## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Bilanciamento domanda e approvvigionamento](design-details-balancing-demand-and-supply.md)   
[Dettagli di progettazione: Concetti centrali del sistema di pianificazione](design-details-central-concepts-of-the-planning-system.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)

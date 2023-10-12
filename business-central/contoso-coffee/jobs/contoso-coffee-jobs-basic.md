---
title: Procedura dettagliata di commesse di base
description: Questo articolo ti guida attraverso diversi processi fondamentali di gestione dei progetti.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---
# <a name="walkthrough-of-basic-jobs"></a>Procedura dettagliata di commesse di base

Questa procedura dettagliata illustra diversi processi principali:

- Aggiunta di task commessa a commesse
- Registrazione del tempo e delle spese materiali per una commessa
- Fatturazione di una commessa

## <a name="adding-a-job-task-to-a-job"></a>Aggiunta di una task commessa a una commessa

### <a name="scenario"></a>Scenario

Simon, il project manager, vuole registrare il tempo dedicato alla formazione del cliente sull'uso di una macchina per caffè espresso in una task distinta nella commessa per l'installazione di una macchina commerciale in loco.

### <a name="steps"></a>Passaggi

1. Crea la task commessa  

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commesse**, quindi scegli il collegamento correlato.  
    2. Seleziona la commessa *J00010*.
    3. Nell'area **Task**, scegli l'azione **Nuova riga**.  Immetti i valori seguenti:
 
    |Nr. task commessa|Descrizione|Tipo task commessa|
    |------------|-----------|-------------|  
    |220|Formazione del cliente|Registrazione|

2. Indenta le task commessa
   1. Nell'area Task, individua l'azione **Indenta task commesse**
   2. Conferma di voler indentare le task selezionando **Sì**.

### <a name="results"></a>Risultati

 - Ora puoi registrare tempi e spese nella nuova task commessa

## <a name="record-time-and-material-expenses-to-a-job"></a>Registrare tempo e spese materiali per una commessa

### <a name="scenario-1"></a>Scenario

Edgin, il tecnico che installa la macchina, deve registrare il tempo impiegato e i materiali utilizzati durante l'installazione della commessa per la fatturazione.  Ha già aggiunto il viaggio e i materiali e ora deve aggiungere il tempo per formare il personale all'uso della macchina.

### <a name="steps-1"></a>Passaggi

1. Crea righe di registrazioni commesse aggiuntive

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni commesse**, quindi scegli il collegamento correlato.  
    2. Seleziona il batch *CONTOSO*.  Vedrai diverse righe di tipi di risorse e di articoli, che riflettono il tempo (per il tecnico e il veicolo) e i materiali (la macchina e le forniture) utilizzati.
    3. Creare una nuova riga. Immetti i valori seguenti:
 
    |Nr. processo|Nr. task commessa|Tipo|Nr.|Descrizione|Quantità|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Risorsa|EDGIN|Formazione del cliente|1|

2. Registra il tempo e le spese
   1. Scegli l'azione **Registra**
   2. Conferma di voler registrare le righe selezionando **Sì**.

### <a name="results-1"></a>Risultati

 - Verranno creati movimenti contabili commesse e movimenti contabili risorse di tipo *Utilizzo*
 - Verranno creati movimenti contabili articoli per rettificare negativamente l'inventario
 - Nella scheda commessa, i costi e i prezzi nell'area Task rifletteranno i nuovi saldi in attesa di fatturazione
 - Nella scheda commessa, la casella Dettagli commessa rifletterà i totali dei prezzi

## <a name="creating-a-sales-invoice-for-a-job"></a>Creazione di una fattura di vendita per una commessa

### <a name="scenario-2"></a>Scenario
Simon deve creare e registrare una fattura da inviare al cliente con il tempo e le spese relativi alla commessa.

### <a name="steps-2"></a>Passaggi
1. Crea la fattura di vendita

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commesse**, quindi scegli il collegamento correlato.  
    2. Nell'elenco delle commesse, scegli l'azione **Crea fattura vendita per commessa**.
    3. Imposta il filtro **Nr. commessa** su *J00010*.
    4. Scegli **OK** per generare la fattura di vendita.  Riceverai una conferma di quante fatture vengono generate

2. Registra la fattura del tempo e delle spese
   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.  
   2. Seleziona l'ultima fattura per aprirla per la revisione.
   3. Scegli l'azione **Registra**.

### <a name="results-2"></a>Risultati

 - Verranno creati movimenti contabili commesse e movimenti contabili risorse di tipo *Vendita*
 - Nella scheda commessa, i costi e i prezzi nell'area Task rifletteranno i nuovi saldi fatturati
 - Nella scheda commessa, la casella Dettagli commessa rifletterà i totali dei prezzi nella sezione Prezzo fatturato

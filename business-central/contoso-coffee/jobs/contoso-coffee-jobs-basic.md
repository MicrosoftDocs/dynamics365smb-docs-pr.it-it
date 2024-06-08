---
title: Procedura dettagliata di commesse di base
description: Questo articolo ti guida attraverso diversi processi fondamentali di gestione dei progetti.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-of-basic-jobs"></a>Procedura dettagliata di commesse di base

Questa procedura dettagliata illustra diversi processi principali:

- Aggiungere attività di progetto a progetti
- Registrare spese per tempo e materiali per un progetto
- Fatturare un progetto

## <a name="adding-a-project-task"></a>Aggiunta di un'attività di progetto

### <a name="scenario"></a>Scenario

Simon, il project manager, vuole che venga registrato il tempo speso a insegnare al cliente come utilizzare la macchina per caffè espresso. Simon vuole utilizzare un'attività separata nel processo per installare una macchina commerciale in loco.

### <a name="steps"></a>Passaggi

1. Crea l'attività di progetto.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
    2. Seleziona la commessa *J00010*.
    3. Nell'area **Attività**, scegli l'azione **Nuova riga** e quindi inserisci i seguenti valori:
 
    |Nr. attività di progetto|Descrizione|Tipo di attività di progetto|
    |------------|-----------|-------------|  
    |220|Formazione del cliente|Registrazione|

2. Indenta le attività di progetto.
   1. Nell'area Attività, individua l'azione **Indenta attività di progetto**.
   2. Conferma che vuoi indentare le attività selezionando **Sì**.

### <a name="results"></a>Risultati

 - Ora puoi registrare tempi e spese nella nuova attività di progetto

## <a name="record-time-and-material-expenses-to-a-project"></a>Registrare spese per tempo e materiali per un progetto

### <a name="scenario-1"></a>Scenario

Edgin, il tecnico che installa la macchina, deve registrare il tempo impiegato e i materiali utilizzati durante l'installazione della commessa per la fatturazione. Edgin ha già aggiunto il viaggio e i materiali e ora deve aggiungere il tempo per formare il personale all'uso della macchina.

### <a name="steps-1"></a>Passaggi

1. Crea le righe di registrazione progetto supplementari.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
    2. Seleziona il batch *CONTOSO*. Sono visualizzate diverse righe di tipi di risorse e di articoli, che riflettono il tempo (per il tecnico e il veicolo) e i materiali (la macchina e le forniture) utilizzati.
    3. Crea una nuova riga, quindi inserisci i seguenti valori:
 
    |Nr. progetto|Nr. attività di progetto|Tipo|Nr.|Descrizione|Quantità|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Risorsa|EDGIN|Formazione del cliente|1|

2. Registra il tempo e le spese.
   1. Scegli l'azione **Registra**.
   2. Conferma di voler registrare le righe selezionando **Sì**.

### <a name="results-1"></a>Risultati

- Vengono creati movimenti contabili progetto e movimenti contabili risorse di tipo *Utilizzo*.
- Vengono creati movimenti contabili articoli per rettificare negativamente l'inventario.
- Nella scheda progetto, i costi e i prezzi nell'area Attività riflettono i nuovi saldi in attesa di fatturazione
- Nella scheda progetto, il riquadro Dettagli progetto riflette i totali dei prezzi.

## <a name="creating-a-sales-invoice-for-a-project"></a>Creazione di una fattura di vendita per un progetto

### <a name="scenario-2"></a>Scenario

Simon deve creare e registrare una fattura da inviare al cliente con il tempo e le spese relativi al progetto.

### <a name="steps-2"></a>Passaggi

1. Crea la fattura di vendita.

    1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.  
    2. Nell'elenco delle commesse, scegli l'azione **Crea fattura di vendita progetto**.
    3. Imposta il filtro **Nr. progetto** su *J00010*.
    4. Scegli **OK** per generare la fattura di vendita. Ricevi una conferma di quante fatture vengono generate.

2. Registra la fattura del tempo e delle spese.

   1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture vendite**, quindi seleziona il collegamento correlato.  
   2. Seleziona l'ultima fattura per aprirla per la revisione.
   3. Scegli l'azione **Registra**.

### <a name="results-2"></a>Risultati

- Vengono creati movimenti contabili progetto e movimenti contabili risorse di tipo *Vendita*.
- Nella scheda progetto, i costi e i prezzi nell'area Attività riflettono i nuovi saldi fatturati
- Nella scheda progetto, la casella Dettagli progetto riflette i totali dei prezzi nella sezione Prezzo fatturato.

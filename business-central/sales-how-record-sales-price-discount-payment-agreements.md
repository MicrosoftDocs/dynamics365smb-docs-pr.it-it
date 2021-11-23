---
title: Impostare prezzi di vendita e sconti per i clienti | Microsoft Docs
description: Descrive come impostare e applicare accordi sui prezzi e sugli sconti per i documenti di vendita.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8b7943caba8482e39217307be904f368f0ec31c0
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752432"
---
# <a name="record-sales-prices-and-discounts"></a>Registrare i prezzi di vendita e gli sconti
> [!NOTE]
> Nel secondo ciclo di rilascio del 2020 abbiamo rilasciato processi semplificati per l'impostazione e la gestione di prezzi e sconti. I nuovi clienti che utilizzano questa versione, trarranno vantaggio dalla nuova esperienza. Per i clienti esistenti, l'utilizzo della nuova esperienza dipende da se l'amministratore ha o meno abilitato l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] supporta varie strategie di prezzo, che vanno da modelli a prezzo unico in cui un articolo viene venduto sempre allo stesso prezzo, ad accordi sui prezzi speciali con clienti specifici, gruppi di clienti o offerte speciali quando si effettua una campagna di vendita. Ad esempio, potresti offrire un prezzo speciale su un ordine di vendita alle seguenti condizioni:

* Quando è per una quantità minima
* È per un certo tipo di articolo  
* Se è creato durante un periodo di tempo specifico

Per utilizzare un modello di prezzo di base, è sufficiente specificare un prezzo unitario per un articolo o una risorsa. Tale prezzo sarà sempre utilizzato sui documenti di vendita. Per i modelli più avanzati, ad esempio, quando stai eseguendo una campagna di vendita e desideri offrire prezzi speciali, puoi specificare i criteri nella pagina **Prezzi di vendita**. Puoi offrire prezzi speciali basati su combinazioni di quanto segue: 

* Cliente
* Articolo
* Unità di misura
* Quantità minima
* Intervalli di date che definiscono quando i prezzi sono validi

Inoltre, dopo aver impostato i prezzi speciali, [!INCLUDE[prod_short](includes/prod_short.md)] può calcolare automaticamente il miglior prezzo sui documenti di vendita e acquisto e sulle righe di registrazione commessa e articolo. Per ulteriori informazioni, vedere [Calcolo del prezzo migliore](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

Nel caso degli sconti, è possibile impostare e utilizzare i seguenti tipi:

| Tipo di sconto: | Descrizione |
| --- | --- |
| **Sconto Riga Vendita** |È possibile fare in modo che venga usato uno sconto sull'importo nelle righe di vendita quando si verifica una determinata combinazione di cliente, articolo, quantità minima, unità di misura o data di inizio o di fine. Queste combinazioni funzionano come per i prezzi di vendita. |
| **Sconto fattura** |Una percentuale di sconto che viene sottratta dal totale nei documenti di vendita se la somma di tutte le righe di un documento supera un determinato valore minimo. |

> [!TIP]  
> Se un articolo non dovrà mai essere venduto a un prezzo scontato, lasciare vuoti i campi relativi allo sconto nella pagina dell'articolo e non includere l'articolo in alcuna impostazione di sconto riga.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Per impostare un prezzo di vendita per un cliente

Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente. 

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Prezzi**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà un prezzo di vendita speciale al cliente.

---

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)  
Per default, lo stato dei nuovi listini prezzi è Bozza. I listini prezzi in bozza non sono inclusi nel calcolo dei prezzi. Quando hai finito di aggiungere righe e desideri iniziare a usare i prezzi puoi modificare lo stato in Attivo.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Clienti**, quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Listini prezzi di vendita**. 
3. Scegliere **Nuovo** per creare un nuovo listino prezzi di vendita.
4. Nelle Schede dettaglio **Generale** e **Imposta** compilare i campi appropriati. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Esistono due modi per aggiungere gli articoli nell'elenco:
   * Per aggiungere molti articoli, scegliere **Suggerisci righe** e quindi immettere i criteri di filtro per specificare i tipi di articolo da aggiungere. Facoltativamente, è possibile inserire altre impostazioni per gli articoli. Queste impostazioni sono specifiche del listino prezzi. Se necessario, è possibile apportare le modifiche in un secondo momento.
   * Per copiare articoli da un altro listino prezzi, scegliere **Copia righe**, quindi scegliere il listino prezzi da copiare.
   * Per aggiungere articoli manualmente, nel campo **Tipo prodotto** in una riga seleziona il tipo di prodotto a cui si riferisce il listino prezzi. In base alla selezione, compilare i restanti campi in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Per iniziare a utilizzare il listino prezzi, nel campo **Stato** scegliere **Attivo**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Utilizzo dei listini prezzi di vendita e di acquisto
> [!NOTE]
> L'utilizzo dei listini prezzi richiede che l'amministratore abbia abilitato la funzionalità **Nuova esperienza prezzo di vendita** in **Gestione funzionalità**. Per ulteriori informazioni, vedere [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

I campi **Collega a - Tipo** e **Collega a - Nr.** consentono di scegliere a cosa collegare il listino prezzi, ad esempio al cliente o al gruppo prezzi cliente. Usa il campo **Visualizza colonne per** per mostrare le colonne rilevanti per i prezzi e gli sconti oppure per i prezzi o gli sconti.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Conversione dei prezzi esistenti quando si attiva l'aggiornamento della funzionalità dei prezzi
Quando abiliti l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita** nella pagina **Gestione funzionalità** si apre la guida **Aggiornamento dati funzionalità**. Utilizza l'interruttore **Usa prezzi predefiniti** come segue:

* Se vuoi lavorare con tutti i prezzi su un'unica pagina, attivalo. I prezzi esistenti vengono convertiti in un listino prezzi predefinito per ciascuno dei seguenti:

    * Vendite
    * Acquisti
    * Ricavi commesse
    * Acquisti commesse 

    Successivamente, puoi modificare tutti i prezzi per queste aree nella pagina **Foglio di lavoro prezzi**. I listini prezzi predefiniti sono impostati nelle pagine **Setup contabilità clienti**, **Setup contabilità fornitori** e **Setup commesse**. 

    > [!NOTE]
    > Se i prezzi sono impostati solo su schede articolo o risorsa, i listini prezzi predefiniti non verranno compilati con tali prezzi durante l'aggiornamento dei dati. Tuttavia, puoi aprire uno qualsiasi dei listini prezzi predefiniti o la pagina Foglio di lavoro prezzi e utilizzare l'azione **Suggerisci righe** per aggiungere i prezzi impostati sulle schede articolo o risorsa. 

* Per utilizzare i listini prezzi di vendita, disattivala. I prezzi esistenti verranno convertiti in un nuovo listino prezzi per ogni combinazione di cliente, gruppo di clienti o campagna e le date di inizio e fine e le valute. Se hai molte combinazioni, avrai molti listini prezzi.

Se hai già abilitato la Nuova esperienza prezzi, puoi creare listini prezzi predefiniti manualmente o specificare un listino prezzi esistente come predefinito. Per impostare un listino prezzi esistente come predefinito, attiva l'interruttore **Consenti aggiornamento impostazioni predefinite** per il listino prezzi. Quindi nelle pagine **Setup contabilità clienti**, **Setup contabilità fornitori** o **Setup commesse** imposta il listino prezzi come predefinito.

### <a name="editing-active-price-lists"></a>Modifica dei listini prezzi attivi
Per consentire alle persone di modificare i prezzi sui listini prezzi attivi per articoli, risorse, clienti, fornitori o altre entità che utilizzano i prezzi, attiva l'interruttore **Consenti modifica prezzo attivo** nelle pagine **Setup contabilità clienti** e **Setup contabilità fornitori**. 

Quando l'interruttore **Consenti modifica prezzo attivo** è disattivato, per aggiornare i prezzi in un listino prezzi è necessario modificare lo stato del listino prezzi in **Bozza**, apportare la modifica, quindi riattivare il listino.

La pagina **Panoramica dei prezzi** fornisce una panoramica di tutti i prezzi nei listini prezzi. È possibile impostare filtri per limitare l'elenco. Dopo aver modificato i prezzi, è necessario utilizzare l'azione **Verifica righe** per verificare i prezzi rispetto ad altre righe del listino prezzi. Ad esempio, la verifica dei prezzi aiuta a evitare prezzi duplicati o in conflitto. 

> [!NOTE]
> Quando modifichi una riga in un listino prezzi attivo, lo stato della riga diventa Bozza e la riga non verrà inclusa nei calcoli dei prezzi finché non utilizzi l'azione **Verifica righe**. Dopo aver verificato il prezzo, lo stato della riga diventa Attivo e verrà utilizzato nei calcoli del prezzo.

Per aggiungere nuovi prezzi, nella pagina **Panoramica dei prezzi** usa l'azione **Aggiungi nuove righe**. La pagina **Foglio di lavoro prezzi** si apre in cui aggiungi le righe di prezzo nei seguenti modi:

* Suggerendole in base a criteri
* Copiandole da altri listini prezzi
* Inserendole manualmente. 

Successivamente, puoi utilizzare l'azione **Implementare variazione prezzi** per confrontare i nuovi prezzi con altri listini per evitare duplicati.

## <a name="to-copy-sales-prices"></a>Per copiare prezzi di vendita
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente.

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)  

Se si desidera copiare prezzi di vendita, ad esempio i prezzi di vendita di un singolo cliente per poterli utilizzare per un gruppo prezzi cliente, eseguire il processo batch **Suggerisci prezzo vendita in prosp.** nella pagina **Prospetto Prezzi Vendita**.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto prezzi vendita**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo vendita in prosp.** .  
3. Nella Scheda dettaglio **Prezzi vendita** immettere i prezzi di vendita originali che si desidera copiare nei campi **Tipo vendita** e **Codice vendita**.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.  
5. Per creare nuovi prezzi mediante il processo batch, selezionare la casella di controllo **Crea nuovi prezzi**.  
6. Selezionare il pulsante **OK** per inserire automaticamente i nuovi prezzi suggeriti nelle righe della pagina **Prospetto prezzi vendita**, indicando che sono validi per il tipo vendita selezionato.  

   > [!NOTE]  
   > Il processo batch fornisce soltanto suggerimenti e non consente di implementare le variazioni consigliate. Se i suggerimenti vengono ritenuti soddisfacenti e si desidera implementarli, vale a dire inserirli nella pagina **Prezzo vendita**, scegliere l'azione **Implementare variazione prezzi** nella pagina **Prospetto prezzi vendita**.

---

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Listini prezzi di vendita**, quindi seleziona il collegamento correlato. 
2. Scegliere il listino prezzi da copiare e quindi scegliere **Copia righe**.
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  
  
---

## <a name="to-bulk-update-item-prices"></a>Per aggiornare in blocco i prezzi degli articoli
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente.

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)

Puoi compilare il **Prospetto Prezzi Vendita** per aggiornare in blocco i prezzi degli articoli, come aumentare tutti i prezzi di una determinata percentuale usando il seguente processo:

* **Suggerisci prezzo articolo in prosp.** suggerisce modifiche applicando un fattore di rettifica ai prezzi di vendita esistenti o copiando gli accordi sui prezzi di vendita esistenti in altri clienti, gruppi di prezzi di clienti o campagne di vendita.
* **Suggerisci prezzo articolo in prosp.** suggerisce modifiche applicando un fattore di rettifica ai prezzi unitari esistenti nelle schede articolo o suggerendo prezzi per nuove combinazioni di valuta, unità di misura e così via. I prezzi unitari degli articoli non vengono modificati.    

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prospetto prezzi vendita**, quindi seleziona il collegamento correlato.  
2. Scegliere l'azione **Suggerisci prezzo articolo in prosp.** .  
3. Nella Scheda dettaglio **Articolo**, riempire il campo **Nr.** o **Categoria registrazione magazzino** o altri campi con i prezzi degli articoli originali che si desidera aggiornare.  
4. Nella sezione superiore della pagina di richiesta compilare i campi **Tipo vendita** e **Codice vendita** con il tipo e il nome con cui si desidera copiare i prezzi di vendita.
5. Se vuoi che il processo batch rettifichi automaticamente i prezzi degli articoli suggeriti, immetti la rettifica nel campo **Fattore Rettifica**. Ad esempio, immetti **1,15** in **Fattore Rettifica** per aumentare del **15%** il prezzo dell'articolo.  
6. Per creare nuovi prezzi mediante il processo batch, attiva l'interruttore **Crea nuovi prezzi**.  
7. Scegli **OK** per compilare le righe nella pagina **Foglio di lavoro prezzi di vendita** con i nuovi prezzi suggeriti.
8. Per implementare i suggerimenti, utilizza l'azione **Implementare variazione prezzi**. Il processo batch crea suggerimenti ma non li implementa.

---

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)

Per aggiornare i prezzi per più articoli, è necessario creare un nuovo listino prezzi e quindi copiare le righe da un listino prezzi esistente. Quando si copiano le righe, è anche possibile utilizzare i filtri per specificare cosa copiare, nonché specificare un numero intero o decimale nel campo **Fattore rettifica** per aumentare o ridurre i prezzi. Il listino prezzi deve essere nello stato **Bozza**. Se necessario, è possibile quindi disattivare il vecchio listino prezzi.

> [!NOTE]
> Non possono esistere due righe con le stesse impostazioni, ma prezzi differenti. In tal caso, verrà visualizzato un messaggio quando si attiva un listino prezzi. È possibile scegliere il prezzo da utilizzare aprendo il listino ed eliminando il prezzo errato.  

## <a name="sales-invoice-discounts-and-service-charges"></a>Sconti fattura di vendita e Addebito assistenza
Quando usi gli sconti fattura, l'importo totale in fattura determina lo sconto applicato. Nella pagina **Sconti fattura clienti** è inoltre possibile aggiungere un addebito di assistenza a fatture che superano un certo importo.  

Se vuoi calcolare automaticamente gli sconti fattura, nella pagina **Setup contabilità clienti** attiva l'interruttore **Calcola sconto fatt.**.  

Per ogni cliente, puoi specificare se offrire sconti in fattura se i criteri sono soddisfatti. Ad esempio, se l'importo della fattura è sufficientemente elevato. Si possono definire le condizioni per gli sconti fattura in valuta locale per i clienti nazionali e in valuta estera per i clienti esteri.  

Per collegare le percentuali di sconto a importi di fatturazione specifici, utilizzare la pagina **Sconti fattura clienti** di ogni cliente. È possibile immettere un numero qualsiasi di percentuali. A ogni cliente è possibile associare una propria pagina oppure è possibile collegare più clienti alla stessa pagina.  

Oltre a oppure invece di una percentuale di sconto, è possibile collegare l'importo di un addebito di assistenza a un importo della fattura specifico.  

Per informazioni sugli sconti per le vendite, vedere [Impostare gli sconti per i clienti](/learn/modules/customer-discounts-dynamics-365-business-central/index) in Microsoft Learn.  

---

### <a name="calculating-invoice-discounts-on-sales"></a>Calcolo degli sconti fattura per le vendite

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Per impostare uno sconto riga vendita per un cliente
Questi passaggi differiscono a seconda se l'amministratore ha attivato o meno l'aggiornamento della funzionalità **Nuova esperienza prezzo di vendita**. Se l'aggiornamento delle funzionalità non è attivato, segui i passaggi nella scheda Esperienza corrente.

#### <a name="current-experience"></a>[Esperienza corrente](#tab/current-experience/)  

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda cliente interessata e scegliere l'azione **Sconti riga**.
3. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Compilare una riga per ogni combinazione che concederà uno sconto riga vendita al cliente.

> [!Note]
> Quando si aprono le pagine **Prezzi vendita** e **Sconti riga vendita** di un cliente specifico, i campi **Filtro tipo vendita** e **Filtro codice vendita** sono impostati per il cliente e non possono essere modificati né rimossi.
>
> Per impostare i prezzi o gli sconti riga per tutti i clienti, un gruppo di prezzi dei clienti o una campagna, è necessario aprire le pagine da una scheda articolo. In alternativa, per i prezzi di vendita, utilizzare la pagina **Prospetto Prezzi Vendita**. Per ulteriori informazioni, vedere [Per aggiornare in blocco i prezzi degli articoli](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

---

#### <a name="new-experience"></a>[Nuova esperienza](#tab/new-experience/)  

1. Scegli la ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Clienti** e quindi scegli il collegamento correlato.
2. Scegli il cliente, quindi l'azione **Listini prezzi di vendita**.
3. Aprire il listino prezzi per il quale specificare lo sconto riga.
4. Creare una nuova riga o scegliere una riga esistente, quindi compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Nel campo **Definisce** scegliere **Prezzo e sconto** o solo **Sconto**. 
6. Nel campo **% sconto riga** specificare la percentuale di sconto.

    > [!TIP]
    > Puoi filtrare le righe scegliendo l'opzione appropriata nel campo **Visualizza colonne per**.
    > [!NOTE]  
    > I codici sconto fattura sono rappresentati da schede clienti esistenti. Usando i nomi cliente come codice ti consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni. Per impostare le condizioni di sconto fattura specifiche del cliente, impostare il campo **Codice sconto fattura** sul codice cliente del cliente, quindi procedere al passaggio successivo.
---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Per impostare uno sconto fattura per un cliente
Dopo avere stabilito a quali clienti si debbano applicare gli sconti fattura, è necessario immettere i codici di sconto fattura nelle schede clienti e impostare le condizioni relative ai singoli codici.

1. Scegli la ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Clienti** e quindi scegli il collegamento correlato.
2. Aprire la pagina relativa al cliente al quale saranno applicati gli sconti fattura.
3. Nel campo **Cod. sconto fatt.** selezionare un codice per le condizioni di sconto fattura in questione che verrà utilizzato per calcolare gli sconti fattura per il cliente. 

> [!NOTE]  
> I codici sconto fattura sono rappresentati da schede clienti esistenti. Usando i nomi cliente come codice ti consente di assegnare rapidamente le condizioni dello sconto fattura ai clienti perché basterà selezionare il nome di un altro cliente che avrà le stesse condizioni.

Ora imposta le condizioni dello sconto fattura di vendita.

1. Nella pagina **Clienti** scegliere l'azione **Sconti fattura**. Verrà visualizzata la pagina **Sconti fattura clienti**.
2. Nel campo **Codice valuta** immettere il codice per una valuta alla quale sono collegate le condizioni dello sconto fattura nella riga. Lasciare il campo vuoto se si desidera impostare le condizioni di sconto fattura in valuta locale.
3. Nel campo **Importo minimo** immettere l'importo minimo che una fattura deve avere affinché le possa essere applicato lo sconto.
4. Nel campo **% sconto** immettere lo sconto fattura sotto forma di percentuale dell'importo fattura.
5. Ripetere i passaggi da 5 a 7 per ogni valuta per la quale il cliente riceverà uno sconto fattura diverso.

---

## <a name="best-price-calculation"></a>Calcolo del prezzo migliore
Dopo aver registrato prezzi speciali e gli sconti riga di vendita e di acquisto, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantisce che il profitto sul commercio degli articoli sia sempre ottimale calcolando automaticamente il miglior prezzo delle vendite e dei documenti di acquisto e delle righe di registrazione magazzino.

Con il termine "miglior prezzo" si intende il prezzo più basso ammissibile che gode dello sconto riga più alto possibile praticabile in una specifica data. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcola automaticamente questo prezzo quando inserisce il prezzo unitario e la percentuale di sconto riga per gli articoli in nuove righe di documenti e di registrazione.

> [!NOTE]  
> Di seguito viene descritto come viene calcolato il prezzo migliore per le vendite. Il calcolo è lo stesso per gli acquisti.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] controlla la combinazione del cliente di fatturazione e dell'articolo e quindi calcola il prezzo unitario applicabile e la percentuale di sconto riga utilizzando i seguenti criteri:

    - Il cliente usufruisce di uno speciale accordo relativo a prezzi o sconti o appartiene a un gruppo che ne usufruisce?
    - L'articolo o il gruppo sconto articolo specificato nella riga è incluso in uno di tali accordi prezzi o sconti?
    - La data dell'ordine, o la data di registrazione per le fatture e le note di credito, è compresa nell'intervallo di validità dell'accordo prezzi o sconti?
    - È stato specificato un codice unità di misura? In caso affermativo, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno controllati i prezzi o gli sconti aventi lo stesso codice di unità di misura, altrimenti verranno verificati prezzi o gli sconti a cui non è associato alcun codice di unità di misura.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifica se si applicano accordi di prezzo/sconto alle informazioni sul documento o sulla riga di registrazione, quindi inserisce il prezzo unitario e la percentuale di sconto riga utilizzando i seguenti criteri:

    - C'è un requisito di quantità minima nell'accordo di prezzo/sconto che è soddisfatto?
    - C'è un requisito di valuta nell'accordo di prezzo/sconto che è soddisfatto? In caso affermativo, il prezzo più basso e lo sconto riga più alto per tale valuta vengono immessi, anche se la valuta locale fornirebbe un prezzo migliore. Se non esistono accordi prezzi o sconti riga per il codice di valuta specificato, in [!INCLUDE[d365fin](includes/d365fin_md.md)] verranno automaticamente selezionati il prezzo più basso e lo sconto riga più alto per la valuta locale.

Se non è possibile calcolare alcun prezzo speciale per l'articolo specificato nella riga, viene recuperato l'ultimo costo diretto o il prezzo unitario dalla scheda articolo immesso.

## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche

[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
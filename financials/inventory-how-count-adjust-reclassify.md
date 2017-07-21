---
title: Conteggio, adeguamento e riclassificazione dell'inventario| Documenti Microsoft
description: "Descrive come eseguire attività di conteggio fisico, rettifiche positive o negative e modificare le informazioni, quali ubicazione o numero di lotto, nei movimenti contabili articoli o nei movimenti warehouse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: it-it
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Procedura: Conteggio, rettifica e riclassificazione dell'inventario
Almeno una volta durante l'anno fiscale, è necessario procedere a un inventario fisico, ovvero conteggiare tutti gli articoli in magazzino, per verificare se la quantità registrata nel database corrisponde alla quantità fisica presente nelle warehouse. Se non si conosce la quantità fisica effettiva, è necessario registrarla nella contabilità generale come parte di una valutazione di magazzino di fine periodo.

Sebbene tutti gli articoli a magazzino vengano conteggiati almeno una volta l'anno, potrebbe essere necessario eseguire il conteggio di determinati articoli con maggiore frequenza, ad esempio nel caso in cui abbiano acquisito maggiore valore o siano prodotti a rapido assorbimento e costituiscano buona parte dell'attività commerciale. A questo scopo, è possibile assegnare speciali periodi di conteggio agli articoli. Per ulteriori informazioni, vedere la sezione "Per eseguire il conteggio ciclico".

Se è necessario rettificare le quantità di magazzino registrate, in relazione al conteggio o per altri scopi, è possibile utilizzare una registrazione di magazzino per modificare i movimenti contabili di inventario direttamente senza registrare transazioni aziendali. In alternativa, è possibile rettificare un singolo articolo nella scheda articolo.

Se è necessario modificare gli attributi dei movimenti contabili articoli oltre alle quantità, è possibile utilizzare le registrazioni di riclassificazione articoli. In genere tra gli attributi da riclassificare vi sono i numeri di serie o di lotto, le date di scadenza e le dimensioni.

## <a name="to-perform-a-physical-inventory"></a>Per eseguire un inventario fisico
Al termine di un anno finanziario, ma anche più spesso, è necessario elaborare un inventario fisico (ovvero conteggiare gli articoli attualmente in magazzino) per controllare se le quantità registrate corrispondono alle quantità fisiche presenti in magazzino. Se esistono differenze, queste devono essere registrate nei conti articoli prima di eseguire la valutazione di inventario.

Oltre al task di conteggio fisico, il processo completo include i tre task seguenti:

- Calcolo delle giacenze previste.
- Stampa del report da utilizzare nel conteggio.
- Immissione e registrazione delle giacenze effettive conteggiate.

### <a name="to-calculate-the-expected-inventory"></a>Per calcolare le giacenze previste
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni inventario fisico**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Calcola giacenze**.
3. Nella finestra **Calcola giacenze** specificare le condizioni da utilizzare per creare le righe registrazioni, ad esempio se includere gli articoli che non hanno inventario registrato.
4. Impostare i filtri se si desidera soltanto calcolare le giacenze per determinati articoli, collocazioni, ubicazioni o dimensioni.
5. Scegliere il pulsante **OK**.

> [!NOTE]  
>   I movimenti articoli vengono elaborati in base alle informazioni inserite e le righe vengono create in registrazioni inventario fisico. Si noti che il campo **Qtà (inv. fisico)** viene compilato automaticamente con la stessa quantità del campo **Qtà (calcolata)** . Con questa funzionalità non è necessario immettere le giacenze conteggiate disponibili per gli articoli quando sono corrispondenti alla quantità calcolata. Tuttavia, se la quantità conteggiata è diversa da quella immessa nel campo **Qtà (calcolata)** , è necessario sovrascriverla con la quantità effettivamente conteggiata.

### <a name="to-print-the-report-used-when-counting"></a>Per stampare il report da utilizzare nel conteggio
1. Nella finestra **Registrazioni inventario fis.** contenente le giacenze previste calcolate, scegliere l'azione **Stampa**.
2. Nella finestra **Lista inventario fisico** specificare se nel report deve essere inclusa la quantità calcolata e se elencare gli articoli di magazzino per numeri seriali/di lotto.
3. Impostare i filtri se si desidera stampare il report solo per determinati articoli, collocazioni, ubicazioni o dimensioni.
4. Selezionare il pulsante **Stampa**.

Gli addetti al magazzino potranno quindi eseguire l'inventario e registrare tutte le differenze nel report stampato.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Per immettere e registrare le giacenze effettive conteggiate
1. In ogni riga della finestra **Registrazioni inventario fis.** in cui le giacenze effettive, determinate dal conteggio fisico, sono diverse dalla quantità calcolata, immettere le giacenze effettive nel campo **Qtà (inv. fisico)**.

    I campi correlati vengono aggiornati di conseguenza.

    > [!NOTE]  
>   Se dal conteggio fisico risultano differenze determinate dalla registrazione degli articoli con codici ubicazione non corretti, le differenze non devono essere inserite nelle registrazioni inventario fisico. In alternativa, utilizzare le registrazioni di riclassificazione o un ordine di trasferimento per reindirizzare gli articoli alle ubicazioni corrette. Per ulteriori informazioni, vedere Registrazioni riclassificazione articoli. o Procedura: Creare ordini di trasferimento.

2. Per rettificare le quantità calcolate con le quantità effettive conteggiate, scegliere l'azione **Registra**.

    Vengono creati sia i movimenti contabili articoli che i movimenti contabili di inventario fisico. Aprire la scheda articolo per visualizzare i movimenti contabili di inventario fisico risultanti.

3. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.
4. Per verificare il conteggio dell'inventario, aprire la scheda articolo in questione e quindi scegliere l'azione **Mov. contabili inventario fis.**.

# <a name="to-perform-cycle-counting"></a>Per eseguire un conteggio ciclico
Sebbene tutti gli articoli a magazzino vengano conteggiati almeno una volta l'anno, potrebbe essere necessario eseguire il conteggio di determinati articoli con maggiore frequenza, ad esempio nel caso in cui abbiano acquisito maggiore valore o siano prodotti a rapido assorbimento e costituiscano buona parte dell'attività commerciale. A questo scopo, è possibile assegnare speciali periodi di conteggio agli articoli.

> [!NOTE]  
>   Se l'ubicazione è impostata per l'utilizzo di stoccaggi e prelievi guidati, utilizzare innanzitutto la finestra **Registrazioni inventario whse.**, quindi usare la funzione **Calcola rettifica whse.** nella finestra **Registrazioni magazzino**.

## <a name="to-set-up-counting-periods"></a>Per impostare i periodi di conteggio
L'inventario fisico viene in genere eseguito ad intervalli regolari, ad esempio con frequenza mensile, trimestrale o annuale. È possibile impostare i periodi di conteggio dell'inventario necessari.

È innanzitutto necessario impostare i periodi di conteggio dell'inventario da utilizzare, quindi assegnarne uno a ciascun articolo. Quando si esegue un inventario fisico e si utilizza la funzione **Calcola conteggio periodo** nelle registrazioni di inventario fisico, le righe relative agli articoli vengono create automaticamente.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Periodi di conteggio inventario fisico**, quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Per assegnare un periodo di conteggio a un articolo  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.  
2. Selezionare l'articolo a cui si desidera assegnare un periodo di conteggio.  
3. Nel campo **Cod. cont. periodo inv. fis.**, selezionare il periodo di conteggio appropriato.  
4. Scegliere il pulsante **Sì** per modificare il codice e calcolare il primo periodo di conteggio per l'articolo. Alla successiva scelta di calcolare un periodo di conteggio nelle registrazioni di inventario fisico, l'articolo verrà visualizzato come riga nella finestra **Selez. articoli inv. fis.**. A questo punto è possibile iniziare a conteggiare l'articolo su base periodica.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Per avviare un conteggio basato sui periodi di conteggio
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni inventario fisico**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Calcola conteggio periodo**.

    Viene visualizzata la finestra **Selez. articoli inv. fis.** contenente gli articoli da conteggiare in base ai periodi di conteggio precedentemente assegnati.
3. Eseguire l'inventario fisico. Per ulteriori informazioni, vedere la sezione "Per eseguire un inventario fisico".

## <a name="to-adjust-the-inventory-of-one-item"></a>Per rettificare l'inventario di un articolo
Dopo aver effettuato un conteggio fisico di un articolo nell'area magazzino, è possibile utilizzare la funzione **Rettifica magazzino** per registrare l'effettiva quantità di magazzino.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli**, quindi scegliere il collegamento correlato.
2. Selezionare l'articolo per cui si desidera rettificare il magazzino e scegliere l'azione **Rettifica magazzino**.
3. Nel campo **Nuovo inventario** immettere la quantità di magazzino che si desidera registrare per l'articolo.
4. Scegliere il pulsante **OK**.

Il magazzino dell'articolo è ora rettificato. La nuova quantità viene mostrata nel campo **Inventario corrente** nella finestra **Rettifica magazzino** e nel campo **Magazzino** nella finestra **Scheda articolo**.

È inoltre possibile utilizzare la funzione **Rettifica magazzino** come semplice mezzo per collocare articoli acquistati nel magazzino se non si utilizzano fatture o ordini di acquisto per registrare gli acquisti. Per ulteriori informazioni, vedere [Procedura: Registrare gli acquisti](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Dopo aver rettificato il magazzino, è necessario aggiornarlo con il valore corrente calcolato. Per ulteriori informazioni, vedere [Procedura: Rivalutare il magazzino](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Per rettificare la quantità di magazzino di uno o più articoli
Nella finestra **Registrazioni magazzino**, è possibile registrare direttamente la transazione dell'articolo per rettificare il magazzino in relazione a rettifiche positive o negative di agli acquisti o vendite senza utilizzare i documenti.

Se le registrazioni magazzino sono spesso utilizzate per la stessa riga di registrazione o per righe di registrazione simili, ad esempio in relazione al consumo di materiale, è possibile utilizzare la finestra **Registrazioni Magazzino Standard** per rendere più semplice questo tipo di lavoro ricorrente. Per ulteriori informazioni, vedere la sezione "Registrazioni standard" in [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni inventario fisico**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Scegliere l'azione **Registra** per procedere con le rettifiche di magazzino.

> [!NOTE]  
>   Dopo aver rettificato il magazzino, è necessario aggiornarlo con il valore corrente calcolato. Per ulteriori informazioni, vedere [Procedura: Rivalutare il magazzino](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Per riclassificare il numero di lotto di un articolo
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni riclassificazioni articoli**, quindi scegliere il collegamento correlato.
2. Nella finestra **Batch reg. riclass. articoli** compilare i campi in base alle esigenze.
3. Nel campo **Nr. lotto**, immettere il numero di lotto corrente di un articolo.
4. Nel campo **Nuovo nr. lotto**, immettere il nuovo numero di lotto di un articolo.
5. Scegliere l'azione **Registra**.

## <a name="see-also"></a>Vedi anche
[Magazzino](inventory-manage-inventory.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


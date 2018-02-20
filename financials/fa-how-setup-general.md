---
title: "Impostare la contabilità generale cespiti| Documenti Microsoft"
description: "Prima di utilizzare i cespiti occorre impostare i conti di default in contabilità generale, le categorie di registrazione, le chiavi di allocazione, le definizioni e i batch utilizzati per la registrazione e i codici di classe."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 29/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 97ff0418c2e3ffe2ace8412bb889fafd5788510b
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-general-fixed-assets-information"></a>Impostare i valori generali per i cespiti
Prima di gestire i cespiti, è necessario impostare i conti C/G di default, le chiavi di allocazione, le definizioni di registrazioni e i batch per la registrazione e la riclassificazione dei cespiti ed è possibile classificare i cespiti in classi, ad esempio materiali e immateriali.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Per impostare i valori predefiniti generali per i cespiti
Si definisce il comportamento generale o la funzionalità dei cespiti e si imposta la numerazione dei documenti nella finestra **Setup cespiti**.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup cespiti**, quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Per impostare le categorie di registrazione dei cespiti
Le categorie di registrazione vengono utilizzate per definire categorie di cespiti. I movimenti per queste categorie registrazione vengono registrati negli stessi conti di contabilità generale.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. cespiti**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**.
3. Nella finestra **Scheda Cat. Reg. Cespite** compilare i campi in base alle esigenze.

    > [!NOTE]  
>   Per assicurarsi che le contropartite per le diverse registrazioni cespiti vengono inserite automaticamente quando si sceglie l'azione **Inserisci conto cespiti** nelle righe di registrazione, seguire il passo successivo, sulla base della registrazione della rivalutazione.
4. Nella Scheda dettaglio **Contropartita**, selezionare nel campo **Contropartita rivalutazione** il conto di contabilità generale per cui si desidera inserire i movimenti di contropartita per la rivalutazione.

Per ulteriori informazioni sull'utilizzo dell'azione **Inserisci conto cespiti** nelle righe registrazioni cespiti in C/G richieste, vedere ad esempio [Rivalutazione dei cespiti](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Per impostare le chiavi di allocazione relative ai cespiti
Le transazioni possono essere assegnate a diversi reparti o progetti, in base alle chiavi di allocazione personalizzate. Ad esempio, è possibile impostare una chiave di allocazione per allocare i costi di ammortamento delle macchine all'amministrazione per il 35% ed al reparto vendite per il 65%. Per ulteriori informazioni, vedere [Allocazione di costi e ricavi](year-allocate-costs-income.md).

Le chiavi di allocazione sono valide per le classi di cespiti e non per singoli cespiti.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. cespiti**, quindi scegliere il collegamento correlato.  
2. Nella finestra **Categorie registrazione cespiti** scegliere l'azione **Allocazioni** e selezionare un tipo di registrazione.
3. Nella finestra **Allocazioni cespiti** compilare i campi in base alle esigenze.
4. Ripetere i passaggi 2 e 3 per ogni tipo di registrazione per cui si intendono definire le chiavi di allocazione.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Per impostare le definizioni registrazioni dei cespiti
Una definizione è un layout predefinito di registrazioni. La definizione contiene informazioni relative ai codici di traccia, ai report e alla numerazione. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] Una definizione delle registrazioni cespiti viene creata automaticamente la prima volta che si apre la finestra **Registrazioni Cespiti**. È possibile impostare definizioni aggiuntive per le registrazioni.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Def. registrazioni cespiti**, quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Per impostare i batch registrazioni cespiti
È possibile impostare più batch di registrazioni, cioè registrazioni individuali per ogni definizione registrazioni. Ad esempio, gli impiegati possono avere propri batch registrazioni in cui le loro iniziali vengono utilizzate come nome batch contabile. Per ulteriori informazioni, vedere [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Def. registrazioni cespiti**, quindi scegliere il collegamento correlato.  
2. Selezionare la definizione di registrazioni opportuna e quindi scegliere l'azione **Batch**.
3. Nella finestra **Batch registrazioni cespiti** compilare i campi in base alle esigenze.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Per impostare le definizioni registrazioni di riclassificazione dei cespiti
È possibile utilizzare le registrazioni di riclassificazione dedicate per trasferire, suddividere o raggruppare i cespiti. Le registrazioni di riclassificazione dei cespiti vengono create automaticamente la prima volta che in [!INCLUDE[d365fin](includes/d365fin_md.md)] si apre la finestra **Reg. ricl. cespiti**. È possibile impostare definizioni aggiuntive per le registrazioni di riclassificazione cespiti. Per ulteriori informazioni, vedere [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Def. reg. riclass. cespiti**, quindi scegliere il collegamento correlato.  
2. Compilare i campi in base alle esigenze.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Per impostare i batch registrazioni di riclassificazione dei cespiti
È possibile impostare più batch di registrazioni, cioè registrazioni individuali per ogni definizione registrazioni di riclassificazione. Ad esempio, gli impiegati possono avere un proprio batch di registrazioni di riclassificazione in cui le loro iniziali vengono utilizzate come nome del batch. Per ulteriori informazioni, vedere [Elaborazione delle registrazioni COGE](ui-work-general-journals.md).

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Def. reg. riclass. cespiti**, quindi scegliere il collegamento correlato.  
2. Selezionare la definizione di registrazioni opportuna e quindi scegliere l'azione **Batch**.
3. Nella finestra **Batch reg. riclass. cespiti** compilare i campi in base alle esigenze.

## <a name="to-set-up-fixed-asset-class-codes"></a>Per impostare i codici di classe cespiti
I codici di classe cespiti possono essere utilizzati per raggruppare i cespiti, ad esempio in beni materiali e immateriali.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Classi cespiti**, quindi scegliere il collegamento correlato.
2. Immettere i codici e i nomi delle classi da creare.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Per impostare i codici di sottoclasse cespiti
I codici di sottoclasse cespite consentono di raggruppare i cespiti in categorie quali edifici, veicoli, mobili e macchinari.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Sottoclassi cespiti**, quindi scegliere il collegamento correlato.
2. Immettere i codici e i nomi delle classi da creare.

## <a name="to-set-up-fixed-asset-location-codes"></a>Per impostare i codici di ubicazione cespiti
I codici di ubicazione cespiti consentono di registrare l'ubicazione del cespite, ad esempio reparto vendite, reception, amministrazione, produzione o warehouse. Queste informazioni sono utili per le attività legate alle assicurazioni e al magazzino.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Sottoclassi cespiti**, quindi scegliere il collegamento correlato.
2. Immettere i codici e i nomi delle ubicazioni cespiti da creare.

## <a name="to-register-opening-entries"></a>Per registrare movimenti di apertura
Nel caso in cui si utilizzino i cespiti in [!INCLUDE[d365fin](includes/d365fin_md.md)] per la prima volta, occorre innanzitutto impostare l'area di applicazione contabilità generale prima di impostare i cespiti. Le modalità del procedimento dipendono dall'eventuale integrazione dei cespiti nella contabilità generale.  

 La seguente procedura viene utilizzata se le transazioni cespiti devono essere registrate in contabilità generale.  

1. Assicurarsi di aver completato la procedura di base per l'impostazione dei cespiti;  
2. Creare una scheda cespite per ogni cespite esistente;  
3. Creare un registro beni ammortizzabili cespiti per ogni scopo di ammortamento (ad esempio dichiarazioni fiscali e rendiconti finanziari). È necessario definire i termini e le condizioni per ogni registro beni ammortizzabili, ad esempio l'integrazione con la contabilità generale.  

    Consentire l'integrazione con la contabilità generale eseguendo i passaggi seguenti. Innanzitutto, accertarsi che l'integrazione con la contabilità generale sia disabilitata per tutti i registri beni ammortizzabili, quindi registrare l'apertura dei movimenti e infine attivare l'integrazione con la contabilità generale.  
4. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registri beni ammortizz.**, quindi scegliere il collegamento correlato.  
5. Selezionare il registro beni ammortizzabili rilevante Nel gruppo **Gestione** della scheda **Pagina iniziale** scegliere **Modifica** per visualizzare la finestra **Scheda registro beni ammortizz.**
6. Nella Scheda dettaglio **Integrazione** assicurarsi che tutti i campi rimangano cancellando tutti i segni di spunta. Nel caso in cui si disponga di diversi registri beni ammortizzabili, disattivare l'integrazione contabilità generale per ciascuno di essi.  
7. Nelle registrazioni cespiti immettere le seguenti righe per ogni cespite:
   * Una riga con il costo di acquisto.
   * Una riga con il fondo ammortamento alla fine dell'anno fiscale precedente.
   * Una riga con il fondo ammortamento dall'inizio dell'anno fiscale corrente alla data in cui [!INCLUDE[d365fin](includes/d365fin_md.md)] è impostato per iniziare il calcolo dell'ammortamento.

    È possibile ora inserire anche gli altri eventuali saldi di apertura, ad esempio svalutazione e rivalutazione.  
8. Dopo aver immesso e registrato le righe delle registrazioni per ogni cespite, abilitare l'integrazione con la contabilità generale nel registro beni ammortizzabili.

Se i cespiti non sono integrati in contabilità generale, saltare i passaggi 6 e 8.

## <a name="see-also"></a>Vedi anche
[Impostazione di cespiti](fa-setup.md)  
[Cespiti](fa-manage.md)  
[Finanze](finance.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


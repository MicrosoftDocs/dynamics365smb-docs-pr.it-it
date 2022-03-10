---
title: Creazione di numerazioni
description: Informazioni su come impostare la numerazione per assegnare codici di identificazione univoci a conti e documenti in Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.search.form: 456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e95b60af569511a8a95154a53f80bcc235f883f5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140477"
---
# <a name="create-number-series"></a>Creazione di numerazioni

Per ogni società impostata, è necessario assegnare codici di identificazione univoci a elementi quali i conti di contabilità generale, i conti clienti e i conti fornitori, le fatture e altri documenti. La numerazione è importante non solo ai fini dell'identificazione. Un sistema di numerazione progettato correttamente semplifica la gestione e l'analisi della società e può ridurre il numero di errori correlati all'immissione dei dati.

> [!Important]
> Per impostazione predefinita, non sono consentite interruzioni nelle numerazioni poiché, per legge, l'esatta cronologia delle transazioni finanziarie deve essere disponibile per la revisione contabile e pertanto deve seguire una sequenza ininterrotta senza numeri cancellati.<br /><br />
> Se si desidera consentire delle interruzioni in determinate numerazioni, consultare prima il proprio revisore o il proprio responsabile della contabilità per assicurarsi di aderire ai requisiti legali nel proprio paese. Per ulteriori informazioni, vedere la sezione [Interruzioni nelle numerazioni](#gaps-in-number-series).

> [!NOTE]  
> Si consiglia di utilizzare gli stessi codici di numerazione visualizzati nella pagina **Elenco nr. serie** nella società di esempio CRONUS. I codici come *P-INV+* potrebbero non avere significato immediato, ma [!INCLUDE[prod_short](includes/prod_short.md)] dispone di un numero di impostazioni predefinite che dipendono da tali codici di numerazione.

Per creare un sistema di numerazione, è necessario impostare uno o più codici per ogni tipo di anagrafica o documento. È possibile, ad esempio, impostare un codice per la numerazione dei clienti, un altro per la numerazione delle fatture di vendita e un altro ancora per la numerazione di documenti in registrazioni COGE. Dopo avere impostato un codice, è necessario configurare almeno una riga di numerazione. Tale riga contiene informazioni quali il primo e l'ultimo numero nella serie e la data di inizio. È possibile impostare più righe di numerazione per codice di numerazione, con una diversa data di inizio per ogni riga. Le numerazioni verranno utilizzate consecutivamente, avviando ciascuna alla rispettiva data di inizio.

> [!NOTE]
> La lunghezza massima di un numero in una serie di numeri è di 20 caratteri. Ci sono alcune situazioni in cui [!INCLUDE[prod_short](includes/prod_short.md)] aggiungerà un numero con un ID generato dal sistema. Ad esempio, quando documenti come fatture vengono utilizzati per applicare transazioni, come pagamenti, [!INCLUDE[prod_short](includes/prod_short.md)] genera identificatori per le transazioni applicate. L'identificatore è composto da un numero di una serie di numeri e da un ID assegnato dal sistema a sei caratteri, come -12345. Se prevedi di elaborare più di 9.999 documenti nei giornali bancari o GIRO o nei giornali di ricevute di contanti, imposta le serie di numeri per questi tipi di documenti in modo da includere meno di 14 caratteri.

In genere, si imposta la serie di numeri per inserire automaticamente il numero immediatamente successivo nelle nuove schede o documenti creati. Tuttavia, è anche possibile impostare una numerazione che consente l'immissione manuale del nuovo numero. A tale scopo selezionare la casella di controllo **Consenti num. manuale**.

Se si desidera utilizzare più codici di numerazione per un tipo di anagrafica, ad esempio per utilizzare una numerazione diversa per diverse categorie di articoli, è possibile utilizzare relazioni tra numerazioni.

## <a name="gaps-in-number-series"></a>Interruzioni nelle numerazioni
Non tutti i record creati in [!INCLUDE[prod_short](includes/prod_short.md)] sono transazioni finanziarie che devono utilizzare numerazioni sequenziali. Le schede cliente, le offerte di vendita e le attività di warehouse sono esempi di record a cui è assegnato un numero di una numerazione, ma che non sono soggetti a controlli finanziari e/o che possono essere eliminati. Per tali numerazioni, è possibile selezionare la casella di controllo **Consenti interruzioni in num.** nella pagina **Righe nr. serie**. Questa impostazione può essere modificata anche dopo aver creato le numerazioni. Per ulteriori informazioni, vedere [Per creare nuove numerazioni](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Comportamento del campo Nr. in documenti e schede
Nella vendita, acquisto e trasferimento di documenti e su tutte le schede, il campo **Nr.** può essere compilato automaticamente da una serie di numeri o manualmente e può essere impostato per essere invisibile.

Il campo **Nr.** può essere compilato in tre modi:

1. Se esiste solo una numerazione per il tipo di documento o scheda dove la casella di controllo **Proponi automaticamente** è selezionata e la casella di controllo **Consenti num. manuale** non è selezionata, il campo viene compilato automaticamente con il numero successivo della numerazione e il campo **Nr.** non sarà visibile.

    > [!NOTE]  
    > Se la serie di numeri non funziona, ad esempio perché ha esaurito i numeri, il campo **Nr.** risulterà visibile e sarà possibile immettere manualmente un numero o risolvere il problema nella pagina **Nr. serie**.

2. Se esiste più di una numerazione per il tipo di documento o scheda e la casella di controllo **Proponi automaticamente** non è selezionata per la numerazione attualmente assegnata, il campo **Nr.** è visibile ed è possibile cercare la pagina **Nr. serie** e selezionare la numerazione che si desidera utilizzare. Il numero successivo della serie viene quindi inserito nel campo **Nr.**.  

3. Se per il tipo di documento o scheda non è stata impostata alcuna numerazione o se è selezionato il campo **Consenti num. manuale** per la numerazione, il campo **Nr.** è visibile ed è necessario inserire qualsiasi numero manualmente. È possibile immettere un massimo di 20 caratteri, tra numeri e lettere.

Quando si apre un nuovo documento o scheda per cui esiste una numerazione, si apre la relativa pagina **Setup numerazione** in modo da poter impostare una numerazione per il tipo di documento o scheda prima di procedere con un'altra immissione di dati.

> [!NOTE]  
> Se è necessario attivare la numerazione manuale, ad esempio su nuove schede articolo create con un processo di migrazione di dati che ha nascosto il campo **Nr.** per impostazione predefinita, passare alla pagina **Setup magazzino** e scegliere il campo **Nr. articoli** per aprire e impostare la relativa numerazione su **Consenti num. manuale**.

## <a name="to-create-a-new-number-series"></a>Per creare nuove numerazioni

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Nr. serie**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.  
3. Nella nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Scegliere l'azione **Righe**.  
5. Nella pagina **Righe nr. serie**, compilare i campi per definire l'uso effettivo e il contenuto delle numerazioni create nel passaggio 2.  
6. Ripetere il passaggio 5 per tutti i vari usi delle numerazioni necessari. Il campo **Data inizio** definisce quale riga di numerazione è attiva.  

> [!TIP]
> Per consentire agli utenti di specificare i numeri manualmente quando registrano un nuovo cliente o fornitore, ad esempio, scegli il campo **Nr. manuali** sulla numerazione stessa. Per non consentire il numero manuale, deseleziona il campo.

Puoi assegnare numerazioni ai modelli che hai impostato per i diversi tipi di cliente e fornitore che i tuoi venditori e acquirenti aggiungono più spesso al tuo [!INCLUDE [prod_short](includes/prod_short.md)]. In tal caso, imposta la numerazione pertinente, collegala tramite relazioni, quindi aggiungi la prima numerazione nella relazione pertinente alla pagina di configurazione pertinente.  

## <a name="to-create-relationships-between-number-series"></a>Per creare relazioni tra numerazioni

È possibile creare relazioni tra codici di numero di serie se ne sono stati impostati più di uno per lo stesso tipo di informazione o transazione di base. Questa funzione può essere utile per selezionare il codice corretto, al momento di utilizzare un numero. Impostando una relazione tra un gruppo di numeri di serie, tutte le numerazioni correlate vengono associate a un solo codice numero di serie. Quindi puoi inserire quel codice in un campo della scheda dettaglio **Numerazione** in una delle pagine di configurazione pertinenti, ad esempio **Setup contabilità clienti**.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Nr. serie**, quindi scegli il collegamento correlato.
2. Selezionare la riga contenente la numerazione per la quale si desidera creare delle relazioni, quindi scegliere **Relazioni**.
3. Nel campo **Codice serie** immettere il codice della numerazione che si desidera associare alla serie selezionata nel passaggio 2.
4. Aggiungere una riga per ogni codice che si desidera associare alla numerazione selezionata.
5. Chiudere la pagina.

Ogni volta che verrà impostato un elemento che richiede un numero, è ora possibile utilizzare le relazioni che sono state create per selezionare la numerazione corretta tra quelle poste in relazione.

## <a name="to-set-up-where-a-number-series-is-used"></a>Per impostare le aree in cui la numerazione viene utilizzata

La seguente procedura illustra come impostare una numerazione per l'area delle vendite. I passaggi sono simili per altre aree.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contabilità clienti**, quindi scegli il collegamento correlato.
2. Nella pagina **Contabilità clienti** nella Scheda dettaglio **Numerazioni**, selezionare la numerazione desiderata per ogni scheda di vendita o documento.

Il numero selezionato risulterà utilizzato per compilare il campo **Nr.** nella scheda o nel documento in questione, in base alle impostazioni effettuate nella serie di numerazione.  



## <a name="see-related-training-at-microsoft-learn"></a>Vedere le informazioni relative al training in [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Vedere anche
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
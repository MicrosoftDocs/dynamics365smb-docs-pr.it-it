---
title: Ammortamento dei cespiti| Documenti Microsoft
description: "È necessario definire come svalutare o ammortizzare ciascun cespite."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: c7521ded4e0857090cfa85c30d0f48af5ee36233
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="depreciate-or-amortize-fixed-assets"></a>Ammortamento dei cespiti
L'ammortamento consente di allocare il costo dei cespiti, come macchinari o attrezzature, in tutto il periodo di ammortamento. Occorre definire le modalità di ammortamento di ogni cespite.  

 L'ammortamento può essere registrato in due modi:  

* automaticamente, effettuando il processo batch **Calcola ammortamento**.  
* manualmente, utilizzando le registrazioni cespiti in C/G.  

Il calcolo dell'ammortamento in [!INCLUDE[d365fin](includes/d365fin_md.md)] può essere effettuato automaticamente su base giornaliera, per cui è possibile calcolare l'ammortamento per qualsiasi periodo. È quindi possibile analizzare gli attuali risultati operativi, ad esempio su base mensile, trimestrale o annuale. Per il calcolo viene utilizzato un anno standard di 360 giorni ed un mese standard di 30 giorni. Per ulteriori informazioni, vedere [Metodi di ammortamento](fa-depreciation-methods.md).  

Se diversi reparti utilizzano lo stesso cespite, l'ammortamento periodico può essere assegnato automaticamente a tali reparti in base a una tabella di allocazione personalizzata.  

Tramite il processo batch **Annulla mov. contabili cespiti** è possibile annullare movimenti di ammortamento errati. Successivamente è possibile registrare l'importo corretto eseguendo nuovamente il processo batch **Calcolo ammortamento**. Gli errori corretti vengono registrati come movimenti contabili cespiti errati.  

L'indicizzazione consente di correggere i valori per le modifiche generali a livello di prezzo. Il processo batch **Indice cespiti** consente di ricalcolare gli importi di ammortamento.  

## <a name="to-calculate-depreciation-automatically"></a>Per calcolare automaticamente l'ammortamento
Una volta al mese, oppure ogniqualvolta sia necessario, è possibile eseguire il processo batch **Calcola Ammortamento**. Il processo non considera i cespiti venduti, bloccati o inattivi né i cespiti che utilizzano il metodo di ammortamento manuale.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Calcolo ammortamento**, quindi scegliere il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere il pulsante **OK**.  

    Il processo batch calcola l'ammortamento e crea righe nelle registrazioni cespiti in contabilità generale.  
4. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.  

    Nella finestra **Registrazioni cespiti in C/G**, nel campo **Nr. giorni di ammortamento** sono indicati i giorni di ammortamento calcolati.  
5. Scegliere l'azione **Registra**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Per registrare un ammortamento manualmente tramite Registrazioni Cespiti in C/G
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.  
2. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.  
3. Nel campo **Tipo reg. cespite** scegliere **Ammortamento**.  
4. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione dell'ammortamento. Per ulteriori informazioni, vedere Impostare la sezione "Per impostare categorie di registrazione cespiti" in [Impostare i valori generali per i cespiti](fa-how-setup-general.md).  
5. Nella scheda **Pagina iniziale** selezionare **Registra** per effettuare la registrazione.  

Se sono state impostate le chiavi di allocazione cespiti per allocare importi a diversi reparti o progetti, gli importi vengono allocati durante la registrazione. Per ulteriori informazioni, vedere [Impostare i valori generali per i cespiti](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Per calcolare le allocazioni nella registrazione cespiti in C/G
Se diversi reparti utilizzano lo stesso cespite, l'ammortamento periodico può essere assegnato automaticamente a tali reparti in base a una tabella di allocazione personalizzata.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.  
2. Creare una riga iniziale e compilare i campi in base alle esigenze.
3. Nel campo **Tipo reg. cespite** scegliere **Allocazione**.  
4. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione dell'allocazione.  
5. Nella scheda **Pagina iniziale** selezionare **Registra** per effettuare la registrazione.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Utilizzare le liste di duplicazione per preparare la registrazione in diversi registri beni ammortizzabili
Quando si compilano righe di registrazioni da contabilizzare in un registro dei beni ammortizzabili, è possibile duplicare le righe in una registrazione distinta e quindi contabilizzarle in un registro dei beni ammortizzabili diverso. Per ulteriori informazioni, vedere la sezione "Per registrare i movimenti in diversi registri beni ammortizzabili".

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registri beni ammortizz.**, quindi scegliere il collegamento correlato.  
2. Aprire il registro beni ammortizzabili e selezionare la casella di controllo **Parte della lista duplicazione**.  

> [!IMPORTANT]  
>   Se è stato selezionato il campo **Usa lista duplicazione**, non utilizzare la numerazione nelle registrazioni. Il motivo è che la numerazione delle registrazioni cespiti in C/G non è la numerazione delle registrazioni del cespite.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Per registrare i movimenti in diversi registri beni ammortizzabili
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.  
2. Nelle registrazioni con cui si desidera registrare l'ammortamento, selezionare la casella di controllo **Usa lista duplicazione**.  
3. Compilare i rimanenti campi, se necessario.  
4. Scegliere l'azione **Registra**.  
5. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti**, quindi scegliere il collegamento correlato.  

    > [!NOTE]  
    >   La finestra **Registrazioni cespiti** contiene le righe nuove per i diversi registri beni ammortizzabili a seconda della lista di duplicazione.  
6. Analizzare o modificare le righe e scegliere l'azione **Registra**.  

    > [!NOTE]  
    >   Un altro modo per duplicare un movimento in un registro separato è l'inserimento di un codice registro beni ammortizzabili nel campo **Duplica nel reg. beni ammortiz.** durante la compilazione in una riga delle registrazioni.  

È possibile copiare movimenti da un registro dei beni ammortizzabili a un altro mediante il processo batch **Copia reg. beni ammortizz.**. Il processo batch crea le righe di registrazione nel batch delle registrazioni specificato nella finestra **Setup registrazioni cespiti** per il registro beni ammortizzabili in cui si desidera copiare. Per ulteriori informazioni, vedere la seguente procedura.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Per copiare i movimenti contabili cespiti tra i registri beni ammortizzabili
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registri beni ammortizz.**, quindi scegliere il collegamento correlato.  
2. Aprire la relativa scheda registro beni ammortizzabili e scegliere l'azione **Copia reg. beni ammortizz.**.  
3. Nella finestra **Copia reg. beni ammortizz.** compilare i campi secondo le necessità.  
4. Scegliere il pulsante **OK**.  

Le righe copiate vengono create nelle registrazioni cespiti in C/G o nelle registrazioni cespiti, a seconda che sia stata attivata l'integrazione contabilità generale per il registro beni ammortizzabili che si sta copiando.  

## <a name="see-also"></a>Vedi anche
[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


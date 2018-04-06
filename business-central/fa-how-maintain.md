---
title: Gestire cespiti| Documenti Microsoft
description: Conservare un record di manutenzione di tutte le riparazioni e i servizi riguardanti un cespite.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ce4dcfdd9b68bc5725538337b7883ba5f140cd1c
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="maintain-fixed-assets"></a>Gestione di cespiti
Le spese di manutenzione sono costi periodici di routine sostenuti per mantenere il valore del cespite. A differenza degli incrementi di capitale, il loro valore non aumenta.

È possibile registrare ed aggiornare file relativi alla manutenzione ed alla riparazione dei cespiti, affinché tutti i dati necessari relativi al cespite siano facilmente accessibili. Ogni volta che un cespite viene mandato in assistenza vengono registrate tutte le informazioni rilevanti, quali data dell'assistenza, numero del fornitore, numero di telefono dell'agente del servizio e così via. Le registrazioni di manutenzione vengono effettuate per ogni cespite dalla relativa scheda dei cespiti.

L'indicizzazione consente di correggere i valori per le modifiche generali a livello di prezzo. Il processo batch **Indice cespiti** consente di ricalcolare i costi di manutenzione.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Per registrare un intervento di manutenzione su un cespite
Ogniqualvolta vengono effettuate operazioni di manutenzione, ad esempio una visita di assistenza, è possibile registrarle in relazione al cespite corrispondente. Quest'operazione viene eseguita nella finestra **Registrazioni Manutenzione**.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cespiti**, quindi scegliere il collegamento correlato.  
2. Selezionare il cespite di cui registrare la manutenzione, quindi scegliere l'azione **Registrazioni manutenzione**.
3. Nella finestra **Registrazioni manutenzione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Per registrare i costi di manutenzione da Registrazioni Cespiti in C/G
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Lista reg. reni ammortizz.**, quindi scegliere il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili assegnato al cespite, quindi scegliere l'azione **Modifica**.
3. Nella finestra **Scheda registro beni ammortizz.**, verificare che la casella di controllo **Manutenzione** non sia selezionata. In questo modo i costi di manutenzione non vengono registrati nella contabilità generale.
4. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Registrazioni cespiti in C/G**, quindi scegliere il collegamento correlato.  
5. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.
6. Nel campo **Tipo reg. cespite** scegliere **Manutenzione**.
7. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della manutenzione.

    > [!NOTE]  
>   Il passaggio 7 funziona solo se è stato impostato quanto segue: nella finestra **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite il campo **Conto manutenzione** contiene il conto di addebito contabilità generale e il campo **Conto saldo manutenzione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione. Per ulteriori informazioni, vedere Impostare la sezione "Per impostare categorie di registrazione cespiti" in [Impostare i valori generali per i cespiti](fa-how-setup-general.md).
8. Scegliere l'azione **Registra**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Per pianificare le visite di assistenza relative ai cespiti
È possibile stampare il report **Manutenzione - Servizio Succ.** per visualizzare per quali cespiti è stata programmata una visita di assistenza. È possibile inoltre utilizzare questo report durante l'aggiornamento del campo **Data Servizio Successivo** nelle schede cespiti.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Prossima assistenza manutenzione**, quindi scegliere il collegamento correlato.  
2. Compilare i campi **Data inizio** e **Data fine**.  
3. Selezionare il pulsante **Stampa** o **Anteprima**.

## <a name="to-monitor-maintenance-costs"></a>Per monitorare i costi di manutenzione
I costi di manutenzione possono essere visualizzati dalle statistiche di un cespite.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cespiti**, quindi scegliere il collegamento correlato.
2. Selezionare il cespite di cui visualizzare i costi di manutenzione, quindi scegliere l'azione **Registri beni ammortizzabili**.
3. Nella finestra **Registro beni amm. cespiti**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Statistiche**.
4. Scegliere il campo **Manutenzione** nella finestra **Statistiche cespiti**.

Viene visualizzata la finestra **Movimenti contabili manutenzioni** con i movimenti che compongono l'importo del campo **Manutenzione**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Per visualizzare o stampare i costi di manutenzione per più cespiti
Nel report **Manutenzione - Analisi** è possibile selezionare se la manutenzione debba essere visualizzata in uno, due o tre codici di manutenzione per una data o un periodo specifico. È possibile visualizzare il totale di tutti i cespiti selezionati o un totale per ogni cespite.

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Analisi manutenzione**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario.
3. Selezionare il pulsante **Stampa** o **Anteprima**.

## <a name="to-view-maintenance-ledger-entries"></a>Per visualizzare i movimenti contabili manutenzioni
I costi di manutenzione possono essere esaminati anche visualizzando i movimenti contabili di manutenzione.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cespiti**, quindi scegliere il collegamento correlato.
2. Selezionare il cespite di cui visualizzare i movimenti contabili, quindi scegliere l'azione **Registri beni ammortizzabili**.
3. Nella finestra **Registro beni amm. cespiti**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Movimenti contabili manutenzioni**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Per visualizzare o stampare i movimenti contabili per più cespiti
Nel report **Manutenzione - Dettagli**, è possibile visualizzare o stampare i movimenti contabili di manutenzione per uno o più cespiti.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Dettagli manutenzione**, quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario.
3. Selezionare il pulsante **Stampa** o **Anteprima**.

## <a name="see-also"></a>Vedi anche
[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Benvenuto in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
title: Gestione di cespiti
description: Crea un registro di manutenzione di eventuali riparazioni e servizi su un cespite per preservare il valore del cespite.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="maintain-fixed-assets"></a><a name="maintain-fixed-assets"></a>Gestione di cespiti

Le spese di manutenzione sono costi periodici di routine sostenuti per mantenere il valore del cespite. A differenza degli incrementi di capitale, il loro valore non aumenta.

È possibile registrare ed aggiornare file relativi alla manutenzione ed alla riparazione dei cespiti, affinché tutti i dati necessari relativi al cespite siano facilmente accessibili. Ogni volta che un cespite viene mandato in assistenza vengono registrate tutte le informazioni rilevanti, quali data dell'assistenza, numero del fornitore, numero di telefono dell'agente del servizio e così via. Le registrazioni di manutenzione vengono effettuate per ogni cespite dalla relativa scheda dei cespiti.

L'indicizzazione consente di correggere i valori per le modifiche generali a livello di prezzo. Il processo batch **Indice cespiti** consente di ricalcolare i costi di manutenzione.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a><a name="to-record-maintenance-work-on-a-fixed-asset"></a>Per registrare un intervento di manutenzione su un cespite

Ogniqualvolta vengono effettuate operazioni di manutenzione, ad esempio una visita di assistenza, è possibile registrarle in relazione al cespite corrispondente. Quest'operazione viene eseguita nella pagina **Registrazioni Manutenzione**.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.  
2. Selezionare il cespite di cui registrare la manutenzione, quindi scegliere l'azione **Registrazioni manutenzione**.
3. Nella pagina **Registrazioni manutenzione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a><a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Per registrare i costi di manutenzione da Registrazioni Cespiti in C/G

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Lista reg. beni ammortizz.**, quindi scegli il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili assegnato al cespite, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda registro beni ammortizz.**, verificare che la casella di controllo **Manutenzione** non sia selezionata. In questo modo i costi di manutenzione non vengono registrati nella contabilità generale.
4. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.  
5. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.
6. Nel campo **Tipo reg. cespite** scegliere **Manutenzione**.
7. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della manutenzione.

    > [!NOTE]  
    >   Il passaggio 7 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite il campo **Conto manutenzione** contiene il conto di addebito contabilità generale e il campo **Conto saldo manutenzione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Scegliere l'azione **Registra**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a><a name="to-follow-up-on-fixed-assets-service-visits"></a>Per pianificare le visite di assistenza relative ai cespiti

È possibile stampare il report **Manutenzione - Servizio Succ.** per visualizzare per quali cespiti è stata programmata una visita di assistenza. È possibile inoltre utilizzare questo report durante l'aggiornamento del campo **Data Servizio Successivo** nelle schede cespiti.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prossima assistenza manutenzione**, quindi seleziona il collegamento correlato.  
2. Compilare i campi **Data inizio** e **Data fine**.  
3. Selezionare il pulsante **Stampa** o **Anteprima**.

## <a name="to-monitor-maintenance-costs"></a><a name="to-monitor-maintenance-costs"></a>Per monitorare i costi di manutenzione

I costi di manutenzione possono essere visualizzati dalle statistiche di un cespite.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite di cui visualizzare i costi di manutenzione, quindi scegliere l'azione **Registri beni ammortizzabili**.
3. Nella pagina **Registro beni amm. cespiti**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Statistiche**.
4. Scegliere il campo **Manutenzione** nella pagina **Statistiche cespiti**.

Viene visualizzata la pagina **Movimenti contabili manutenzioni** con i movimenti che compongono l'importo del campo **Manutenzione**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Per visualizzare o stampare i costi di manutenzione per più cespiti

Nel report **Manutenzione - Analisi** è possibile selezionare se la manutenzione debba essere visualizzata in uno, due o tre codici di manutenzione per una data o un periodo specifico. È possibile visualizzare il totale di tutti i cespiti selezionati o un totale per ogni cespite.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Analisi manutenzione**, quindi scegli il collegamento correlato.
2. Compilare i campi, se necessario.
3. Selezionare il pulsante **Stampa** o **Anteprima**.

## <a name="to-view-maintenance-ledger-entries"></a><a name="to-view-maintenance-ledger-entries"></a>Per visualizzare i movimenti contabili manutenzioni

I costi di manutenzione possono essere esaminati anche visualizzando i movimenti contabili di manutenzione.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite di cui visualizzare i movimenti contabili, quindi scegliere l'azione **Registri beni ammortizzabili**.
3. Nella pagina **Registro beni amm. cespiti**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Movimenti contabili manutenzioni**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Per visualizzare o stampare i movimenti contabili per più cespiti

Nel report **Manutenzione - Dettagli**, è possibile visualizzare o stampare i movimenti contabili di manutenzione per uno o più cespiti.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dettagli manutenzione**, quindi scegli il collegamento correlato.
2. Compilare i campi in base alle esigenze.
3. Seleziona il pulsante **Stampa** o **Anteprima**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/paths/manage-fixed-assets-maintenance-insurances/)

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

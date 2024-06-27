---
title: Gestione dei cespiti
description: Registrare le riparazioni e gli interventi di assistenza su un cespite per preservarne il valore.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Gestione dei cespiti

I costi di manutenzione sono spese operative per le cose che fai per preservare le condizioni dei tuoi cespiti. A differenza dei miglioramenti di capitale, la manutenzione non aumenta il valore dei cespiti.

Ogni volta che invii un cespite in assistenza, registri informazioni quali data dell'intervento di assistenza, il fornitore che ha effettuato il lavoro e il numero di telefono dell'agente di assistenza. Le informazioni sulla manutenzione vengono immesse in più pagine:

* Scheda cespite
* Ordine di acquisto
* Fattura di acquisto
* Reg. cespiti in C/G

L'indicizzazione consente di correggere i valori per le modifiche generali a livello di prezzo. Usa l'azione **Indice cespiti** per ricalcolare i costi di manutenzione.

## Registrare un costo di manutenzione direttamente su un cespite

Ogniqualvolta vengono effettuate operazioni di manutenzione per un cespite, ad esempio una visita di assistenza, è possibile registrarle nella pagina **Registrazioni manutenzione**.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Cespiti**, quindi scegli il collegamento correlato.  
2. Selezionare il cespite di cui registrare la manutenzione, quindi scegliere l'azione **Registrazioni manutenzione**.
3. Nella pagina **Registrazioni manutenzione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Registrare costi di manutenzione da una registrazione cespiti in C/G

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Lista reg. beni ammortizz.**, quindi scegli il collegamento correlato.  
2. Selezionare il registro beni ammortizzabili assegnato al cespite, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda registro beni ammortizz.**, assicurati che la casella di controllo **Manutenzione** non sia selezionata in modo da non registrare i costi di manutenzione nella contabilità generale.
4. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni cespiti in C/G**, quindi scegli il collegamento correlato.  
5. Creare una riga di registrazione iniziale e compilare i campi in base alle esigenze.
6. Nel campo **Tipo reg. cespite** scegliere **Manutenzione**.
7. Scegliere l'azione **Inserisci conto cespiti**. Una seconda riga di registrazione viene creata per la contropartita impostata per la registrazione della manutenzione.

    > [!NOTE]  
    > Il passaggio 7 funziona solo se è stato impostato quanto segue: nella pagina **Scheda Cat. Reg. Cespite** della categoria di registrazione del cespite il campo **Conto manutenzione** contiene il conto di addebito contabilità generale e il campo **Conto saldo manutenzione** contiene il conto C/G in cui si desidera registrare i movimenti di contropartita per la rivalutazione. Per ulteriori informazioni, vedere [Per impostare le categorie di registrazione dei cespiti](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Scegli l'azione **Registra**.

## Registrare i costi di manutenzione da una fattura di acquisto

I passaggi seguenti descrivono come registrare i costi di manutenzione per un cespite da una fattura di acquisto. I passaggi sono simili per un ordine di acquisto.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fattura di acquisto**, quindi scegli il collegamento correlato.
2. Compilare i campi appropriati nella Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nel campo **Tipo** della Scheda dettaglio **Righe** scegli **Cespite**.
4. Nel campo **Nr.** scegli il cespite, quindi specifica la quantità e il costo.
5. Nel campo **Tipo reg. cespite** scegli **Manutenzione**.
6. Registra la fattura di acquisto.

## Follow up delle visite di assistenza

Puoi stampare il report **Manutenzione - Servizio Succ.** per elencare i cespiti pianificati per l'assistenza. È possibile inoltre utilizzare questo report quando si vuole aggiornare il campo **Data servizio successivo** nelle schede cespiti.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Prossima assistenza manutenzione**, quindi seleziona il collegamento correlato.  
2. Compilare i campi **Data inizio** e **Data fine**.  
3. Seleziona il pulsante **Stampa** o **Anteprima**.

## Monitorare i costi di manutenzione

Puoi visualizzare le statistiche per monitorare i costi di manutenzione.  

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite di cui visualizzare i costi di manutenzione, quindi scegliere l'azione **Registri beni ammortizzabili**.
3. Nella pagina **Registro beni amm. cespiti**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Statistiche**.
4. Scegliere il campo **Manutenzione** nella pagina **Statistiche cespiti**.

Usa la pagina **Movimenti contabili manutenzioni** per visualizzare i movimenti che compongono l'importo nel campo **Manutenzione**.

## Visualizzare o stampare i costi di manutenzione per più cespiti

Nel report **Manutenzione - Analisi** è possibile scegliere di esaminare la manutenzione in base a uno, due o tre codici di manutenzione per una data o un periodo specifico. Il report può mostrare il totale di tutti i cespiti selezionati o un totale per ogni cespite.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Analisi manutenzione**, quindi scegli il collegamento correlato.
2. Compila i campi come necessario.
3. Seleziona il pulsante **Stampa** o **Anteprima**.

## Visualizzare i movimenti contabili di manutenzione

I costi di manutenzione possono essere esaminati anche visualizzando i movimenti contabili di manutenzione.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Cespiti**, quindi scegli il collegamento correlato.
2. Selezionare il cespite di cui visualizzare i movimenti contabili, quindi scegliere l'azione **Registri beni ammortizzabili**.
3. Nella pagina **Registro beni amm. cespiti**, selezionare il registro beni ammortizzabili cespiti rilevante quindi scegliere l'azione **Movimenti contabili manutenzioni**.

## Visualizzare o stampare i movimenti contabili di manutenzione per più cespiti

Nel report **Manutenzione - Dettagli**, è possibile visualizzare o stampare i movimenti contabili di manutenzione per uno o più cespiti.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dettagli manutenzione**, quindi scegli il collegamento correlato.
2. Compila i campi in base alle esigenze.
3. Seleziona il pulsante **Stampa** o **Anteprima**.

## Vedere anche

[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Dati finanziari](finance.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

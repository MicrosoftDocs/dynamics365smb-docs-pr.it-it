---
title: Suggerimento automatico dei valori in Business Central
description: 'Per evitare i calcoli manuali e per completare i task in modo rapido e accurato, è possibile impostare l''immissione automatica dei dati in modo che Business Central compili i campi selezionati.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Lascia [!INCLUDE[prod_short](includes/prod_short.md)] Suggerisci valori
[!INCLUDE[prod_short](includes/prod_short.md)] può aiutare a completare le attività in modo più rapido e più corretto precompilando campi o righe intere con dati che verrebbero altrimenti calcolati e immessi manualmente. Sebbene tale l'immissione dei dati automatica sia sempre corretta, è possibile modificarla in seguito se lo si desidera.

La funzionalità che fornisce in automatico i valori dei campi è in genere offerta per le attività in cui si devono immettere grandi volumi di dati transazionali e per cui si desidera evitare errori e risparmiare tempo. Questo articolo contiene una selezione di tali funzionalità. Nei futuri aggiornamenti di [!INCLUDE[prod_short](includes/prod_short.md)] verranno aggiunte altre sezioni.

## La casella di controllo **Suggerisci importo contropartita** nella pagina **Batch registrazioni COGE**
Ad esempio, quando si inseriscono righe di giornale generale per più spese che devono essere tutte registrate sullo stesso conto bancario, ogni volta che si inserisce una nuova riga di giornale per una spesa, è possibile fare in modo che il campo  **Importo**  nella riga del conto bancario venga automaticamente aggiornato con l'importo che bilancia le spese. Per ulteriori informazioni sull'utilizzo delle registrazioni COGE, vedere [Utilizzare le registrazioni COGE](ui-work-general-journals.md).

### Per compilare automaticamente il campo **Importo** nelle righe di registrazione COGE di contropartita
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
2. Nella riga del batch delle registrazioni COGE preferito, selezionare la casella di controllo **Suggerisci importo contropartita**.
3. Aprire le registrazioni COGE e procedere a registrare e contabilizzare le transazioni utilizzando la funzionalità descritta per l'immissione automatica di un valore nel campo.       

Per informazioni su come impostare un batch registrazioni COGE personale, ad esempio per la gestione delle spese, vedi [Utilizzare le registrazioni COGE](ui-work-general-journals.md).

## Il campo **Compila automaticamente data di ricezione** nella pagina **Registrazione pagamenti**
La pagina  **Registra pagamenti clienti** mostra i pagamenti in entrata in sospeso come righe che rappresentano documenti di vendita in cui un importo è dovuto per il pagamento. Per ulteriori informazioni sul collegamento dei pagamenti dei clienti, vedere [Riconciliare i pagamenti dei clienti dall'elenco dei documenti di vendita non pagati](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Le azioni principali da compiere sulla pagina sono compilare la casella di controllo  **Pagamento effettuato** e il campo  **Data di ricezione** . È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo che inserisca automaticamente la data di lavoro nel campo **Data ricezione** quando si seleziona la casella di controllo **Pagamento effettuato**.

### Per compilare automaticamente il campo **Data ricezione** nella pagina **Registrazione pagamenti**
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazione pagamenti**, quindi scegli il collegamento correlato.
2. Selezionare la casella di controllo **Compila automaticamente data di ricezione**.
3. Aprire la pagina  **Registra pagamenti clienti** e procedere all'elaborazione dei pagamenti in entrata dei clienti utilizzando la funzionalità descritta per l'inserimento automatico di un valore di campo.

## Vedere anche
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Dati finanziari](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
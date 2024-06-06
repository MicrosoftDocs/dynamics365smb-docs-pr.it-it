---
title: Creare una fattura di vendita progetto per fatturare un progetto
description: Descrive come fatturare ai clienti le spese progetto durante lo svolgimento di un progetto e l'accumulo dei costi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
---
# Fatturare i progetti

Durante il progetto, è possibile che si accumulino i costi di progetto derivanti da utilizzo delle risorse, materiali e acquisti correlati al progetto. Durante l'esecuzione del progetto, tali transazioni vengono inserite nella registrazione progetti. È importante registrare tutti i costi nella registrazione progetti prima di fatturare al cliente.

> [!NOTE]
> Puoi inoltre acquistare risorse esterne non correlate a un progetto, ad esempio, per fatturare a un fornitore per il lavoro eseguito. Per ulteriori informazioni, vedi [Registrare gli acquisti](purchasing-how-record-purchases.md).

Puoi fatturare l'intero progetto dalla pagina **Righe attività di progetto** oppure fatturare solo le righe fatturabili selezionate nella pagina **Righe di pianificazione progetto**. La fatturazione può essere effettuata dopo il termine del progetto oppure a determinati intervalli durante l'esecuzione del progetto in base a un'apposita programmazione.

> [!NOTE]  
> Se selezioni **Fatturabile** nel campo **Tipo di riga progetto** dei documenti di acquisto per gli acquisti correlati al progetto, vengono create le righe di pianificazione progetto che sono pronte per la fatturazione al cliente. Per ulteriori informazioni, vedere [Gestire gli approvvigionamenti per un progetto](projects-how-manage-project-supplies.md).

Puoi anche fatturare una società che non è il cliente finale. A volte la parte a cui è rivolto un progetto è diversa dalla parte che paga il conto. Nella pagina **Progetti** è possibile specificare il cliente che beneficerà del progetto nei campi **Vendere a** e la parte che fattura nei campi **Fatturare a**.

## Per creare più fatture di vendita progetto

Puoi creare una fattura per un progetto o per una o più attività di progetto per un cliente al completamento del lavoro da fatturare o al raggiungimento della data per la fatturazione in base a una programmazione di fatturazione.

Nella procedura che segue viene mostrato come utilizzare un processo batch per fatturare più progetti.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetto - Crea fattura vendita**, quindi scegli il collegamento correlato.  
2. Compila i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Imposta i filtri se desideri limitare i progetti che devono essere elaborati nel processo batch.
4. Scegliere il pulsante **OK** per creare le fatture di assistenza.  

È possibile rivedere e pubblicare le fatture create nella finestra **Fatture vendita**.

> [!NOTE]
> In alternativa, fattura a un cliente selezionando il progetto, quindi scegliendo l'azione **Crea fattura vendita**. 

## Per creare e registrare una fattura di vendita progetto da righe di pianificazione progetto

Puoi creare una fattura da righe di pianificazione progetto e indicare in quella occasione la quantità dell'articolo, la risorsa o il conto CoGe che vuoi fatturare.

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.
2. Apri un progetto pertinente.
3. Selezionare un'attività di progetto per il quale il campo **Tipo di attività di progetto** contiene **Registrazione**, quindi scegliere l'azione **Righe di pianificazione progetto**.  
4. In una riga di pianificazione progetto, nel campo **Qtà da trasferire in fattura**, immetti la quantità dell'articolo, la risorsa, il tipo del conto di contabilità generale che vuoi fatturare.  
5. Scegliere l'azione **Crea fattura di vendita**.
6. Nella pagina **Progetto - Trasferimento a fattura vendita**, immetti la data di registrazione e se vuoi creare una nuova fattura o aggiungere questa fattura a una esistente.
7. Scegli il pulsante **OK**.  
8. Nella pagina **Righe pianificazione progetto** scegli l'azione **Fatture/Note credito vendite**.

    Verrà visualizzata la pagina **Fatture di vendita** nella quale sarà mostrata la quantità che è stata trasferita in fattura.
9. Apportare tutte le modifiche aggiuntive, quindi scegliere l'azione **Registra**.

> [!NOTE]  
> La procedura sopra riportata è simile per la creazione, la revisione e la registrazione di una nota di credito di vendita correlata a un progetto.

## Vedere anche

[Gestione di progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

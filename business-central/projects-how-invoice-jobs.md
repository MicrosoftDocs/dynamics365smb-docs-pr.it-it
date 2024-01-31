---
title: Creare una fattura di vendita per fatturare una commessa
description: Viene descritto come fatturare ai clienti le spese commessa durante lo svolgimento di un progetto e l'accumulo dei costi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Fatturazione di commesse

Durante il progetto, è possibile che si accumulino i costi di commessa derivanti dall'utilizzo delle risorse, dai materiali e dagli acquisti correlati alla commessa. A seconda dello stato di avanzamento della commessa, tali transazioni vengono inserite nelle registrazioni commesse. È importante registrare tutti i costi prima di fatturare al cliente.

> [!NOTE]
> Puoi inoltre acquistare risorse esterne non correlate a un processo, ad esempio, per fatturare a un fornitore per il lavoro eseguito. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).

È possibile fatturare l'intera commessa dalla pagina **Righe task commessa** oppure fatturare solo le righe fatturabili selezionate dalla pagina **Righe pianificazione**. La fatturazione può essere effettuata dopo la chiusura della commessa oppure durante lo svolgimento delle operazioni correlate alla commessa, a determinati intervalli basati su un'apposita programmazione.

> [!NOTE]  
> Se si seleziona **Fatturabile** nel campo **Tipo riga commessa** dei documenti di acquisto per gli acquisti correlati alla commessa, vengono create le righe di pianificazione commessa che sono pronte per la fatturazione al cliente. Per ulteriori informazioni, vedere [Gestire gli approvvigionamenti per un progetto](projects-how-manage-project-supplies.md).

Puoi anche fatturare una società che non è il cliente finale. A volte la parte a cui è rivolto un progetto è diversa dalla parte che paga il conto. Nella pagina **Processi** è possibile specificare il cliente che beneficerà del progetto nei campi **Vendere a** e la parte che fattura nei campi **Fatturare a**. 

## Per creare più fatture di vendita commesse

È possibile creare una fattura per una commessa o per uno o più task commessa per un cliente al completamento del lavoro da fatturare o al raggiungimento della data per la fatturazione in base a una programmazione di fatturazione.

Nella procedura che segue viene mostrato come utilizzare un processo batch per fatturare più commesse.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Commessa - Crea fattura vendita**, quindi seleziona il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Impostare i filtri se si desidera limitare le commesse che devono essere elaborate nel processo batch.
4. Scegliere il pulsante **OK** per creare le fatture di assistenza.  

È possibile rivedere e pubblicare le fatture create nella finestra **Fatture vendita**.

> [!NOTE]
> In alternativa, fatturare a un cliente selezionando la commessa, quindi scegliendo l'azione **Crea fattura vendita per commessa**. 

## Per creare e registrare una fattura di vendita commessa dalle righe di pianificazione commessa

È possibile creare una fattura da righe di pianificazione commessa e indicare in quella occasione la quantità dell'articolo, la risorsa o il conto di contabilità generale che si desidera fatturare.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.
2. Aprire una commessa appropriata.
3. Selezionare un task commessa per il quale il campo **Tipo task commessa** contiene **Registrazione**, quindi scegliere l'azione **Righe pianificazione commessa**.  
4. In una riga di pianificazione commessa, nel campo **Qtà da trasferire in fattura** , immettere la quantità dell'articolo, la risorsa, il tipo del conto di contabilità generale che si desidera fatturare.  
5. Scegliere l'azione **Crea fattura di vendita**.
6. Nella pagina **Commessa - Crea fattura vendita**, immettere la data di registrazione e se si desidera creare una nuova fattura o aggiungere questa fattura a una esistente.
7. Scegliere il pulsante **OK**.  
8. Nella pagina **Righe pianificazione commessa** scegliere l'azione **Fatture/Note credito vendite**.

    Verrà visualizzata la pagina **Fatture di vendita** nella quale sarà mostrata la quantità che è stata trasferita in fattura.
9. Apportare tutte le modifiche aggiuntive, quindi scegliere l'azione **Registra**.

> [!NOTE]  
>   La procedura sopra riportata è simile per la creazione, la revisione e la registrazione di una nota di credito di vendita correlata a una commessa.

## Vedere anche

[Gestione di progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Registrare il consumo o l'utilizzo di articoli e di risorse per progetti
description: Questo articolo descrive come registrare il consumo o l'utilizzo degli articoli o delle risorse per progetti nella gestione progetti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
---
# Registrare il consumo o l'utilizzo per progetti

Dalla pagina **Scheda progetto**, è possibile aprire la pagina **Righe di pianificazione progetto** per esaminare e registrare l'utilizzo delle varie parti del progetto. Queste informazioni vengono aggiornate automaticamente quando modifichi e trasferisci informazioni tra progetti e registrazioni progetti o fatture di progetto. Ciò richiede che sia stata attivato l'interruttore **Applica collegamento utilizzo per impostazione predefinita** nella pagina **Setup progetto**. Per ulteriori informazioni, vedere [Impostare progetti](projects-how-setup-jobs.md).  

Ad esempio, per le righe di pianificazione di tipo **Budget**, puoi immettere la quantità di una risorsa e specificare la quantità da trasferire nella registrazione progetti. Se il tipo di righe di pianificazione è **Fatturabile**, puoi immettere la quantità della risorsa e specificare la quantità da trasferire in una fattura. Per ulteriori informazioni sulla fatturazione al cliente, vedere [Fatturare progetti](projects-how-invoice-jobs.md). Confrontando la quantità originale, la quantità residua o la quantità registrata è possibile rivedere rapidamente le informazioni sull'utilizzo. Per ulteriori informazioni sulla stima dei valori a budget durante la pianificazione, vedere [Gestire budget di progetti](projects-how-manage-budgets.md).  

Di seguito viene descritto come registrare le quantità e i costi (previsti) effettivi con una registrazione progetti. In alternativa puoi utilizzare i documenti di acquisto per registrare l'acquisto per un progetto. Per ulteriori informazioni vedere [Gestire approvvigionamenti di progetti](projects-how-manage-project-supplies.md).

## Per registrare l'utilizzo per una riga di pianificazione progetto di tipo Budget

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Seleziona il progetto, quindi scegli l'azione **Righe pianificazione progetto**. 
3. Selezionare una riga di pianificazione progetto di tipo **Budget** o **Budget e fatturabile** per la quale si desidera registrare l'utilizzo.   

    > [!NOTE]
    > È inoltre possibile registrare l'utilizzo per una riga di pianificazione progetto di tipo **Fatturabile**. In genere, queste righe vengono utilizzate per creare fatture, ma è anche possibile trasferire le informazioni a una registrazione. Per ulteriori informazioni, vedere [Fatturare progetti](projects-how-invoice-jobs.md) 

4. Nel campo **Qtà da trasferire per registrazione**, immetti la quantità da trasferire. La quantità di default è il valore che si immette nel campo **Quantità**.

    Il campo **Quantità residua** mostra la quantità che rimane per completare il progetto e da trasferire nella registrazione.
5. Scegliere l'azione **Crea righe registrazioni progetti**.

    > [!TIP]
    > Se si aggiungono più righe di pianificazione progetto per questo progetto, attendere fino a quando non sono state aggiunte tutte le righe di pianificazione progetto.
6. Nella pagina **Riga di pianificazione progetto di trasferimento progetto** compilare i campi come necessario, quindi scegliere il pulsante **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Scegliere l'azione **Apri registrazione progetti**.  
8. Nella pagina **Registrazione progetti**, selezionare la riga pertinente e scegliere l'azione **Registra**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Nella pagina **Righe di pianificazione progetto**, esaminare l'utilizzo registrato osservando i campi **Quantità**, **Quantità residua** e **Qtà da trasferire per registrazione**.  
10. Ripetere i passaggi da 3 a 8 per registrare altri utilizzi.  

## Per creare righe di registrazione progetto manualmente

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
2. Nel campo **Nome batch** scegliere un batch di registrazioni progetti pertinente.  
3. In una nuova riga, immettere il numero di documento, il numero di progetto, il numero di attività di progetto, il tipo e la quantità del tipo consumata.  
4. Una volta completate le righe di registrazione progetto, scegliere l'azione **Registra**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Per visualizzare le stime di utilizzo del progetto e gli aggiornamenti della registrazione

È possibile visualizzare l'utilizzo del progetto fino al completamento di un progetto in un unico passaggio. A questo scopo, utilizzare il processo batch **Progetto - Calcolo utilizzo residuo** per tutte le attività fino al termine del progetto incluso.  

In questo modo è possibile tenere traccia e confrontare le stime iniziali rispetto ai risultati effettivi ed apportare modifiche o creare nuovi movimenti in base alle esigenze. Ad esempio, è possibile che si sia stimato che un progetto richieda 10 ore e ad oggi siano state impiegate 15 ore. È possibile aggiungere le cinque ore in più nella riga di registrazione esistente o creare una nuova riga registrazioni per indicare le cinque ore come straordinario, ovvero un altro tipo di lavoro. Vengono calcolati il costo e il prezzo appropriati ed è quindi possibile contabilizzarli nella registrazione.  

> [!NOTE]  
> I movimenti articoli creano movimenti contabili articoli e riducono la quantità di inventario. Il processo batch **Registra costo magazzino in C/GL** trasferisce il costo dal magazzino alla contabilità generale. I movimenti risorse creano movimenti contabili risorse.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
2. Selezionare una registrazione progetti corrispondente, quindi scegliere l'azione **Calc. utilizzo residuo**.  
3. Nella pagina **Progetto - Calcolo utilizzo residuo**, immettere il numero di documento e la data di registrazione che deve essere inserita nelle registrazioni, quindi scegliere **OK**.  
4. Aggiornare le registrazioni con tutte le necessarie modifiche.  
5. Scegliere **Registra**.

## Creare documenti di prelievo di magazzino o di warehouse per un progetto

Usare le azioni **Crea prelievo di magazzino** e **Crea prelievo warehouse** nella pagina **Scheda progetto**. Per creare o registrare un documento di prelievo, utilizzare le azioni **Righe stoccaggio/prelievo/movimento** o **Righe prelievo registrate**. Per ulteriori informazioni vedere [Flussi per produzione, assemblaggio e progetti](design-details-internal-warehouse-flows.md).

È possibile usare le azioni nelle seguenti condizioni:

* Lo **Stato** del progetto è **Aperto**.
* Il **Tipo di riga** della riga di pianificazione progetto è **Budget** o **Budget e fatturabile**.
* Il **Tipo** della riga di pianificazione progetto è **Articolo**.
* **Richiesto prelievo** è abilitata per la relativa posizione.
* **Stoccaggi e prelievi guidati** è disabilitata.

> [!NOTE] 
> Sebbene l'impostazione sia denominata **Richiesto prelievo**, è comunque possibile registrare il consumo direttamente dalla riga di registrazione progetto per l'ubicazione. Se l'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizzare la pagina **Prelievi magazzino** per organizzare e stampare le informazioni di prelievo. Puoi anche utilizzare la pagina per inserire e pubblicare il risultato del prelievo, che a sua volta registra il consumo degli articoli. 
> 
> Se l'ubicazione è impostata in modo da richiedere l'elaborazione di prelievi e di spedizioni, indicando che hai scelto i campi **Richiesta prelievo** e **Richiesta spedizione** nella pagina **Scheda ubicazione**, usa la pagina **Prelievo warehouse** per gestire il prelievo. I prelievi warehouse sono simili ai prelievi in magazzino. La differenza è che, anziché pubblicare le informazioni sul prelievo, registri il prelievo. Questa registrazione non registra il consumo, ma rende gli articoli disponibili per la pubblicazione. Il responsabile di warehouse può utilizzare i prospetti prelievi per organizzare le informazioni di prelievo prima di creare le istruzioni di prelievo dalla singola warehouse

## Per esaminare le righe di pianificazione per un movimento contabile progetto

Dopo avere registrato le righe di registrazione progetto, è possibile visualizzare le righe di pianificazione associate ai movimenti di registrazione progetto che sono stati registrati.

> [!NOTE]  
> Ciò richiede che la casella di controllo **Applica collegamento di utilizzo** sia stata selezionata per il progetto. Per ulteriori informazioni, vedere [Impostare progetti](projects-how-setup-jobs.md).  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni progetti**, quindi scegli il collegamento correlato.  
2. Selezionare una registrazione progetti pertinente, quindi scegliere l'azione **Movimenti contabili**.  
3. Nella pagina **Movimenti contabili progetto** scegliere l'azione **Mostra righe di pianificazione progetto collegate**.

## Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

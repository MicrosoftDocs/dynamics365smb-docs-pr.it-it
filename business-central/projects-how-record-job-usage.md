---
title: Registrare il consumo o l'utilizzo di articoli e di risorse nella commessa
description: Questo articolo descrive come registrare il consumo o l'utilizzo degli articoli o delle risorse nelle commesse nella gestione progetti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# Registrare il consumo o l'utilizzo per le commesse

Dalla pagina **Scheda commessa**, è possibile aprire la pagina **Righe pianificazione commessa** per rivedere e registrare l'utilizzo delle varie parti della commessa. Queste informazioni vengono aggiornate automaticamente quando modifichi e trasferisci informazioni tra commesse e registrazioni commesse o fatture di commessa. Questo richiede che sia stata attivato l'interruttore **Applica collegamento utilizzo per impostazione predefinita** nella pagina **Setup commesse**. Per ulteriori informazioni vedi [Impostazione di commesse](projects-how-setup-jobs.md).  

Ad esempio, per le righe di pianificazione di tipo **Budget**, puoi immettere la quantità di una risorsa e specificare la quantità da trasferire nelle registrazioni commesse. Se il tipo di righe di pianificazione è **Fatturabile**, puoi immettere la quantità della risorsa e specificare la quantità da trasferire in una fattura. Per ulteriori informazioni sulla fatturazione al cliente, vedi [Fatturazione di commesse](projects-how-invoice-jobs.md). Confrontando la quantità originale, la quantità residua o la quantità registrata è possibile rivedere rapidamente le informazioni sull'utilizzo. Per ulteriori informazioni sulla stima dei valori a budget durante la pianificazione, vedi [Gestire i budget delle commesse](projects-how-manage-budgets.md).  

Di seguito viene descritto come registrare le quantità e i costi (previsti) effettivi con la registrazione delle commesse. In alternativa puoi utilizzare i documenti di acquisto per registrare l'acquisto di una commessa. Per ulteriori informazioni vedi [Gestire gli approvvigionamenti delle commesse](projects-how-manage-project-supplies.md).

## Per registrare l'utilizzo per una riga di pianificazione commessa di tipo Budget

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Commesse**, quindi scegli il collegamento correlato.  
2. Seleziona la commessa, quindi scegli l'azione **Righe pianificazione commessa**. 
3. Selezionare una riga di pianificazione commessa di tipo **Budget** o **Budget e fatturabile** per la quale si desidera registra l'utilizzo.   

    > [!NOTE]
    > È inoltre possibile registrare l'utilizzo per una riga pianificazione commessa di tipo **Fatturabile**. In genere, queste righe vengono utilizzate per creare fatture, ma è anche possibile trasferire le informazioni a una registrazione. Per ulteriori informazioni vedi [Fatturazione di commesse](projects-how-invoice-jobs.md) 

4. Nel campo **Qtà da trasferire per registrazione**, immetti la quantità da trasferire. La quantità di default è il valore che si immette nel campo **Quantità**.

    Il campo **Quantità residua** mostra la quantità che rimane per completare la commessa e da trasferire nelle registrazioni.
5. Scegliere l'azione **Crea righe registrazioni commesse**.

    > [!TIP]
    > Se si aggiungono più righe di pianificazione commessa per questa commessa, attendere fino a quando non sono state aggiunte tutte le righe di pianificazione commessa.
6. Nella pagina **Trasferimento commessa a riga pianificazione** compilare i campi in base alle esigenze, quindi scegliere **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Scegliere l'azione **Apri registrazioni commesse**.  
8. Nella pagina **Registrazioni commesse**, selezionare la riga pertinente e scegliere l'azione **Registra**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Nella pagina **Righe pianificazione commessa**, esaminare l'utilizzo registrato osservando i campi **Quantità**, **Quantità residua** e **Qtà da trasferire per registrazione**.  
10. Ripetere i passaggi da 3 a 8 per registrare altri utilizzi.  

## Per creare le righe delle registrazioni delle commesse manualmente

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni commesse**, quindi scegli il collegamento correlato.  
2. Nel campo **Nome batch** scegliere un nome batch di registrazioni commesse pertinente.  
3. In una nuova riga, immettere il numero di documento, il numero di commessa, il numero di task commessa, il tipo e la quantità del tipo consumata.  
4. Una volta completate le righe di registrazione commessa, scegliere l'azione **Registra**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Per visualizzare le stime di utilizzo della commessa e gli aggiornamenti della registrazione

È possibile visualizzare l'utilizzo della commessa fino al completamento di un progetto in un unico passaggio. A questo scopo, utilizzare il processo batch **Commessa - Calc. utilizzo residuo** per tutti i task fino al termine della commessa incluso.  

In questo modo è possibile tenere traccia e confrontare le stime iniziali rispetto ai risultati effettivi ed apportare modifiche o creare nuovi movimenti in base alle esigenze. Ad esempio, è possibile che si sia stimato che una commessa richieda 10 ore e ad oggi siano state impiegate 15 ore. È possibile aggiungere le cinque ore in più nella riga di registrazione esistente o creare una nuova riga registrazioni per indicare le cinque ore come straordinario, ovvero un altro tipo di lavoro. Vengono calcolati il costo e il prezzo appropriati ed è quindi possibile contabilizzarli nella registrazione.  

> [!NOTE]  
> I movimenti articoli creano movimenti contabili articoli e riducono la quantità di inventario. Il processo batch **Registra costo magazzino in C/GL** trasferisce il costo dal magazzino alla contabilità generale. I movimenti risorse creano movimenti contabili risorse.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni commesse**, quindi scegli il collegamento correlato.  
2. Selezionare una registrazione commessa corrispondente, quindi scegliere l'azione **Calc. utilizzo residuo**.  
3. Nella pagina **Commessa - Calc. utilizzo residuo**, immettere il numero di documento e la data di registrazione che deve essere inserita nelle registrazioni, quindi scegliere **OK**.  
4. Aggiornare le registrazioni con tutte le necessarie modifiche.  
5. Scegliere **Registra**.

## Creare inventario e warehouse per le righe di pianificazione per una commessa

Per creare documenti di selezione magazzino e warehouse per il processo, l'amministratore deve abilitare **Aggiornamento funzionalità: abilitazione del prelievo magazzino e warehouse da commesse** nella pagina **Gestione funzionalità**.

La funzione aggiunge le azioni **Crea prelievo magazzino** e **Crea prelievo warehouse** alla **Scheda commessa**. Per creare o registrare un documento di prelievo, utilizzare le azioni **Righe stoccaggio/prelievo/movimento** o **Righe prelievo registrate**. Per ulteriori informazioni vedi [Flussi per produzione, assemblaggio e attività lavorative](design-details-internal-warehouse-flows.md).

È possibile usare le azioni nelle seguenti condizioni:

* Lo **Stato** del lavoro è **Apri**.
* Il **Tipo di riga** della riga di pianificazione del lavoro è **Bilancio** o **Sia budget sia fatturabile**.
* Il **Tipo** della riga di pianificazione del lavoro è **Articolo**.
* **Richiesto prelievo** è abilitata per la relativa posizione.
* **Stoccaggi e prelievi guidati** è disabilitata.

> [!NOTE] 
> Sebbene l'impostazione sia chiamata **Richiesto prelievo**, è comunque possibile registrare il consumo direttamente dalla riga del giornale di registrazione commessa per l'ubicazione. Se l'ubicazione è impostata in modo da richiedere l'elaborazione dei prelievi ma non l'elaborazione delle spedizioni, utilizzare la pagina **Prelievi magazzino** per organizzare e stampare le informazioni di prelievo. Puoi anche utilizzare la pagina per inserire e pubblicare il risultato del prelievo, che a sua volta registra il consumo degli articoli. 
> 
> Se l'ubicazione è impostata in modo da richiedere l'elaborazione di prelievi e di spedizioni, indicando che hai scelto i campi **Richiesta prelievo** e **Richiesta spedizione** nella pagina **Scheda ubicazione**, usa la pagina **Prelievo warehouse** per gestire il prelievo. I prelievi warehouse sono simili ai prelievi in magazzino. La differenza è che, anziché pubblicare le informazioni sul prelievo, registri il prelievo. Questa registrazione non registra il consumo, ma rende gli articoli disponibili per la pubblicazione. Il responsabile di warehouse può utilizzare i prospetti prelievi per organizzare le informazioni di prelievo prima di creare le istruzioni di prelievo dalla singola warehouse

## Per esaminare le righe di pianificazione per un movimento contabile commessa

Dopo avere registrato le righe di registrazione commessa registrate, è possibile visualizzare le righe di pianificazione associate ai movimenti di registrazione commesse che sono stati registrati.

> [!NOTE]  
> Ciò richiede che la casella di controllo **Applica collegamento di utilizzo** sia stata selezionata la commessa. Per ulteriori informazioni, vedere [Impostare le commesse](projects-how-setup-jobs.md).  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni commesse**, quindi scegli il collegamento correlato.  
2. Selezionare una registrazione commessa corrispondente, quindi scegliere l'azione **Mov. contabili**.  
3. Nella pagina **Movimenti contabili commesse** scegliere l'azione **Mostra righe pianificazione commessa collegate**.

## Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Lavorare con periodi di inventario
description: È possibile controllare l'intervallo temporale durante il quale si possono registrare modifiche al magazzino defininendo periodi di magazzino.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="work-with-inventory-periods"></a>Lavorare con periodi di inventario

I periodi di magazzino definiscono un periodo di tempo durante il quale è possibile registrare modifiche al magazzino. Un periodo di magazzino è definito dalla data in cui termina, ovvero la data di fine. Quando si Chiudi un periodo di inventario, non è possibile registrare alcuna modifica all'inventario, prevista o fatturata, prima di questa data di fine. Non è possibile registrare nuovi valori nell'inventario prima della data di scadenza. Se nel periodo chiuso sono presenti voci di articoli aperti, ovvero quantità positive che non sono ancora state applicate alle transazioni in uscita, è comunque possibile applicare quantità in uscita a queste voci, anche se il periodo è chiuso.  

Nelle sezioni successive viene descritto come effettuare le seguenti operazioni:

* Creare periodi di magazzino.  
* Chiudere periodi di magazzino.  
* Riaprire periodi di magazzino.  

## <a name="to-create-an-inventory-period"></a>Per creare un periodo di magazzino

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Periodi di magazzino**, quindi scegli il collegamento correlato.  
2. Creare una nuova riga.  
3. Nel campo **Data fine** immettere l'ultima data del periodo di magazzino che si desidera definire. Quando il periodo è chiuso, non sarà possibile registrare le variazioni di inventario prima di tale data.  
4. Nel campo **Nome** immettere un nome descrittivo. Scegli il pulsante **OK**.  

## <a name="to-close-inventory-periods"></a>Per Chiudi periodi di inventario

Il campo **Chiuso** indica se il periodo di magazzino è chiuso, ovvero se non è più possibile apportare modifiche al relativo valore. Non puoi modificare questo campo.  

Puoi Chiudi qualsiasi periodo di inventario, se si verifica quanto segue:  

* Non devono esserci movimenti contabili articoli in uscita, ovvero giacenze negative, nel periodo.  
* Il costo di tutti gli articoli deve essere stato rettificato tramite il processo batch **Rettifica costo - Mov. art.**.  

Questo significa che tutte le quantità relative a transazioni in uscita, ad esempio ordini di vendita, trasferimenti in uscita, fatture di vendita, resi di acquisto o note di credito di acquisto, devono essere collegate a quantità esistenti in magazzino.  

### <a name="to-close-an-inventory-period"></a>Per chiudere un periodo di magazzino

1. Prima di chiudere un periodo di magazzino, scegliere l'azione **Rettifica costo - Movimenti articoli** per assicurarsi di registrare tutte le rettifiche dei costi.

    Eseguire il report  **Chiudi Periodo di inventario – Test** per determinare se ci sono voci di articoli in uscita aperte nel periodo di inventario o articoli il cui costo non è stato ancora modificato.  
2. Scegliere l'azione **Report test**.  

    Eseguire il processo batch **Registra costo magazzino in C/G** per fare in modo che tutti i costi vengano registrati nella contabilità generale.  
3. Scegliere l'azione **Registra magazzino in C/G**.  
4. Nella pagina **Periodi magazzino** selezionare il periodo di magazzino che si desidera chiudere.  
5. Scegliere l'azione **Chiudi periodo**. Dopo la chiusura del periodo di inventario, non è possibile registrare le variazioni di inventario prima della data di fine. Prima di chiudere il periodo di magazzino, è necessario rettificare il costo di tutti gli articoli tramite il processo batch **Rettifica costo - Mov. art.**.  
6. Fare clic su **Sì** per confermare la chiusura del periodo oppure su **No** per annullarla.  
7. Il periodo di inventario è chiuso e al termine viene visualizzato un messaggio di conferma.  

## <a name="reopening-inventory-periods"></a>Riapertura dei periodi di inventario
Dopo aver chiuso il periodo di inventario, non è possibile eliminarlo. È tuttavia possibile riaprirlo se si desidera consentire la registrazione prima della data di fine del periodo stesso. Riaprendo un periodo vengono riaperti anche tutti i periodi con date di fine successive a quella del periodo riaperto.  

### <a name="to-reopen-an-inventory-period"></a>Per riaprire un periodo di magazzino
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Periodi di magazzino**, quindi scegli il collegamento correlato.  
2. Selezionare il periodo di magazzino che si desidera riaprire.  
3. Scegliere l'azione **Riapri periodo**. Confermare che si desidera riaprire il periodo.  
4. Vengono riaperti anche tutti i periodi con date di fine successive a quella del periodo selezionato.  

## <a name="see-also"></a>Vedere anche
[Dettagli di progettazione: periodi di inventario](design-details-inventory-periods.md)    
[Finanze](finance.md)    
[Magazzino](inventory-manage-inventory.md)    
[Utilizzare Financials](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

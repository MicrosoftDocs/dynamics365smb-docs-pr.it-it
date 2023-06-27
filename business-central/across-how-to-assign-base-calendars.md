---
title: Impostare i calendari di base
description: 'Puoi assegnare un calendario di base alla tua società e ai partner aziendali, per calcolare le date di consegna e ricevimento in base ai giorni lavorativi specificati.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7600, 7601, 7602, 5703'
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="set-up-base-calendars"></a>Impostare i calendari di base

È possibile assegnare un calendario di base alla società e ai partner commerciali, quali clienti, fornitori o magazzini. I giorni lavorativi specificati nel calendario verranno utilizzati per il calcolo delle date di consegna e di carico nelle righe dei futuri ordini di vendita, di acquisto, di trasferimento e di produzione. L'operazione principale da eseguire per impostare un nuovo calendario di base consiste nello specificare e definire i giorni non lavorativi.  

## <a name="to-set-up-a-base-calendar"></a>Per impostare un calendario base

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Calendario base**, quindi scegli il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  
3.  Compilare il campo **Codice**.  
4. Scegliere l'azione **Mantenere variazioni calendario base**.
5. Nella pagina **Variazioni calendario base**, utilizzare il campo **Sistema ricorrente** per contrassegnare una data o un giorno particolare come giorno non lavorativo ricorrente. È possibile selezionare l'opzione **Ricorrente annuale** o **Ricorrente settimanale**.  

    Se si seleziona **Ricorrente annuale**, sarà necessario immettere anche la data pertinente nel campo **Data**.  

    Se si seleziona **Ricorrente settimanale**, sarà necessario selezionare anche il giorno della settimana pertinente nel campo **Giorno**. Se si lascia vuoto il campo, sarà necessario compilare il campo **Data**. Il campo **Giorni** viene compilato automaticamente.  

Quando si inserisce un movimento, il campo **Non lavorativo** viene selezionato. È possibile rimuovere il segno di spunta per impostarlo come giorno lavorativo.  
 Quando si torna alla Scheda Calendario Base, si noterà che le date impostate come giorni non lavorativi sono state aggiornate. Tali movimenti sono ora visualizzati in rosso e il campo **Non lavorativo** è selezionato.  

> [!NOTE]  
>  Quando si imposta un nuovo calendario di base, è possibile selezionare e copiare righe da un calendario esistente. È possibile effettuare questa operazione nella pagina **Variazioni calendario base** pertinente.  

> [!IMPORTANT]  
>  Qualsiasi calendario di base definito per il fornitore o l'ubicazione influisce sul modo in cui le date vengono calcolate e arrotondate in base ai giorni lavorativi.
Specifica una formula di data per il tempo necessario per il rifornimento dell'articolo. Viene utilizzato per il calcolo del campo **Data carico pianificato**, se calcolato in avanti, e del campo **Order Date**, se calcolato a ritroso. Vedere [Calcolo lead time](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation"></a>Calcolo lead time

Qualsiasi calendario di base definito per il fornitore o l'ubicazione influisce sul modo in cui le date vengono calcolate e arrotondate in base ai giorni lavorativi. Di conseguenza, i due campi data principali nelle righe ordine di acquisto vengono calcolati come segue secondo condizioni diverse.

|Direzione di calcolo|Calendario del fornitore definito|Calendario del fornitore non definito|
|---------------------|-----------------------|---------------------------|
|Avanti|data di carico pianificata = data dell'ordine + lead time fornitore (in base al calendario del fornitore e arrotondato al giorno lavorativo successivo prima nel calendario fornitore, quindi nel calendario ubicazione)|data di carico pianificata = data ordine + lead time fornitore (in base al calendario ubicazione)|
|Aut. fine|data dell'ordine = data di carico pianificata - lead time fornitore (in base al calendario del fornitore e arrotondato al giorno lavorativo precedente prima nel calendario fornitore, quindi nel calendario ubicazione)|data ordine = data di carico pianificata - lead time fornitore (in base al calendario ubicazione)|

> [!NOTE]
> Oltre al calcolo del lead time che influisce sulla data di carico pianificata e sulla data ordine, come illustrato nella tabella di cui sopra, il tempo di gestione warehouse e lead time di sicurezza possono essere aggiunti alle formule per comporre il valore nel campo **Data carico prevista** come segue: Data carico pianificato + Lead time di sicurezza + Tempo gestione entrata da magazzino = Data carico prevista..

> [!Important]
> Se l'ubicazione utilizza un calendario significativamente diverso rispetto ai fornitori, è importante impostare calendari specifici per tali fornitori, per calcolare i lead time fornitore ottimali. Per ulteriori informazioni su come impostare i calendari fornitore, vedere [Per assegnare un calendario di base](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

Il contenuto del campo **Calcolo lead time** viene copiato dalla scheda articolo o dalla scheda USK, se il lead time è definito per l'articolo, o nella pagina **Catalogo articolo fornitori**, se il lead time è definito per il fornitore.

## <a name="to-customize-a-calendar"></a>Per personalizzare un calendario
L'operazione principale da eseguire per personalizzare un calendario di base per la propria società, o per uno dei partner commerciali, è la modifica dello stato dei giorni lavorativi e non lavorativi.

Mentre un calendario di base standard mostra solitamente tutti i sabati come giorni non lavorativi, il calendario personalizzato di una determinata ubicazione potrebbe ad esempio riportare come giorni lavorativi tutti i sabati dei mesi di novembre e dicembre e del mese precedente il periodo di ferie.

Nella seguente procedura viene utilizzato l'esempio di un'ubicazione. L’esempio presuppone che si sia già provveduto all' assegnazione di un calendario di base al magazzino.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Aprire l'ubicazione da aggiornare e selezionare il campo **Calendario personalizzato**. Si noti che un calendario deve essere selezionato nel campo **Codice calendario base** .
3. Nella pagina **Voci calendario personalizzato** visualizzata, scegliere l'azione **Mantenere variazioni calendario personalizzato**.
4. In **Variazioni calendario personalizzato**, aggiungere le righe per le voci di calendario personalizzato.

    Quando si inserisce una nuova riga, la casella di controllo **Non lavorativo** è selezionata. È possibile deselezionare la casella di controllo se si desidera modificare lo stato di tale data in in giorno lavorativo.

    Utilizzare il campo **Sistema ricorrente** per impostare una data o un giorno particolare come giorno non lavorativo ricorrente. È possibile selezionare l'opzione **Ricorrente annuale** o **Ricorrente settimanale**.

    Se si seleziona **Ricorrente annuale**, sarà necessario immettere anche la data pertinente nel campo **Data**. Se si seleziona **Ricorrente settimanale**, sarà necessario selezionare anche il giorno della settimana pertinente nel campo **Giorno**. Se si lascia vuoto il campo, sarà necessario compilare il campo **Data**. Il campo **Giorno** viene compilato automaticamente. Tale opzione può essere utile per contrassegnare una singola data come giorno non lavorativo (o lavorativo).

5. Scegliere il pulsante **OK**.

Nella pagina **Voci calendario personalizzato** si noterà che le date sono state aggiornate in base alle variazioni specificate.

Quando si torna alla scheda Ubicazione, sarà possibile osservare che il campo **Calendario personalizzato** ora contiene la parola **Sì** ad indicare che è stato impostato un calendario personalizzato.

> [!Important]
> Se non si compila il campo **Cod. ubicazione** nella riga di un ordine, verrà utilizzato il calendario della propria società.


Se non si compila il campo **Cod. spedizioniere** nella riga dell'ordine, verrà utilizzato il calendario della propria società.

> [!NOTE]  
> Se si apportano modifiche a un calendario di base per cui esistono variazioni personalizzate, tutti i calendari personalizzati esistenti verranno aggiornati automaticamente.

## <a name="to-assign-a-base-calendar"></a>Per assegnare un calendario di base
La procedura riportata di seguito programma come esempio le date di consegna nelle righe dell'ordine di vendita per un cliente.

I calendari di base vengono assegnati a società, clienti, fornitori, ubicazioni e spedizionieri come segue:  

-   Nelle schede **Cliente** e **Informazioni società** , il calendario di base è assegnato nella Scheda dettaglio **Spedizione**.  
-   Nella scheda **Fornitore** , il calendario di base è assegnato nella Scheda dettaglio **Carico**.  
-   Nella scheda **Ubicazione** , il calendario di base è assegnato nella Scheda dettaglio **Warehouse**.  
-   Nella pagina **Spedizionieri** , il calendario di base è assegnato nella pagina **Servizi spedizioniere** .  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Clienti**, quindi scegli il collegamento correlato.  
2.  Aprire la scheda **Cliente** per la quale assegnare un calendario di base.  
3.  Nella Scheda dettaglio **Spedizione**, nel campo **Codice calendario base** , selezionare il calendario di base che si intende assegnare.  

> [!IMPORTANT]  
>  -   Se non si assegna un calendario di base a una società, tutte le date verranno calcolate come giorni lavorativi.  
> -   Se non si specifica un'ubicazione nella riga di un ordine, tutte le date verranno calcolate come giorni lavorativi.  
> -   Qualsiasi calendario di base definito per il fornitore o l'ubicazione influisce sul modo in cui le date vengono calcolate e arrotondate in base ai giorni lavorativi.

> [!NOTE]  
>  Prima di creare voci di calendario personalizzate, è innanzitutto necessario assegnare un calendario di base alla società.  

## <a name="see-also"></a>Vedere anche
[Acquisti](purchasing-manage-purchasing.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

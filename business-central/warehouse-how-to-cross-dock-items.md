---
title: Sottoporre gli articoli a cross-dock
description: La funzionalità di cross-docking è disponibile se l'ubicazione è stata impostata in modo da richiedere l'elaborazione degli stoccaggi e dei carichi warehouse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15, 5703, 7302, 7332, 5768'
ms.date: 04/01/2021
ms.author: edupont
---
# Sottoporre gli articoli a cross-dock

Gli articoli cross-dock sono articoli che ricevi e spedisci senza stoccarli. I processi di stoccaggio e prelievo richiedono una gestione limitata degli articoli. È possibile sottoporre gli articoli a cross-dock per le spedizioni e per gli ordini di produzione.

## Zone e collocazioni cross-dock

Se utilizzi le collocazioni, imposta almeno una collocazione cross-dock, quindi specifica la collocazione nel campo **Codice collocazione cross-dock** sulle tue ubicazioni. Se utilizzi stoccaggi e prelievi diretti, configura una zona di cross-dock.

Quando prepari una spedizione o prelevi gli articoli per la produzione e usi le collocazioni, l'articolo viene automaticamente prelevato da una collocazione di cross-dock prima di qualsiasi altra collocazione. Prima di prelevare gli articoli dall'area in cui vengono solitamente immagazzinati, è necessario esaminare l'area di cross-dock per verificare se gli articoli necessari sono disponibili in tale ubicazione.  

Se sono state calcolate le quantità di cross-dock, durante la registrazione del carico vengono create delle righe di stoccaggio nella collocazione di cross-docking per i calcoli di cross-docking. Le altre righe di stoccaggio vengono create seguendo la normale procedura.  

## Righe cross-dock selezionate per una ricevuta

<!--If a receipt contains items that you want to store, that is, items that you are not cross-docking, you must register a put-away for those items.-->

Se si desidera registrare gli articoli di cross-docking immediatamente in modo da renderli disponibili per il prelievo, è necessario registrare anche uno stoccaggio per i rimanenti articoli della riga di carico, ovvero quelli che devono essere effettivamente posti a magazzino. Se si sottopone a cross-dock solo alcuni articoli di una riga di carico, è quindi necessario stoccare gli articoli rimanenti il più rapidamente possibile. In alternativa, è possibile impostare criteri di logistica di warehouse che favoriscano il cross-dock di intere righe di carico ogni qualvolta possibile.

Nell'istruzione di stoccaggio, elimina le righe dell'istruzione Prendere e Mettere per ciascuna riga di carico degli articoli da stoccare. Puoi creare le righe delle istruzioni in un secondo tempo come righe di stoccaggio dal prospetto stoccaggi o dal carico registrato. Una volta eliminate le righe delle istruzioni, puoi eseguire lo stoccaggio e registrare le righe per gli articoli di cross-dock.  

## Informazioni sul prospetto stoccaggi

Se attivi l'interruttore **Usa prospetto stoccaggi** nella pagina Scheda ubicazione e hai registrato il carico con i cross-dock calcolati, tutte le righe di carico verranno rese disponibili nel prospetto. Le informazioni su cross-dock andranno perse e non potranno essere ricreate. Pertanto, per utilizzare la funzionalità di cross-dock, è consigliabile inoltrare le righe al prospetto stoccaggi eliminando le istruzioni di stoccaggio anziché utilizzare la funzione di inoltro automatico fornita dal campo **Usa prospetto stoccaggi**.  

Se registri il carico warehouse e l'interruttore **Usa prospetto stoccaggi** è disattivato, gli articoli da sottoporre a cross-dock vengono visualizzati come righe separate nell'istruzione di stoccaggio. Il campo **Informazioni cross-dock** su ciascuna riga di stoccaggio mostra se la riga contiene:

* Articoli cross-dock.
* Tutti gli articoli di un carico devono essere immagazzinati.
* Alcuni articoli di un carico devono essere immagazzinati e altri devono essere sottoposti a cross-dock.

I dipendenti possono facilmente capire perché l'intera quantità non viene immagazzinata.  

[!INCLUDE [prod_short](includes/prod_short.md)] non mantiene separati i record per gli articoli sottoposti a cross-dock ma vengono registrati come istruzioni di stoccaggio ordinarie.  

## Per impostare la warehouse per il cross-docking  

1. Se usi le collocazioni, imposta almeno una collocazione di cross-dock. Se utilizzi stoccaggi e prelievi diretti, configura una zona di cross-dock.  

    Per una collocazione cross-dock è selezionato il campo **Collocazione cross-dock** e devono essere selezionati i tipi di collocazione **Ricevi** e **Prelievo**. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).  

    Se si utilizzano le zone, creare una zona per le collocazioni cross-dock e selezionare il campo **Zona collocazione cross-dock**. Per ulteriori informazioni, vedere [Impostare ubicazioni per l'utilizzo di collocazioni](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazione**, quindi scegli il collegamento correlato.  
3. Nella pagina **Ubicazione** selezionare l'ubicazione in cui si desidera impostare la warehouse per il cross-dock, quindi scegliere l'azione **Modifica**.  
4. Nella Scheda dettaglio **Warehouse** attiva l'interruttore **Usa cross-docking** e compila il campo **Calc. scadenza cross-dock** specificando l'intervallo di tempo per la ricerca delle opportunità di cross-dock.

    L'opzione **Usa cross-docking** è disponibile solo se i campi **Richiesto carico**, **Richiesta spedizione** **Richiesto prelievo** e **Richiesto stoccaggio** sono selezionati.  

5.  Se si utilizzano le collocazioni, nella Scheda dettaglio **Collocazioni** immettere nel campo **Codice collocazione cross-dock** il codice della collocazione da utilizzare come collocazione di default per il cross-dock.  
6.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Unità di stockkeeping**, quindi scegli il collegamento correlato.  
7.  Per ciascun articolo o unità di stockkeeping che si desidera sottoporre a cross-dock, selezionare l'articolo, quindi scegliere l'azione **Modifica**.
8. Nella pagina **Scheda unità di stockkeeping** selezionare la casella di controllo **Usa cross-docking**.  

> [!NOTE]  
>  È possibile utilizzare il cross-dock solo se l'ubicazione prevede l'elaborazione degli stoccaggi e dei carichi warehouse.  

## Per sottoporre a cross-dock gli articoli senza visualizzare le opportunità  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2.  Creare un carico warehouse per un articolo arrivato e che può essere sottoposto a cross-dock. Per ulteriori informazioni, vedere [Ricevere articoli](warehouse-how-receive-items.md).  
3.  Compilare il campo **Qtà da ricevere** e scegliere l'azione **Calcola cross-dock**.  

    I documenti di origine in uscita in cui vengono richiesti gli articoli programmati per uscire dalla warehouse entro il periodo di tempo indicato nella formula di data vengono identificati.  [!INCLUDE[prod_short](includes/prod_short.md)] calcola le quantità affinché sia possibile sottoporre a cross-dock il maggior numero possibile di articoli in modo da evitare lo stoccaggio, senza l'accumulo di un numero eccessivo di articoli nell'area di cross-dock. Il valore nel campo **Qtà per cross-dock** corrisponde pertanto alla somma di tutte le righe in uscita per cui viene richiesto l'articolo entro il periodo di tolleranza meno la quantità degli articoli che sono già stati posizionati nell'area di cross-dock oppure al valore contenuto nel campo **Qtà da ricevere** della riga di carico, a seconda di quale valore sia inferiore. Non è possibile sottoporre a cross-dock una quantità di articoli superiore a quella ricevuta.  

4.  Se si desidera sottoporre a cross-dock la quantità suggerita, registrare il carico. In alternativa, è possibile scegliere di modificare la quantità da sottoporre a cross-dock impostando un valore superiore o inferiore, quindi registrare il carico.  

    A questo punto, le quantità da sottoporre a cross-dock vengono visualizzate come righe nell'istruzione di stoccaggio, supponendo che il campo **Usa prospetto stoccaggi** sia deselezionato. Anche le quantità non sottoposte a cross-dock vengono visualizzate come righe nell'istruzione di stoccaggio.  

    Se si utilizzano le collocazioni, gli articoli sottoposti a cross-dock vengono assegnati alla collocazione di cross-dock di default specificata nella scheda ubicazione.  

5.  Eliminare le righe **Prendere** e **Mettere** per gli articoli che non verranno sottoposti a cross-dock.  
6.  Stampare l'istruzione di stoccaggio per le righe rimanenti e posizionare le quantità del carico da immagazzinare nelle collocazioni o nell'area appropriata della warehouse. Posizionare gli articoli di cross-dock nell'area o nella collocazione designata dal criterio di logistica di warehouse. Talvolta, i criteri di logistica di warehouse prevedono che tali articoli vengano lasciati nell'area di carico.  
7.  Per registrare gli articoli sottoposti a cross-dock come articoli stoccati e disponibili per il prelievo, scegliere l'azione **Registra**.  

## Per sottoporre a cross-dock gli articoli dopo la visualizzazione delle opportunità  
1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2.  Creare un carico warehouse per un articolo arrivato e che può essere sottoposto a cross-dock. Per ulteriori informazioni, vedere [Ricevere articoli](warehouse-how-receive-items.md).  

    Si desidera visualizzare le righe dei documenti di origine in cui viene richiesto l'articolo prima di registrare il carico.  
3.  Scegliere l'azione **Calcola cross-dock**.  

    Nella pagina **Opportunità di cross-dock** sono riportati i dettagli essenziali relativi alle righe per cui viene richiesto l'articolo, tra cui il tipo di documento, la quantità richiesta e la data di scadenza. Sulla base di queste informazioni, è possibile stabilire la quantità di articoli da sottoporre a cross-dock, dove posizionare gli articoli nell'area di cross-dock o come raggrupparli.  

4.  Scegliere l'azione **Autocompilazione qtà. fino a cross-dock** per vedere come vengono calcolate le quantità nelle righe di carico. Quando si modifica il numero di articoli nel campo **Qtà per cross-dock** di ogni riga, il calcolo viene aggiornato mentre si apportano le modifiche. Ciò non significa che lo specifico ordine di spedizione o di produzione riceverà effettivamente la quantità di articoli suggerita per il cross-dock, in quanto tali modifiche vengono apportate esclusivamente a scopo di test. Il processo può tuttavia fornire informazioni utili nel caso in cui siano coinvolte più unità di misura.  
5.  Se si desidera impegnare una quantità dell'articolo per una determinata riga ordine, posizionare il cursore sulla riga e scegliere l'azione **Impegno**. Nella pagina **Impegni** è possibile impegnare una qualsiasi quantità disponibile dell'articolo per questo ordine specifico. Tale impegno viene considerato come qualsiasi altro impegno e non ha priorità più alta perché è stato creato in relazione al cross-docking. Per ulteriori informazioni, vedere [Prenotare articoli](inventory-how-to-reserve-items.md).   
6.  Al termine delle operazioni di ricalcolo o impegno, fare clic su **OK** per immettere il calcolo rettificato nel campo **Qtà per cross-dock** della riga di carico oppure fare clic su **Annulla** per tornare al carico warehouse, dove è possibile calcolare nuovamente il cross-dock, se necessario.  
7.  A questo punto, registrare il carico e procedere con l'istruzione di stoccaggio come descritto nei passaggi da 3 a 7 nella sezione “Per sottoporre a cross-dock gli articoli senza visualizzare le opportunità”.  

> [!NOTE]  
>  nel processo di stoccaggio nella warehouse è possibile continuare a modificare le quantità da immagazzinare o da sottoporre a cross-dock a seconda delle esigenze. È ad esempio possibile scegliere di sottoporre a cross-dock una quantità aggiuntiva per accelerare la registrazione del cross-dock.  

## Per visualizzare gli articoli sottoposti a cross-dock in una spedizione o in un prospetto prelievi  
Se si utilizzano le collocazioni, ogni volta che si visualizza una spedizione o il prospetto prelievi, è possibile verificare il calcolo aggiornato della quantità di ciascun articolo nelle collocazioni di cross-dock. Tali informazioni risultano particolarmente utili se si è in attesa di ricevere un articolo. Quando l'articolo è finalmente disponibile nella collocazione di cross-dock, è possibile creare rapidamente un prelievo per tutti gli articoli da spedire. Nel prospetto prelievi è possibile modificare le righe in base alle esigenze e creare un prelievo.  

Durante il prelievo degli articoli per la spedizione, è necessario cercare gli articoli prima nell'area di cross-dock. Se, durante il processo di carico, sono stati esaminati i documenti di origine alla base del cross-dock, si sa con maggiore certezza se l'articolo è reperibile o meno nell'area di cross-dock.  

Quando viene rilasciato un ordine di produzione, le righe vengono rese disponibili nel prospetto prelievi e, se si esamina il campo **Qtà in collocazione cross-dock** è possibile stabilire se gli articoli attesi sono arrivati e sono stati posizionati nelle collocazioni di cross-dock. Quando si crea un'istruzione di prelievo, viene suggerito automaticamente di prelevare prima gli articoli sottoposti a cross-dock e solo in seguito viene eseguita la ricerca degli articoli nelle collocazioni di immagazzinamento.  

Se non si utilizzano le collocazioni, si consiglia di controllare periodicamente l'area di cross-dock o basarsi sulle notifiche di carico per verificare se gli articoli per la produzione sono arrivati.  

## Vedere anche  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
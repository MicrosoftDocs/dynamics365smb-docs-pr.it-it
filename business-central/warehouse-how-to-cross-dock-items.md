---
title: Sottoporre gli articoli a cross-dock
description: Scopri come ricevere e spedire articoli senza stoccarli.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# <a name="cross-dock-items"></a>Sottoporre gli articoli a cross-dock

Gli articoli cross-dock sono articoli che ricevi e spedisci senza stoccarli. I processi di stoccaggio e prelievo richiedono una gestione limitata degli articoli. È possibile sottoporre gli articoli a cross-dock per le spedizioni e per gli ordini di produzione.

## <a name="cross-dock-bins-and-zones"></a>Zone e collocazioni cross-dock

Se utilizzi le collocazioni, imposta almeno una collocazione cross-dock, quindi specifica la collocazione nel campo **Codice collocazione cross-dock** sulle tue ubicazioni. Se utilizzi stoccaggi e prelievi diretti, configura una zona di cross-dock.

Quando prepari una spedizione o prelevi gli articoli per la produzione e usi le collocazioni, l'articolo viene automaticamente prelevato da una collocazione di cross-dock prima di qualsiasi altra collocazione. Prima di prelevare gli articoli dall'area in cui vengono solitamente immagazzinati, è necessario esaminare l'area di cross-dock per verificare se gli articoli necessari sono disponibili in tale ubicazione.  

Se sono state calcolate le quantità di cross-dock, durante la registrazione del carico vengono create delle righe di stoccaggio nella collocazione di cross-docking per i calcoli di cross-docking. Le altre righe di stoccaggio vengono create seguendo la normale procedura.  

## <a name="cross-dock-select-lines-for-a-receipt"></a>Righe cross-dock selezionate per una ricevuta

Se si desidera registrare gli articoli di cross-docking immediatamente in modo da renderli disponibili per il prelievo, è necessario registrare anche uno stoccaggio per i rimanenti articoli della riga di carico, ovvero quelli che devono essere effettivamente posti a magazzino. Se si sottopone a cross-dock solo alcuni articoli di una riga di carico, è quindi necessario stoccare gli articoli rimanenti il più rapidamente possibile. In alternativa, è possibile impostare criteri di logistica di warehouse che favoriscano il cross-dock di intere righe di carico ogni qualvolta possibile.

Nell'istruzione di stoccaggio, elimina le righe dell'istruzione Prendere e Mettere per ciascuna riga di carico degli articoli da stoccare. Puoi creare le righe delle istruzioni in un secondo tempo come righe di stoccaggio dal prospetto stoccaggi o dal carico registrato. Una volta eliminate le righe delle istruzioni, puoi eseguire lo stoccaggio e registrare le righe per gli articoli di cross-dock.  

## <a name="about-the-put-away-worksheet-page"></a>Pagina Informazioni sul prospetto stoccaggi

Se attivi l'interruttore **Usa prospetto stoccaggi** nella pagina **Scheda ubicazione** e hai registrato il carico con i cross-dock calcolati, tutte le righe di carico verranno rese disponibili nel prospetto. Le informazioni su cross-dock andranno perse e non potranno essere ricreate. Pertanto, per utilizzare la funzionalità di cross-dock, è consigliabile inoltrare le righe al prospetto stoccaggi eliminando le istruzioni di stoccaggio anziché utilizzare la funzione di inoltro automatico fornita dal campo **Usa prospetto stoccaggi**.  

Se registri il carico warehouse e l'interruttore **Usa prospetto stoccaggi** è disattivato, gli articoli da sottoporre a cross-dock vengono visualizzati come righe separate nelle istruzioni di stoccaggio. Il campo **Informazioni cross-dock** su ciascuna riga di stoccaggio mostra se la riga contiene:

* Articoli cross-dock.
* Tutti gli articoli di un carico devono essere immagazzinati.
* Alcuni articoli di un carico devono essere immagazzinati e altri devono essere sottoposti a cross-dock.

[!INCLUDE [prod_short](includes/prod_short.md)] non conserva record separati per gli articoli sottoposti a cross-dock. Li registra come istruzioni di stoccaggio ordinarie.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Per impostare la warehouse per il cross-docking

1. Se usi le collocazioni, imposta almeno una collocazione di cross-dock. Se utilizzi stoccaggi e prelievi diretti, configura una zona di cross-dock.  

    Per una collocazione cross-dock è selezionato il campo **Collocazione cross-dock** e devono essere selezionati i tipi di collocazione **Ricevi** e **Prelievo**. Per ulteriori informazioni sulle collocazioni, vai a [Creare le collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazione](warehouse-how-to-set-up-bin-types.md).  

    Se si utilizzano le zone, creare una zona per le collocazioni cross-dock e selezionare il campo **Zona collocazione cross-dock**. Per ulteriori informazioni sulle zone, vai a [Impostazione delle ubicazioni per usare le collocazioni](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ubicazione**, quindi scegli il collegamento correlato.  
3. Nella pagina **Ubicazione** selezionare l'ubicazione in cui si desidera impostare la warehouse per il cross-dock, quindi scegliere l'azione **Modifica**.  
4. Nella Scheda dettaglio **Warehouse** attiva l'interruttore **Usa cross-docking** e compila il campo **Calc. scadenza cross-dock** specificando l'intervallo di tempo per la ricerca delle opportunità di cross-dock.

    L'opzione **Usa cross-docking** è disponibile solo se i campi **Richiesto carico**, **Richiesta spedizione** **Richiesto prelievo** e **Richiesto stoccaggio** sono selezionati.  

5. Se usi le collocazioni, nella Scheda dettaglio **Collocazioni** immetti nel campo **Codice collocazione cross-dock** il codice della collocazione da utilizzare come collocazione predefinita per il cross-dock.  
6. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Unità di stockkeeping**, quindi scegli il collegamento correlato.  
7. Per ciascun articolo o unità di stockkeeping che si desidera sottoporre a cross-dock, selezionare l'articolo, quindi scegliere l'azione **Modifica**.
8. Nella pagina **Scheda unità di stockkeeping** selezionare la casella di controllo **Usa cross-docking**.  

> [!NOTE]  
>  È possibile utilizzare il cross-dock solo se l'ubicazione prevede l'elaborazione degli stoccaggi e dei carichi warehouse.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Per sottoporre a cross-dock gli articoli senza visualizzare le opportunità

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2. Creare un carico warehouse per un articolo arrivato e che può essere sottoposto a cross-dock. Per ulteriori informazioni sul ricevimento, vai a [Ricevere articoli](warehouse-how-receive-items.md).  
3. Compilare il campo **Qtà da ricevere** e scegliere l'azione **Calcola cross-dock**.  

    I documenti di origine in uscita in cui vengono richiesti gli articoli programmati per uscire dalla warehouse entro il periodo di tempo indicato nella formula di data vengono identificati. [!INCLUDE[prod_short](includes/prod_short.md)] calcola le quantità affinché sia possibile sottoporre a cross-dock il maggior numero possibile di articoli in modo da evitare lo stoccaggio, senza l'accumulo di un numero eccessivo di articoli nell'area di cross-dock. Il valore nel campo **Qtà per cross-dock** corrisponde pertanto alla somma di tutte le righe in uscita per l'articolo entro il periodo di tolleranza meno la quantità che è già stata posizionata nell'area di cross-dock oppure al valore contenuto nel campo **Qtà da ricevere** della riga di carico, a seconda di quale valore sia inferiore. Non è possibile sottoporre a cross-dock una quantità di articoli superiore a quella ricevuta.  

4. Per sottoporre a cross-dock la quantità suggerita, registra il carico. In alternativa, è possibile scegliere di modificare la quantità da sottoporre a cross-dock impostando un valore superiore o inferiore, quindi registrare il carico.  

    A questo punto, le quantità da sottoporre a cross-dock vengono visualizzate come righe nell'istruzione di stoccaggio, supponendo che il campo **Usa prospetto stoccaggi** sia deselezionato. Anche le quantità non sottoposte a cross-dock vengono visualizzate come righe nell'istruzione di stoccaggio.  

    Se si utilizzano le collocazioni, gli articoli sottoposti a cross-dock vengono assegnati alla collocazione di cross-dock di default specificata nella scheda ubicazione.  

5. Elimina le righe **Prendere** e **Mettere** per gli articoli che non verranno sottoposti a cross-dock.  
6. Stampare l'istruzione di stoccaggio per le righe rimanenti e posizionare le quantità del carico da immagazzinare nelle collocazioni o nell'area appropriata della warehouse. Posizionare gli articoli di cross-dock nell'area o nella collocazione designata dal criterio di logistica di warehouse. Talvolta, i criteri di logistica di warehouse prevedono che tali articoli vengano lasciati nell'area di carico.  
7. Per registrare gli articoli sottoposti a cross-dock come articoli stoccati e disponibili per il prelievo, scegliere l'azione **Registra**.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Per sottoporre a cross-dock gli articoli dopo la visualizzazione delle opportunità

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2. Crea un carico warehouse per un articolo arrivato e che può essere sottoposto a cross-dock.  

    Si desidera visualizzare le righe dei documenti di origine in cui viene richiesto l'articolo prima di registrare il carico.  
3. Scegliere l'azione **Calcola cross-dock**.  

   Nella pagina **Opportunità di cross-dock** sono riportati i dettagli essenziali relativi alle righe per cui viene richiesto l'articolo, tra cui il tipo di documento, la quantità richiesta e la data di scadenza. Sulla base di queste informazioni, è possibile stabilire la quantità di articoli da sottoporre a cross-dock, dove posizionare gli articoli nell'area di cross-dock o come raggrupparli.  

4. Scegli l'azione **Autocompilazione qtà. fino a cross-dock** per vedere come vengono calcolate le quantità nelle righe di carico. Quando modifichi il numero di articoli nel campo **Qtà per cross-dock** di ogni riga, il calcolo viene aggiornato. L'aggiornamento non significa che la spedizione o l'ordine di produzione riceveranno effettivamente gli articoli suggeriti per il cross-docking. È solo a scopo di test. Il processo può tuttavia fornire informazioni utili nel caso in cui siano coinvolte più unità di misura.  
5. Per impegnare una quantità dell'articolo per una riga ordine, scegli la riga e scegli l'azione **Impegno**. Sulla pagina **Prenotazione** impegna la quantità disponibile dell'articolo. L'impegno viene considerato come qualsiasi altro impegno e non ha priorità più alta perché è stato creato in relazione al cross-docking. Per ulteriori informazioni sugli impegni, vai a [Impegnare articoli](inventory-how-to-reserve-items.md).   
6. Al termine delle operazioni di ricalcolo o impegno, fai clic su **OK** per immettere il calcolo rettificato nel campo **Qtà per cross-dock** della riga di carico oppure fai clic su **Annulla** per tornare al carico warehouse e calcolare nuovamente il cross-dock.  
7. Registra il carico. Puoi procedere con l'istruzione di stoccaggio come descritto nei passaggi da 3 a 7 nella sezione [Per sottoporre a cross-dock gli articoli senza visualizzare le opportunità](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > nel processo di stoccaggio nella warehouse è possibile continuare a modificare le quantità da immagazzinare o da sottoporre a cross-dock a seconda delle esigenze. È ad esempio possibile scegliere di sottoporre a cross-dock una quantità aggiuntiva per accelerare la registrazione del cross-dock.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Per visualizzare gli articoli sottoposti a cross-dock in una spedizione o in un prospetto prelievi

Se usi le collocazioni, quando apri una spedizione o il prospetto prelievi, la quantità di ciascun articolo nelle collocazioni di cross-dock viene aggiornata. Quando l'articolo è disponibile nella collocazione di cross-dock, è possibile creare un prelievo per tutti gli articoli da spedire. Nel prospetto prelievi è possibile modificare le righe in base alle esigenze.  

Quando viene rilasciato un ordine di produzione, le righe vengono rese disponibili nel prospetto prelievi e il campo **Qtà in collocazione cross-dock** indica se gli articoli attesi sono arrivati e sono stati posizionati nelle collocazioni di cross-dock. Quando crei un'istruzione di prelievo, [!INCLUDE [prod_short](includes/prod_short.md)] suggerisce di selezionare prima gli articoli del cross-dock. Gli articoli nelle collocazioni di stoccaggio vengono suggeriti in seguito.  

Se non si utilizzano le collocazioni, ti consigliamo di controllare periodicamente l'area di cross-dock o basarsi sulle notifiche di carico per verificare se gli articoli per la produzione sono arrivati.  

## <a name="see-also"></a>Vedere anche

[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

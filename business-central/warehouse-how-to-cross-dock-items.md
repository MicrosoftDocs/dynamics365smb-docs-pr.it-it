---
title: 'Procedura: Articoli di cross-dock | Documenti Microsoft'
description: La funzionalità di cross-docking è disponibile se l'ubicazione è stata impostata in modo da richiedere l'elaborazione degli stoccaggi e dei carichi warehouse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 125d8e152f2bc745b248b3418849cc87422a4982
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391626"
---
# <a name="cross-dock-items"></a>Sottoporre gli articoli a cross-dock
La funzionalità di cross-docking è disponibile se l'ubicazione è stata impostata in modo da richiedere l'elaborazione degli stoccaggi e dei carichi warehouse.  

Quando vengono sottoposti a cross-dock, gli articoli vengono gestiti durante il carico e la spedizione senza essere mai immagazzinati effettivamente. Ciò consente di accelerare i tempi dei processi di stoccaggio e prelievo e di ridurre al minimo la gestione fisica degli articoli. È possibile sottoporre gli articoli a cross-dock sia per le spedizioni che per gli ordini di produzione. Quando si prepara una spedizione o si prelevano articoli per la produzione e si utilizzano le collocazioni, l'articolo viene automaticamente prelevato da una collocazione di cross-dock prima di qualsiasi altra collocazione. Prima di prelevare gli articoli dall'area in cui vengono solitamente immagazzinati, è necessario esaminare l'area di cross-dock per verificare se gli articoli necessari sono disponibili in tale ubicazione.  

Se sono state calcolate le quantità di cross-dock, durante la registrazione del carico vengono create delle righe di stoccaggio nella collocazione di cross-docking per i calcoli di cross-docking. Le altre righe di stoccaggio vengono create seguendo la normale procedura.  

Se si desidera registrare gli articoli di cross-docking immediatamente in modo da renderli disponibili per il prelievo, è necessario registrare anche uno stoccaggio per i rimanenti articoli della riga di carico, ovvero quelli che devono essere effettivamente posti a magazzino. Se si sottopone a cross-dock solo alcuni articoli di una riga di carico, è quindi necessario stoccare gli articoli rimanenti il più rapidamente possibile. In alternativa, è possibile impostare criteri di logistica di warehouse che favoriscano il cross-dock di intere righe di carico ogni qualvolta possibile.  

Nell'istruzione di stoccaggio è possibile eliminare, per ciascuna riga di carico, le righe di istruzione di prelievo e posizionamento relative ai carichi che devono essere posti a warehouse. Tali righe possono essere ricreate in un secondo tempo come righe di stoccaggio dal prospetto stoccaggi o dal carico registrato. Una volta eliminate, è possibile eseguire lo stoccaggio e registrare le righe relative agli articoli di cross-dock.  

Se è stato selezionato il campo **Usa prospetto stoccaggi** della scheda ubicazione e si è registrato il carico con i cross-dock calcolati, tutte le righe di carico verranno rese disponibili nel prospetto. Le informazioni su cross-dock andranno perse e non potranno essere ricreate. Pertanto, se si desidera utilizzare la funzionalità di cross-dock, è consigliabile inoltrare le righe al prospetto stoccaggi eliminando le istruzioni di stoccaggio anziché utilizzare la funzione di inoltro automatico fornita dal campo **Usa Prospetto Stoccaggi**.  

Se si registra il carico warehouse e il campo **Usa prospetto stoccaggi** non è selezionato, gli articoli da sottoporre a cross-dock vengono visualizzati come righe separate nell'istruzione di stoccaggio. Il campo **Informazione Cross-Dock** di ciascuna riga di stoccaggio indica se la riga contiene articoli di cross-dock, articoli da porre a magazzino che fanno parte dello stesso carico o articoli da porre a magazzino derivanti da una riga di carico in cui sono specificati anche alcuni articoli da sottoporre a cross-dock. Grazie a questo campo i dipendenti possono facilmente verificare il motivo per cui non viene immagazzinata l'intera quantità di carico.  

I record degli articoli sottoposti a cross-dock non vengono tenuti separati, bensì vengono registrati come istruzioni di stoccaggio ordinarie.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Per impostare la warehouse per il cross-docking  
1.  Impostare almeno una collocazione di cross-dock, se si utilizzano le collocazioni. Impostare una zona di cross-dock, se si utilizzano stoccaggi e prelievi guidati.  

    Per una collocazione cross-dock è selezionato il campo **Collocazione cross-dock** e devono essere selezionati i tipi di collocazione **Ricevi** e **Prelievo**. Per ulteriori informazioni, vedere [Creare collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md).  

    Se si utilizzano le zone, creare una zona per le collocazioni cross-dock e selezionare il campo **Zona collocazione cross-dock**. Per ulteriori informazioni, vedere [Impostare ubicazioni per l'utilizzo di collocazioni](warehouse-how-to-set-up-locations-to-use-bins.md).  

2.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ubicazione** e quindi scegliere il collegamento correlato.  
3.  Nella pagina **Ubicazione** selezionare l'ubicazione in cui si desidera impostare la warehouse per il cross-dock, quindi scegliere l'azione **Modifica**.  
4.  Nella Scheda dettaglio **Warehouse** selezionare la casella di controllo **Usa cross-docking** e compilare il campo **Calc. scadenza cross-dock** specificando l'intervallo di tempo per la ricerca delle opportunità di cross-dock.

    L'opzione **Usa cross-docking** è disponibile solo se i campi **Richiesto carico**, **Richiesta spedizione** **Richiesto prelievo** e **Richiesto stoccaggio** sono selezionati.  

5.  Se si utilizzano le collocazioni, nella Scheda dettaglio **Collocazioni** immettere nel campo **Codice collocazione cross-dock** il codice della collocazione da utilizzare come collocazione di default per il cross-dock.  
6.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Unità di stockkeeping** e quindi selezionare il collegamento correlato.  
7.  Per ciascun articolo o unità di stockkeeping che si desidera sottoporre a cross-dock, selezionare l'articolo, quindi scegliere l'azione **Modifica**.
8. Nella pagina **Scheda unità di stockkeeping** selezionare la casella di controllo **Usa cross-docking**.  

> [!NOTE]  
>  È possibile utilizzare il cross-dock solo se l'ubicazione prevede l'elaborazione degli stoccaggi e dei carichi warehouse.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Per sottoporre a cross-dock gli articoli senza visualizzare le opportunità  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Carichi warehouse** e quindi scegliere il collegamento correlato.  
2.  Creare un carico warehouse per un articolo arrivato e che può essere sottoposto a cross-dock. Per ulteriori informazioni, vedere [Ricevere articoli](warehouse-how-receive-items.md).  
3.  Compilare il campo **Qtà da ricevere** e scegliere l'azione **Calcola cross-dock**.  

    I documenti di origine in uscita in cui vengono richiesti gli articoli programmati per uscire dalla warehouse entro il periodo di tempo indicato nella formula di data vengono identificati.  [!INCLUDE[prod_short](includes/prod_short.md)] calcola le quantità affinché sia possibile sottoporre a cross-dock il maggior numero possibile di articoli in modo da evitare lo stoccaggio, senza l'accumulo di un numero eccessivo di articoli nell'area di cross-dock. Il valore nel campo **Qtà per cross-dock** corrisponde pertanto alla somma di tutte le righe in uscita per cui viene richiesto l'articolo entro il periodo di tolleranza meno la quantità degli articoli che sono già stati posizionati nell'area di cross-dock oppure al valore contenuto nel campo **Qtà da ricevere** della riga di carico, a seconda di quale valore sia inferiore. Non è possibile sottoporre a cross-dock una quantità di articoli superiore a quella ricevuta.  

4.  Se si desidera sottoporre a cross-dock la quantità suggerita, registrare il carico. In alternativa, è possibile scegliere di modificare la quantità da sottoporre a cross-dock impostando un valore superiore o inferiore, quindi registrare il carico.  

    A questo punto, le quantità da sottoporre a cross-dock vengono visualizzate come righe nell'istruzione di stoccaggio, supponendo che il campo **Usa prospetto stoccaggi** sia deselezionato. Anche le quantità non sottoposte a cross-dock vengono visualizzate come righe nell'istruzione di stoccaggio.  

    Se si utilizzano le collocazioni, gli articoli sottoposti a cross-dock vengono assegnati alla collocazione di cross-dock di default specificata nella scheda ubicazione.  

5.  Eliminare le righe **Prendere** e **Mettere** per gli articoli che non verranno sottoposti a cross-dock.  
6.  Stampare l'istruzione di stoccaggio per le righe rimanenti e posizionare le quantità del carico da immagazzinare nelle collocazioni o nell'area appropriata della warehouse. Posizionare gli articoli di cross-dock nell'area o nella collocazione designata dal criterio di logistica di warehouse. Talvolta, i criteri di logistica di warehouse prevedono che tali articoli vengano lasciati nell'area di carico.  
7.  Per registrare gli articoli sottoposti a cross-dock come articoli stoccati e disponibili per il prelievo, scegliere l'azione **Registra**.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Per sottoporre a cross-dock gli articoli dopo la visualizzazione delle opportunità  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Carichi warehouse** e quindi scegliere il collegamento correlato.  
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

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Per visualizzare gli articoli sottoposti a cross-dock in una spedizione o in un prospetto prelievi  
Se si utilizzano le collocazioni, ogni volta che si visualizza una spedizione o il prospetto prelievi, è possibile verificare il calcolo aggiornato della quantità di ciascun articolo nelle collocazioni di cross-dock. Tali informazioni risultano particolarmente utili se si è in attesa di ricevere un articolo. Quando l'articolo è finalmente disponibile nella collocazione di cross-dock, è possibile creare rapidamente un prelievo per tutti gli articoli da spedire. Nel prospetto prelievi è possibile modificare le righe in base alle esigenze e creare un prelievo.  

Durante il prelievo degli articoli per la spedizione, è necessario cercare gli articoli prima nell'area di cross-dock. Se, durante il processo di carico, sono stati esaminati i documenti di origine alla base del cross-dock, si sa con maggiore certezza se l'articolo è reperibile o meno nell'area di cross-dock.  

Quando viene rilasciato un ordine di produzione, le righe vengono rese disponibili nel prospetto prelievi e, se si esamina il campo **Qtà in collocazione cross-dock** è possibile stabilire se gli articoli attesi sono arrivati e sono stati posizionati nelle collocazioni di cross-dock. Quando si crea un'istruzione di prelievo, viene suggerito automaticamente di prelevare prima gli articoli sottoposti a cross-dock e solo in seguito viene eseguita la ricerca degli articoli nelle collocazioni di immagazzinamento.  

Se non si utilizzano le collocazioni, si consiglia di controllare periodicamente l'area di cross-dock o basarsi sulle notifiche di carico per verificare se gli articoli per la produzione sono arrivati.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
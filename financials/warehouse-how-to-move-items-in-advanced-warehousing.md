---
title: 'Procedura: Spostare articoli in configurazioni di warehouse di base | Documenti Microsoft'
description: Nelle configurazioni warehouse avanzate, ovvero le ubicazioni con stoccaggi e prelievi guidati, occorre preparare le movimentazioni warehouse tra collocazioni nel prospetto movimentazioni, un'operazione in genera affidata a un responsabile di reparto, quindi creare le movimentazioni warehouse che dovranno essere eseguite dagli impiegati warehouse.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/232017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4caa041c6b3acef5d0cbf6c037f0ec535cd3176e
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Spostare articoli in configurazioni di warehouse avanzate
Nelle configurazioni warehouse avanzate, ovvero le ubicazioni con stoccaggi e prelievi guidati, occorre preparare le movimentazioni warehouse tra collocazioni nel prospetto movimentazioni, un'operazione in genera affidata a un responsabile di reparto, quindi creare le movimentazioni warehouse che dovranno essere eseguite dagli impiegati warehouse.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Per spostare gli articoli con il prospetto movimentazioni warehouse
La finestra **Prospetto movimentazioni** include due funzioni che consentono di compilare automaticamente le righe. La prima è la funzione **Calcola rifornimento collocazione**. Questa funzione utilizza le valutazioni collocazioni per suggerire il rifornimento delle collocazioni con valutazione elevata spostando articoli dalle collocazioni con valutazione bassa. La seconda funzione è **Prendi contenuto collocazione**, che inserisce nelle righe del prospetto i dati per l'intero contenuto della collocazione o delle collocazioni specificate.

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Movimento worksheet**, quindi scegliere il collegamento correlato.  
2.  Immettere le informazioni di movimentazione warehouse nelle righe del prospetto secondo le esigenze.  
3. Scegliere l'azione **Crea movimento** per creare un documento di movimentazione warehouse che potrà essere registrato al termine dell'operazione di movimentazione.  

### <a name="to-register-the-warehouse-movement"></a>Per registrare la movimentazione warehouse  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Movimentazioni**, quindi scegliere il collegamento correlato.  
2.  Aprire la movimentazione warehouse che si desidera elaborare.  
3.  Nelle righe di tipo di azione **Posizione** specificare dove, quali e quando spostare l'articolo in questione modificando i campi **Cod. zona**, **Cod. collocazione**, **Qtà da gestire** o **Data scadenza**.  

    Se la warehouse è stata impostata in modo che i codici di collocazione riflettano la struttura fisica della warehouse, sarà possibile prelevare quantità di vari articoli da collocazioni a massa consecutive e posizionarle nelle collocazioni di prelievo in sequenza da inizio ordine, anche queste probabilmente ubicate in prossimità l'una dell'altra.  
4.  Nelle righe di tipo azione **Prendere** specificare nel campo **Qtà da gestire** una quantità parte del contenuto collocazione che si desidera spostare. Tutti gli altri campi nelle righe di tipo azione **Prendere** sono di sola lettura.  
5.  Per spostare tutte le quantità suggerite specificate nel campo **Quantità**, scegliere l'azione **Autocompil. qtà da gestire**.  
6. Scegliere l'azione **Registra**.  

> [!NOTE]  
>  Se per una determinata ubicazione sono previsti stoccaggi e prelievi guidati, non è possibile spostare manualmente gli articoli all'interno o all'esterno delle collocazioni di tipo RICEVI poiché gli articoli presenti in dette collocazioni devono essere registrati come stoccati prima di essere inseriti nella giacenza disponibile.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Per registrare la movimentazione di un articolo già effettuata  
Se l'ubicazione utilizza stoccaggi e prelievi guidati ed è necessario spostare articoli in altre collocazioni per cui non esistono movimentazioni, prelievi o stoccaggi warehouse precedenti, è possibile registrare la posizione corretta degli articoli nella warehouse tramite la finestra **Registrazioni riclass.whse.**

1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registr. riclassificaz. whse.**, quindi scegliere il collegamento correlato.  
2.  Compilare i campi **Nr. articolo**, **Codice Da zona**, **Dal codice collocazione**, **A codice zona** e **A codice collocazione**.  
3.  Scegliere l'azione **Registra**.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


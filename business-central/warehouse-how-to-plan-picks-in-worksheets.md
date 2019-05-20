---
title: 'Procedura: Pianificare prelievi nei prospetti | Documenti Microsoft'
description: Se la warehouse prevede l'elaborazione dei prelievi e delle spedizioni, è possibile fare in modo che le righe dei documenti di spedizione non vengano convertite automaticamente in istruzioni di prelievo, bensì vengano rese disponibili per il prospetto prelievi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f0bf6da083b69d76c3f2ad75e8fb9b9d6bfdc5d9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248527"
---
# <a name="plan-picks-in-worksheets"></a>Pianificare prelievi nei prospetti
Se la warehouse prevede l'elaborazione dei prelievi e delle spedizioni, è possibile fare in modo che le righe dei documenti di spedizione non vengano convertite automaticamente in istruzioni di prelievo, bensì vengano rese disponibili per il prospetto prelievi.  

> [!NOTE]  
>  Se le istruzioni di prelievo da warehouse sono già state create e si desidera combinarle in un'unica istruzione di prelievo per migliorarne l'efficienza, è necessario eliminare i singoli prelievi da warehouse. Le righe da prelevare possono essere ora elencate nel prospetto.  

Nel prospetto prelievi è possibile impostare liste di prelievi per gli addetti alla warehouse in modo da ridurre il tempo necessario per spostarsi da un punto all'altro della warehouse e prelevare gli articoli. Sono inoltre presenti campi che contengono informazioni sulle quantità degli articoli disponibili nelle collocazioni di cross-dock. Tali informazioni risultano particolarmente utili per pianificare le assegnazioni delle mansioni, in quanto il programma propone automaticamente di eseguire il prelievo da una collocazione di cross-dock prima che da qualsiasi altra collocazione, indipendentemente dall'unità di misura. Le righe del prospetto possono provenire da numerosi documenti di origine ed essere ordinate per articolo, numero di scaffale, documento di origine, data di scadenza o indirizzo di spedizione.  

Se di effettua l'ordinamento in base alla data di scadenza, è possibile scegliere di eliminare dal prospetto tutte le righe, eccetto quelle che richiedono attenzione immediata. Le righe meno urgenti non vengono di fatto eliminate, ma vengono semplicemente inviate di nuovo al prospetto **Selezione prelievo**. Le righe vengono ordinate in base alla data di scadenza prima della creazione del prelievo e, pertanto, è possibile assegnare direttamente il prelievo a un addetto specifico.  

> [!NOTE]  
>  Il prelievo per la spedizione warehouse di articoli assemblati nell'ordine di vendita spedito segue gli stessi passaggi dei normali prelievi warehouse per la spedizione, come descritto in questo argomento. Tuttavia, il numero delle righe prelievo per quantità da spedire può essere molti a uno perché vengono selezionati i componenti, non l'articolo assemblato.  
>   
>  Le righe prelievi warehouse vengono create per il valore nel campo **Quantità residua** sulle righe dell'ordine di assemblaggio collegato alla riga dell'ordine di vendita spedito. In questo modo si garantisce che tutti i componenti vengano prelevati con una sola azione.  
>   
>  Per ulteriori informazioni, vedere "Gestione di articoli da assemblare su ordine in spedizioni warehouse" in Spedizione warehouse.  
>   
>  Per informazioni sul prelievo generale di componenti per gli ordini di assemblaggio, incluse le situazioni in cui l'articolo di assemblaggio non fa parte di una spedizione vendita, vedere [Prelevare per assemblaggio o produzione in configurazioni di warehouse avanzate](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>Per pianificare prelievi nel prospetto  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prospetto prelievi** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Prendi documenti warehouse**.  
3.  Selezionare le spedizioni per cui preparare un prelievo. A questo punto, le righe possono essere ordinate solo in certa misura, ma l'ordinamento specificato in questa fase non viene applicato all'istruzione di prelievo. È inoltre possibile eliminare alcune righe per creare un prelievo più efficace. Se ad esempio vi sono diverse righe con articoli nelle collocazioni di cross-dock, può essere utile creare un prelievo per tutte le righe associate a tali righe. Gli articoli sottoposti a cross-dock verranno spediti insieme agli altri articoli e nelle collocazioni di cross-dock sarà disponibile una maggiore quantità di spazio per ulteriori articoli in entrata.  
4.  Scegliere l'azione **Crea prelievo** e compila la pagina di richiesta **Crea prelievo**. Le righe di prelievo create verranno ordinate in base ai criteri di ordinamento specificati in questa finestra. È ad esempio possibile creare un prelievo per ciascuna zona e ordinare le righe in base alla valutazione della collocazione all'interno di ciascun prelievo.  
5.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Prelievi** e quindi scegliere il collegamento correlato. Viene visualizzata la pagina **Prelievi**.  
6.  È possibile individuare l'assegnazione di prelievo appena creata selezionando il prelievo con il numero più elevato.  
7.  Se necessario, modificare l'ID utente assegnato e la modalità di ordinamento delle righe nel prelievo.  
8.  Scegliere l'azione **Stampa** per stampare le istruzioni per il prelievo.  
9. Dopo avere eseguito il prelievo, scegliere l'azione **Registra**.  

Se la numerazione delle collocazioni riflette la disposizione fisica della warehouse, le righe ordinate in base al codice di collocazione consentono all'impiegato warehouse di prelevare gli articoli per più spedizioni in un unico giro della warehouse. L'addetto preleva da ciascuna collocazione il numero di articoli richiesto per ciascuna riga di spedizione ponendoli insieme agli altri articoli per quella determinata spedizione. Se il responsabile del prelievo preleva articoli per più spedizioni in una singola visita a una collocazione, può risparmiare parecchio tempo.  

Un'altra opzione di ordinamento efficace è rappresentata dalla valutazione delle collocazioni, nel caso in cui la disposizione fisica della warehouse rifletta maggiormente un ordinamento in base alla valutazione della collocazione piuttosto che al codice della collocazione.  

Nel prospetto prelievi è inoltre possibile ordinare le righe in base all'indirizzo di spedizione, che consente di assemblare e spedire gli ordini innanzitutto ai clienti delle aree geografiche più distanti.  

## <a name="see-also"></a>Vedi anche
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

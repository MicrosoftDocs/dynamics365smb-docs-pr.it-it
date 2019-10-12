---
title: 'Procedura: Ricevere articoli | Documenti Microsoft'
description: Quando gli articoli arrivano in una warehouse impostata per l'elaborazione dei carichi warehouse, è necessario recuperare le righe del documento di origine rilasciato che ha dato origine al carico.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ea8d952f6ef88415b0fef27c1694ad7d29672e64
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310457"
---
# <a name="receive-items"></a>Ricevere articoli
Quando gli articoli arrivano in una warehouse che non è impostata per l'elaborazione dei carichi warehouse, occorre registrare semplicemente la ricezione nel documento aziendale correlato, ad esempio un ordine di acquisto, un ordine di reso da vendita o un ordine di trasferimento in entrata.

Quando gli articoli arrivano in una warehouse impostata per l'elaborazione dei carichi warehouse, è necessario recuperare le righe del documento di origine rilasciato che ha dato origine al carico. Se si utilizzano le collocazioni, è possibile accettare la collocazione di default specificata oppure, se l'articolo non è mai stato utilizzato in precedenza nella warehouse, specificare la collocazione in cui si desidera stoccarlo. È necessario immettere le quantità degli articoli ricevuti e registrare il carico.  

## <a name="to-receive-items-with-a-purchase-order"></a>Per ricevere gli articoli con un ordine di acquisto
Di seguito viene descritto come ricevere gli articoli con un ordine di acquisto. I passaggi riguardanti gli ordini di reso vendita e gli ordini di trasferimento sono simili.  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini acquisto** e selezionare il collegamento correlato.
2. Aprire un ordine di acquisto esistente o crearne uno. Per ulteriori informazioni, vedere [Registrare gli acquisti](purchasing-how-record-purchases.md).
3. Nel campo **Qtà da Ricevere** immettere la quantità ricevuta.

    Il valore nel campo **Qtà ricevuta** viene aggiornato. Se si tratta di una ricezione parziale, il valore è inferiore al valore nel campo **Quantità**.
4. Scegliere l'azione **Registra**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Per ricevere gli articoli con un carico warehouse
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Carichi warehouse** e quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Nuovo**.  

    Compilare i campi della Scheda dettaglio **Generale**. Quando si recuperano le righe dei documenti di origine, alcune informazioni vengono copiate in ciascuna riga.  

    Per la configurazione warehouse con stoccaggi e prelievi guidati, se l'ubicazione dispone di una zona e di una collocazione di default per i carichi, i campi **Cod. zona** e **Cod. Collocazione** vengono compilati automaticamente ma è possibile modificarli in base alle esigenze.  

    > [!NOTE]  
    >  Se si desidera ricevere gli articoli con codici classe warehouse diversi dal codice classe della collocazione specificato nel campo **Cod. collocazione** della testata del documento, è necessario eliminare il contenuto del campo **Cod. collocazione** della testata prima di recuperare le righe del documento di origine per gli articoli.  
3.  Scegliere l'azione **Prendi documenti origine**. Verrà visualizzata la pagina **Documenti origine**.

    Da un carico warehouse o una spedizione warehouse nuova o aperta, è possibile utilizzare la pagina **Filtri per ottenere documenti origine** per recuperare le righe del documento di origine rilasciato che definiscono quali articoli ricevere o spedire.

    1. Scegliere l'azione **Usa filtri per richiamare doc. orig.**.  
    2. Per impostare un nuovo filtro, immettere un codice descrittivo nel campo **Codice**, quindi scegliere l'azione **Modifica**.  
    3. Definire il tipo di righe del documento origine che si desidera recuperare compilando i campi Filtro appropriati.  
    4. Scegliere l'azione **Esegui**.  

    Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono inserite nella pagina **Carico warehouse** da cui è stata attivata la funzione di filtro.  

    Le combinazioni di filtri definite vengono salvate nella pagina **Filtri per ottenere documenti origine** finché non saranno necessarie in momento successivo. È possibile creare un numero indefinito di combinazioni di filtri. È possibile modificare i criteri in qualsiasi momento scegliendo l'azione **Modifica**.

4.  Selezionare i documenti di origine per i quali si desidera ricevere gli articoli, quindi scegliere **OK**.  

    Le righe dei documenti di origine verranno visualizzate nella pagina **Carico warehouse**. Il campo **Qtà da ricevere** viene compilato con la quantità inevasa per ciascuna riga, ma è possibile modificare tale quantità in base alle esigenze. Se è stato eliminato il contenuto del campo **Cod. collocazione** della Scheda dettaglio **Generale** prima di recuperare le righe, è necessario immettere un codice collocazione appropriato in ogni riga di carico.  

    > [!NOTE]  
    >  Per compilare il campo **Qtà da ricevere** in tutte le righe con zero, scegliere l'azione **Eliminare qtà da ricevere**. Per immettere nuovamente la quantità inevasa, selezionare l'azione **Autocompilazione qtà da ricevere**.  

    > [!NOTE]  
    >  Non è possibile ricevere un numero di articoli maggiore di quello indicato nel campo **Qtà inevasa** della riga del documento di origine. Per ricevere più articoli, recuperare un altro documento di origine contenente una riga per l'articolo utilizzando la funzione di filtro appropriata.  

5.  Registrare il carico warehouse. I campi relativi alle quantità nei documenti di origine vengono aggiornati e gli articoli vengono registrati come parte dell'inventario della società.  

Se si utilizza lo stoccaggio warehouse, le righe di carico vengono inviate alla funzione di stoccaggio warehouse. Gli articoli, sebbene ricevuti, non possono essere prelevati finché non sono messi a magazzino. Gli articoli ricevuti vengono inclusi nell'inventario disponibile solo dopo la registrazione dello stoccaggio.  

Se non si utilizza lo stoccaggio warehouse ma si impiegano le collocazioni, viene registrato lo stoccaggio degli articoli nella collocazione specificata nella riga del documento di origine.  

> [!NOTE]  
>  La funzione **Registra e stampa** consente di registrare il carico e di stampare un'istruzione di stoccaggio indicante la posizione in cui immagazzinare gli articoli.  
>   
>  Se l'ubicazione utilizza stoccaggi e prelievi guidati, vengono utilizzati i modelli di stoccaggio per calcolare la migliore posizione di stoccaggio per gli articoli. Questa viene quindi stampata nell'istruzione di stoccaggio.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

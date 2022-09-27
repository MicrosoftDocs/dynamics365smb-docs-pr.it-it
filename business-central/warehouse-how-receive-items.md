---
title: Ricevere articoli
description: Questo articolo offre una panoramica dei diversi modi per ricevere gli articoli in una warehouse, ad esempio articoli con un ordine di acquisto o articoli con un carico warehouse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 6cca8d8f9b0ec28b149532581f9bc458022c3cd5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529516"
---
# <a name="receive-items"></a>Ricevere articoli

Quando gli articoli arrivano in una warehouse che non è impostata per l'elaborazione dei carichi warehouse, occorre registrare semplicemente la ricezione nel documento aziendale correlato, ad esempio un ordine di acquisto, un ordine di reso da vendita o un ordine di trasferimento in entrata.

Quando gli articoli arrivano in una warehouse impostata per l'elaborazione dei carichi warehouse, è necessario recuperare le righe del documento di origine rilasciato che ha dato origine al carico. Se si utilizzano le collocazioni, è possibile accettare la collocazione di default specificata oppure, se l'articolo non è mai stato utilizzato in precedenza nella warehouse, specificare la collocazione in cui si desidera stoccarlo. È necessario immettere le quantità degli articoli ricevuti e registrare il carico.  

## <a name="receive-items-with-a-purchase-order"></a>Ricevere gli articoli con un ordine di acquisto

Di seguito viene descritto come ricevere gli articoli con un ordine di acquisto. I passaggi riguardanti gli ordini di reso vendita e gli ordini di trasferimento sono simili.  

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Aprire un ordine di acquisto esistente o crearne uno. Ulteriori informazioni in [Registrare gli acquisti](purchasing-how-record-purchases.md).
3. Nel campo **Qtà da Ricevere** immettere la quantità ricevuta.

   > [!NOTE]
   > Se la quantità ricevuta è superiore a quella ordinata nell'ordine acquisto, in base al campo **Quantità**, e il fornitore è stato configurato per consentire le ricevute in eccesso, puoi utilizzare il campo **Ricezione eccessiva** per gestire la quantità in eccesso. Ulteriori informazioni nella sezione [Per ricevere più articoli di quelli ordinati](warehouse-how-receive-items.md#receive-more-items-than-ordered).
4. Scegli l'azione **Registra**.

  Il valore nel campo **Qtà ricevuta** viene aggiornato. Se si tratta di una ricezione parziale, il valore è inferiore al valore nel campo **Quantità**.

> [!NOTE]
> Se si utilizza un documento di magazzino per registrare la ricevuta, non è possibile utilizzare l'azione **Registra** sull'ordinedi acquisto. Al contrario, un addetto al magazzino ha già registrato la quantità dell'ordine d'acquisto ricevuta. Ulteriori informazioni in [Per ricevere gli articoli con un carico warehouse](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Ricevere gli articoli con un carico warehouse

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Carichi warehouse**, quindi seleziona il collegamento correlato.  
2. Scegli l'azione **Nuovo**.  

    Compila i campi della Scheda dettaglio **Generale**. Quando si recuperano le righe dei documenti di origine, alcune informazioni vengono copiate in ciascuna riga.  

    Per la configurazione warehouse con stoccaggi e prelievi guidati, se l'ubicazione dispone di una zona e di una collocazione di default per i carichi, i campi **Cod. zona** e **Cod. Collocazione** vengono compilati automaticamente ma è possibile modificarli in base alle esigenze.  

    > [!NOTE]  
    > Se si desidera ricevere gli articoli con codici classe warehouse diversi dal codice classe della collocazione specificato nel campo **Cod. collocazione** della testata del documento, è necessario eliminare il contenuto del campo **Cod. collocazione** della testata prima di recuperare le righe del documento di origine per gli articoli.  
3. Scegli l'azione **Prendi documenti origine**. Verrà visualizzata la pagina **Documenti origine**.

    Da un carico warehouse o una spedizione warehouse nuova o aperta, è possibile utilizzare la pagina **Filtri per ottenere documenti origine** per recuperare le righe del documento di origine rilasciato che definiscono quali articoli ricevere o spedire.

    1. Scegliere l'azione **Usa filtri per richiamare doc. orig.**.  
    2. Per impostare un nuovo filtro, immetti un codice descrittivo nel campo **Codice**, quindi scegli l'azione **Modifica**.  
    3. Definisci il tipo di righe del documento origine che desideri recuperare compilando i campi Filtro appropriati.  
    4. Scegli **Esegui**.  

    Tutte le righe del documento origine rilasciato che soddisfano i criteri di filtro vengono inserite nella pagina **Carico warehouse** da cui è stata attivata la funzione di filtro. 

    Le combinazioni di filtri definite vengono salvate nella pagina **Filtri per ottenere documenti origine** finché non saranno necessarie in momento successivo. È possibile creare un numero indefinito di combinazioni di filtri. È possibile modificare i criteri in qualsiasi momento scegliendo l'azione **Modifica**.

4. Seleziona i documenti di origine per i quali si desidera ricevere gli articoli, quindi scegli **OK**.  

    Le righe dei documenti di origine verranno visualizzate nella pagina **Carico warehouse**. Il campo **Qtà da ricevere** viene compilato con la quantità inevasa per ciascuna riga, ma è possibile modificare tale quantità in base alle esigenze. Se è stato eliminato il contenuto del campo **Cod. collocazione** della Scheda dettaglio **Generale** prima di recuperare le righe, è necessario immettere un codice collocazione appropriato in ogni riga di carico.  

    > [!NOTE]  
    >  Per compilare tutte le righe del campo **Qtà da ricevere** con zero, scegli l'azione **Eliminare qtà da ricevere**. Per immettere nuovamente la quantità inevasa, selezionare l'azione **Autocompilazione qtà da ricevere**.  
    >
    >  Non è possibile ricevere un numero di articoli maggiore di quello indicato nel campo **Qtà inevasa** della riga del documento di origine. Per ricevere più articoli, recuperare un altro documento di origine contenente una riga per l'articolo utilizzando la funzione di filtro.  

5. Registrare il carico warehouse. I campi relativi alle quantità nei documenti di origine vengono aggiornati e gli articoli vengono registrati come parte dell'inventario della società.  

Se si utilizza lo stoccaggio warehouse, le righe di carico vengono inviate alla funzione di stoccaggio warehouse. Gli articoli, sebbene ricevuti, non possono essere prelevati finché non sono messi a magazzino. Gli articoli ricevuti vengono inclusi nell'inventario disponibile solo dopo la registrazione dello stoccaggio.  

Se non si utilizza lo stoccaggio warehouse ma si impiegano le collocazioni, viene registrato lo stoccaggio degli articoli nella collocazione specificata nella riga del documento di origine.  

> [!NOTE]  
> La funzione **Registra e stampa** consente di registrare il carico e di stampare un'istruzione di stoccaggio indicante la posizione in cui immagazzinare gli articoli.  
>
> Se l'ubicazione utilizza stoccaggi e prelievi guidati, vengono utilizzati i modelli di stoccaggio per calcolare la migliore posizione di stoccaggio per gli articoli. Questa viene quindi stampata nell'istruzione di stoccaggio.

## <a name="receive-more-items-than-ordered"></a>Ricevere più articoli di quelli ordinati

Quando si ricevono più merci di quelle ordinate, è possibile che si intenda mantenerle anziché annullare il carico. Ad esempio, potrebbe essere più economico mantenere l'eccesso nell'inventario anziché restituirlo oppure il fornitore potrebbe offrire uno sconto per accettarlo.

### <a name="set-up-over-receipts"></a>Configurare le ricevute in eccesso

È necessario definire una percentuale in base alla quale consentire il superamento della quantità ordinata durante la ricezione. Si definisce questo in un codice di ricevuta in eccesso, che contiene la percentuale nel campo **% tolleranza per ricezione eccessiva**. Quindi assegni il codice alle schede degli articoli e/o venditori rilevanti.  

Di seguito viene descritto come confgurare e assegnare un codice di ricevuta eccessiva a un articolo. I passaggi sono simili per configurarlo per un fornitore.

1. Scegli l'icona a forma di ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , inserisci **Elemento** e scegli il link relativo.
2. Apri la scheda per un articolo che sospetti possa essere talvolta consegnato con una quantità superiore a quella ordinata.
3. Scegli **Ricerca** nel campo **Codice di ricezione eccessiva**.
4. Scegli l'azione **Nuovo**.
5. Nella pagina **Codici di ricezione eccessiva**, creare una o più nuove righe che definiscono diversi criteri di ricezione eccessiva. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Seleziona una riga, quindi scegli **OK**.

Il codice di ricezione eccessiva viene assegnato all'articolo. Qualsiasi ordine di acquisto o ricevuta di magazzino per l'articolo ora consente di ricevere più della quantità ordinata in base alla percentuale di tolleranza di ricezione specificata.

> [!NOTE]
> È possibile configurare un flusso di lavoro di approvazione per richiedere che le ricezioni eccessive debbano essere approvate prima di poter essere gestite. In tal caso, è necessario selezionare la casella di conteollo **Approvazione richiesta** nella pagina **Codici di ricezione eccessiva**. Ulteriori informazioni in [Creare workflow](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Eseguire una ricezione in eccesso

Sulle righe di acquisto e sulle righe di ricevuta del magazzino, il campo **Quantità di ricezione eccessiva** viene utilizzato per registrare le quantità ricevute in eccesso, ovvero le quantità che superano il valore nel campo **Quantità**, la quantità ordinata.

Quando si gestisce una ricezione in eccesso, puoi aumentare il valore nel campo **Qtà da Ricevere** per la quantità effettivamente ricevuta. Il campo **Quantità di ricezione in eccesso** viene quindi aggiornato per mostrare la quantità in eccesso. In alternativa, è possibile inserire la quantità in eccesso nel campo **Quantità di ricezione in eccesso**. Il campo **Qtà da Ricevere** viene quindi aggiornato per mostrare la quantità ordinata più quella in eccesso. La seguente procedura ha descritto come compilare il campo **Qtà da Ricevere**.  

1. In un ordine di acquisto o in un documento di ricevuta di magazzino in cui la quantità ricevuta è superiore a quella ordinata, immettere la quantità effettivamente ricevuta nel campo **Qtà da Ricevere**.

    Se l'aumento rientra nella tolleranza specificata dal codice di ricezione eccessiva assegnato, il campo **Quantità di ricezione eccessiva** viene aggiornato per mostrare la quantità che il valore nel campo **Quantità** ha superato.

    Se l'aumento è superiore alla tolleranza specificata, la ricezione eccessiva non è consentita. In tal caso, è possibile verificare se esiste un altro codice di ricezione eccessiva che lo consenta. In caso contrario, è possibile ricevere solo la quantità ordinata e la quantità in eccesso deve essere gestita altrimenti, ad esempio, restituendola al fornitore.

2. Registra la ricevuta come faresti per qualsiasi altra ricevuta.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] non include funzionalità per avviare automaticamente l'amministrazione finanziaria delle ricezioni eccessive. È necessario gestirle manualmente in accordo con il fornitore, ad esempio, chiedendo al fornitore di inoltrare una fattura nuova o aggiornata.

## <a name="see-related-microsoft-training"></a>Vedi il relativo [training Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Vedere anche

[Warehouse Management](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Dettagli di progettazione: Warehouse Management](design-details-warehouse-management.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

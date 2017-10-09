---
title: Creazione di articoli in assistenza | Documenti Microsoft
description: "Quando si riceve un articolo non registrato per l'assistenza è possibile registrarlo come articolo in assistenza."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: acd3305694186793ccc5c305573f62c16a718531
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-items"></a>Procedura: Creare articoli in assistenza
In [!INCLUDE[d365fin](includes/d365fin_md.md)], il termine "articolo in assistenza" si riferisce alle attrezzature o agli articoli che necessitano di assistenza. Quando si crea un ordine di assistenza, si specificano gli articoli che necessitano di assistenza. Nell'ordine, è possibile collegare un articolo in assistenza a un articolo in magazzino o a un gruppo di articoli in assistenza.    

Quando si riceve un articolo che necessita di assistenza, è possibile registrarlo come articolo in assistenza. Questa operazione può essere effettuata in vari modi. Ad esempio, è possibile creare un articolo in assistenza nella pagina **Articoli in assistenza**, o nell'ambito di un altro processo, ad esempio quando si lavora con un ordine di assistenza.   

## <a name="to-create-a-service-item"></a>Per creare un articolo in assistenza  
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Articoli in assistenza**, quindi scegliere il collegamento correlato.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Per creare articoli in assistenza all'interno di un ordine di assistenza  
Quando si ricevono articoli su cui prestare assistenza e li si intende registrare come articoli in assistenza, è possibile crearli come articoli in assistenza nelle finestre **Ordine Assistenza** o **Offerte Assistenza**.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini assistenza**, quindi scegliere il collegamento correlato.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Scegliere l'azione **Crea articolo in assistenza**.  

    Viene assegnato un numero all'articolo in assistenza e viene creata una scheda articolo in assistenza. Il campo **Nr. articolo in assistenza** viene compilato con il numero del nuovo articolo in assistenza.

## <a name="to-create-a-service-item-when-shipping-items"></a>Per creare un articolo in assistenza durante la spedizione degli articoli  
Quando si spediscono articoli registrando ordini o fatture di assistenza, gli articoli spediti vengono automaticamente registrati come articoli in assistenza se è rispettata la seguente condizione. Gli articoli devono appartenere a un gruppo di articoli in assistenza per cui la casella di controllo **Crea articolo in assistenza** risulta selezionata. Se i numeri seriali degli articoli sono registrati nella finestra Righe tracciabilità articolo, tali informazioni verranno automaticamente copiate nel campo **Nr. seriale** della scheda relativa all'articolo in assistenza al momento della creazione degli articoli stessi.  

La seguente procedura indica le modalità di creazione di articoli in assistenza durante la spedizione degli articoli presenti negli ordini di assistenza.  

1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordini assistenza**, quindi scegliere il collegamento correlato.  
2. Aprire l'ordine di assistenza desiderato.  
3. Scegliere l'azione **Registra** o **Registra e stampa**.  
4. Scegliere l'azione **Spedizione** o **Spedizione e fattura**.  
5. Verranno automaticamente creati gli articoli in assistenza per gli articoli dell'ordine che appartengono a un gruppo di articoli in assistenza impostato per la creazione di articoli in assistenza. A tali articoli verranno inoltre assegnati i numeri seriali eventualmente registrati nella finestra **Righe tracciabilità articolo**.  

> [!NOTE]  
>  Se un articolo è una distinta base e la distinta base è stata espansa, gli articoli in essa contenuti verranno trattati come normali articoli. Vengono creati articoli in assistenza in base alla condizione specificata per il gruppo degli articoli in assistenza ed eventualmente alla condizione specificata per i numeri seriali. Inoltre, se viene creato un articolo in assistenza per una distinta base espansa composta da altri componenti DB, tali articoli verranno creati come componenti articolo in assistenza per l'articolo in assistenza della distinta base espansa.  
>   
>  Se un articolo è una distinta base e la distinta base non è stata espansa, verrà creato un articolo in assistenza in base alla condizione specificata per il gruppo di articoli in assistenza ed eventualmente alla condizione specificata per i numeri seriali.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Per inserire una spesa iniziale per un articolo in assistenza
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Compiti di assistenza**, quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Prospetto interv. articolo**.
3. Scegliere la riga di assistenza e quindi **Azioni**, **Funzioni**, quindi l'azione **Inserisci spesa iniziale**.  

    Verrà inserita una riga di assistenza di tipo **Costo** in cui viene indicata la spesa iniziale. La spesa iniziale viene applicata all'articolo in assistenza selezionato.

## <a name="see-also"></a>Vedi anche  
[Procedura: Impostare gli articoli in assistenza e i componenti degli articoli in assistenza](service-how-setup-service-items.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  
[Gestione assistenza](service-service.md)  


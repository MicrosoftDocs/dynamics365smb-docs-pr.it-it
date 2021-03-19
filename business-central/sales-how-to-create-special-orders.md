---
title: 'Procedura: Creare ordini speciali | Documenti Microsoft'
description: È possibile creare un ordine speciale per uno specifico articolo non presente in catalogo che deve venire spedito a un determinato cliente. L'articolo viene spedito dal fornitore abituale alla warehouse dell'azienda e a questo punto può essere spedito al cliente da solo oppure insieme ad altri articoli di un ordine diverso.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd22ee25cb472a827468c578ccdb8a7427490bc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383027"
---
# <a name="create-special-orders"></a>Creare ordini speciali
È possibile creare un ordine speciale per uno specifico articolo non presente in catalogo che deve venire spedito a un determinato cliente. L'articolo viene spedito dal fornitore abituale alla warehouse dell'azienda e a questo punto può essere spedito al cliente da solo oppure insieme ad altri articoli di un ordine diverso.  

Gli ordini speciali implicano il collegamento dell'ordine di acquisto all'ordine di vendita allo scopo di garantire che lo specifico articolo presente in catalogo venga prelevato e consegnato al cliente.  

Prima di poter utilizzare questa funzionalità è necessario impostare le schede per il cliente, il fornitore e l'articolo interessati dall'ordine.  

## <a name="to-create-a-special-order"></a>Per creare un ordine speciale  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordine vendita** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Creare e compilare un  ordine di vendita per l'articolo. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
3.  Nella Scheda dettaglio **Righe** compilare la riga di vendita. Nel campo **Codice acquisto** selezionare un codice di acquisto per il quale il campo **Ordine speciale** sia selezionato.

    È quindi necessario creare un ordine di acquisto da una richiesta di approvvigionamento.  
4. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Richiesta di approvvigionamento** e quindi scegliere il collegamento correlato.  
5. Scegliere l'azione **Ordine speciale** e scegliere l'azione **Ottieni ordini vendite**.  
6.  Nella pagina **Prendi ordini vendite** vengono visualizzati i risultati in cui **Nr. documento** è il numero dell'ordine di vendita. Scegliere il pulsante **OK**. Viene creata una riga di richiesta di approvvigionamento per l'articolo.  
7.  Nella riga di richiesta di approvvigionamento selezionare **Nuovo** nel campo **Messaggio azione**.  
8.  Nella pagina **Prospetto rich.** scegliere l'azione **Esegui messaggi di azione**. Viene aperta la pagina **Approv. - Esegui mess. azioni**. Scegliere il pulsante **OK**.  

    Verrà quindi visualizzato un messaggio con l'informazione che gli ordini di acquisto sono stati creati. Scegliere il pulsante **OK**.  

Un ordine di acquisto creato come ordine speciale per un ordine di vendita viene rispettato dal sistema di pianificazione poiché pareggia la domanda e l'offerta. Ossia, l'ordine di acquisto (approvvigionamento) resta collegato all'ordine di vendita (domanda), anche se l'ordine di acquisto può approvvigionare un'altra domanda precedente. Per ulteriori informazioni, vedere [Dettagli di programmazione: Metodi di riordino](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Se l'elemento è già prenotato, non è possibile utilizzare la funzionalità ordine speciale. Pertanto, per gli articoli venduti in ordini speciali, assicurarsi che il campo **Impegno** nella scheda articolo non sia impostato su **Sempre**.  

## <a name="see-also"></a>Vedi anche  
[Utilizzare gli articoli di catalogo](inventory-how-work-nonstock-items.md)  
[Vendite](sales-manage-sales.md)  
[Effettuare spedizioni dirette](sales-how-drop-shipment.md)   
[Dettagli di progettazione: Metodi di riordino](design-details-reservation-order-tracking-and-action-messaging.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
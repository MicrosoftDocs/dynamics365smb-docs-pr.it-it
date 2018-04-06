---
title: 'Procedura: Creare ordini speciali | Documenti Microsoft'
description: "È possibile creare un ordine speciale per uno specifico articolo non presente in stock che deve venire spedito a un determinato cliente. L'articolo viene spedito dal fornitore abituale alla warehouse dell'azienda e a questo punto può essere spedito al cliente da solo oppure insieme ad altri articoli di un ordine diverso."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 84b7a66734b3da5bdbc474bc43e463481c7f6ba5
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="create-special-orders"></a>Creare ordini speciali
È possibile creare un ordine speciale per uno specifico articolo non presente in stock che deve venire spedito a un determinato cliente. L'articolo viene spedito dal fornitore abituale alla warehouse dell'azienda e a questo punto può essere spedito al cliente da solo oppure insieme ad altri articoli di un ordine diverso.  

Gli ordini speciali implicano il collegamento dell'ordine di acquisto all'ordine di vendita allo scopo di garantire che lo specifico articolo non presente in stock venga prelevato e consegnato al cliente.  

Prima di poter utilizzare questa funzionalità è necessario impostare le schede per il cliente, il fornitore e l'articolo interessati dall'ordine.  

## <a name="to-create-a-special-order"></a>Per creare un ordine speciale  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Ordine di vendita**, quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Creare e compilare un  ordine di vendita per l'articolo. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).
3.  Nella Scheda dettaglio **Righe** compilare la riga di vendita. Nel campo **Codice acquisto** selezionare un codice di acquisto per il quale il campo **Ordine speciale** sia selezionato.

    È quindi necessario creare un ordine di acquisto da una richiesta di approvvigionamento.  
4. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Richiesta di approvvigionamento**, quindi scegliere il collegamento correlato.  
5. Scegliere l'azione **Ordine speciale** e scegliere l'azione **Ottieni ordini vendite**.  
6.  Nella finestra **Prendi ordini vendite** vengono visualizzati i risultati in cui **Nr. documento** è il numero dell'ordine di vendita. Scegliere il pulsante **OK**. Viene creata una riga di richiesta di approvvigionamento per l'articolo.  
7.  Nella riga di richiesta di approvvigionamento selezionare **Nuovo** nel campo **Messaggio azione**.  
8.  Nella finestra **Richiesta di approvv.** scegliere l'azione **Esegui messaggi di azione**. Viene aperta la finestra **Approv. - Esegui mess. azioni**. Scegliere il pulsante **OK**.  

    Verrà quindi visualizzato un messaggio con l'informazione che gli ordini di acquisto sono stati creati. Scegliere il pulsante **OK**.  

Un ordine di acquisto creato come ordine speciale per un ordine di vendita viene rispettato dal sistema di pianificazione poiché pareggia la domanda e l'offerta. Ossia, l'ordine di acquisto (approvvigionamento) resta collegato all'ordine di vendita (domanda), anche se l'ordine di acquisto può approvvigionare un'altra domanda precedente. Per ulteriori informazioni, vedere [Dettagli di programmazione: Metodi di riordino](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Se l'elemento è già prenotato, non è possibile utilizzare la funzionalità ordine speciale. Pertanto, per gli articoli venduti in ordini speciali, assicurarsi che il campo **Impegno** nella scheda articolo non sia impostato su **Sempre**.  

## <a name="see-also"></a>Vedi anche  
[Utilizzare gli articoli non in stock](inventory-how-work-nonstock-items.md)  
[Vendite](sales-manage-sales.md)  
[Effettuare spedizioni dirette](sales-how-drop-shipment.md)   
[Dettagli di progettazione: Metodi di riordino](design-details-reservation-order-tracking-and-action-messaging.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


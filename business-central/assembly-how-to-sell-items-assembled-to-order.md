---
title: Come vendere articoli assemblati su ordine | Microsoft Docs
description: Se l'articolo è impostato per l'assemblaggio su ordine, si presume che l'articolo non sia in magazzino e debba essere combinato in modo specifico a un ordine di vendita. Quando si immette l'articolo in una riga dell'ordine di vendita, un ordine di assemblaggio viene automaticamente creato e collegato all'ordine di vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 99111bce195e4436aac597cc4eb2e5f8f3ef77cd
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747293"
---
# <a name="sell-items-assembled-to-order"></a>Vendere articoli assemblati su ordine
Se il campo **Criteri di assemblaggio** nella scheda articolo di un articolo di assemblaggio è **Assemblaggio su ordine**, non si prevede che l'articolo sia nel magazzino e deve essere assemblato in modo specifico a un ordine di vendita. Quando si immette l'articolo in una riga dell'ordine di vendita, un ordine di assemblaggio viene automaticamente creato e collegato all'ordine di vendita.  

> [!NOTE]  
>  Se alcuni articoli di assemblaggio su ordine sono già in magazzino, è possibile dedurne la relativa quantità dall'ordine di assemblaggio e impegnarla dal magazzino. Per altre informazioni, vedere [Vendere gli articoli di magazzino nei flussi assemblaggio su ordine](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

In questa procedura, si elabora la vendita di un articolo che verrà assemblato in base alle specifiche richieste dal cliente. I passaggi includono l'avvio della riga dell'ordine di vendita, la personalizzazione dell'articolo di assemblaggio attraverso la modifica di componenti e risorse, il controllo della disponibilità per definire una data di consegna e il rilascio dell'ordine di vendita per l'assemblaggio e la spedizione immediata.  

> [!NOTE]  
>  La procedura seguente non include i passaggi standard dell'ordine di vendita da eseguire prima del passaggio di immissione dell'articolo di assemblaggio su ordine in una riga dell'ordine di vendita.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Per vendere un articolo assemblato su ordine  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ordini vendita** e quindi scegliere il collegamento correlato.  
2.  Creare un ordine di vendita. Per ulteriori informazioni, vedere [Vendere prodotti](sales-how-sell-products.md).  
3.  Nel campo **Nr.** immettere un articolo impostato per l'assemblaggio su ordine.  
4.  Nel campo **Cod. ubicazione** specificare da quale ubicazione verrà venduto l'articolo. Il processo di assemblaggio avverrà in tale ubicazione.  
5.  Nel campo **Quantità** immettere il numero di unità da vendere.  

    > [!NOTE]  
    >  Se uno o più componenti della quantità richiesta dell'articolo di assemblaggio non sono disponibili, viene aperta una pagina di avviso di disponibilità dettagliata. Per ulteriori informazioni, vedere Disponibilità assemblaggio.  

    Un ordine di assemblaggio viene ora automaticamente creato e collegato alla riga dell'ordine di vendita. La data di scadenza dell'ordine di assemblaggio è sincronizzata alla data di spedizione della riga dell'ordine di vendita.  

    La quantità da vendere viene copiata nel campo **Qtà per assemblaggio su ordine**, in cui si indica che il setup dell'articolo prevede l'assemblaggio su ordine dell'intera quantità presente nella riga di vendita. È possibile ridurre la quantità da assemblare su ordine, ad esempio se si è a conoscenza che alcuni articoli sono già disponibili. Per altre informazioni, vedere [Vendere gli articoli di magazzino nei flussi assemblaggio su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Per indicare che il cliente desidera un articolo aggiuntivo in un kit, nella Scheda dettaglio **Righe** scegliere l'azione **Riga**, l'azione **Assemblaggio su ordine**, quindi l'azione **Righe di assemblaggio su ordine** per visualizzare e modificare i componenti di assemblaggio standard. In alternativa, scegliere il campo **Qtà per assemblaggio su ordine** .  
7.  Nella pagina **Righe di assemblaggio su ordine** creare una nuova riga di tipo **Articolo** per il contenuto del kit aggiuntivo richiesto. La riga rappresenta un componente di assemblaggio aggiuntivo.  

    È anche possibile personalizzare l'ordine aumentando la quantità di un articolo standard nel kit. È possibile eseguire questa operazione aumentando il valore del campo **Quantità per** nella riga specifica dell'ordine di assemblaggio.  

    > [!NOTE]  
    >  La pagina **Righe di assemblaggio su ordine** contiene solo i campi di base che un agente dovrà utilizzare per personalizzare la lista dei componenti, aggiungere i numeri di tracciabilità articolo o risolvere i problemi di disponibilità dei componenti. Per vedere altre informazioni sull'ordine di assemblaggio, ad esempio la data di inizio dell'ordine di assemblaggio, scegli l'azione **Mostra documenti**. Viene aperta una visualizzazione completa dell'ordine di assemblaggio collegato alla riga dell'ordine di vendita. Non è possibile modificare il contenuto della maggior parte dei campi della testata ordine di assemblaggio, né registrare l'output di assemblaggio da questa posizione perché è necessario utilizzare la registrazione di spedizione della riga ordine di vendita.  
    >   
    >  Nella testata degli ordini di assemblaggio collegati, soltanto il campo **Data inizio** può essere modificato per consentire agli addetti all'assemblaggio di specificare una data antecedente alla data di scadenza per l'inizio del processo. È possibile modificare tutti i campi nelle righe dell'ordine di assemblaggio collegato in modo da permettere agli addetti alla warehouse di immettere i dati relativi al consumo durante il processo.  

8.  Esaminare o rispondere ai problemi di disponibilità dei componenti. Ad esempio, selezionare un articolo sostitutivo disponibile o definire una data di scadenza successiva.  
9. Chiudere la pagina **Righe di assemblaggio su ordine**. L'ordine di assemblaggio collegato è ora pronto per iniziare l'assemblaggio degli articoli personalizzati entro la data di scadenza.  
10. Nell'ordine di vendita, scegliere l'azione **Rilascio** per notificare al reparto di assemblaggio che il processo di assemblaggio può iniziare.  
11. Nel reparto di assemblaggio eseguire i passaggi di assemblaggio degli articoli venduti in questa procedura. Per ulteriori informazioni, vedere [Assemblare articoli](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Vedi anche  
[Gestione assemblaggio](assembly-assemble-items.md)  
[Utilizzare le distinte base](inventory-how-work-BOMs.md)  
[Magazzino](inventory-manage-inventory.md)  
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
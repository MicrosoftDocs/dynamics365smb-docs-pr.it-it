---
title: 'Procedura: Aggiornare i dati delle transazioni IVA'
description: Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti nella versione italiana di Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 74fbb94b4f383dd5516f5f845396491f3e2a7cee
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780158"
---
# <a name="update-vat-transactions-data"></a>Aggiornare i dati delle transazioni IVA
Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti eseguendo il report **Aggiorna data transazione IVA**. È inoltre necessario eseguire questo report se sono state apportate modifiche al setup in base ai nuovi requisiti delle autorità fiscali.  

È possibile eseguire il report **Aggiorna data transazione IVA** come test prima di modificare i dati. Dopo avere verificato che i filtri soddisfano le previsioni e le richieste delle autorità fiscali, eseguire nuovamente il report per apportare le modifiche appropriate ai dati.  

> [!CAUTION]  
>  Prima di eseguire il report **Aggiorna data transazione IVA**, è necessario attivare il log delle modifiche nella pagina **Setup log modifiche**. Inoltre, è necessario attivare la registrazione delle modifiche nel campo **Includi in report transazioni IVA** nella tabella **Movimenti IVA**.  

## <a name="to-update-vat-transaction-data"></a>Per aggiornare i dati delle transazioni IVA  

1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Aggiorna data transazione IVA** e quindi scegliere il collegamento correlato.  
2.  Facoltativamente, nella Scheda dettaglio **Movimenti IVA** impostare i filtri appropriati.  
3.  Nella Scheda dettaglio **Opzioni** compilare i campi come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Confronta con soglia**|Selezionare per confrontare i movimenti IVA rispetto agli importi di soglia specificati nel setup registrazioni IVA.|  
    |**Mostra solo elenco**|Selezionare se non si desidera aggiornare i dati.<br /><br /> Se si seleziona questo campo, [!INCLUDE[prod_short](../../includes/prod_short.md)] stampa un report in modo da poter verificare le modifiche prima che i dati vengano modificati. Il report contiene una riga per ogni documento in cui l'imponibile IVA sia uguale o maggiore degli importi di soglia. **Avviso:** Non selezionare questo campo e il campo **Imposta Includi in report transazioni IVA**.|  
    |**Imposta Includi in report transazioni IVA**|Selezionare per impostare **Imposta Includi in report transazioni IVA** su **Sì** in tutti i movimenti IVA in cui gli importi soddisfano gli importi di soglia specificati nel setup registrazioni IVA. **Avviso:** Se si seleziona questo campo, i dati vengono aggiornati. È consigliabile eseguire il report come test prima di eseguirlo per modificare i dati.|  

4.  Scegliere il pulsante **Stampa** per aggiornare i dati delle transazioni IVA oppure scegliere il pulsante **Anteprima** per visualizzare le modifiche.  

Quando si esegue il report, [!INCLUDE[prod_short](../../includes/prod_short.md)] elabora i movimenti IVA in base ai filtri impostati. Le seguenti regole sono applicabili:  

- Il campo **In blacklist** per il movimento IVA deve essere vuoto.  
- Il campo **Tipo** del movimento IVA non deve essere **Liquidazione**.  

## <a name="see-also"></a>Vedi anche  
[Impostare l'IVA](../../finance-setup-vat.md)  
 [Preparare i report di transazioni IVA](how-to-prepare-for-vat-transactions-reports.md)   
 [IVA italiana](italian-vat.md)   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
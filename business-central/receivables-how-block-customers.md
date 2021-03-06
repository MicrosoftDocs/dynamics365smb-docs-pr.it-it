---
title: Come bloccare le vendite per i clienti
description: Se necessario, è possibile impedire a un cliente di essere incluso nei documenti di vendita e in altre transazioni di vendita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1caf2fb0586cf704e5fc1354b3b4a0be096dc709
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781740"
---
# <a name="block-customers"></a>Blocca clienti
È possibile bloccare un cliente, ad esempio a causa di insolvenza, in modo che il cliente non possa essere aggiunto ai documenti di vendita o che non sia possibile registrare transazioni per il cliente.

Oltre a bloccare un cliente, è possibile impostare le transazioni crediti v/clienti per il cliente con stato in sospeso collegato ai solleciti. Per ulteriori informazioni, vedere [Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md).   

Nella seguente tabella vengono illustrate le opzioni per bloccare i clienti.  

|Opzione|Descrizione|  
|--------------------|------------|  
|**Vuoto**|Per il cliente sono consentite tutte le transazioni.|
|**Spedizione**|Non è possibile creare nuovi ordini e nuove spedizioni per il cliente. È possibile fatturare le spedizioni esistenti non ancora fatturate.|  
|**Fattura**|Non è possibile creare nuovi ordini, nuove spedizioni o nuove fatture per il cliente. Non è possibile fatturare le spedizioni esistenti non ancora fatturate. Puoi comunque inviare promemoria e note di addebito interessi al cliente.|  
|**Tutto**|Non è consentita alcuna transazione, inclusi i pagamenti, per il cliente.|  

## <a name="to-block-a-customer"></a>Per bloccare un cliente  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Selezionare un cliente, quindi scegliere l'azione **Modifica**.
3. Nel campo **Bloccato**, scegliere cosa bloccare, come descritto nella tabella precedente.

## <a name="see-also"></a>Vedere anche  
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Come bloccare le vendite ai clienti
description: 'Se necessario, è possibile impedire a un cliente di essere incluso nei documenti di vendita e in altre transazioni di vendita.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="block-customers"></a>Blocca i clienti
È possibile bloccare un cliente, ad esempio a causa di insolvenza, in modo che non possa essere aggiunto ai documenti di vendita o che non possano essere registrate transazioni per quel cliente.

Oltre a bloccare un cliente, è possibile impostare le transazioni crediti v/clienti per il cliente con stato in sospeso collegato ai solleciti. Per ulteriori informazioni, vedere [Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md).   

Nella seguente tabella vengono illustrate le opzioni per bloccare i clienti.  

|Opzione|Descrizione|  
|--------------------|------------|  
|**Vuoto**|Per il cliente sono consentite tutte le transazioni.|
|**Spedizione**|Non è possibile creare nuovi ordini o nuove spedizioni per questo cliente. È possibile fatturare le spedizioni esistenti non ancora fatturate.|  
|**Fattura**|Non è possibile creare nuovi ordini, nuove spedizioni e nuove fatture per questo cliente. Le spedizioni esistenti non ancora fatturate non potranno essere fatturate. Puoi comunque inviare promemoria e note di addebito interessi al cliente.|  
|**Tutto**|Non è consentita alcuna transazione, inclusi i pagamenti, per il cliente.|  

## <a name="to-block-a-customer"></a>Per bloccare un cliente
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Selezionare un cliente, quindi scegliere l'azione **Modifica**.
3. Nel campo **Bloccato**, scegliere cosa bloccare, come descritto nella tabella precedente.

## <a name="see-also"></a>Vedere anche
[Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Riscuotere i saldi inevasi](receivables-collect-outstanding-balances.md)  
[Gestione della contabilità clienti](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

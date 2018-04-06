---
title: Gestione dei prezzi di assistenza | Documenti Microsoft
description: In questo argomento viene descritto come applicare il prezzo migliore agli ordini di assistenza, di impostare accordi di prezzi di assistenza personalizzati per i vari clienti, di migliorare l'efficienza degli addetti all'assistenza e di accelerare il processo di fatturazione.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b2607dce0b62a3a1433362491692687d4c868d06
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="service-price-management"></a>Gestione dei prezzi di assistenza
La funzionalità di gestione dei prezzi di assistenza consente di applicare il prezzo migliore agli ordini di assistenza, di impostare accordi di prezzi di assistenza personalizzati per i vari clienti, di migliorare l'efficienza degli addetti all'assistenza e di accelerare il processo di fatturazione.  
  
Può altresì essere utilizzata per impostare gruppi di prezzi di assistenza diversi, tenendo in considerazione l'articolo o il gruppo di articoli in assistenza oltre che il tipo di guasto che ha originato il compito di assistenza. Tali gruppi possono essere impostati per un periodo di tempo limitato o per un determinato cliente o valuta. È inoltre possibile utilizzare le strutture di calcolo dei prezzi come modelli per assegnare un determinato prezzo a uno specifico compito di assistenza.  
  
Ad esempio, ciò consente di assegnare articoli specifici inclusi nel prezzo di assistenza, oltre al tipo di lavoro previsto. È inoltre possibile utilizzare IVA e importi sconti diversi per i diversi gruppi di prezzi di assistenza. Per assicurarsi che vengano applicati i prezzi corretti, è possibile assegnare prezzi fissi, minimi o massimi, a seconda dei contratti stipulati con i clienti.  
  
Prima di rettificare il prezzo di un articolo in assistenza in un ordine di assistenza, viene fornita una sintesi dei futuri risultati della rettifica del prezzo. È possibile approvare i risultati oppure apportare modifiche aggiuntive, se si desidera ottenere un risultato diverso. L'intera rettifica viene effettuata riga per riga, pertanto non verranno create righe aggiuntive.  
  
Infine, grazie alle statistiche sui gruppi di prezzi di assistenza e ai report standard, è possibile tenere traccia della redditività di ciascun gruppo di prezzi di assistenza.  
  
## <a name="service-price-adjustment-groups"></a>Gruppi di rettifica dei prezzi di assistenza  
I gruppi di rettifica dei prezzi di assistenza consentono di impostare diversi tipi di rettifiche ai prezzi. È ad esempio possibile impostare un gruppo di rettifica dei prezzi di assistenza per rettificare i prezzi dei pezzi di ricambio, uno per rettificare i prezzi della manodopera, un altro ancora per i prezzi di costo e così via. È anche possibile specificare se la rettifica dei prezzi di assistenza dovrà essere applicata solo a uno specifico articolo o risorsa oppure a tutti gli articoli o le risorse.  
  
Ciascun gruppo di rettifica dei prezzi di assistenza contiene le informazioni relative alle rettifiche da apportare alle righe di assistenza.  
  
La funzione di rettifica dei prezzi di assistenza non viene applicata agli articoli in assistenza che appartengono a contratti di assistenza. È possibile rettificare solo i prezzi di assistenza per gli articoli che fanno parte di un ordine di assistenza. Non è possibile rettificare il prezzo di un articolo in assistenza se dispone di garanzia. Non è possibile rettificare il prezzo di un articolo in assistenza in un ordine di assistenza se la riga di assistenza collegata a esso è stata registrata come fattura, completamente o in parte.  
  
Quando si esegue la funzione di rettifica dei prezzi di assistenza, tutti gli sconti presenti nell'ordine verranno sostituiti dai valori di rettifica dei prezzi di assistenza.  
  
## <a name="service-price-groups"></a>Gruppi di definizione dei prezzi di assistenza  
I gruppi di prezzi di assistenza consentono di impostare gruppi di articoli in assistenza a cui verranno applicate le stesse definizioni speciali del prezzo di assistenza. Dopo aver impostato i gruppi di prezzi di assistenza, è possibile assegnarli agli articoli in assistenza nelle relative righe. È inoltre possibile assegnare gruppi di prezzi di assistenza ai gruppi di articoli in assistenza.  
  
Prima di assegnare un gruppo di prezzi di assistenza a un articolo in assistenza, è necessario determinare a quale area guasto, valuta o gruppo di rettifica dei prezzi di assistenza si applichi il gruppo di prezzi di assistenza. È necessario determinare in base a quale importo è necessario rettificare il prezzo di assistenza e se l'importo deve includere IVA e sconti. È inoltre necessario determinare se la rettifica riguarda un importo fisso oppure deve essere applicata solo a determinate condizioni.  
  
Quando si assegna un gruppo di prezzi di assistenza a un articolo in assistenza, all'articolo vengono applicate tutte le definizioni speciali del prezzo di assistenza impostate in questo gruppo.  
  
## <a name="service-pricing"></a>Definizione dei prezzi di assistenza  
I tipi effettivi di definizione dei prezzi di assistenza (prezzo e tipo di rettifica prezzo) vengono impostati per una combinazione di gruppi di prezzi di assistenza e gruppi di prezzi ai clienti. Per ogni tipo di definizione del prezzo di assistenza viene selezionato un gruppo di rettifica del prezzo di assistenza. Vengono inoltre specificati il tipo di rettifica del prezzo di assistenza, ovvero fisso, massimo o minimo, e il prezzo effettivo.  
  
Ad esempio è possibile impostare tipi di definizione del prezzo di assistenza per un gruppo di prezzi di assistenza per una radio. Per i clienti senza un gruppo di prezzi è possibile decidere di determinare il prezzo dell'assistenza con il prezzo di manodopera più alto, che corrisponde al gruppo di rettifica del prezzo della manodopera. Per i clienti con un particolare gruppo di prezzi è possibile decidere di determinare il prezzo dell'assistenza con un prezzo fisso di manodopera, ovvero lo stesso gruppo di rettifica del prezzo della manodopera.  
  
## <a name="service-price-adjustment"></a>Rettifica dei prezzi di assistenza  
La rettifica dei prezzi di assistenza consente di rettificare il prezzo di un articolo, risorsa, conto di contabilità generale o costo in un ordine di assistenza.  
  
Una volta immesso un articolo nella riga di articolo in assistenza, immettere tutte le informazioni relative ai costi di tale articolo nelle righe di assistenza. Quando si esegue la funzione Rettifica prezzo assistenza, è possibile visualizzare un'anteprima delle rettifiche ai prezzi. È possibile apportare eventuali modifiche, se necessario. Una volta confermate le modifiche, le rettifiche verranno calcolate e trasferite nelle rispettive righe di assistenza. A questo punto sarà possibile registrare l'ordine di assistenza.  
  
In base al tipo di rettifica dei prezzi di assistenza, viene calcolato l'importo totale delle rettifiche.  
  
Nella seguente tabella vengono illustrati i calcoli.  
  
|Opzione | Description |  
|----------------------------------|---------------------------------------|  
|**Prezzo fisso**|Viene applicato un prezzo fisso per l'articolo in assistenza, la risorsa, il conto di contabilità generale o il costo, indipendentemente dai costi effettivi o dai normali addebiti. Se si seleziona questa opzione, la rettifica del prezzo di assistenza raggiungerà l'importo esatto specificato nel gruppo di prezzi di assistenza.|  
|**Massimo**|Viene stabilito un limite massimo al prezzo che verrà applicato al cliente, indipendentemente dal costo reale o dal normale addebito. Se si seleziona questa opzione, la rettifica del prezzo di assistenza verrà effettuata solo qualora il prezzo totale superi l'importo specificato nel gruppo di prezzi di assistenza.|  
|**Minimo**|Viene stabilito un limite minimo al prezzo che verrà applicato al cliente, indipendentemente dal costo reale o dal normale addebito. Se si seleziona questa opzione, la rettifica del prezzo di assistenza verrà effettuata solo qualora il prezzo totale sia inferiore all'importo specificato nel gruppo di prezzi di assistenza.|  
  
## <a name="see-also"></a>Vedi anche  
[Impostare prezzi e costi aggiuntivi per i servizi assistenza](service-how-setup-service-costs-pricing.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  


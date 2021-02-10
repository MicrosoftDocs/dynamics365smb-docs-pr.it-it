---
title: Risoluzione dei problemi relativi agli errori di sincronizzazione | Microsoft Docs
description: Fornisce alcune indicazioni per l'identificazione e la risoluzione degli errori di sincronizzazione.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 1c2181ee381425a168a9b6b6ce321e595a01ed8e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754994"
---
# <a name="troubleshooting-synchronization-errors"></a>Risoluzione dei problemi relativi agli errori di sincronizzazione
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Ci sono molte parti mobili coinvolte nell'integrazione di [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)] e a volte le cose vanno male. Questo argomento evidenzia alcuni degli errori tipici che si verificano e fornisce alcuni suggerimenti su come risolverli.

Gli errori si verificano spesso a causa di un'operazione che un utente ha eseguito per i record associati o di un errore di impostazione dell'integrazione. Per gli errori relativi ai record associati, gli utenti possono risolverli da soli. Questi errori sono causati da azioni quali l'eliminazione di dati in una, ma non entrambe, le app aziendali e quindi la sincronizzazione. Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Esempio
Questo video mostra un esempio di come risolvere gli errori che si sono verificati durante la sincronizzazione con Sales. Il processo sarà lo stesso per tutte le integrazioni. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Gli errori correlati all'impostazione dell'integrazione richiedono in genere l'attenzione dell'amministratore. È possibile visualizzare questi errori nella pagina **Errori di sincronizzazione integrazione**. Esempi di alcuni problemi tipici sono:  
  
* Le autorizzazioni e i ruoli assegnati agli utenti non sono corretti.  
* L'account amministratore è stato specificato come utente di integrazione.  
* La password dell'utente di integrazione è impostata per richiedere una modifica quando l'utente esegue l'accesso.  
* I tassi di cambio per le valute non sono specificati nell'una o nell'altra app.  
  
È necessario risolvere manualmente gli errori, ma in alcuni casi la pagina risulta utile. Ad esempio:  

* I campi **Origine** e **Destinazione** possono contenere collegamenti alla riga in cui è stato trovato l'errore. Fare clic sul collegamento per indagare sull'errore.  
* Le azioni **Elimina movimenti risalenti a più di 7 giorni prima** e **Elimina tutti i movimenti** puliranno l'elenco. In genere, si utilizzano queste azioni dopo aver risolto la causa di un errore che interessa molti record. Tuttavia, prestare attenzione. Queste azioni potrebbero eliminare errori che sono ancora rilevanti.

A volte i timestamp sui record possono causare conflitti. La tabella "Record integrazione CDS" mantiene i timestamp "Data ultima modifica sincr." e "Data ultima modifica sincr. CDS" per l'ultima integrazione eseguita in entrambe le direzioni di una riga. Questi timestamp vengono confrontati con i timestamp nei record Business Central e Sales. In Business Central, il timestamp è nella tabella Record integrazione.

È possibile filtrare i record che devono essere sincronizzati confrontando i timestamp delle righe nella tabella "Mapping tabella integrazione" campi "Sinc. filtro data modifica" e "Sinc. fltr. data mod. tab. int.".

Il messaggio di errore di conflitto "Impossibile aggiornare il record del cliente perché ha una data di modifica più recente del record dell'account" o "Impossibile aggiornare il record dell'account perché ha una data di modifica più recente del record del cliente" può verificarsi se una riga ha un timestamp che è più grande di IntegrationTableMapping. "Sinc. filtro data modifica" ma non è più recente del timestamp sul record di integrazione delle vendite. Significa che la riga di origine è stato sincronizzato manualmente e non dal movimento coda processi. 

Il conflitto si verifica perché anche la riga di destinazione è stato modificato: il timestamp della riga è più recente del timestamp del record di integrazione delle vendite. Il controllo della destinazione avviene solo per le tabelle bidirezionali. 

Questi record vengono spostati nella pagina "Record di sincronizzazione ignorati", che si apre dalla pagina Setup connessione Microsoft Dynamics in Business Central. In questa pagina è possibile specificare le modifiche da conservare, quindi sincronizzare nuovamente i record.

## <a name="remove-couplings-between-records"></a>Rimuovere associazioni tra record
Quando qualcosa va storto nell'integrazione ed è necessario annullare l'associazione dei record per interrompere la sincronizzazione, è possibile farlo per uno o più record alla volta. È possibile annullare l'associazione di uno o più record nelle pagine di elenco o nella pagina **Errori di sincronizzazione dati associati** scegliendo una o più righe e quindi **Elimina associazione**. È inoltre possibile rimuovere tutte le associazioni per una o più mapping di tabella nella pagina **Mapping tabella integrazione**. 

## <a name="see-also"></a>Vedere anche
[Integrazione con Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Impostazione di account utente per l'integrazione con Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Impostare una connessione a Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  

---
title: 'Procedura: Preparare i report di transazioni IVA'
description: È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 85a21861550f76fdeb269a37883f5e42aea3b823
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "912555"
---
# <a name="prepare-for-vat-transactions-reports"></a>Preparare i report di transazioni IVA
È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA. L'autorità fiscale stabilisce le soglie richieste per la dichiarazione. Attualmente, la soglia è impostata su zero, a indicare che tutte le transazioni vengono dichiarate. Per prepararsi per le dichiarazioni, è necessario impostare la registrazione IVA in modo da includere gli importi di dichiarazione della transazione IVA.  

## <a name="to-set-up-vat-transaction-amounts"></a>Per impostare gli importi delle transazioni IVA  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Cat. reg. business IVA** e scegliere il collegamento correlato.  
2.  Scegliere l'azione **Importo report transazioni IVA**.  
3.  Compilare i campi come indicato nella tabella seguente.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|  
    |**Persona fisica**|Selezionare se questo cliente è una persona fisica.|  
    |**Soggetto residente**|Specificare se il cliente è residente in Italia.<br /><br /> Se un cliente non è un residente, è necessario specificare anche un rappresentante fiscale nella Scheda dettaglio **Commercio estero**.|  
    |**Primo nome**|Specifica il nome della persona.|  
    |**Cognome**|Specifica il cognome della persona.|  
    |**Data di nascita**|Specifica la data di nascita della persona.|  
    |**Luogo di nascita**|Specifica il luogo di nascita della persona.|  

3.  Se il cliente non è in residente in Italia e non è una persona fisica, è necessario specificare un rappresentante fiscale per il cliente.  

    > [!NOTE]  
    >  Prima di poter specificare un rappresentante fiscale, è necessario creare il rappresentante fiscale come contatto.  

### <a name="to-specify-a-tax-representative-for-a-non-resident-customer"></a>Per specificare un rappresentante fiscale per un cliente non residente  

1.  Scegliere l'icona ![Cerca pagina o report](../../media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.  
2. Selezionare un cliente.
2.  Compilare i campi nella Scheda dettaglio **Commercio estero** come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo di rappresentante fiscale**|Specifica se il rappresentante fiscale è un cliente o un contatto. È necessario impostare il campo su **Contatto**.|  
    |**Nr. rappresentante fiscale**|Specificare il contatto che è il rappresentante fiscale per il cliente.|  

    È necessario impostare le informazioni di modo che [!INCLUDE[d365fin](../../includes/d365fin_md.md)] terrà traccia delle nuove transazioni che corrispondono alle soglie specificate dalle autorità fiscali. Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti. Per ulteriori informazioni, vedere [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md). È quindi possibile creare i report transazioni IVA. Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).

## <a name="see-also"></a>Vedi anche  
 [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md)   
 [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md)   
 [IVA italiana](italian-vat.md)

---
title: 'Preparare report di transazioni IVA [IT]'
description: Il seguente articolo spiega come preparare e inviare i report periodici delle transazioni IVA alle autorità fiscali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/17/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Preparare report di transazioni IVA nella versione italiana
È necessario inviare i report periodici alle autorità fiscali per visualizzare l'elenco tutte le transazioni che includono l'IVA. L'autorità fiscale stabilisce le soglie richieste per la dichiarazione. Attualmente, la soglia è impostata su zero, a indicare che tutte le transazioni vengono dichiarate. Per prepararsi per le dichiarazioni, è necessario impostare la registrazione IVA in modo da includere gli importi di dichiarazione della transazione IVA.  

## Per impostare gli importi delle transazioni IVA  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup registrazioni IVA**, quindi scegli il collegamento correlato.  
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

### Per specificare un rappresentante fiscale per un cliente non residente  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Clienti**, quindi scegli il collegamento correlato.  
2. Selezionare un cliente.
2.  Compilare i campi nella Scheda dettaglio **Commercio estero** come descritto nella tabella riportata di seguito.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo di rappresentante fiscale**|Specifica se il rappresentante fiscale è un cliente o un contatto. È necessario impostare il campo su **Contatto**.|  
    |**Nr. rappresentante fiscale**|Specificare il contatto che è il rappresentante fiscale per il cliente.|  

    Imposti le informazioni di modo che [!INCLUDE[prod_short](../../includes/prod_short.md)] tenga traccia delle nuove transazioni che soddisfano le soglie specificate dalle autorità fiscali. Prima di creare il primo report transazioni IVA, è necessario preparare i dati esistenti. Per ulteriori informazioni, vedere [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md). È quindi possibile creare i report transazioni IVA. Per ulteriori informazioni, vedere [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md).

## Vedere anche  
 [Aggiornare i dati delle transazioni IVA](how-to-update-vat-transactions-data.md)   
 [Creare report elettronici di transazioni IVA](how-to-create-electronic-vat-transactions-reports.md)   
 [IVA italiana](italian-vat.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
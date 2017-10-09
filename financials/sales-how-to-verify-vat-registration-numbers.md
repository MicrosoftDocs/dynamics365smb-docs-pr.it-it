---
title: 'Procedura: Verificare i numeri di partita IVA | Documenti Microsoft'
description: "È possibile utilizzare un servizio Web dell'UE per verificare che i numeri di partita IVA immessi nelle schede cliente, fornitore o contatto siano validi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Procedura: verificare i numeri di partita IVA
È possibile utilizzare un servizio Web dell'UE per verificare che i numeri di partita IVA immessi nelle schede cliente, fornitore o contatto siano validi.  

 Quando si modifica il campo **Partita IVA** in una scheda in cui il valore nel campo **Codice paese** è un paese UE, il nuovo numero di partita IVA e il proprio ID utente vengono registrati nella finestra **Log partita IVA**. Per verificare un numero di partita IVA, fare clic sul pulsante **Verifica partita IVA** nella finestra **Log partita IVA**. Una nuova riga viene creata ogni volta che si utilizza la funzione di verifica. Se si è potuto verificare il numero, il campo  **Stato** contiene **Valido**. Se non si è potuto verificare il numero, il campo**Stato** contiene **Non valido** ed è necessario quindi modificare il numero nel campo **Partita IVA** nella scheda e avviare nuovamente la funzione di verifica.  

 L'URL di gestione del servizio Web di default viene impostato nel campo **URL convalida partita IVA** della finestra **Setup contabilità generale**.  

 Nella tabella **Formato nr. partita IVA**, è possibile cambiare per ogni paese i diversi formati di numero di partita IVA che gli utenti possono immettere nel campo **Partita IVA**.  

> [!WARNING]  
>  Questo servizio Web utilizza il protocollo HTTP, il che significa che i dati trasferiti tramite il servizio non sono crittografati.  

> [!NOTE]  
>  È possibile che si verifichino periodi di inattività per questo servizio per i quali Microsoft non è responsabile, in quanto il servizio fa parte di un'ampia rete dell'UE di registri IVA locali.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>Per verificare un numero di partita IVA da una scheda cliente  
Di seguito viene descritto come verificare un numero di partita IVA per un cliente. I passaggi sono simili per un contatto o un fornitore.   
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Clienti**, quindi scegliere il collegamento correlato.  

2.  Aprire la scheda di un cliente in cui si desidera verificare il numero di partita IVA.  

    > [!NOTE]  
    >  Il campo **Codice paese** nella scheda cliente deve contenere un paese UE.  
3.  Nella Scheda dettaglio **Fatturazione**, fare clic sul pulsante Drilldown a discesa accanto al campo **Partita IVA**.  

    La finestra **Log partita IVA** si apre visualizzando una riga in cui il campo **Stato** contiene **Non verificato**.  
4.  Scegliere l'azione **Verifica partita IVA**.  

     Una nuova riga viene creata quando il campo **Stato** contiene **Valido** o **Non valido**.  
5.  Se il campo **Stato** contiene **Non valido**, modificare il numero nel campo **Partita IVA** nella scheda quindi ripetere i passaggi da 3 a 4.  

## <a name="see-also"></a>Vedi anche  
[Finanze](finance.md)  
[Procedura: Registrare nuovi clienti](sales-how-register-new-customers.md)  
[Procedura: Registrare nuovi fornitori](purchasing-how-register-new-vendors.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


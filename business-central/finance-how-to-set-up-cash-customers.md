---
title: Come impostare un cliente per vendite in contanti | Microsoft Docs
description: Questo argomento descrive la procedura per impostare i clienti che pagano in contanti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a4f73de177129f5bc33808e6acf74bd273ae0d33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915562"
---
# <a name="set-up-cash-customers"></a>Impostare i clienti per vendite in contanti
Non è possibile creare una fattura senza un numero di cliente. Ciò si applica anche nel caso di una vendita in contanti, quando non ci sarebbe niente da registrare in un conto cliente.  

## <a name="to-set-up-a-cash-customer"></a>Per impostare un cliente per vendite in contanti  
1.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cliente** e quindi scegliere il collegamento correlato.  
2.  Creare una nuova scheda **Cliente**. Per ulteriori informazioni, vedere [Registrare nuovi clienti](sales-how-register-new-customers.md).
3.  Nel campo **Nr.** immettere ad esempio **Incassi**.  
4.  Nel campo **Nome** immettere ad esempio **Vendita in Contante**.  
5.  Nella Scheda dettaglio **Fatturazione** compilare i campi **Cat. reg. cliente** e **Cat. reg. business**.  

 È stato così impostato un nuovo cliente con informazioni sufficienti per la fatturazione.  

> [!NOTE]  
>  Può essere stata scelta una categoria di registrazione che viene utilizzata anche per le vendite a credito interne. Se si desidera mantenere separati i dati sulle vendite in contanti, ad esempio con un conto speciale di vendita o incassi, è possibile impostare per questo scopo una nuova categoria di registrazione.  
>   
>  È necessario immettere un numero di conto incassi per la categoria di registrazione, anche se il saldo di questo conto dopo la registrazione di una fattura corrisponderà sempre a 0.  

## <a name="see-also"></a>Vedere anche
[Gestione della contabilità clienti](receivables-manage-receivables.md)  
[Registrare nuovi clienti](sales-how-register-new-customers.md)    
[Finanze](finance.md)  


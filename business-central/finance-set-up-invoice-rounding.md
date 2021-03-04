---
title: Impostare l'arrotondamento delle fatture | Microsoft Docs
description: È possibile arrotondare gli importi delle fatture quando si creano fatture. È inoltre possibile che la normativa o le autorità locali impongano una modalità di arrotondamento specifica, ad esempio a un importo divisibile per 0,05.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 302552a32e2c6322c156a22095c926dee40b4cf7
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746593"
---
# <a name="set-up-invoice-rounding"></a>Impostare l'arrotondamento delle fatture
Se è necessario arrotondare gli importi delle fatture quando si creano le fatture, è possibile utilizzare la funzione di arrotondamento automatica. Quando una fattura viene arrotondata, viene aggiunta un'ulteriore riga con l'importo di arrotondamento. Questa riga verrà contabilizzata insieme alle altre righe della fattura.

> [!NOTE]  
>  È possibile che la normativa o le autorità locali impongano una modalità di arrotondamento specifica, ad esempio a un importo divisibile per 0,05.  

Per utilizzare l'arrotondamento fattura automatico, è necessario:  

* Specificare i conti di contabilità generale in cui verranno registrate le differenze di arrotondamento.  
* Impostare regole per l'arrotondamento delle fatture nella valuta locale e in una valuta estera.  
* Attivare la funzione.  

> [!NOTE]  
>  Oltre alle funzionalità di arrotondamento fattura, sono disponibili le funzionalità di arrotondamento importo unitario e arrotondamento importo per eseguire l'arrotondamento degli importi sulle fatture.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Impostare i conti contabilità generale per le differenze di arrotondamento fattura
Per utilizzare la funzione di arrotondamento fattura automatico, è necessario impostare il conto o i conti di contabilità generale in cui verranno registrate le differenze di arrotondamento. Prima di ciò è necessario impostare le categorie di registrazione articolo/servizio IVA. Per ulteriori informazioni, vedere [Impostare l'IVA](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Per impostare i conti contabilità generale per le differenze di arrotondamento fattura  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano dei conti** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Piano dei conti** impostare il conto e assegnargli il nome **Arrotondamento fattura** o simile. In [!INCLUDE[prod_short](includes/prod_short.md)] il nome del conto verrà utilizzato come testo per le fatture arrotondate.  
3. A seconda che si utilizzi l'IVA o la tassa sulla vendita, nei campi **Cat. reg. art./serv. imposta** o **Cat. reg. art./serv. IVA**, scegliere una categoria di registrazione per gli importi arrotondati. È possibile impostare un nuovo codice di gruppo da utilizzare per l'arrotondamento delle fatture.
4. Lasciare vuoti i campi **Tipo reg. gen.** e **Cat. reg. business imposta** o **Cat. reg. business IVA**. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

A questo punto è possibile assegnare il conto arrotondamento fatture alle categorie di registrazione nella pagina **Categorie registrazione fornitori**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Impostare l'arrotondamento per le valute locali ed estere
Prima di poter utilizzare la funzione di arrotondamento delle fatture, è necessario impostare le regole di arrotondamento per le valute locali ed estere.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Per impostare l'arrotondamento per le valute estere  
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Valute** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Valute** scegliere la valuta estera per aprire la **Scheda valuta**, quindi compilare i campi **Precisione arrot. importo**, **Precisione arrot. importo unit.**, **Precisione arrot. fatt.** e **Tipo arrot. fatt.**.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Per impostare l'arrotondamento per la valuta locale
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità generale** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Setup contabilità generale**, nella Scheda dettaglio **Generale**, compilare i campi **Precisione arrot. fatt.** e **Tipo arrot. fatt.**.  

## <a name="activate-the-invoice-rounding-function"></a>Attivare la funzione di arrotondamento fatture  
Per assicurarsi che le fatture di acquisto e vendita vengano arrotondate automaticamente è necessario attivare la funzione di arrotondamento fatture. È possibile attivare la funzione di arrotondamento in maniera indipendente per le fatture relative alle vendite e gli acquisti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup contabilità clienti e vendite** o **Setup contabilità fornitori e acquisti** e quindi scegliere il collegamento correlato.  
2. Nella Scheda dettaglio **Generale** selezionare la casella di controllo **Arrotondamento fattura**.  

## <a name="see-also"></a>Vedere anche  
[Fatturare le vendite](sales-how-invoice-sales.md)  
[Registrare gli acquisti](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
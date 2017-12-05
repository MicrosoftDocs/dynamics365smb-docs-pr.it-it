---
title: Scegliere il metodo di pagamento elettronico | Microsoft Docs
description: Elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: it-it
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Eseguire i pagamenti con servizio di conversione di dati bancari o bonifico SEPA
Nella finestra **Registraz. pagamenti** è possibile elaborare i pagamenti ai fornitori esportando un file con le informazioni di pagamento dalle righe registrazioni. È quindi possibile caricare il file sul sito elettronico della banca dove vengono elaborati i trasferimenti di denaro correlati. [!INCLUDE[d365fin](includes/d365fin_md.md)] supporta il formato di bonifico SEPA, ma nel proprio paese potrebbero essere disponibili anche altri formati di pagamento elettronico.   

 Per abilitare i bonifici SEPA, è necessario innanzitutto impostare un conto corrente bancario, un fornitore e il batch registrazioni COGE su cui si basano le registrazioni pagamenti. Successivamente si preparano i pagamenti dei fornitori compilando automaticamente la finestra **Registraz. pagamenti** con i pagamenti in scadenza insieme alle date di registrazione specificate.  

> [!NOTE]  
>  Una volta verificato che i pagamenti sono stati elaborati correttamente dalla banca, è possibile passare alla registrazione delle righe di registrazione pagamenti.  

 Nella tabella seguente viene descritta una sequenza di task, con collegamenti agli argomenti che li descrivono.   

|**Per**|**Vedere**|  
|------------|-------------|  
|Attivare la funzionalità In modo inverso, è possibile utilizzare la funzionalità Servizio di conversione di dati bancari per convertire tutti i file di rendiconto bancario in un formato che è possibile importare o per convertire i file di pagamento esportati nel formato richiesto dalla banca.|[Procedura: Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-statement-service.md)|  
|Impostare un conto corrente bancario, un fornitore e le registrazioni pagamenti per bonifici SEPA.|[Procedura: Impostare il bonifico SEPA](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Compilare le registrazioni di pagamento con le righe per i pagamenti dovuti ai fornitori, con l'opzione di inserire le date di registrazione in base alla data di scadenza dei reltivi documenti di acquisto.|[Gestire la contabilità fornitori](payables-manage-payables.md)|  
|Esportare le righe registrazione pagamenti in un file in formato di bonifico SEPA.|[Procedura: esportare pagamenti in un file della banca](payables-how-export-payments-bank-file.md)|  
|Analizzare quali pagamenti sono stati esportati e in quali file.|Registri di bonifici|  
|Quando il pagamento elettronico viene elaborato correttamente dalla banca, registrare i pagamenti.|[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)|  

## <a name="see-also"></a>Vedi anche  
[Procedura: Impostare il servizio di conversione di dati bancari](bank-how-setup-bank-statement-service.md)  
[Procedura: Impostare il bonifico SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Gestire la contabilità fornitori](payables-manage-payables.md)   
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Riscuotere pagamenti con addebito diretto SEPA](finance-collect-payments-with-sepa-direct-debit.md)   


---
title: Mapping dei campi per l'esportazione dei file di pagamento bancario | Microsoft Docs
description: Quando si esportano campi pagamento tramite la funzionalità servizio di conversione dati bancari, i dati esportati sono esposti al provider del servizio di conversione dati bancari.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 80112e892c72283254d3894e6ce4102cc9350e0b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "802068"
---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a>Mapping dei campi durante l'esportazione dei file di pagamento tramite il servizio di conversione dati bancari
Quando si esportano campi pagamento tramite la funzionalità servizio di conversione dati bancari, i dati esportati sono esposti al provider del servizio di conversione dati bancari. Il provider di servizi è responsabile per la privacy di questi dati. Per ulteriori informazioni sul funzionamento della funzionalità di servizio di conversione dati bancari, vedere [Informazioni sul framework di scambio dati](across-about-the-data-exchange-framework.md).  

> [!CAUTION]  
>  Quando si esportano campi pagamento tramite la funzionalità servizio di conversione dati bancari, alcuni dei dati aziendali verranno esposti al provider del servizio. Il provider di servizi, AMC Consult A/S, è responsabile per la privacy di questi dati. Per maggiori informazioni, vedere [Informativa sulla privacy di AMC](https://go.microsoft.com/fwlink/?LinkId=510158).  

La tabella seguente elenca i campi in [!INCLUDE[d365fin](includes/d365fin_md.md)] da cui è possibile esportare i dati verso il provider di servizi.  

|Campo mappato|Campo nella tabella|Tavolo|Descrizione|  
|------------------|--------------------|-----------|---------------------------------------|  
|Nr. creditore|Nr. creditore|Conto bancario|L'identificatore assegnato alla società dalla banca per riscuotere i pagamenti|  
|N. conto bancario mittente|Nr./IBAN Conto corrente|Conto bancario|Il numero del conto corrente bancario della società (IBAN o altro) specificato nella scheda conto corrente bancario|  
|Compensazione bancaria standard mittente|Compensazione bancaria standard|Conto bancario|Il registro dei nomi di banche nazionali utilizzato per il conto corrente bancario mittente|  
|Codice compensazione bancaria mittente|Codice compensazione bancaria|Conto bancario|L'identificatore della banca del mittente in relazione al registro dei nomi di banca utilizzato|  
|Codice SWIFT banca ordinante|Codice SWIFT|Conto bancario|Identificatore SWIFT del conto bancario mittente|  
|Valuta conto bancario mittente|Codice valuta|Conto bancario|Il codice valuta del conto corrente mittente|  
|Nr. documento|Nr. documento|Riga registrazioni COGE|Il numero del documento della riga di pagamento.|  
|Collega-a nr. doc. est.|Collega-a nr. doc. est.|Riga registrazioni COGE|Il numero del documento esterno della fattura o della nota di credito a cui è collegata la riga di pagamento.|  
|ID destinatario|Nr. conto|Riga registrazioni COGE|Il numero del cliente o del fornitore specificato nella riga del pagamento|  
|Tipo pagamento|Tipo pagam. conversione dati banca|Metodo di pagamento|Il tipo di bonifico bancario, ad esempio nazionale o internazionale|  
|Riferimento pagamento|Riferimento pagamento|Riga registrazioni COGE|Il riferimento pagamento della riga di pagamento.|  
|Indirizzo destinatario|Indirizzo|Clienti/Fornitori|L'indirizzo del destinatario specificato nella scheda cliente o fornitore|  
|Città destinatario|Città|Clienti/Fornitori|La città del destinatario specificata nella scheda cliente o fornitore|  
|Nome destinatario|Nome|Clienti/Fornitori|Il nome del destinatario specificata nella scheda cliente o fornitore|  
|Codice paese destinatario|Cod. paese|Clienti/Fornitori|Il paese del destinatario specificato nella scheda cliente o fornitore|  
|CAP destinatario|CAP|Clienti/Fornitori|Il codice postale del destinatario specificato nella scheda cliente o fornitore|  
|N. conto bancario destinatario|Nr./IBAN Conto corrente|Conto corrente clienti/Conto corrente fornitori|Il numero (IBAN o altro) del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|  
|Codice compensazione bancaria destinatario|Compensazione bancaria standard|Conto corrente clienti/Conto corrente fornitori|Il registro dei nomi di banche nazionali utilizzato per il conto corrente bancario destinatario|  
|Compensazione bancaria standard destinatario|Codice compensazione bancaria|Conto corrente clienti/Conto corrente fornitori|L'identificatore del conto corrente bancario destinatario in relazione al registro dei nomi di banca utilizzato|  
|Indirizzo e-mail destinatario|E-Mail|Clienti/Fornitori|Indirizzo di posta elettronica del destinatario|  
|Messaggio al destinatario 1|Messaggio al destinatario|Riga registrazioni COGE|Il messaggio al destinatario specificato nella riga di pagamento|  
|Importo|Importo|Riga registrazioni COGE|Importo nella riga del pagamento|  
|Codice valuta|Codice valuta|Riga registrazioni COGE|Codice valuta nella riga di pagamento.|  
|Data bonifico|Data di registrazione:|Riga registrazioni COGE|Data di registrazione della riga di pagamento|  
|Importo fattura|Importo originario|Dettagli movimenti contabili clienti/fornitori|L'importo nel movimento a cui è collegato il pagamento|  
|Data fattura|Data documento|Dettagli movimenti contabili clienti/fornitori|La data della fattura nel movimento a cui è collegato il pagamento|  
|Indirizzo banca destinatario|Indirizzo|Conto corrente clienti/Conto corrente fornitori|L'indirizzo del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|  
|L'indirizzo del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|Città|Conto corrente clienti/Conto corrente fornitori|La città del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|  
|Nome banca destinatario|Nome|Conto corrente clienti/Conto corrente fornitori|Il nome del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|  
|Paese banca destinatario|Cod. paese|Conto corrente clienti/Conto corrente fornitori|Il paese del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|  
|CAP banca destinatario|CAP|Conto corrente clienti/Conto corrente fornitori|Il codice postale del conto corrente bancario destinatario specificato nella scheda conto corrente bancario del cliente o del fornitore|  
|Indirizzo banca mittente|Indirizzo|Conto bancario|L'indirizzo del conto corrente bancario del mittente specificato nella scheda conto corrente bancario|  
|Città banca mittente|Città|Conto bancario|La città del conto corrente bancario del mittente specificato nella scheda conto corrente bancario|  
|Nome banca mittente|Nome|Conto bancario|Il nome del conto corrente bancario del mittente specificato nella scheda conto corrente bancario|  
|Paese conto bancario mittente|Cod. paese|Conto bancario|Il paese del conto corrente bancario del mittente specificato nella scheda conto corrente bancario|  
|CAP banca mittente|CAP|Conto bancario|Il codice postale del conto corrente bancario del mittente specificato nella scheda conto corrente bancario|  
|Definizione registrazioni COGE|Nome def. registrazioni|Riga registrazioni COGE|Il template delle registrazioni COGE utilizzato per la riga di pagamento|  
|Nome batch registrazioni COGE|Nome batch contabile|Riga registrazioni COGE|Il nome del batch registrazioni COGE utilizzato per la riga di pagamento|  
|Nome banca mittente- Conv. dati|Nome banca – Conversione dati|Conto bancario|Il nome del conto corrente bancario del mittente che viene richiesto dal servizio di conversione dati bancari e viene specificato nella scheda conto corrente bancario|  

## <a name="see-also"></a>Vedi anche  
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)
[Impostare il Servizio di conversione dati bancari](bank-how-setup-bank-data-conversion-service.md)   
[Eseguire i pagamenti con servizio di conversione di dati bancari o bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   

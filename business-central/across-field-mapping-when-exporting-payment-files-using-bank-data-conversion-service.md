---
title: Mapping dei campi per l'esportazione dei file di pagamento bancario | Microsoft Docs
description: 'Quando si esportano file di pagamento utilizzando l''estensione AMC Banking 365 Fundamentals, i dati esportati sono esposti al provider di servizi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Mappatura dei campi quando si esportano file di pagamento utilizzando l'estensione AMC Banking 365 Fundamentals
Quando si esportano file di pagamento utilizzando l'estensione AMC Banking 365 Fundamentals, i dati esportati sono esposti al provider di servizi. Il provider di servizi è responsabile per la privacy di questi dati. Per ulteriori informazioni sull'estensione AMC Banking 365 Fundamentals, vedere [Utilizzare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Quando si esportano file di pagamento tramite l'estensione AMC Banking 365 Fundamentals, alcuni dei dati aziendali verranno esposti al provider del servizio. Il provider di servizi, AMC Consult A/S, è responsabile per la privacy di questi dati. Per maggiori informazioni, vedere [Informativa sulla privacy di AMC](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> Nella versione generica di [!INCLUDE[prod_short](includes/prod_short.md)], viene installato e connesso un provider di servizi globale per convertire i dati bancari in qualsiasi formato di file richiesto dalla banca. Nelle versioni per il Nord America, lo stesso servizio può essere utilizzato per inviare file di pagamento come trasferimento elettronico di fondi (EFT), ad esempio la rete ACH (Automated Clearing House) comunemente utilizzata, tuttavia con un processo leggermente diverso.

La tabella seguente elenca i campi in [!INCLUDE[prod_short](includes/prod_short.md)] da cui è possibile esportare dati.  

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
|Nome banca mittente- Conv. dati|Nome banca – Conversione dati|Conto bancario|Il nome del conto corrente bancario del mittente che viene richiesto dall'estensione AMC Banking 365 Fundamentals e che viene specificato nella scheda conto corrente bancario|  

## Vedere anche  
[Impostazione dello scambio di dati](across-set-up-data-exchange.md)  
[Scambio di dati in modalità elettronica](across-data-exchange.md)
[Utilizzare l'estensione AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)   
[Effettuare pagamenti con l'estensione AMC Banking 365 Fundamentals o il bonifico SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
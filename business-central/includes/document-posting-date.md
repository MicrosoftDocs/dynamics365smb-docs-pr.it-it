---
author: brentholtorf
ms.topic: include
ms.date: 11/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

I campi **Data documento** e **Data di registrazione**  nei documenti di vendita e di acquisto possono aiutarti a rispettare gli standard contabili e a garantire calcoli finanziari accurati. I campi hanno scopi diversi:

- Per [!INCLUDE [prod_short](prod_short.md)] per calcolare correttamente gli addebiti di interessi e l'importo dovuto sulle fatture di vendita, la **Data documento** deve coincidere con una delle seguenti date:

   - La data sulla fattura di vendita inviata al cliente. 
   - La data sulla fattura di acquisto ricevuta dal fornitore.
- La **Data pubblicazione** mostra quando è stato registrato un documento in [!INCLUDE [prod_short](prod_short.md)]. Molti standard e regole contabili richiedono alle aziende di registrare e segnalare le transazioni finanziarie in base alla data in cui si sono verificate.

A seconda dei processi aziendali, queste date potrebbero essere o meno le stesse. Se sono le stesse, puoi configurare [!INCLUDE [prod_short](prod_short.md)] per aggiornare la data sui documenti di vendita e di acquisto con la data in cui li hai registrati.  
  
Per impostare automaticamente le date dei documenti sulle date di registrazione, nelle pagine **Setup contabilità clienti e vendite** e **Setup contabilità fornitori e acquisti**, attivare l'interruttore **Collega la data del documento alla data di registrazione**.

> [!NOTE]
> L'impostazione non influisce sulle registrazioni di vendite o acquisti.
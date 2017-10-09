---
title: "Registrare le entrate o le spese direttamente nella contabilità generale| Documenti Microsoft"
description: "Per le attività aziendali che non vengono rappresentate da un documento, ad esempio le spese più piccole o le ricevute di pagamento, è possibile creare le transazioni correlate registrando le righe nella finestra Registrazioni COGE."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 43065620f34a7ef02e5247e78acf306500f82d90
ms.contentlocale: it-it
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Procedura: Registrare le transazioni direttamente nella contabilità generale
La maggior parte delle transazioni finanziarie vengono registrate nella contabilità generale attraverso i documenti aziendali dedicati quali fatture di acquisto e ordini di vendita. Per le attività aziendali che non vengono rappresentate da un documento in [!INCLUDE[d365fin](includes/d365fin_md.md)], ad esempio le spese più piccole o le ricevute di pagamento, è possibile creare le transazioni correlate registrando le righe nella finestra **Registrazioni COGE**.

Un tipico utilizzo delle registrazioni COGE consiste nel registrare le spese dei dipendenti effettuate con denaro personale durante le attività lavorative, al fine di provvedere successivamente al rimborso. Per altre informazioni, vedere [Procedura: Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md).

Le registrazioni COGE includono le transazioni finanziarie direttamente nei conti di contabilità generale e in altri conti, ad esempio i conti correnti bancari, i conti clienti e i conti fornitori. La contabilizzazione mediante una registrazione generale crea sempre movimenti nei conti di contabilità generale. Ciò è vero anche quando, ad esempio, viene contabilizzata una riga di registrazione in un conto cliente, in quanto tramite una categoria di registrazione viene registrata una riga in un conto crediti nella contabilità generale. È possibile personalizzare la versione delle registrazioni generali impostando un batch o una definizione di registrazioni. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).

Diversamente dai movimenti che vengono registrati con i documenti che richiedono un processo di nota di credito, è possibile stornare correttamente i movimenti che vengono registrati con le registrazioni COGE. Per ulteriori informazioni, vedere [Procedura: Stornare le registrazioni](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Per registrare una transazione direttamente in un conto di contabilità generale
1. Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Registrazioni COGE**, quindi scegliere il collegamento correlato.
2. Aprire il batch registrazioni COGE appropriato. Per ulteriori informazioni, vedere [Utilizzo delle registrazioni COGE](ui-work-general-journals.md).
3. In una nuova riga di registrazione, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Ripetere il passaggio 3 tutte le transazioni separate da registrare.

    > [!TIP]  
    > Se si immettono più righe di transazione sopra a una riga di contropartita, ad esempio, per un conto corrente bancario, seleziona la casella di controllo **Suggerisci importo contropartita** nella riga per il batch nella finestra **Batch registrazioni COGE**. Il campo **Importo** nella riga di contropartita viene precompilato automaticamente con il valore necessario per pareggiare le transazioni.
5. Scegliere l'azione **Registra** per registrare le transazioni nei conti C/G specificati.

## <a name="see-also"></a>Vedi anche
[Utilizzo delle registrazioni COGE](ui-work-general-journals.md)  
[Procedura: Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md)  
[Procedura: Stornare le registrazioni](finance-how-reverse-journal-posting.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


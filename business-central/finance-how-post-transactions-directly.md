---
title: Registrare le entrate o le spese direttamente nella contabilità generale
description: È possibile creare transazioni nella pagina Registrazioni COGE per attività commerciali che non coinvolgono un documento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Registrare le transazioni direttamente nella contabilità generale

Le registrazioni generali vengono utilizzate per la contabilizzazione diretta nei conti C/G e in altri conti delle transazioni finanziarie, ad esempio i conti correnti bancari, i conti clienti, fornitori e dipendenti.  

Un tipico utilizzo delle registrazioni COGE consiste nel registrare le spese dei dipendenti durante le attività lavorative per i rimborsi. Per altre informazioni, vedere [Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md).

Le registrazioni COGE includono le transazioni finanziarie direttamente nei conti di contabilità generale e in altri conti, ad esempio i conti correnti bancari, i conti clienti e i conti fornitori. La contabilizzazione mediante una registrazione COGE crea movimenti nei conti CoGe. I movimenti vengono creati anche quando, ad esempio, viene contabilizzata una riga di registrazione in un conto cliente, in quanto tramite una categoria di registrazione viene registrato un movimento in un conto crediti C/G. È possibile personalizzare la versione delle registrazioni generali impostando un batch o una definizione di registrazioni. Per ulteriori informazioni, vedere [Utilizzare le registrazioni COGE](ui-work-general-journals.md).

I movimenti registrati con documenti richiedono un processo di nota di credito. Tuttavia, è possibile stornare i movimenti registrati nella registrazione COGE. Per ulteriori informazioni, vedere [Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md).

## Per registrare una transazione direttamente in un conto di contabilità generale

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni COGE**, quindi scegli il collegamento correlato.
2. Aprire il batch registrazioni generale. Per ulteriori informazioni, vedere [Utilizzare le registrazioni COGE](ui-work-general-journals.md).
3. In una nuova riga di registrazione, compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Ripetere il passaggio 3 per tutte le transazioni da registrare.

    > [!TIP]  
    > Se si immettono più righe di transazione sopra una riga di contropartita, ad esempio, per un conto corrente bancario, seleziona la casella di controllo **Suggerisci importo contropartita** nella riga per il batch nella pagina **Batch registrazioni COGE**. Il campo **Importo** nella riga di contropartita viene precompilato automaticamente con il valore necessario per pareggiare le transazioni.
5. Scegliere l'azione **Registra** per registrare le transazioni nei conti C/G specificati.

## Vedere anche

[Usare le registrazioni COGE](ui-work-general-journals.md)  
[Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md)  
[Stornare le registrazioni e annullare carichi/spedizioni errati](finance-how-reverse-journal-posting.md)  
[Finanze](finance.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Gestione degli approvvigionamenti per un progetto
description: Descrive i diversi modi per gestire gli approvvigionamenti e gli acquisti di materiale e servizi per i progetti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-project-supplies"></a>Gestione degli approvvigionamenti per un progetto

Devi gestire gli approvvigionamenti di progetto di articoli, servizi e spese come un aspetto integrale e critico dell'esecuzione di tutti i progetti. È possibile utilizzare le giacenze o effettuare acquisti specifici per dei progetti mediante gli ordini di acquisto e/o le fatture di acquisto. Ad esempio, per completare un progetto relativa a un intervento di assistenza su un computer è richiesto un nuovo disco. Si crea quindi una fattura di acquisto per acquistare il nuovo disco e si registra il progetto che la utilizza.

Se il processo di acquisto non richiede la registrazione separata della transazione fisica, è possibile elaborare un acquisto nella pagina **Registrazione progetti in C/G**. Per ulteriori informazioni, vedere [Per registrare un spesa correlata a un progetto](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## <a name="to-purchase-items-or-services-for-a-project"></a>Per acquistare articoli o servizi per un progetto

Nella procedura riportata di seguito viene illustrato come utilizzare una fattura di acquisto per acquistare i prodotti per un progetto. La stessa procedura vale anche quando si utilizza un ordine di acquisto.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari. Per ulteriori informazioni, vedi [Registrare gli acquisti](purchasing-how-record-purchases.md).
3. Nel campo **Nr. progetto** e **Nr. attività di progetto** selezionare le informazioni del progetto per la quale si desidera acquistare articoli o servizi. Utilizzare gli strumenti di personalizzazione se un campo non è visibile. Per ulteriori informazioni, vedi [Personalizzare l'area di lavoro](ui-personalization-user.md).

    Il valore che si seleziona nel campo **Tipo di riga progetto** definisce se viene creata una riga di pianificazione quando si registra l'utilizzo dell'articolo. Se il campo contiene **Fatturabile**, vengono create righe di pianificazione progetto che sono pronte per la fatturazione al cliente. Per ulteriori informazioni, vedere [Fatturare progetti](projects-how-invoice-jobs.md).
4. Scegli l'azione **Registra**.

## <a name="to-view-the-value-of-purchases-for-a-project"></a>Per visualizzare il valore degli acquisti per un progetto

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Progetti**, quindi scegli il collegamento correlato.
2. Apri una scheda progetto pertinente.

    Nella Scheda dettaglio **Attività**, il campo **Ordini inevasi** mostra l'importo inevaso totale, in valuta locale, degli articoli a magazzino e dei servizi sui documenti di acquisto per la riga di attività di progetto.  

    Il campo **Importo carichi non fatt.** mostra il valore di articoli spediti su documenti di acquisto, ma non ancora fatturati.  
3. Scegliere uno dei campi per aprire la pagina **Righe acquisto** dove è possibile esaminare le informazioni sulle righe del documento di vendita correlate, inclusi gli articoli o i servizi che vengono ricevuti.

## <a name="to-post-a-project-related-expense"></a>Per registrare una spesa correlata a un progetto

Se si incorre in spese di progetto straordinarie o eccezionali, è possibile utilizzare la pagina **Registrazione progetti in C/G** per registrarle direttamente nel conto progetto correlato.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni progetti in C/G**, quindi scegli il collegamento correlato.  
2. Creare una nuova riga e immettere le informazioni sulla spesa, incluse le informazioni nei campi **Nr. progetto** e **Nr. attività di progetto**.  
3. Una volta completate le registrazioni, scegliere l'azione **Registra**.

## <a name="see-also"></a>Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

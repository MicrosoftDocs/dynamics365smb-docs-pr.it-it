---
title: Processo batch di suggerimento di pagamenti ai fornitori
description: È possibile specificare le impostazioni di pagamento del fornitore per ottenere suggerimenti per i pagamenti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 09/07/2023
ms.custom: bap-template
---
# Sugg. pagamenti fornitore

Nella pagina **Registraz. pagamenti** è possibile utilizzare il processo batch **Sugg. pagamenti fornitore** per suggerire le righe di pagamento. In base alle tue impostazioni, [!INCLUDE [prod_short](includes/prod_short.md)] suggerisce le righe per i pagamenti:

* Pagamenti prossimi alla scadenza
* Pagamenti per cui è disponibile uno sconto sul pagamento

Per trarre completamente vantaggio dai pagamenti suggeriti, è prima necessario assegnare una priorità ai fornitori. Per saperne di più sulla definizione delle priorità dei fornitori, vai a [Attribuire un ordine di priorità ai fornitori](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Il processo batch esclude i movimenti contabili fornitori che lo sono **In attesa** o che sono già applicati e hanno un valore nel campo **Collega a ID**.  

> [!IMPORTANT]  
> Per trarre vantaggio dagli sconti sui pagamenti, se si è immesso un importo disponibile, l'importo verrà utilizzato per:  
>
> * Movimenti fornitori scaduti con priorità innanzitutto in ordine di priorità.
> * Movimenti fornitori scaduti senza priorità.  
> * Movimenti fornitori che vengono qualificati per gli sconti sui pagamenti. Le voci sono organizzate per numero del fornitore.  

## Per utilizzare la funzione di suggerimento pagamenti fornitori

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.  
2. Aprire le registrazioni e scegliere l'azione **Sugg. pagamenti fornitore**.  
3. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Scegliere il pulsante **OK**.  

## Per inserire la data di scadenza come data di registrazione nelle righe di registrazione pagamenti

Quando si esegue il processo batch **Sugg. pagamenti fornitore** per creare righe di pagamento per i fornitori, è possibile compilare due campi speciali per assicurarsi che le righe generate utilizzino la data di scadenza per calcolare la data di registrazione. Questi campi sono **Calcola data di registrazione da Collega a - Scadenza doc.** e **Offset Collega a - Scadenza doc.**  

> [!IMPORTANT]  
> Non è possibile utilizzare il campo **Calcola data di registrazione da Collega a - Scadenza doc** insieme al campo **Trova sconti pagamenti** o al campo **Raggruppa per fornitore**. Se la data di registrazione è basata sulla data di scadenza, gli sconti sui pagamenti potrebbero non essere calcolati correttamente, in quanto la data di registrazione potrebbe essere successiva alla data dello sconto sul pagamento.  

Inoltre, se la data di registrazione calcolata è già trascorsa, la data di registrazione viene spostata alla data di lavoro e viene visualizzato un avviso.  

È possibile inoltre creare manualmente le righe di pagamento utilizzando la data di scadenza per calcolare la data di registrazione. Dopo che si collegano movimenti contabili fornitori, è possibile utilizzare l'azione **Calcola data registrazione** per aggiornare la data di registrazione nella riga di registrazione con la data di scadenza della fattura relativa di acquisto. Per ulteriori informazioni su questo processo manuale, andare ad [Collegare manualmente le transazioni di acquisto](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Se la fattura di acquisto è scaduta, la data di registrazione viene impostata sulla data di lavoro e il carattere nella riga diventa di colore rosso.  

## Vedere anche

[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Effettuare i pagamenti](payables-make-payments.md)  
[Usare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

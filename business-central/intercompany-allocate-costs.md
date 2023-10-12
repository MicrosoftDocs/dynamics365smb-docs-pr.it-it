---
title: Allocare costi a partner IC | Microsoft Docs
description: Scopri come le impostazioni IVA per clienti e fornitori determinano se e come viene calcolata l'IVA.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners"></a>Allocare costi a partner IC
Quando si utilizzano registrazioni intercompany per trasferire documenti tra società partner, le impostazioni relative all'IVA (principalmente la categoria registrazione business IVA) assegnate ai conti cliente o fornitore (associati al partner IC) determinano se e come l'IVA viene calcolata e registrata. È inoltre possibile eseguire distribuzioni dei costi direttamente da un ordine acquisto alle società partner. Ad esempio, se si registra una fattura acquisto di un fornitore esterno e si desidera distribuire alcuni o tutti i costi a uno o più partner IC.

È possibile allocare i costi a uno o più partner IC utilizzando quanto segue:

* **Registrazione COGE intercompany** - Queste registrazioni sono utili quando si acquista un servizio. Ad esempio, quando una società madre acquista un servizio per configurare sistemi informatici in due filiali. La fattura viene inviata alla società madre, ma i costi vengono allocati ai partner IC. Per ulteriori informazioni, vedere [Utilizzo di documenti e registrazioni intercompany](intercompany-how-work-documents-journals.md).
* Ordini e fatture acquisto: l'utilizzo di documenti acquisto è utile quando le funzioni di acquisto, ad esempio delle spese operative, sono centralizzate in una società e quindi allocate ai partner IC.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Allocare i costi utilizzando registrazioni COGE intercompany
Per immettere una riga in registrazioni COGE intercompany, attenersi alla seguente procedura. 

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazione COGE intercompany**, quindi scegli il collegamento correlato.
2. Se necessario, nel campo **Nr. documento esterno**, immettere il numero documento sulla fattura del fornitore.
3. Nel campo **Tipo di documento**, scegliere **Fattura**.
4. Nel campo **Tipo conto** scegliere **Fornitore**.
5. Nel campo **Nr. conto** scegliere il fornitore.
6. Nel campo **Quantità** immettere un importo negativo pari all'importo nella fattura.
7. Nel campo **Tipo contropartita** scegliere **Conto C/G**.
8. Nel campo **Contropartita** scegliere la contropartita da utilizzare.
9. Per allocare i costi a partner IC, attenersi alla seguente procedura:
   1. Creare una nuova riga.
   2. Scegliere l'opzione che lascia il campo **Tipo di documento** vuoto.
   3. Nel campo **N. documento** immettere un numero diverso dal numero nel campo **Nr. documento esterno**. L'allocazione dei costi è considerata una transazione diversa.
   4. Nel campo **Tipo conto** scegliere **Partner IC**.
   5. Nel campo **Nr. conto** selezionare il partner IC a cui allocare il costo.
   6. Nel campo **Tipo contropartita** scegliere **Conto C/G**.
   7. Nel campo **Nr. contropartita** scegliere il conto C/G in cui registrare l'importo ricevuto dal partner IC.
   1. Nel campo **Importo**, immettere l'importo della fattura da allocare al partner IC.
   1. Nel campo **Nr. conto C/G partner IC** scegliere il conto C/G in cui registrare l'importo per il partner IC. 
   1. Compilare i rimanenti campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Ripetere questi passaggi per ogni partner IC che deve condividere il costo.
1. Per registrare il documento e allocare i costi, scegliere **Registra**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a>Allocare i costi utilizzando un documento acquisto
La procedura seguente descrive come allocare i costi utilizzando una fattura acquisto. I passaggi sono simili a quelli per un ordine acquisto.

> [!NOTE]
> Per completare questi passaggi è necessario personalizzare la pagina **Fattura acquisto**aggiungendo i campi **Codice partner IC**, **Tipo rif. partner IC** e **Partner IC**. Per ulteriori informazioni, vedere [Per avviare la personalizzazione di una pagina tramite il banner Personalizzazione](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fattura di acquisto**, quindi scegli il collegamento correlato.
2. Nel campo **Tipo** scegliere **Conto C/G**.
   
   Conto C/G è l'unica opzione che puoi utilizzare per allocare i costi.  
1. Nel campo **Nr.** scegliere il conto C/G in cui registrare.
1. Nel campo **Codice partner IC** selezionare il partner IC a cui allocare il costo.
1. Nel campo **Tipo rif. partner IC** scegli il conto C/G da utilizzare per l'allocazione. Questo conto mapperà la spesa a un conto nel piano dei conti del partner IC.
1. Nel campo **Quantità**, specificare il numero di unità da addebitare al partner IC.
1. Nel campo **Costo unitario diretto IVA escl. (o IVA inclusa)** immettere il costo per articolo da addebitare al partner IC.
1. Compilare i rimanenti campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Per registrare l'ordine acquisto, scegliere **Registra**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a>Inviare i costi allocati a partner IC
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Casella trans. in uscita IC**, quindi scegli il collegamento correlato.
2. Scegliere le righe da inviare, quindi scegliere l'azione **Invia a partner IC**. 
3. Per allocare i costi, scegliere l'azione **Completa azioni riga**.

## <a name="calculating-vat-for-cost-distributions"></a>Calcolo dell'IVA per le distribuzioni dei costi
Quando si utilizza un documento per distribuire i costi a partner IC, è necessario tenere presenti due impostazioni IVA: 
* Le impostazioni nel conto C/G per le spese:
   * Se le categorie registrazione business generali o IVA sono impostate nel conto C/G, il calcolo dipende dalle categorie e dalle categorie di prodotti della riga di documento.
   * Se le categorie registrazione business generale o IVA non sono specificate nel conto C/G, il calcolo dipende da quanto segue:
* Le impostazioni della categoria di registrazione nel partner IC
   * Indica se il partner IC è assegnato a un numero di cliente che non include categorie registrazione business generale o IVA specificate.
   * Non esiste alcun numero di cliente associato al partner IC. Quindi le categorie registrazione business generale o IVA sono vuote e viene utilizzata la riga nel setup registrazione IVA, che di solito è un gruppo in cui è specificata l'IVA allo 0%.

> [!NOTE]
> È importante convalidare sia il setup partner IC sia il setup conto C/G (per il conto spesa utilizzato per la distribuzione dei costi) prima di allocare i costi ai partner IC.

## <a name="see-also"></a>Vedere anche
[Impostare la contabilità interaziendale](intercompany-how-setup.md)  
[Gestione delle transazioni Intercompany](intercompany-manage.md)  
[Finanze](finance.md)  
[Impostazione di dati finanziari](finance-setup-finance.md)  
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

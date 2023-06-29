---
title: Uso dell'IVA non detraibile
description: Questo articolo spiega come usare e riportare l'IVA non detraibile.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="use-non-deductible-vat"></a><a name="use-non-deductible-vat"></a>Uso dell'IVA non detraibile

Questo articolo spiega come usare e riportare l'IVA non detraibile.

## <a name="create-a-purchase-invoice-with-non-deductible-vat"></a><a name="create-a-purchase-invoice-with-non-deductible-vat"></a>Creare una fattura di acquisto con IVA non detraibile

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture di acquisto**, quindi seleziona il collegamento correlato.
2. Seleziona **Nuovo** per creare una fattura di acquisto e inserire le informazioni appropriate nell'intestazione della fattura.
3. Nella sezione **Righe**, crea una nuova riga di qualsiasi tipo, in base al gruppo di registrazione dell'attività IVA e al gruppo di registrazione del prodotto IVA in cui si configura l'IVA non detraibile.
4. Nei campi **Quantità** e **Costo unitario diretto**, immetti i valori appropriati.

    Se hai selezionato la casella di controllo **Mostra IVA non detraibile nelle righe** nella pagina **Setup IVA**, gli importi nei campi **Imponibile IVA non detraibile** e **Importo IVA non detraibile** sono calcolati in base al campo **% IVA non detraibile** nella pagina **Setup registrazioni IVA**.

5. Contabilizzare la fattura.

## <a name="create-a-purchase-order-with-non-deductible-vat"></a><a name="create-a-purchase-order-with-non-deductible-vat"></a>Creare un ordine di acquisto con IVA non detraibile

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini acquisto**, quindi scegli il collegamento correlato.
2. Seleziona **Nuovo** per creare un ordine di acquisto e inserire le informazioni appropriate nell'intestazione del documento.
3. Nella sezione **Righe**, crea una nuova riga di qualsiasi tipo, in base al gruppo di registrazione dell'attività IVA e al gruppo di registrazione del prodotto IVA in cui si configura l'IVA non detraibile.
4. Nei campi **Quantità** e **Costo unitario diretto**, immetti i valori appropriati.

    Se hai selezionato la casella di controllo **Mostra IVA non detraibile nelle righe** nella pagina **Setup IVA**, gli importi nei campi **Imponibile IVA non detraibile** e **Importo IVA non detraibile** sono calcolati in base al campo **% IVA non detraibile** nella pagina **Setup registrazioni IVA**.

5. Registrare l'ordine di acquisto.

## <a name="adjust-rounded-vat-amounts-before-document-posting"></a><a name="adjust-rounded-vat-amounts-before-document-posting"></a>Adeguare gli importi IVA arrotondati prima della registrazione del documento

Se gli importi IVA non vengono arrotondati allo stesso modo nel proprio ambiente e nel sistema contabile esterno (il documento fattura originale), è possibile rettificare l'importo IVA prima di registrare il documento. Per apportare questa rettifica, attenersi alla seguente procedura prima di registrare il documento.

1. Nel riquadro Azioni, seleziona **Statistiche**.
2. Se utilizzi una fattura di acquisto, procedi nel seguente modo:

    1. Nella scheda dettaglio **Righe** seleziona l'importo dell'IVA o l'importo dell'IVA non detraibile.
    2. Imposta i valori necessari dal documento originale, quindi chiudi la pagina **Statistiche fatture acquisto**.

3.  Se utilizzi l'ordine di acquisto, procedi nel seguente modo:

    1. Nella Scheda dettaglio **Fatturazione**, seleziona **Nr. righe di imposta** per aprire la pagina **Righe Importi IVA**.
    2. Seleziona l'importo dell'IVA o l'importo dell'IVA non detraibile che si desidera correggere.
    3. Inserisci i valori necessari dal documento originale, chiudi la pagina **Righe importo IVA**, quindi chiudi la pagina **Statistiche ordini d'acquisto**.

Per utilizzare le rettifiche degli importi IVA, è necessario abilitare le rettifiche. Nella pagina **Impostazione della contabilità generale**, nel campo **Max. differenza IVA permessa**, inserisci l'importo massimo dell'IVA consentito per la correzione. Quindi, nella pagina **Setup contabilità fornitori**, seleziona **Permetti differenze IVA**.

È possibile modificare i valori dei campi **Importo IVA** e **Importo IVA non detraibile**. Il valore del campo **Importo IVA detraibile** è il risultato di questi due valori. L'importo inserito nel campo **Importo IVA non detraibile** non può essere superiore all'importo inserito nel campo **Importo IVA**. Il campo **Max. differenza IVA permessa** nella pagina **Impostazione della contabilità generale** funziona in modo indipendente per gli importi IVA detraibili e non detraibili nelle pagine delle statistiche quando si desidera rettificare l'IVA importi.

> [!IMPORTANT]
> Non è possibile utilizzare l'IVA non detraibili sulle fatture di pagamento anticipato.

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Gestione contabile](finance.md)  
[Setup dei calcoli e registrazione dei metodi per l'IVA](finance-setup-vat.md)  
[Impostare l'IVA non detraibile](finance-setup-nondeductible-vat.md)  
[Dichiarare l'IVA all'autorità fiscale](finance-how-report-vat.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

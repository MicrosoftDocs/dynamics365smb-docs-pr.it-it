---
title: Impostare la ritenuta d'acconto (IT)
description: 'Nella versione italiana, le società devono versare la ritenuta allo Stato per i servizi di terzi e gli acquisti dai fornitori. Scopri come si fa.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: null
ms.date: 10/29/2021
ms.author: edupont
---
# <a name="set-up-withholding-tax-in-the-italian-version"></a><a name="set-up-withholding-tax-in-the-italian-version"></a>Impostare la ritenuta d'acconto nella versione italiana

Le società devono versare la ritenuta allo Stato per i servizi di terzi e gli acquisti dai fornitori. La ritenuta viene calcolata al momento del pagamento della fattura anziché durante la registrazione della fattura.

## <a name="to-set-up-withholding-tax-codes"></a><a name="to-set-up-withholding-tax-codes"></a>Per impostare i codici ritenuta

1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ritenuta**, quindi scegli il collegamento per la pagina **Codice**.  

2. Nella pagina **Codice** per aggiungere un nuovo codice di ritenuta, scegli l'azione **Nuovo** quindi immetti le informazioni nei campi pertinenti. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

3. Per aggiungere righe al codice di ritenuta d'acconto, scegli l'azione **Righe codice ritenuta**.

4. Immettere informazioni nei campi rilevanti. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

5. Ripeti questi passaggi per ulteriori codici.  

## <a name="to-set-up-withholding-tax-for-vendors"></a><a name="to-set-up-withholding-tax-for-vendors"></a>Per impostare la ritenuta per i fornitori

1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Fornitori**, quindi scegli il collegamento correlato.

2. Apri la scheda fornitore pertinente.

3. Compilare i relativi campi. In particolare ai fini della ritenuta d'acconto, è necessario aggiungere le seguenti informazioni:

    * Dati personali del fornitore.
    * Dettagli di contatto per il fornitore.
    * Dettagli di fatturazione per il fornitore.
    * Informazioni di pagamento per il fornitore.
    * Informazioni di conto lavoro per il fornitore.
    * Informazioni di commercio estero per il fornitore.
    * I campi pertinenti sulla scheda dettaglio **Ritenute e Contributi**, come il campo **Cod. ritenuta**.

## <a name="to-calculate-withholding-tax-for-purchase-invoices"></a><a name="to-calculate-withholding-tax-for-purchase-invoices"></a>Per calcolare la ritenuta per le fatture di acquisto

1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture di acquisto**, quindi scegli il collegamento correlato.

2. Apri la fattura di acquisto rilevante.

3. Scegli l'azione **Ritenute - INPS**.

4. Nella pagina **Scheda ritenute e contributi**, rivedi le informazioni nei vari campi e assicurati che il campo **Cod. ritenuta** specifica il codice corretto per il fornitore.

5. Per calcolare l'importo della ritenuta prima della registrazione, scegli l'azione **Calcola**.  

## <a name="to-make-a-vendor-payment"></a><a name="to-make-a-vendor-payment"></a>Per effettuare un pagamento fornitore

1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Registrazioni pagamenti**, quindi scegli il collegamento correlato.

2. Per creare una nuova riga di registrazione pagamenti, immetti le informazioni rilevanti nei campi.

3. Per effettuare un pagamento fornitore scegli l'azione **Registra**.  

    > [!NOTE]
    > L'importo nella nuova riga nella pagina **Registrazioni pagamenti** corrisponde all'importo di pagamento della ritenuta.

## <a name="see-also"></a><a name="see-also"></a>Vedere anche

[Stampa di report delle ritenute](how-to-print-withholding-tax-reports.md)  
[Impostare l'IVA](../../finance-setup-vat.md)  
[VAT record](../../finance-how-report-vat.md)  
[Funzionalità locale per l'Italia](italy-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Selezione report in Business Central
description: Informazioni su come impostare i report utilizzati per stampare vari tipi di documenti in Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/09/2022
ms.author: bholtorf
---
# <a name="report-selection-for-documents-in-business-central"></a><a name="report-selection-for-documents-in-business-central"></a><a name="report-selection-for-documents-in-business-central"></a>Selezione dei report per i documenti in Business Central

Puoi impostare report predefiniti da utilizzare per stampare documenti relativi alle vendite, agli acquisti e all'assistenza, come ordini, offerte e fatture. Ad esempio, se si dispone di un layout specifico per le fatture vendita, è possibile specificare tale report nella pagina **Selezioni report - Vendite** di modo che venga utilizzato per inviare o stampare fatture vendita.  

## <a name="available-report-selections"></a><a name="available-report-selections"></a><a name="available-report-selections"></a>Selezioni report disponibili

Le pagine **Selezioni report** specificano quale report verrà stampato nelle diverse situazioni. [!INCLUDE [prod_short](includes/prod_short.md)] fornisce le configurazioni predefinite, ma è possibile modificarle se necessario. È inoltre possibile aggiungere report alle pagine **Selezione report**, ad esempio per stampare più di un report per tipo di documento. 

La tabella seguente descrive dove è possibile trovare informazioni sulle diverse pagine.  

|Area o attività  |Ulteriori informazioni|
|--------------|----------|
|Esempio di funzionamento della selezione report (vendite)|[Selezione report per documenti di vendita](#example-report-selection-for-sales-documents) riportato di seguito|
|Layout predefinito per e-mail con documenti vendita e acquisto  |[Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definire layout di assegni     |[Selezionare un layout degli assegni](finance-how-define-check-layouts.md) |
|Definire report per report IVA (Germania)|[Impostare report per l'IVA e l'Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] può includere ulteriori pagine **Selezione report**, a seconda della posizione e del settore, ad esempio. Per controllare la configurazione scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") e immetti **Selezione report**, quindi scegli il collegamento pertinente.

La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] include le pagine **Selezione report** seguenti:

* **Selezione report - Vendite**  
* **Selezione report - Acquisto**  
* **Selezione report - Magazzino**  
* **Selezione report - Flusso di cassa**  
* **Selezione report - Warehouse**  
* **Selezione report - Conto bancario**  
* **Selezione report - Commessa**  
* **Selezione report - Assistenza**

## <a name="example-report-selection-for-sales-documents"></a><a name="example-report-selection-for-sales-documents"></a><a name="example-report-selection-for-sales-documents"></a>Esempio: Selezione report per documenti vendita

La pagina **Selezione report - Vendite** offre i report predefiniti da utilizzare in diversi scenari per ogni tipo di documento correlato. Scegli un tipo di documento nel campo **Utilizzo**, quindi aggiungi o esamina la selezione report. Puoi impostare più di un report e specificare la sequenza in cui i report devono essere inviati o stampati.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Non puoi inviare tutti i tipi di documenti come allegati di posta elettronica. Per quelli che puoi, la pagina **Selezione report** contiene campi aggiuntivi.  

Ad esempio, nelle pagine **Selezione report - Vendite** e **Selezione report - Acquisto**, i seguenti campi consentono di configurare la posta elettronica:

|Nome campo |Descrizione  |
|-----------|-------------|
|**Utilizza per corpo e-mail**| Inserisci le informazioni di riepilogo, come il numero della fattura, la data di scadenza o un collegamento al servizio di pagamento, in un'e-mail.        |
|**Utilizza per allegato e-mail**| Allega il relativo documento all'e-mail.|
|**Descrizione layout corpo e-mail**|Specifica il layout del corpo dell'e-mail da utilizzare. In genere, è un layout di report personalizzato. |

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Impostare testi e-mail riutilizzabili e layout](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Selezionare un layout degli assegni](finance-how-define-check-layouts.md)  
[Impostare report per l'IVA e l'Intrastat (Germania)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  
[Definire layout di documenti per clienti e fornitori](ui-define-customer-vendor-document-layouts.md)  
[Configurare le stampanti](ui-specify-printer-selection-reports.md)  
[Report finanziari e analisi in Business Central](finance-reports.md)  
[Report di contabilità clienti e analisi in Business Central](receivables-reports.md)  
[Report di contabilità fornitori e analisi in Business Central](payables-reports.md)  
[Report cespiti e analisi in Business Central](fa-reports.md)  
[Report di progetto e analisi in Business Central](project-reports.md)  
[Report delle vendite e analisi in Business Central](sales-reports.md)  
[Report di acquisto e analisi in Business Central](purchase-reports.md)  
[Report di inventario e warehouse e analisi in Business Central](inventory-WMS-reports.md)  
[Report di assemblaggio e analisi in Business Central](assembly-reports.md)  
[Report di produzione e analisi in Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

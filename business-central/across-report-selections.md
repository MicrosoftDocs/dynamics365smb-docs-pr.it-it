---
title: Selezione report in Business Central
description: Informazioni su come impostare i report utilizzati per stampare vari tipi di documenti in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: d30baa44894658c03c3deffdf24a7923293b88fd
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024639"
---
# <a name="report-selection-in-business-central"></a>Selezione report in Business Central

È possibile impostare report predefiniti che saranno utilizzati diversi documenti acquisto e vendite (ordini, offerte, fatture, note di credito e così via). Ad esempio, se si dispone di un layout specifico per le fatture vendita, è possibile specificare tale report nella pagina **Selezioni report - Vendite** di modo che venga utilizzato per inviare o stampare fatture vendita.  

Le pagine **Selezioni report** specificano quale report verrà stampato nelle diverse situazioni. [!INCLUDE [prod_short](includes/prod_short.md)] include configurazioni predefinite, ma ovviamente puoi modificare queste impostazioni predefinite. È inoltre possibile aggiungere report alle pagine **Selezione report**, ad esempio per stampare più di un report per tipo di documento.  

## <a name="available-report-selections"></a>Selezioni report disponibili

[!INCLUDE [prod_short](includes/prod_short.md)] include pagine **Selezione report** differenti per aree diverse. Le tabelle seguenti descrivono dove è possibile trovare informazioni sulle diverse pagine.  

|Area o attività  |Ulteriori informazioni|
|--------------|----------|
|Esempio di funzionamento della selezione report (vendite)|[Selezione report per documenti di vendita](#example-report-selection-for-sales-documents)|
|Layout predefinito per e-mail con documenti vendita e acquisto  |[Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Definire layout di assegni     |[Selezionare un layout degli assegni](finance-how-define-check-layouts.md) |
|Definire report per report IVA (Germania)|[Impostare report per l'IVA e l'Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] può includere ulteriori pagine **Selezione report**, a seconda della posizione e del settore, ad esempio. Puoi sempre controllare la configurazione scegliendo l'icona a forma di ![Lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettendo **Selezioni report**, quindi scegli il collegamento pertinente.

La versione predefinita di [!INCLUDE [prod_short](includes/prod_short.md)] include le pagine **Sezione report** seguenti:

* **Selezione report - Vendite**  
* **Selezione report - Acquisto**  
* **Selezione report - Magazzino**  
* **Selezione report - Flusso di cassa**  
* **Selezione report - Warehouse**  
* **Selezione report - Conto bancario**  
* **Selezioni report - Sollecito/Addebito interessi**  

## <a name="example-report-selection-for-sales-documents"></a>Esempio: Selezione report per documenti vendita

La pagina **Selezione report - Vendite** definisce i report predefiniti da utilizzare in diversi scenari per ogni tipo di documento correlato. Scegli un tipo di documento nel campo **Utilizzo**, quindi aggiungi o esamina la selezione report. Puoi impostare più di un report e l'ordine di sequenza in cui i rapporti devono essere inviati o stampati.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Alcuni tipi di documento possono essere inviati come allegati di posta elettronica e altri no. Ogni pagina **Selezione report** mostra altri campi se il tipo supporta la posta elettronica per impostazione predefinita.  

Ad esempio, nelle pagine **Selezione report - Vendite** e **Selezione report - Acquisto**, i seguenti campi consentono di configurare la posta elettronica:

|Nome campo |Descrizione  |
|-----------|-------------|
|**Utilizza per corpo e-mail**| Specifica le informazioni riepilogative, come il numero di fattura, la data di scadenza e il collegamento del servizio di pagamento, che verranno aggiunte al testo del messaggio e-mail inviato.        |
|**Utilizza per allegato e-mail**| Specifica che il documento correlato verrà allegato al messaggio di posta elettronica.|
|**Descrizione layout corpo e-mail**|Specifica il layout del corpo del messaggio di posta elettronica utilizzato, in genere un layout di report personalizzato. |

## <a name="see-also"></a>Vedere anche

[Impostare testi e layout e-mail riutilizzabili per documenti vendita e acquisto](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Selezionare un layout degli assegni](finance-how-define-check-layouts.md)  
[Impostare report per l'IVA e l'Intrastat (Germania)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  
[Definire layout di documenti per clienti e fornitori](ui-define-customer-vendor-document-layouts.md)  
[Configurare le stampanti](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Panoramica dei task per impostare gli acquisti
description: Descrive i task per definire i criteri di acquisto della società e impostare i processi di acquisto.
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: bholtorf
---
# Impostazioni acquisti

Prima di poter gestire i processi di acquisto, è necessario configurare le regole e i valori che definiscono i criteri di acquisto dell'azienda.

È necessario definire l'impostazione generale nella pagina **Setup contabilità fornitori**, che in genere viene eseguita una volta durante l'implementazione iniziale. Scopri di più nella sezione seguente, [Setup contabilità fornitori](#purchases-and-payables-setup).

Una serie di attività specifiche correlate alla registrazione di nuovi fornitori è quella di prendere nota di tutti gli accordi riguardanti sconti o prezzi speciali in essere con ogni fornitore.

L'impostazione degli acquisti correlata all'aspetto contabile, come i metodi di pagamento e le valute, è descritta nella sezione Impostazione degli aspetti finanziari. Per ulteriori informazioni, vedi [Impostazione degli aspetti finanziari](finance-setup-finance.md). Allo stesso modo, l'impostazione dell'acquisto relativo all'inventario, come le unità di misura e i codici di tracciabilità degli articoli, può essere trovata nella [sezione Setup magazzino](inventory-setup-inventory.md).

## Setup contabilità fornitori

Prima di lavorare con la contabilità fornitori, specifica nella pagina **Setup contabilità fornitori** come vengono registrati i valori di acquisto e le numerazioni utilizzate per i fornitori e i documenti di acquisto.

### Impostazioni generali

Nella Scheda dettaglio **Generale** specifichi le opzioni, quali le modalità di calcolo e di registrazione degli sconti e gli eventuali arrotondamenti delle fatture. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Alcuni campi richiedono un'attenzione speciale, come il campo **Calc. sc. fatt. per ID IVA/ID imposta**, che specifica se lo sconto fattura viene calcolato in base all'ID imposta o al totale fattura. Per ulteriori informazioni, vedi [Combinare le categorie di registrazione IVA nei setup registrazione IVA](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

Allo stesso modo, il campo **Collegamenti tra valute** può comportare piccole differenze di arrotondamento quando si applicano movimenti in valute diverse. Per ulteriori informazioni, vedi [Abilitare il collegamento dei movimenti contabili fornitore in valute diverse](finance-how-enable-application-ledger-entries-different-currencies.md).

Inoltre, alcuni campi cambiano il loro comportamento o dipendono da come sono impostati altri campi. Ad esempio, la funzione **Verifica pagamento anticipato durante la registrazione** è influenzata da come il campo **Aggiornamento automatico pagamento anticipato** è impostato per controllare i pagamenti anticipati in sospeso.

Leggi i dettagli sui campi [**Nr. doc. esterno obblig.**](#external-document-number) e [**Storno esatto costo obblig.**](#exact-cost-reversing) di seguito.

### Impostazioni delle numerazioni

Nella Scheda dettaglio **Numerazioni** è necessario specificare codici di identificazione univoci che verranno utilizzati per fornitori, fatture e altri documenti di acquisto. La numerazione è importante non solo per i processi interni, ma potrebbe anche essere necessaria per seguire le normative locali. Quindi potrebbe valere la pena considerare di impostare tutte le numerazioni nella pagina **Numerazioni** in anticipo invece di crearne di nuove in **Setup contabilità fornitori**. Per ulteriori informazioni, vedi [Creare numerazioni](ui-create-number-series.md).

## Numero di documento esterni

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Storno esatto costo

La funzione **Storno esatto costo obblig.** aiuta a garantire che le merci restituite siano valutate allo stesso costo di quando erano state originariamente estratte dall'inventario, utilizzando un collegamento fisso invece di seguire un metodo di determinazione dei costi FIFO (first in, first-out). Scopri di più nella sezione [Dettagli di progettazione: Collegamento fisso](design-details-item-application.md#fixed-application). Se successivamente viene aggiunto un costo addizionale all'acquisto originale, il valore del reso da acquisto verrà automaticamente aggiornato.

Con la funzione abilitata, una transazione di reso può essere registrata solo specificando il numero di movimento contabile dell'articolo nel campo **Collega-a mov. art.** nella riga dell'ordine di reso acquisto. Il campo non viene visualizzato per impostazione predefinita nella scheda dettaglio **Righe**. Scopri come aggiungere campi alle pagine nella sezione [Personalizzare l'area di lavoro](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Altre impostazioni di acquisto

| A | Vedere |
| --- | --- |
| Crea una scheda fornitore per ogni fornitore da cui acquisti. |[Registrare nuovi fornitori](purchasing-how-register-new-vendors.md) |
| Attribuisci un ordine di priorità ai fornitori. |[Attribuire un ordine di priorità ai fornitori](purchasing-how-prioritize-vendors.md) |
| Inserisci le informazioni sul conto bancario, inclusi i codici IBAN e SWIFT, sulla scheda del tuo fornitore. | [Impostare i conti correnti fornitori](purchasing-how-set-up-vendors-bank-accounts.md) |
| Imposta gli acquirenti, assegna loro fornitori e codici per tenere traccia delle statistiche. |[Impostare gli addetti agli acquisti](purchasing-how-setup-purchasers.md) |
| Immetti i diversi sconti e i prezzi speciali concessi dai fornitori per articolo, quantità e/o data. |[Registrazione di prezzi, sconti e contratti di pagamento per gli acquisti](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definisci quanto paghi gli articoli e i servizi acquistati dalla tua azienda.  | [Impostare prezzi e sconti](across-prices-and-discounts.md) |
| Crea righe standard da inserire nei documenti di acquisto ricorrenti. | [Impostare righe di acquisto ricorrenti](purchasing-how-work-recurring-purchase-lines.md) |
| Crea sequenze di attività per collegare i processi eseguiti da utenti diversi, come la richiesta e l'approvazione degli ordini di acquisto. | [Impostare i workflow di approvazione acquisti](across-set-up-workflows.md) |
| Gestisci le interazioni commerciali con i tuoi fornitori, importa i documenti di fatturazione ricevuti e registra i nuovi fornitori utilizzando il client di posta elettronica di Outlook. | [Impostare il componente aggiuntivo Business Central per Outlook](admin-outlook.md) |
| Esamina le ricevute di spesa, converti documenti cartacei ed elettronici in righe di giornale di registrazione e digitalizza le fatture cartacee dei fornitori. | [Impostare documenti in entrata](across-how-setup-income-documents.md) |
| Specificare report predefiniti da utilizzare per diversi tipi di documenti. |[Selezione report in Business Central](across-report-selections.md)|
|Specifica se gli utenti possono registrare le fatture di acquisto e se devono registrarle insieme a una spedizione. |[Definire un criterio di registrazione delle fatture per gli utenti](admin-setup-invoice-posting-policy.md)|

## Vedi le informazioni relative al training in [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/).

## Vedere anche

[Acquisti](purchasing-manage-purchasing.md)  
[Panoramica dell'impostazione](setup.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

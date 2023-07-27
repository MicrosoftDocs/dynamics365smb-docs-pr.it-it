---
title: 'Dettagli di progettazione: IVA non detraibile'
description: 'Questo articolo fornisce informazioni sull''imposta sul valore aggiunto (IVA) non detraibile è l''IVA che è dovuta da un acquirente, ma che non è detraibile dal proprio debito IVA dell''acquirente.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# Dettagli di progettazione: IVA non detraibile

L'imposta sul valore aggiunto (IVA) non detraibile è l'IVA che è dovuta da un acquirente, ma che non è detraibile dal proprio debito IVA dell'acquirente. Poiché può essere difficile sapere dove e come viene utilizzato un articolo, è necessario contattare le autorità fiscali locali del proprio paese o area geografica per determinare se una determinata percentuale dell'IVA è detraibile. Anche quando si sa che una determinata percentuale dell'IVA non è detraibile, esistono diversi modelli per la gestione degli importi indeducibili in quanto relativi a **articoli** e **cespiti**.

## Prerequisiti per l'utilizzo dell'IVA non detraibile

Per utilizzare e registrare l'IVA non detraibile, attieniti alla seguente procedura.

1. Nella pagina **Setup IVA**, seleziona **Abilita IVA non detraibile** per abilitare la funzione.
2. Nella pagina **Setup registrazione IVA**, seleziona quali categorie di registrazione IVA possono utilizzare l'IVA non detraibile.

## Esempi

Per i seguenti esempi, l'IVA non detraibile è abilitata e la seguente configurazione è stata completata:

- Il campo **Cat. reg. art./serv. IVA** è impostato su **NDVAT**.
- Nella pagina **Setup registrazione IVA**:

    - **NDVAT** è impostato come categoria di registrazione prodotti IVA e **DOMESTIC** è impostato come categoria di registrazione IVA commerciale.
    - Il valore **Codice IVA** deve essere univoco.
    - Il campo **% IVA** è impostato su **25**.
    - Il campo **Consenti IVA non detraibile** è impostato su **Consenti**.
    - Il campo **% IVA non detraibile** è impostato su **100**.
    - Il campo **Tipologia IVA** è impostato su **IVA normale**.
    - Sono configurati solo il conto IVA vendite e il conto IVA acquisti.

Tutti gli esempi utilizzano articoli e cespiti in cui la categoria di registrazione del prodotto IVA è **NDVAT**.

### Articoli

Una nuova posizione ha **NDVAT** impostato come categoria di registrazione prodotto IVA. Nel documento di acquisto, **Quantità** = **1** e **Costo unitario diretto IVA escl.** = **1.000,00**.

Indipendentemente dall'opzione utilizzata, i risultati nel **movimento IVA** sono gli stessi.

| Tipo di documento | Tipo | Base | Importo | Imponibile IVA non detraibile | Importo IVA non detraibile |
|---|---|---|---|---|---|
| Fattura | Acquisti | 0.00 | 0.00 | 1,000.00 | 250.00 |

I dettagli sono riportati nei **Movimenti di valorizzazione**.

> [!NOTE]
> È possibile abilitare il campo **Utilizza per costo articolo** nella pagina **Setup IVA**.

#### Usa per costo dell'articolo non è abilitato

| Tipo mov. articolo | Tipo movimento | Importo costo (effettivo) | Quantità mov. contabili art. |
|---|---|---|---|
| Acquisti | Costo diretto | 1,000.00 | 1 |

#### Usa per costo dell'articolo è abilitato

| Tipo mov. articolo | Tipo movimento | Importo costo (effettivo) | Quantità mov. contabili art. |
|---|---|---|---|
| Acquisti | Costo diretto | 1,250.00 | 1 |

### Cespiti

Un nuovo cespite ha il conto costi di acquisizione impostato per utilizzare **NDVAT** come categoria di registrazione prodotto IVA. Nel documento di acquisto, **Quantità** = **1** e **Costo unitario diretto IVA escl.** = **1.000,00**.

Indipendentemente dall'opzione utilizzata, i risultati nel **movimento IVA** sono gli stessi.

| Tipo di documento | Tipo | Base | Importo | Imponibile IVA non detraibile | Importo IVA non detraibile |
|---|---|---|---|---|---|
| Fattura | Acquisti | 0.00 | 0.00 | 1,000.00 | 250.00 |

I dettagli sono riportati in **Movimenti contabili cespiti**.

> [!NOTE]
> È possibile abilitare il campo **Utilizza per costo cespite** nella pagina **Setup IVA**.

#### Utilizza per costo cespite non è abilitata

| Tipo di documento | Tipo registrazione cespite | Importo | Importo IVA |
|---|---|---|---|
| Fattura | Costo di acquisto | 1,000.00 | 250.00 |

#### Utilizza per costo cespite è abilitata

| Tipo di documento | Tipo registrazione cespite | Importo | Importo IVA |
|---|---|---|---|
| Fattura | Costo di acquisto | 1,000.00 | 250.00 |
| Fattura | Costo di acquisto | 250.00 | 0.00 |

## Vedere anche

[Impostare l'IVA non detraibile](finance-setup-nondeductible-vat.md)  
[Dati finanziari](finance.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

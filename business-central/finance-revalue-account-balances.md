---
title: Rivalutare i saldi dei conti di contabilità generale
description: Scopri come rivalutare i saldi dei conti di contabilità generale prima di produrre i rendiconti finanziari.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# <a name="revalue-general-ledger-account-balances"></a>Rivalutare i saldi dei conti di contabilità generale

Se si utilizzano conti di contabilità generale per registrare voci del bilancio patrimoniale in valute estere, devi rivalutare i saldi dei conti prima di produrre rendiconti finanziari. I tassi di cambio cambiano spesso e la rivalutazione aiuta a rendere i rendiconti finanziari più accurati.

## <a name="set-up-revaluations"></a>Impostare le rivalutazioni

Puoi impostare ciascun conto che desideri includere nelle rivalutazioni nella pagina **Scheda conto C/G**. Puoi selezionare se registrare le rettifiche di rivalutazione nei conti utili/perdite realizzati o non realizzati. La registrazione di utili e perdite durante una rettifica del tasso di cambio segue la normale routine di registrazione. Ad esempio, puoi farlo per ogni configurazione nella pagina **Valute**. Per ulteriori informazioni sulle rettifiche dei tassi di cambio, vedi [Aggiornare i tassi di cambio valuta](finance-how-update-currencies.md).

Per ridurre al minimo gli errori, nel campo **Registrazione valuta di origine**, puoi impostare una convalida per le valute per le quali desideri consentire la registrazione nei singoli conti C/G:

* Tutte le valute (vuoto)
* Più valute
* Stessa valuta
* Valuta locale

## <a name="run-a-revaluation"></a>Eseguire una rivalutazione

Per rivalutare gli importi in valuta estera nella valuta locale per i saldi dei conti C/G, nella pagina  **Piano dei conti**, utilizza l'azione **Rivalutazione valuta C/G** per avviare un processo batch. Il processo batch crea movimenti di rettifica nella registrazione selezionata. Quando registri i movimenti, rettifichi il saldo in valuta locale (VL) per il conto. I saldi dei conti C/G che vengono sempre visualizzati in VL ora riflettono le modifiche alle valute in cui sono stati registrati i movimenti. Questa rivalutazione ti consente di produrre un rendiconto finanziario più accurato con meno sforzo.

Se utilizzi una valuta contabile addizionale (VA), i movimenti di rivalutazione C/G hanno un importo VA. L'importo corrispondente solo all'importo VL in questi movimenti, non al saldo VA nel conto C/G. Se rettifichi i tassi VA dopo aver registrato le rettifiche, esegui ancora una volta la rettifica del tasso di cambio valuta per rettificare tutti i movimenti C/G.

> [!IMPORTANT]
> La rivalutazione del conto C/G potrebbe non soddisfare tutti i requisiti per registrazioni di transazioni e cespiti che necessitano di rivalutazione. Ad esempio, per strumenti finanziari, titoli, beni in leasing o se li utilizzi per volumi specifici o di grandi dimensioni di transazioni o beni. Ti consigliamo di discutere con il tuo revisore se puoi utilizzare questa funzionalità e, in tal caso, come dovresti utilizzarla. Ad esempio, se consentirai alle valute di mescolarsi per un conto o se devi tenere un conto separato per ciascun cespite che desideri monitorare.

> [!NOTE]
> La rivalutazione non offre la possibilità di applicare o annullare l'applicazione dei movimenti, come avviene con i movimenti contabili clienti e fornitori. Le rettifiche avvengono in base al saldo per valuta.

## <a name="revaluate-accounts-vs-customer-and-vendor-exchange-rate-adjustments"></a>Rivalutazione dei conti e rettifiche del tasso di cambio di clienti e fornitori

La rivalutazione semplifica l'attività di rettifica dei saldi dei conti C/G. La funzionalità rivaluta il saldo per valuta per conto C/G in modo molto simile a quanto fai per le rettifiche ai conti C/G collegati a conti bancari. Se utilizzi un conto C/G per tenere traccia di più cespiti, prendi in considerazione l'utilizzo di un conto fornitore o cliente.

> [!NOTE]
> La rivalutazione del conto C/G potrebbe non soddisfare tutti i requisiti per registrazioni di transazioni e cespiti che necessitano di rivalutazione. Ad esempio, per strumenti finanziari, titoli, beni in leasing o se li utilizzi per volumi specifici o di grandi dimensioni di transazioni o beni. Ti consigliamo di discutere con il tuo revisore se puoi utilizzare questa funzionalità e, in tal caso, come dovresti utilizzarla. Ad esempio, se consentirai alle valute di mescolarsi per un conto o se devi tenere un conto separato per ciascun cespite che desideri monitorare.

Gli esempi seguenti illustrano la differenza tra l'utilizzo di un conto C/G e l'utilizzo di un conto fornitore per tenere traccia del saldo di due cespiti monetari che utilizzano una valuta estera.

**Utilizza un conto C/G** Se utilizzi un conto C/G per tenere traccia di più cespiti (ad esempio, prestiti o cespiti) nella stessa valuta o di singole transazioni parziali per lo stesso cespite ma sempre nella stessa valuta, la rivalutazione C/G effettua un movimento per rivalutazione per la valuta. Ciò significa che non puoi tenere traccia delle rettifiche relative a singoli cespiti o singole transazioni per lo stesso cespite.

**Utilizza un conto fornitore** Se imposti più cespiti come fornitori e registri transazioni negli essi, nella stessa valuta o in valute diverse, otterrai una rettifica per valuta per fornitore. Oppure, se attivi l'interruttore **Registrazione per movimento** nel movimento della coda di processi **Rettifica tasso di cambio valuta** otterrai un movimento di rettifica per ogni movimento contabile fornitore separato.

Questa differenza è importante quando valuti se la rivalutazione C/G è la funzionalità giusta per le tue esigenze di reporting.

> [!TIP]
> Ti consigliamo di chiedere al tuo commercialista o revisore dei conti per sapere quale tipo di conto è più adatto per la tua attività. Inoltre, potrebbe esserci un'app per [!INCLUDE [prod_short](includes/prod_short.md)] in [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) che è perfetta per i tuoi scenari aziendali.

## <a name="see-also"></a>Vedere anche

[Esaminare gli importi nei conti di contabilità generale](finance-review-accounts.md)  
[Informazioni sulla contabilità generale e sul piano dei conti](finance-general-ledger.md)  

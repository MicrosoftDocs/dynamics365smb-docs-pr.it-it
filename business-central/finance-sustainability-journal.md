---
title: Registrare movimenti di sostenibilità
description: Informazioni su come registrare le emissioni di gas serra (GHG).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="record-sustainability-entries"></a>Registrare movimenti di sostenibilità

Al momento, l'unico modo per registrare le emissioni di gas serra (GHG) nel registro della sostenibilità consiste nell'utilizzare i giornali di registrazione della sostenibilità.

## <a name="sustainability-journals"></a>Giornali di registrazione della sostenibilità

I giornali di registrazione della sostenibilità sono progettati per tenere traccia e registrare le attività correlate alla sostenibilità utilizzando la stessa esperienza utente di altre registrazioni in Business Central. Gli utenti che dispongono delle informazioni necessarie possono inserire manualmente le emissioni in un giornale. In alternativa, se non dispongono di queste informazioni, possono utilizzare formule integrate per calcolare accuratamente le emissioni in base a specifici parametri noti che corrispondono a vari tipi di origini e conti.

Le informazioni immesse in un giornale di registrazione sono temporanee e possono essere modificate fintanto che sono nel giornale. Quando si esegue la registrazione, le informazioni vengono trasferite ai movimenti contabili sostenibilità in singoli conti di sostenibilità, dove non possono essere modificate. Si possono tuttavia inserire storni o correzioni dei movimenti.

### <a name="use-journal-templates-and-batches"></a>Usare batch e definizioni di registrazioni

Per impostazione predefinita, esistono due modelli registrazioni sostenibilità: quello standard e quello ricorrente.

Per ogni definizione registrazioni è possibile impostare le proprie registrazioni personali come batch registrazioni. A tal fine, seleziona l'azione **Batch** nella pagina **Modelli registrazioni sostenibilità**, quindi crea il nuovo **batch registrazione sostenibilità** nella nuova pagina. Ad esempio, puoi definire il tuo batch di registrazioni per ciascun ambito di emissione utilizzando l'opzione **Ambito emissioni** e successivamente scegliere tra i tre ambiti esistenti. Per ciascun batch, puoi aggiungere o modificare i valori per **Codice origine** e **Codice causale**.

> [!TIP]
> Se hai molte righe, puoi ridurre il rischio di errori disponendo un batch di registrazioni per ciascun tipo di emissione. In alternativa, puoi utilizzare il batch comune per tutti i tipi di emissione.

### <a name="validate-sustainability-journals"></a>Convalidare i giornali di registrazione della sostenibilità

Nella pagina **Setup sostenibilità** puoi attivare un controllo in background che ti aiuta a prevenire i ritardi nella registrazione. In caso di errori durante l'utilizzo del giornale di registrazione della sostenibilità, la convalida ti avvisa tramite notifica e ti impedisce di registrare il giornale.

Quando abiliti la convalida, la Scheda dettaglio **Verifica registrazione** mostra i problemi nella riga corrente e nell'intero batch. La convalida si attiva quando si carica un batch registrazioni e quando si seleziona un'altra riga di registrazione. Il riquadro **Totale problemi** nella Scheda dettaglio mostra il numero totale dei problemi individuati da [!INCLUDE [prod_short](includes/prod_short.md)]. Puoi selezionare il riquadro per aprire una panoramica dei problemi.

### <a name="work-with-sustainability-journals"></a>Utilizzare registrazioni di sostenibilità

Per iniziare a utilizzare le registrazioni di sostenibilità, segui questi passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazione sostenibilità**, quindi seleziona il collegamento correlato.
2. Nella pagina **Registrazione sostenibilità** immetti tutte le righe che intendi registrare nello stesso batch.
3. Puoi lasciare vuoto il campo **Tipo di documento** oppure puoi selezionare **Fattura** o **Nota di credito**.
4. Nel campo **Nr. conto** puoi selezionare solo i conti di sostenibilità non bloccati dove il campo **Registrazione diretta** è selezionato e il campo **Tipo di contabilità** è impostato su **Registrazione**. I conti devono inoltre essere configurati con una categoria e una sottocategoria.

    > [!NOTE]
    > Se utilizzi un batch in cui è configurato l'ambito di emissione, il valore di **Ambito emissioni** nel conto di sostenibilità deve essere uguale al valore di **Ambito emissioni** presente nel batch.

5. Puoi registrare gli importi manualmente o utilizzare le formule.

    - Se disponi di informazioni precise sull'emissione e desideri registrarle (ovvero, le hai sulla fattura ricevuta), devi selezionare il campo **Inserimento manuale** per indicare che inserirai gli importi manualmente. In questo caso, non puoi immettere i dati direttamente nei campi **Combustibile/elettricità**, **Distanza**, **Importo personalizzato**, **Moltiplicatore installazione** e **Fattore temporale** in quanto non sono modificabili. Invece, i campi **Emissioni CO2**, **Emissioni CH4** ed **Emissioni N2O** restano modificabili, quindi puoi inserire i tuoi dati direttamente in questi campi.
    - Se non conosci con precisione l'emissione e devi calcolarla, non selezionare il campo **Inserimento manuale**. In questo caso, i campi **Emissione CO2**, **Emissione CH4** ed **Emissione N2O** diventano non modificabili. Puoi tuttavia inserire i dettagli del calcolo in base alla formula che intendi utilizzare. Altre informazioni sulle formule definite nella **categoria del conto di sostenibilità** sono disponibili in [Contabilità generale e piano dei conti di sostenibilità](finance-sustainability-accounts-ledger.md#account-categories).

6. Per registrare il giornale, seleziona l'azione **Registra**. Quando segui una registrazione in un giornale di registrazione della sostenibilità, i movimenti vengono generati nel registro di sostenibilità.

Se la formula che utilizzi è basata sull'opzione **Calcola da contabilità generale** nella categoria del conto di sostenibilità, devi utilizzare l'azione **Raccogli importo da movimenti C/G** prima di registrare il giornale, per calcolare le emissioni in base a questa origine dati. Inoltre, se dopo aver compilato le righe della registrazione hai apportato modifiche ai fattori di emissione, devi selezionare l'azione **Ricalcola** per ottenere l'importo corretto nella registrazione.

### <a name="recurring-journals"></a>Registrazioni periodiche

Una registrazione periodica è una registrazione di sostenibilità con campi specifici per la gestione di transazioni registrate frequentemente con poche modifiche o nessuna. Alcuni esempi includono le transazioni di sostenibilità come elettricità, calore o altre transazioni simili. Puoi utilizzare le registrazioni periodiche per registrare importi fissi e variabili.

Quando utilizzi una registrazione periodica, i movimenti che registrerai regolarmente devono essere creati una sola volta. Le informazioni, come i conti, le dimensioni e i valori dimensioni, restano nelle registrazioni dopo la contabilizzazione. Ogni volta che effettui una registrazione, puoi apportare tutte le modifiche che ritieni necessarie.

Il campo **Metodo ricorrenza** è importante. Determina il modo in cui l'importo nella riga di registrazione viene gestito dopo la registrazione. Ad esempio, se utilizzi lo stesso importo ogni volta che registri la riga, puoi selezionare l'opzione **C Costante** per fare in modo che l'importo resti dopo la registrazione. Se utilizzi gli stessi conti e lo stesso testo nella riga, ma l'importo varia a ogni registrazione, puoi selezionare l'opzione **V Variabile** per fare in modo che l'importo venga eliminato dopo la registrazione.

Anche il campo **Frequenza ricorrenza** è importante e deve essere impostato. Questo campo contiene una formula di data che determina la frequenza di registrazione del movimento nella riga di registrazione. Altre informazioni sono disponibili in [Usare le formule data](ui-enter-date-ranges.md#use-date-formulas).

Il campo **Data di scadenza** determina la data in cui la riga sarà registrata per l'ultima volta. Oltre tale data, la riga non verrà più registrata. Il vantaggio dell'utilizzo del campo **Data di scadenza** è che la riga non viene eliminata immediatamente dal giornale di registrazione. È possibile inserire una data successiva in modo da poter utilizzare la riga in futuro. Se il campo è vuoto, la riga verrà registrata ogni volta fino a quando non verrà eliminata dal giornale di registrazione.

## <a name="see-also"></a>Vedere anche

[Dati finanziari](finance.md)  
[Panoramica della gestione della sostenibilità](finance-manage-sustainability.md)  
[Setup sostenibilità](finance-sustainability-setup.md)  
[Contabilità generale e piano dei conti di sostenibilità](finance-sustainability-accounts-ledger.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Come registrare movimenti di sostenibilità
description: Scopri come registrare le emissioni di gas serra.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Come registrare movimenti di sostenibilità  

In questo momento, l'unico modo per registrare emissioni di gas serra nel **Registro della sostenibilità** è utilizzare le **Registrazioni di sostenibilità**.   

## Registrazione di sostenibilità  

Le **registrazioni di sostenibilità** sono progettate per tenere traccia e registrare le attività relative alla sostenibilità utilizzando la stessa esperienza utente di altre registrazioni in Business Central. Nella registrazione, gli utenti hanno la possibilità di inserire manualmente le emissioni se possiedono le informazioni necessarie. In alternativa, se non dispongono di questi dati, possono utilizzare formule integrate per calcolare accuratamente le emissioni sulla base di specifici parametri noti corrispondenti a vari tipi di origini e conti. 

Le informazioni immesse in una registrazione sono temporanee e possono essere modificate mentre si trovano nella registrazione. Quando si registra la registrazione, le informazioni vengono trasferite in **Movimenti contabili sostenibilità** in singoli **Conti di sostenibilità**, dove non può essere modificata. Puoi tuttavia stornare o correggere i movimenti.  

### Usare batch e definizioni di registrazioni 

Esistono due **Modelli registrazioni sostenibilità** per impostazione predefinita: quello standard e quello ricorrente. Per ogni definizione registrazioni è possibile impostare le proprie registrazioni personali come batch registrazioni. Per fare ciò, devi scegliere l'azione **Batch** nella pagina **Modelli registrazioni sostenibilità** e creare il nuovo **batch di registrazioni di sostenibilità** nella nuova pagina. Ad esempio, puoi definire il tuo batch di registrazioni per ciascun ambito di emissione, utilizzando l'opzione **Ambito emissioni** in cui puoi scegliere tra tre ambiti esistenti. Puoi anche aggiungere o modificare il **codice sorgente** e il **codice motivo** per ciascuno dei batch. 

>[!TIP]
>Puoi avere un batch registrazioni per ciascuno dei tipi di emissioni, se si dispone di molte righe in modo da ridurre la possibilità di commettere errori, ma è anche possibile utilizzare il batch comune per tutti i tipi di emissioni.   

### Convalidare le registrazioni di sostenibilità 

Puoi abilitare un controllo in background nella pagina **Setup sostenibilità** che ti aiuterà a prevenire ritardi durante la registrazione. Il controllo ti avviserà quando è presente un errore durante l'utilizzo della **registrazione di sostenibilità** e ciò ti impedirà di registrare la registrazione.  

Quando abiliti la convalida, la Scheda dettaglio **Verifica registrazione** mostrerà i problemi nella riga corrente e nell'intero batch. La convalida si verifica quando si carica un batch registrazioni e quando si sceglie un'altra riga di registrazione. Il riquadro **Totale problemi** nella Scheda dettaglio mostra il numero totale di problemi rilevati da [!INCLUDE [prod_short](includes/prod_short.md)] ed è possibile selezionarlo per aprire una panoramica dei problemi. 

### Utilizzare registrazioni di sostenibilità 

Per iniziare a utilizzare le **registrazioni di sostenibilità**, procedi come segue:   

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi 3.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazione sostenibilità**, quindi seleziona il collegamento correlato. 
2. Nella pagina **Registrazione sostenibilità**, puoi immettere tutte le righe che intendi registrare con lo stesso batch.  
3. Come **Tipo di documento**, puoi mantenere l'opzione vuota o scegliere di utilizzare **Fattura** o **Nota di credito**.  
4. Nel campo **Nr. conto** , puoi scegliere solo **Conti di sostenibilità** con il campo **Registrazione diretta** selezionato, **Registrazione** come **Tipo di contabilità** e conto non bloccato. Inoltre, i conti devono essere configurati con categoria e sottocategoria.  

>[!NOTE]
>Se si utilizza il batch in cui è configurato l'ambito di emissione, l'**Ambito di emissione** nel **Conto di sostenibilità** deve essere uguale all'**Ambito emissioni** nel batch utilizzato.  

5. Hai due opzioni: registrare manualmente gli importi o utilizzare le formule.   

    1. Se disponi di informazioni precise sull'emissione, desideri registrarle (ovvero, le hai sulla fattura ricevuta), devi selezionare il campo **Inserimento manuale** per specificare che gli importi verranno inseriti manualmente. In questo caso, non puoi inserire i tuoi dati nei campi **Combustibile/Elettricità**, **Distanza**, **Importo personalizzato**, **Moltiplicatore installazione** e **Fattore temporale** , poiché non saranno modificabili per questa scelta. Tuttavia, i campi **Emissioni CO2**, **Emissioni CH4** e **Emissioni N2O** saranno modificabili e potrai inserire i tuoi dati direttamente lì. 
    2. Se non conosci con precisione le tue emissioni, devi calcolarle, e non è necessario aver selezionato il campo **Inserimento manuale** e in questo caso i campi **Emissioni CO2**, **Emissioni CH4** e **Emissioni N2O** non saranno modificabili, ma puoi immettere i dettagli del calcolo in base alla formula che stai utilizzando. Puoi trovare ulteriori informazioni sulle formule utilizzate e definite in **Categoria conto di sostenibilità** in [Contabilità generale e grafico dei conti di sostenibilità](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Per registrare le registrazioni, scegli l'azione **Registra**. Quando si registra in una **Registrazione sostenibilità**, i movimenti vengono generati nel **Registro di sostenibilità**. 

Nel caso in cui la tua formula sia basata sull'opzione **Calcola da contabilità generale** nella **Categoria conto di sostenibilità**, devi utilizzare l'azione **Raccogli importo da movimenti C/G** prima di registrare la registrazione per calcolare le emissioni in base a questa origine dati. Inoltre, se dopo aver compilato le righe della registrazione sono state apportate modifiche ai fattori di emissione, devi scegliere l'azione **Ricalcola** per ottenere l'importo corretto nella registrazione.  

### Registrazioni periodiche 

Una registrazione periodica è una **Registrazione di sostenibilità** con campi specifici per la gestione di transazioni registrate frequentemente con poche modifiche o nessuna. Ad esempio, transazioni di sostenibilità come elettricità, calore o altre transazioni simili. L'utilizzo di registrazioni periodiche ti consente di registrare importi fissi e variabili. Con una registrazione periodica, crei movimenti che verranno registrati regolarmente solo una volta. Ad esempio, i conti, le dimensioni e i valori dimensioni e così via, resteranno nelle registrazioni dopo la contabilizzazione. Se sono necessarie modifiche, puoi apportarle ogni volta che esegui una registrazione. 

Il campo **Metodo ricorrenza** è importante. Determina come trattare l'importo nella riga delle registrazioni dopo la registrazione. Ad esempio, se utilizzi lo stesso importo ogni volta che registri la riga, puoi scegliere di mantenere l'importo e in questo caso, devi utilizzare **F Fissato** come opzione. Se nella riga vengono utilizzati i medesimi conti e lo stesso testo e l'importo varia a ogni registrazione, puoi scegliere di eliminare l'importo dopo la registrazione e in questo caso, sceglierai l'opzione **V-Variabile**. 

Devi inoltre configurare il campo **Frequenza periodica** poiché questo campo della formula della data determina la frequenza di registrazione del movimento nella riga di registrazione e deve essere compilato. Ulteriori informazioni in [Usare le formule data](ui-enter-date-ranges.md#use-date-formulas).  

Il campo **Data di scadenza** determina la data in cui la riga sarà registrata per l’ultima volta. Oltre tale data, la riga non verrà più registrata. Quando si utilizza il campo **Data di scadenza**, la riga non viene immediatamente eliminata dalla registrazione. È possibile inserire una data successiva in modo da poter utilizzare la riga in futuro. Se il campo rimane vuoto, la riga verrà registrata ogni volta fino a quando non verrà eliminata dalle registrazioni.  

## Vedere anche  
[Finanze](finance.md)    
[Panoramica della gestione della sostenibilità](finance-manage-sustainability.md)   
[Setup sostenibilità](finance-sustainability-setup.md)   
[Contabilità generale e grafico dei conti di sostenibilità](finance-sustainability-accounts-ledger.md)   
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]

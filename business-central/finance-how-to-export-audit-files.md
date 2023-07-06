---
title: Esportazione file di controllo
description: 'Questo articolo spiega come impostare diversi formati di esportazione e quindi utilizzarli, in base ai requisiti del revisore o dell''autorità.'
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# <a name="audit-file-export"></a>Esportazione file di controllo

L'esportazione delle informazioni contabili dal sistema è una richiesta comune da parte di alcune autorità locali o revisori. Le esportazioni di formati e informazioni richieste possono differire. I movimenti per l'esportazione sono in genere movimenti di contabilità generale (G/L) o movimenti di imposta sul valore aggiunto (IVA). Tuttavia, a volte sono necessarie altre informazioni.

**Esportazione dei file di controllo** è un'estensione preinstallata che consente di esportare diverse voci, in base ai requisiti del revisore o dell'autorità. Indipendentemente dal tipo di formato o dalle voci, è possibile utilizzare la funzionalità dell'estensione per controllare il processo di esportazione dei dati. La funzionalità non ha un formato di file preinstallato per l'esportazione. Pertanto, devi installare un'app con un formato specifico (ad esempio SIE, SAF-T o FAC) o svilupparne una tua.

> [!NOTE]
> Attualmente, puoi selezionare il formato SIE o SAF-T come app aggiuntiva. I partner possono anche sviluppare un formato personalizzato. Il numero di formati disponibili aumenterà nel tempo.

## <a name="set-up-audit-file-export"></a>Configurazione dell'esportazione dei file di controllo

1. Seleziona il pulsante di ricerca ![Lente d'ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), inserisci **Configurazione dell'esportazione dei file di controllo**, quindi seleziona il collegamento correlato.
2. Nella pagina **Configurazione dell'esportazione dei file di controllo**, attieniti alla seguente procedura:

    1. Nella Scheda dettaglio **Generale**, nel campo **Codice formato di esportazione file di controllo**, specifica il codice per il formato di esportazione del file di controllo predefinito. Sono disponibili solo i formati abilitati durante l'installazione di un formato file specifico da Gestione funzionalità e quelli aggiunti come formato personalizzato.
    2. Nella Scheda dettaglio **Qualità dei dati**, seleziona la casella di controllo **Controlla informazioni società** per ricevere una notifica sui campi delle informazioni sulla società che non sono state impostate correttamente.
    3. Seleziona la casella di controllo **Controlla cliente** se desideri ricevere una notifica se i campi non sono impostati correttamente per clienti specifici.
    4. Seleziona la casella di controllo **Controlla fornitore** se desideri ricevere una notifica se i campi non sono impostati correttamente per fornitori specifici.
    5. Seleziona la casella di controllo **Controlla conto corrente bancario** se desideri ricevere una notifica se i campi non sono impostati correttamente per conti correnti bancari specifici.
    6. Seleziona la casella di controllo **Controlla codice postale** se desideri ricevere una notifica se un codice postale non è stato impostato correttamente.
    7. Seleziona la casella di controllo **Controlla indirizzo** se desideri ricevere una notifica se un indirizzo non è stato impostato correttamente.
    8. Nel campo **Codice postale predefinito**, inserisci il codice postale da utilizzare se sulla scheda cliente o fornitore non è specificato alcun codice postale.

3. Seleziona il pulsante di ricerca ![Lente d'ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), inserisci **Configurazione formato dell'esportazione dei file di controllo**, quindi seleziona il collegamento correlato.
4. Nella pagina **Configurazione formato dell'esportazione dei file di controllo**, attieniti alla seguente procedura:

    1. Seleziona il formato di file di esportazione file di controllo che desideri configurare. Sono disponibili solo i formati abilitati durante l'installazione di un formato file specifico da Gestione funzionalità e quelli aggiunti come formato personalizzato.
    2. Nel campo **Nome file di controllo**, specifica il nome file predefinito o il modello di nome file per il file di controllo che si desidera esportare.
    3. Seleziona la casella di controllo **Archivia in file Zip** per comprimere automaticamente i file esportati.

## <a name="provide-the-gl-account-mapping-for-audit-file-export"></a>Fornisci il mapping del conto Co.Ge. per l'esportazione del file di controllo

La maggior parte dei formati richiesti dalle autorità per i conti Co.Ge. richiede un piano dei conti standard specifico. Pertanto, dopo aver configurato i conti Co.Ge., il file esportato sarà basato sulle mappature. Puoi utilizzare più mapping nel tuo sistema.

Segui questi passaggi per fornire il mapping del conto Co.Ge. per l'esportazione del file di controllo.

1. Seleziona il pulsante di ricerca ![Lente d'ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), inserisci **Mapping conto C/G**, quindi seleziona il collegamento correlato.
2. Nella pagina **Mapping C/G**, seleziona **Nuovo** per creare un mapping.
3. Nel campo **Codice**, specificare il mapping che rappresenta il periodo di dichiarazione.
4. Nel campo **Tipo di conto standard**, seleziona il tipo di conti C/G standard.
5. Nel campo **Formato esportazione file di controllo**, specifica il formato di esportazione del file di controllo a cui sono collegati i conti Co.Ge. standard.
6. Nel campo **Tipo di periodo**, il sistema specifica un periodo contabile o un tipo di periodo personalizzato con data e ora di inizio flessibili, in base alla selezione. Se selezioni un periodo contabile specifico, il campo sarà impostato su **Periodo contabile**. In caso contrario, verrà impostato su **Intervallo dati**.
7. Nel campo **Periodo contabile**, specifica la data di inizio del periodo contabile che verrà utilizzato come periodo contabile, se si desidera che siano uguali.
8. Se imposti il campo **Periodo contabile**, i campi **Data di inizio** e **Data di fine** vengono impostati automaticamente, in base al periodo specificato. In caso contrario, puoi impostare manualmente le date di inizio e di fine per i report.
9. Se hai già aggiunto un piano dei conti standard, procedi nel seguente modo:

    1. Nel campo **Nr. categoria conto standard**, specifica la categoria del conto standard o del codice di raggruppamento utilizzato per il mapping.
    2. Nel campo **Nr. conto standard**, specifica il codice del conto standard o del codice di raggruppamento utilizzato per il mapping.

10. Seleziona la casella di controllo **Includi saldo in entrata** per considerare il saldo in entrata del conto C/G di tipo **contropartita** deve essere considerato per la mappatura al posto del saldo periodo di dichiarazione.
11. Per avviare il mapping, attieniti a questa procedura:

    1. Per generare le righe nella pagina **Mappatura conto C/G** in base a un piano dei conti esistente, seleziona **Inizializza origine per la mappatura**. Per copiare il mapping del conto C/G da un altro codice di mapping, seleziona **Copia da un'altra mappatura**. Al termine della creazione delle righe, tutti i conti C/G che hanno registrato movimenti verranno contrassegnati in verde.
    2. Per contrassegnare solo i conti C/G con inserimenti, seleziona **Aggiorna disponibilità movimento C/G**. Se l'opzione **Includi saldo in entrata** è abilitata, tutti i movimenti C/G registrati vengono presi in considerazione per il calcolo. In caso contrario, vengono considerate solo le registrazioni C/G del periodo contabile.

## <a name="export-the-audit-file"></a>Esportazione del file di controllo

1. Seleziona il pulsante di ricerca ![Lente d'ingrandimento che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), inserisci **Documenti dell'esportazione dei file di controllo**, quindi seleziona il collegamento correlato.
2. Nella pagina **Documenti dell'esportazione del file di controllo**, seleziona **Nuovo**.
3. Nella Scheda dettaglio **Generale**, attieniti alla seguente procedura:

    1. Nel campo **Formato dell'esportazione del file di controllo**, seleziona il formato utilizzato per esportare il file di controllo.
    2. Nel campo **Codice mappatura conto C/G**, seleziona il codice di mapping conto C/G per il periodo contabile.
    3. Seleziona la casella di controllo **Suddivisa per mese** se devono essere generati più file di controllo al mese.
    4. Seleziona la casella di controllo **Suddivisa per data** se devono essere generati più file di controllo al giorno.
    5. Nel campo **Commento testata**, inserisci il commento da includere nell'intestazione del file di controllo.
    6. Nel campo **Contatto**, specifica il contatto che viene esportato nella testata del file di controllo.
    7. Seleziona la casella di controllo **Crea più file Zip** per generare più file zip.

        > [!IMPORTANT]
        > Seleziona questa casella di controllo solo se in precedenza hai installato alcune delle app di formato o ne hai creata una personalizzata. L'installazione di uno o più dei formati specifici probabilmente aggiungerà campi e funzioni alla funzionalità **Esportazione dei file di controllo**, in base ai requisiti di formato.

4. Nella Scheda dettaglio **Elaborazione**, attieniti alla seguente procedura:

    1. Seleziona la casella di controllo **Elaborazione parallela** se desideri che la generazione del file di controllo venga elaborata da processi paralleli in background. Deseleziona la casella di controllo per esportare i dati nella sessione corrente.
    2. Se hai selezionato la casella di controllo **Elaborazione parallela**, nel campo **Numero massimo di lavori** , specifica il numero massimo di processi in background che possono essere eseguiti contemporaneamente.
    3. Nel campo **Prima data/ora inizio**, specifica la prima data e ora in cui il processo in background deve essere eseguito. Se esegui il processo selezionando **Avvia**, puoi tenere traccia dello stato nelle Schede dettaglio **Elaborazione** e **Righe**.

5. Al termine, seleziona **Scarica come file** per scaricare il file di controllo per la riga selezionata.

> [!IMPORTANT]
> Se hai più movimenti da esportare, ti sconsigliamo di esportarli nella sessione corrente, a causa di possibili problemi di prestazioni. Ti consigliamo invece di utilizzare l'elaborazione parallela durante i giorni o le ore non lavorative.

## <a name="see-also"></a>Vedere anche
[Gestione contabile](finance.md)  
[Informazioni sulla contabilità generale e sul piano dei conti](finance-general-ledger.md)  
[Usare le dimensioni](finance-dimensions.md)  
[Utilizzare Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

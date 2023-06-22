---
title: Esaminare i conti di contabilità generale
description: Puoi tenere traccia dei tuoi progressi quando rivedi gli importi nei conti di contabilità generale.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
---

# <a name="review-amounts-in-general-ledger-accounts" />Esaminare gli importi nei conti di contabilità generale

Potresti avere dei conti di contabilità generale che esamini spesso. Oppure potresti voler accelerare il processo di revisione alla fine del mese. Per aiutarti a tenere traccia di ciò che hai fatto e per velocizzare le revisioni, usa l'azione **Revisiona movimenti** nella pagina **Piano dei conti** o **Scheda conto C/G** per ogni account. 

## <a name="set-up-accounts-for-reviews" />Impostare i conti per la revisione

Sulla pagina **Scheda conto C/G** per ciascun conto, specifica come consentire le revisioni nel campo **Criteri di revisione**.

|Criterio di revisione  |Descrizione  |
|---------|---------|
|Nessuno     | Non puoi contrassegnare i movimenti per il conto come revisionati. Ad esempio, utilizza questa opzione per conti fornitori, clienti e conti bancari in cui sono disponibili altri modi per verificarne gli importi.        |
|Consenti revisione     | Non è necessario includere i movimenti in una revisione e gli importi dei movimenti di addebito e accredito non devono essere bilanciati. Rimuovi una revisione, ad esempio, se hai commesso un errore.        |
|Consenti revisione e corrispondi saldo     | Gli importi totali dei movimenti in dare e avere nella revisione devono corrispondere. I campi **Dare** e **Avere** mostrano tali importi e il campo **Saldo** mostra il totale. Questa impostazione ti consente anche di rimuovere una revisione. Quando rimuovi una revisione da uno o più movimenti, i movimenti in dare e avere devono comunque essere bilanciati.        |

## <a name="mark-entries-as-reviewed" />Contrassegnare i movimenti come revisionati

Scegli le voci che hai rivisto, quindi usa l'azione **Imposta selezionato come revisionato**. Ogni volta che contrassegni uno o più movimenti come revisionati, ai movimenti viene assegnato lo stesso numero nella colonna **Identificatore di revisione**. L'identificatore di revisione è un modo pratico per tenere traccia dei movimenti che sono stati rivisti contemporaneamente. [!INCLUDE [prod_short](includes/prod_short.md)] registra anche l'utente che ha eseguito la revisione e quando l'ha eseguita.

Se contrassegni i movimenti come rivisti, ma ti penti di averlo fatto, usa l'azione **Imposta selezionato come non rivisto**.

* Se al conto viene assegnato il criterio Revisione consentita, l'azione reimposta l'identificatore di revisione su 0 e rimuove la persona, la data e l'ora della revisione. 
* Se viene assegnato il criterio Revisione consentita e corrispondenza saldo, il credito e il debito devono comunque essere bilanciati. Ad esempio, se uno dei movimenti in una revisione è un errore, puoi scegliere un altro movimento con il valore corretto. Il movimento sostituito non deve avere lo stesso identificatore di revisione.

> [!TIP]
> Un modo veloce per scegliere più movimenti è tenere premuto Ctrl o Maiusc mentre selezioni. Ctrl consente di selezionare voci specifiche e Maiusc seleziona tutte le voci tra la prima e l'ultima voce selezionata.

## <a name="review-accounts-that-have-old-entries" />Esaminare i conti con movimenti precedenti

Potresti avere movimenti di periodi passati che hai già rivisto o semplicemente non hanno bisogno di una revisione. Vuoi iniziare a rivedere i movimenti ad esempio dall'inizio dell'anno o del periodo contabile. È possibile lasciare i movimenti come sono. Tuttavia, se vuoi analizzare i dati in Excel o utilizzare la modalità di analisi, contrassegna i movimenti come revisionati. Per ulteriori informazioni sull'analisi dei movimenti, vai a [Analizzare i movimenti](#analyze-entries). Per contrassegnare i movimenti come revisionati, aggiungi un filtro nel riquadro Filtro per visualizzare solo quelle voci, quindi scegli l'azione **Contrassegna i movimenti selezionati come revisionati**.

## <a name="filter-entries" />Filtrare i movimenti

Per avere un quadro più chiaro, esistono diversi modi per filtrare i movimenti nella pagina **Revisiona movimenti C/G**.

* Utilizza le azioni **Mostra movimenti revisionati** e **Nascondi movimenti revisionati** per mostrare solo le voci che hai o non hai revisionato. Per cancellare i filtri, utilizza l'azione **Mostra tutti i movimenti**.
* Usa il riquadro Filtro. Ad esempio, puoi filtrare per numero di conto o, se hai voci precedenti e desideri contrassegnarle tutte come revisionate, per data di pubblicazione.

## <a name="analyze-entries" />Analizzare i movimenti

Ci sono un paio di modi per analizzare i movimenti di contabilità generale che hai revisionato.

* Attiva la modalità di analisi, ad esempio, per raggruppare i movimenti in base al loro identificatore di revisione. Per ulteriori informazioni sulla modalità di analisi, vai a [Analizzare i dati della pagina elenco utilizzando la modalità di analisi](analysis-mode.md).
* Esporta i movimenti in Excel.

## <a name="see-also" />Vedere anche

[Informazioni sulla contabilità generale e sul piano dei conti](finance-general-ledger.md)  
[Impostare o modificare il piano dei conti](finance-setup-chart-accounts.md)  

---
title: Utilizzare i conti statistici per analizzare i dati non transazionali
description: Descrive come utilizzare i conti statistici come un'altra origine di dati per le tue analisi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
ms.service: dynamics-365-business-central
---
# <a name="analyze-data-with-statistical-accounts"></a>Analizzare i dati con i conti statistici

Utilizza i conti statistici per integrare le informazioni nei report finanziari. I conti statistici ti consentono di aggiungere metriche basate su dati non transazionali. Aggiungi i dati non transazionali come unità basate su numeri, ad esempio:

* Numero di dipendenti
* Metratura
* Il numero di clienti con conti scaduti

Ad esempio, puoi misurare ricavi o costi in base al numero di persone in un reparto. L'organico del dipartimento è l'unità per il conto statistico. L'immagine seguente mostra un esempio di report che utilizza un conto statistico per mostrare i ricavi per dipendente.

:::image type="content" source="media/statistical account report example.png" alt-text="Un esempio di report che include i dati di un conto statistico.":::

In termini di funzionamento, i conti statistici sono simili ai conti di registrazione. Memorizzano le transazioni registrate utilizzando i giornali di registrazione dei conti statistici, in modo da poter utilizzare le transazioni come dati per i report finanziari. Per ulteriori informazioni sui report finanziari, vedi [Preparare Financial Reporting con i dati finanziari e le categorie di conti](bi-how-work-account-schedule.md). 

Ci sono un paio di differenze fondamentali tra i conti statistici e i conti di registrazione. I conti statistici sono entità separate e non sono inclusi nei report di bilancio di verifica. Inoltre, non è necessario bilanciare gli importi in dare e avere quando si utilizzano i giornali di registrazione dei conti statistici per registrare le voci in un conto statistico. Registri solo l'importo.

## <a name="set-up-a-statistical-account"></a>Impostare un conto statistico

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Conti statistici**, quindi scegli il collegamento correlato.
1. Compila i campi della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account"></a>Registrare gli importi in un conto statistico

1. Per registrare gli importi di cui vuoi tenere traccia, nella pagina **Conti statistici** , scegli l'azione **Registro conti statistici**.
1. Nel campo **Data di registrazione** immetti l'ultima data del periodo di registrazione per cui vuoi registrare gli importi.
1. Facoltativo: se desideri tenere traccia degli importi per un documento specifico, nel campo **Numero documento** inserisci l'ID del documento.
1. Nel campo **Numero conto statistico** , scegli il conto statistico in cui inserire gli importi.
1. Nel campo **Descrizione**, immetti una breve descrizione di ciò che stai misurando.  
1. Immetti l'importo da registrare nel campo **Importo**. 
1. Facoltativo: se desideri includere il conto statistico in analisi più avanzate, specifica le dimensioni nei campi **Codice reparto** e **Codice gruppo clienti**. Per ulteriori informazioni sulle dimensioni, vai ad [Analisi dei dati per dimensioni](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts"></a>Verificare gli importi in un conto statistico

Nella pagina **Conti statistici** , utilizza l'azione **Saldo conti statistici** per verificare che gli importi registrati siano corretti per ciascun periodo.  

## <a name="include-the-statistical-account-in-a-financial-report"></a>Includere il conto statistico in un report finanziario

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Report finanziari**, quindi scegli il collegamento correlato.
1. Crea un nuovo report finanziario in uno dei seguenti modi:
    1. Per iniziare da zero, scegli **Nuovo**. Per ulteriori informazioni sulla creazione di report finanziari, vai a [Creare un nuovo report finanziario](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Per utilizzare le impostazioni di un report simile già in tuo possesso, scegli il report da copiare, quindi scegli l'azione **Copia report finanziario**. Puoi modificare le impostazioni che copi nel nuovo report.
1. Aggiungi il conto statistico:
    1. Se inizi da zero, scegli l'azione **Modifica definizione di riga**.
    1. Per utilizzare una definizione di riga di un report esistente, scegli il report da cui copiare, quindi scegli l'azione **Copia definizione di riga**.
1. Nella pagina **Definizione di riga**, nel campo **Nr. riga** definisci dove verrà visualizzata la riga nella sequenza di righe sul report.
1. Nel campo **Descrizione**, immetti il testo che indica ciò che stai misurando.
1. Nel campo **Tipo totale** , scegli **Conti statistici**.
1. Nel campo **Totale** scegli un conto statistico.
1. Nel campo **Tipo riga** scegli se visualizzare il saldo alla data di registrazione o all'inizio del periodo di registrazione oppure se visualizzare la variazione dell'importo durante il periodo.
1. Compilare i campi rimanenti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Vedere anche

[Business Intelligence finanziario](bi.md)  
[Report finanziari e analisi in Business Central](finance-reports.md)

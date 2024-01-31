---
title: Informazioni sulla funzionalità di pianificazione
description: Scopri come la pianificazione utilizza i dati di domanda e offerta per suggerire come bilanciare l'offerta per soddisfare la domanda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.form: '5430,'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Informazioni sulla funzionalità di pianificazione

Il sistema di pianificazione considera tutti i dati relativi a domande e approvvigionamento, confronta i risultati e crea suggerimenti per bilanciare l'approvvigionamento in modo da soddisfare la domanda.  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md).  

> [!NOTE]  
> Per tutti i campi citati in questo argomento, leggere la descrizione comando per comprenderne la funzione. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Domanda e offerta

La pianificazione è costituita da due elementi, la domanda e l'approvvigionamento. Questi devono bilanciarsi per garantire che la domanda sia soddisfatta.  

- La domanda è un qualsiasi fabbisogno lordo quale un ordine di vendita, un ordine di assistenza o un componente necessario per ordini di produzione o assemblaggio, un trasferimento in uscita, un ordine programmato o una previsione. Inoltre, vi sono altri tipi tecnici di domanda, ad esempio una produzione negativa o un ordine di acquisto, una giacenza negativa e un reso di acquisto.  
- L'approvvigionamento si riferisce a qualsiasi tipo di rifornimento, quale magazzino, ordine di acquisto, ordine di assemblaggio, ordine di produzione o trasferimento in entrata. In modo analogo, può essere presente un ordine di vendita o di assistenza negativo oppure un componente necessario o un reso vendite negativo, che rappresentano un tipo di approvvigionamento.  

Un altro obiettivo del sistema di pianificazione consiste nel garantire che il magazzino non aumenti in modo superfluo. Nel caso di un calo della domanda, verrà suggerito dal sistema di pianificazione di rimandare, ridurre in quantità o annullare gli ordini di rifornimento esistenti.  

## Calcolo della pianificazione

Il sistema di pianificazione si basa sulla domanda anticipata ed effettiva da parte dei clienti, nonché sui parametri di riordino del magazzino. L'esecuzione del calcolo della pianificazione ha come risultato alcune azioni specifiche suggerite dall'applicazione ([Messaggi di azione](production-how-to-run-mps-and-mrp.md#action-messages)) da adottare relativamente al possibile rifornimento da fornitori, trasferimenti tra magazzini o produzione. Se sono già presenti ordini di rifornimento, le azioni suggerite possono consistere nell'aumento o nell'accelerazione di tali ordini per rispondere alle modifiche nella domanda.  

Le base della procedura di pianificazione consiste nel calcolo del fabbisogno da lordo a netto. Il fabbisogno netto determina il rilascio degli ordini pianificati, la cui programmazione si basa sulle informazioni relative al ciclo (articoli lavorati) o sul lead time della scheda articolo (articoli acquistati). Le quantità relative al rilascio degli ordini pianificati sono basate sul calcolo della pianificazione e sono influenzate dai parametri impostati nelle singole schede articolo.  

> [!TIP]
> Il sistema di pianificazione si basa sul modo in cui l'organizzazione utilizza le sedi. Per ulteriori informazioni, vedere [Pianificazione con o senza sedi](production-planning-with-without-locations.md).

## Pianificazione con ordini di trasferimento manuali

Nel campo **Sistema di Rifornimento** in una scheda SKU, puoi impostare il sistema di pianificazione per creare ordini di trasferimento per bilanciare l'approvvigionamento e la domanda tra le ubicazioni.  

Oltre a tali ordini di trasferimento automatici, è possibile che in alcuni casi sia necessario eseguire uno spostamento generale delle quantità di magazzino in un'altra ubicazione, indipendentemente dalla domanda esistente. A tale scopo, è necessario creare manualmente un ordine di trasferimento per la quantità da spostare. Per evitare che tale ordine di trasferimento manuale venga manipolato dal sistema di pianificazione, impostare **Flessibilità pianificazione** nelle righe di trasferimento su Nessuna.  

Se si desidera invece fare in modo che il sistema di pianificazione rettifichi le quantità e le date dell'ordine di trasferimento in base alla domanda esistente, impostare il campo **Flessibilità pianificazione** sul valore di default Illimitata.

## Parametri di pianificazione

I parametri di pianificazione determinano i tempi, le quantità e le modalità di rifornimento in base alle diverse impostazioni nella scheda articolo (unità di stockkeeping, USK) e in Setup manufacturing.  

I parametri di pianificazione seguenti sono presenti nella scheda articolo o USK:  

- Periodo di stabilizzazione  
- Quantità di smorzamento  
- Metodo di riordino  
- Punto riordino
- Giacenza massima  
- Livello di overflow  
- Intervallo di tempo  
- Periodo di accumulo lotti  
- Periodo di riprogrammazione  
- Qtà di riordino  
- Lead time di sicurezza  
- Scorta di sicurezza  
- Criteri di assemblaggio  
- Politica di produzione  

I modificatori di ordini seguenti sono presenti nella scheda articolo o USK:  

- Quantità minima ordine  
- Quantità massima ordine  
- Molteplicità ordine  

I campi di setup di pianificazione globale nella pagina **Setup manufacturing** includono:  

- Cod. ultimo livello dinamico  
- Previsione della domanda corrente  
- Usa previsioni per le ubicazioni  
- Lead time di sicurezza di default  
- Livello di overflow vuoto  
- Calcolo combinato MPS/MRP
- Componenti nell'ubicazione  
- Periodo di stabilizzazione di default  
- Quantità di smorzamento di default  

Per ulteriori informazioni, vedi [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)  

## Altri campi di pianificazione importanti

### Flessibilità pianificazione

Nella maggior parte degli ordini di approvvigionamento, ad esempio gli ordini di produzione, è possibile selezionare **Illimitata** o **Nessuna** nel campo **Flessibilità pianificazione** delle righe.

Ciò indica se l'approvvigionamento rappresentato dalla riga dell'ordine di produzione viene considerato dal sistema di pianificazione durante il calcolo dei messaggi d'azione.
Se nel campo è impostato il valore **Illimitata**, il sistema di pianificazione include la riga nel calcolo dei messaggi di azione. Se nel campo è impostato il valore **Nessuna**, la riga sarà fissa e non modificabile e non verrà inserita nel calcolo dei messaggi di azione.

### Avviso

Nel campo **Avviso** della pagina **Prospetto pianificazione** viene visualizzato un messaggio per ogni riga di pianificazione creata per una situazione insolita. L'utente può scegliere di leggere ulteriori informazioni. Sono disponibili i seguenti tipi di avviso:

- Emergenza
- Eccezione
- Attenzione
- Emergenza

L'avviso di emergenza è visualizzato in due situazioni:

- Alla data di inizio pianificazione le giacenze sono negative.
- Sono presenti eventi di approvvigionamento o domanda arretrati.

Se le giacenze di un articolo sono negative alla data di inizio pianificazione, viene suggerito un ordine di approvvigionamento di emergenza per la quantità negativa dal sistema di pianificazione che pervenga alla data di inizio pianificazione. Il testo di avviso riporta la data di inizio e la quantità dell'ordine di emergenza.

Tutte le righe di documento con data di scadenza precedente la data di inizio pianificazione sono consolidate in un unico ordine di approvvigionamento di emergenza che pervenga nella data di inizio pianificazione.

### Eccezione

L'avviso di eccezione viene visualizzato se la proiezione delle giacenze disponibili scende al di sotto della scorta di sicurezza.

Il sistema di pianificazione suggerisce un ordine di approvvigionamento per soddisfare la domanda alla data di scadenza. Il testo dell'avviso riporta la quantità di scorte di sicurezza dell'articolo e la data in cui è stata intaccata.

Intaccare il livello di scorta di sicurezza è considerata un'eccezione perché non dovrebbe verificarsi se il punto di riordino è stato impostato correttamente.

> [!NOTE]
> L'approvvigionamento nelle righe di pianificazione con avvisi di eccezione in genere non viene modificato in base ai parametri di pianificazione. Al contrario, il sistema di pianificazione suggerisce solo un approvvigionamento per coprire la quantità di domanda esatta. Tuttavia, è possibile impostare la pianificazione in modo da rispettare parametri specifici per le righe di pianificazione con determinati avvisi. Per ulteriori informazioni, vedere la descrizione del campo **Rispetta parametri di pianificazione per avvisi di eccezione** nell'articolo [Eseguire la pianificazione completa, MPS o MRP](production-how-to-run-mps-and-mrp.md).

### Attenzione

L'avviso Attenzione è visualizzato in due situazioni:

- La data di inizio pianificazione precede la data di lavoro.
- La riga di pianificazione suggerisce di cambiare un ordine di acquisto o di produzione rilasciato.

> [!NOTE]
> Nella pianificazione delle righe con avvisi, il campo **Accetta messaggio errore** non è selezionato perché si prevede che l'addetto alla pianificazione effettui ulteriori indagini su tali righe prima di eseguire il piano.

## Prospetti pianificazione e richieste di approvvigionamento

Come descritto in [Pianificazione](production-planning.md), è possibile scegliere tra due fogli di lavoro per la maggior parte delle attività di pianificazione, il prospetto pianificazione e la richiesta di approvvigionamento. La maggior parte dei processi viene descritta in base al prospetto pianificazione, ma esistono un paio di scenari in cui è preferibile la richiesta di approvvigionamento.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

### Richiesta di approvvigionamento

La pagina **Richiesta di approvvigionamento** viene elenca gli articoli da ordinare. Esistono due modi per immettere gli articoli nella richiesta:

- Immettere gli articoli manualmente nella richiesta e compilare i relativi campi.

- Utilizzare il processo batch **Calcola piano**. Calcola un piano di rifornimento per gli articoli e le unità di stockkeeping il cui sistema di rifornimento è impostato su **Acquisto** o **Trasferimento**. Quando si utilizza questo processo batch, il campo **Messaggio azione** viene compilato automaticamente con un suggerimento di azione che è possibile adottare per il rifornimento dell'articolo. Può trattarsi di aumentare la quantità dell'articolo in un ordine esistente o creare un nuovo ordine, ad esempio.

- Se è stato utilizzato il processo batch **Calcola Piano** dalla pagina **Prospetto pianificazione** per calcolare un piano di rifornimento, sarà possibile utilizzare il processo batch **Esegui messaggi di azione** per copiare le proposte di ordine di acquisto e di trasferimento dal prospetto di pianificazione alla richiesta di approvvigionamento. Ciò si rivela particolarmente utile se la responsabilità della gestione degli ordini di produzione e degli ordini di acquisto/trasferimento è affidata a utenti distinti.

- È possibile utilizzare l'azione **Spedizione diretta** per compilare le righe della richiesta di approvvigionamento. Questa funzione utilizza il processo batch **Prendi ordini vendite** per determinare le righe dell'ordine di vendita da indicare per una spedizione diretta.

- È possibile utilizzare l'azione **Ordine speciale** per compilare le righe della richiesta di approvvigionamento. Questa azione utilizza il processo batch **Prendi ordini vendite** per determinare le righe dell'ordine di vendita da indicare per un ordine speciale.

Le righe della richiesta di approvvigionamento contengono informazioni dettagliate relative agli articoli da riordinare. È possibile modificare ed eliminare le righe per rettificare il piano di rifornimento, nonché elaborare ulteriormente le righe utilizzando il processo batch **Esegui messaggi di azione**. 

Per dettagli sulla pianificazione con posizioni e trasferimenti, vedere [Pianificazione con o senza ubicazioni](production-planning-with-without-locations.md).

> [!TIP]
> Quando lavori nelle pagina **Richiesta di approvvigionamento** o **Prospetto pianificazione**, puoi organizzare le righe ordinandole in base al nome di una colonna. Ciò è particolarmente utile nella pagina Prospetto pianificazione perché può essere utilizzato per ordini di produzione multilivello. Per impostazione predefinita, le righe sono ordinate in base al campo **Nr. articolo**. Per raggruppare le righe per un ordine multilivello, ordina in base al campo **Nr. ordine rif.** . Anche i campi **Ordine MPS** e **Livello pianificazione** possono aiutare a mostrare la gerarchia delle righe.

## Vedere anche

[Dettagli di progettazione: pianificazione approvvigionamento](design-details-supply-planning.md)  
[Pianif.](production-planning.md)  
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)  
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: "Informazioni sulla funzionalità di pianificazione | Microsoft Docs"
description: Il sistema di pianificazione considera tutti i dati relativi a domande e approvvigionamento, confronta i risultati e crea suggerimenti per bilanciare l'approvvigionamento in modo da soddisfare la domanda.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a00f88aaf70464c8911d59b829b08dda900dc474
ms.contentlocale: it-it
ms.lasthandoff: 12/14/2017

---
# <a name="about-planning-functionality"></a>Informazioni sulla funzionalità di pianificazione
Il sistema di pianificazione considera tutti i dati relativi a domande e approvvigionamento, confronta i risultati e crea suggerimenti per bilanciare l'approvvigionamento in modo da soddisfare la domanda.  

Per informazioni dettagliate, vedere [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md).  

> [!NOTE]  
> Per tutti i campi citati in questo argomento, leggere la descrizione comando per comprenderne la funzione. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Domanda e approvvigionamento  
La pianificazione è costituita da due elementi, la domanda e l'approvvigionamento. Tali elementi devono essere proporzionati uno all'altro per assicurare che la domanda sia soddisfatta in modo tempestivo ed economicamente vantaggioso.  

- Domanda è il termine comune utilizzato per qualsiasi fabbisogno lordo quale un ordine di vendita, un ordine di assistenza, un componente necessario da un assemblaggio o ordine di produzione, un trasferimento in uscita, un ordine programmato o una previsione. Oltre a questi, il programma supporta altri tipi tecnici di domanda, ad esempio una produzione negativa o un ordine di acquisto, una giacenza negativa e un reso di acquisto.  
- Approvvigionamento è la parola comune utilizzata per qualsiasi tipo di rifornimento, quale magazzino, ordine di acquisto, ordine di assemblaggio, ordine di produzione o trasferimento in entrata. In modo analogo, può essere presente un ordine di vendita o di assistenza negativo oppure un componente necessario o un reso vendite negativo, che rappresentano tutti un tipo di approvvigionamento.  

Un altro obiettivo del sistema di pianificazione consiste nel garantire che il magazzino non aumenti in modo superfluo. Nel caso di un calo della domanda, verrà suggerito dal sistema di pianificazione di rimandare, ridurre in quantità o annullare gli ordini di rifornimento esistenti.  

## <a name="planning-calculation"></a>Calcolo della pianificazione  
Il sistema di pianificazione si basa sulla domanda anticipata ed effettiva da parte dei clienti, nonché sui parametri di riordino del magazzino. L'esecuzione del calcolo della pianificazione ha come risultato alcune azioni specifiche suggerite dal programma (messaggi di azione) da adottare relativamente al possibile rifornimento da fornitori, trasferimenti tra magazzini o produzione. Se sono già presenti ordini di rifornimento, le azioni suggerite possono consistere nell'aumento o nell'accelerazione di tali ordini per rispondere alle modifiche nella domanda.  

Le base della procedura di pianificazione consiste nel calcolo del fabbisogno da lordo a netto. Il fabbisogno netto determina il rilascio degli ordini pianificati, la cui programmazione si basa sulle informazioni relative al ciclo (articoli lavorati) o sul lead time della scheda articolo (articoli acquistati). Le quantità relative al rilascio degli ordini pianificati sono basate sul calcolo della pianificazione e sono influenzate dai parametri impostati nelle singole schede articolo.  

## <a name="planning-with-manual-transfer-orders"></a>Pianificazione con ordini di trasferimento manuali
Come indicato nel campo **Sistema di Rifornimento** in una scheda USK, è possibile impostare il sistema di pianificazione in modo da creare ordini di trasferimento per bilanciare l'approvvigionamento e la domanda tra le ubicazioni.  

Oltre a tali ordini di trasferimento automatici, è possibile che in alcuni casi sia necessario eseguire uno spostamento generale delle quantità di magazzino in un'altra ubicazione, indipendentemente dalla domanda esistente. A tale scopo, è necessario creare manualmente un ordine di trasferimento per la quantità da spostare. Per evitare che tale ordine di trasferimento manuale venga manipolato dal sistema di pianificazione, impostare **Flessibilità pianificazione** nelle righe di trasferimento su Nessuna.  

Se si desidera invece fare in modo che il sistema di pianificazione rettifichi le quantità e le date dell'ordine di trasferimento in base alla domanda esistente, impostare il campo **Flessibilità pianificazione** sul valore di default Illimitata.

## <a name="planning-parameters"></a>Parametri di pianificazione  
I parametri di pianificazione determinano i tempi, le quantità e le modalità di rifornimento in base alle diverse impostazioni nella scheda articolo (unità di stockkeeping, USK) e in Setup manufacturing.  

I parametri di pianificazione seguenti sono presenti nella scheda articolo o USK:  

-   Periodo di stabilizzazione  
-   Quantità di smorzamento  
-   Metodo di riordino  
-   Punto riordino
-   Giacenza massima  
-   Livello di overflow  
-   Intervallo di tempo  
-   Periodo di accumulo lotti  
-   Periodo di riprogrammazione  
-   Qtà di riordino  
-   Lead time di sicurezza  
-   Scorta di sicurezza  
-   Criteri di assemblaggio  
-   Politica di produzione  

I modificatori di ordini seguenti sono presenti nella scheda articolo o USK:  

-   Quantità minima ordine  
-   Quantità massima ordine  
-   Molteplicità ordine  

I campi di setup di pianificazione globale nella finestra **Setup manufacturing** includono:  

-   Cod. ultimo livello dinamico  
-   Previsione produzione corrente  
-   Usa previsioni per le ubicazioni  
-   Lead time di sicurezza di default  
-   Livello di overflow vuoto  
-   Calcolo combinato MPS/MRP   
-   Componenti nell'ubicazione  
-   Periodo di stabilizzazione di default  
-   Quantità di smorzamento di default  

Per ulteriori informazioni, vedere [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Altri campi di pianificazione rilevanti
### <a name="planning-flexibility"></a>Flessibilità pianificazione
Nella maggior parte degli ordini di approvvigionamento, ad esempio gli ordini di produzione, è possibile selezionare **Illimitata** o **Nessuna** nel campo **Flessibilità pianificazione** delle righe.

Ciò indica se l'approvvigionamento rappresentato dalla riga dell'ordine di produzione viene considerato dal sistema di pianificazione durante il calcolo dei messaggi d'azione.
Se nel campo è impostato il valore **Illimitata**, il sistema di pianificazione include la riga nel calcolo dei messaggi di azione. Se nel campo è impostato il valore **Nessuna**, la riga sarà fissa e non modificabile e non verrà inserita nel calcolo dei messaggi di azione.

### <a name="warning"></a>Avviso
Nel campo **Avviso** della finestra **Prospetto pianificazione** viene visualizzato un messaggio per ogni riga di pianificazione creata per una situazione insolita. L'utente può scegliere di leggere ulteriori informazioni. Sono disponibili i seguenti tipi di avviso:

- Emergenza
- Eccezione
- Attenzione
- Emergenza

L'avviso di emergenza è visualizzato in due situazioni:

- Alla data di inizio pianificazione le giacenze sono negative.
- Sono presenti eventi di approvvigionamento o domanda arretrati.

Se le giacenze di un articolo sono negative alla data di inizio pianificazione, viene suggerito un ordine di approvvigionamento di emergenza per la quantità negativa dal sistema di pianificazione che pervenga alla data di inizio pianificazione. Il testo di avviso riporta la data di inizio e la quantità dell'ordine di emergenza.

Tutte le righe di documento con data di scadenza precedente la data di inizio pianificazione sono consolidate in un unico ordine di approvvigionamento di emergenza che pervenga nella data di inizio pianificazione.

### <a name="exception"></a>Eccezione
L'avviso di eccezione viene visualizzato se la proiezione delle giacenze disponibili scende al di sotto della scorta di sicurezza.

Il sistema di pianificazione suggerisce un ordine di approvvigionamento per soddisfare la domanda alla data di scadenza. Il testo dell'avviso riporta la quantità di scorte di sicurezza dell'articolo e la data in cui è stata intaccata.

Intaccare il livello di scorta di sicurezza è considerata un'eccezione perché non dovrebbe verificarsi se il punto di riordino è stato impostato correttamente.

> [!NOTE]
> L'approvvigionamento nelle righe di pianificazione con avvisi di eccezione in genere non viene modificato in base ai parametri di pianificazione. Al contrario, il sistema di pianificazione suggerisce solo un approvvigionamento per coprire la quantità di domanda esatta. Tuttavia, è possibile impostare la pianificazione in modo da rispettare parametri specifici per le righe di pianificazione con determinati avvisi. Per ulteriori informazioni, vedere "Rispetta parametri di pianificazione per avvisi di eccezione" in Calcola piano - Pianif. magaz.

### <a name="attention"></a>Attenzione
L'avviso di attenzione è visualizzato in due situazioni:

- La data di inizio pianificazione precede la data di lavoro.
- La riga di pianificazione suggerisce di cambiare un ordine di acquisto o di produzione rilasciato.

> [!NOTE]
> Nella pianificazione delle righe con avvisi, il campo **Accetta messaggio errore** non è selezionato perché si prevede che l'addetto alla pianificazione effettui ulteriori indagini su tali righe prima di eseguire il piano.

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)  
[Pianif.](production-planning.md)   
[Impostazione della produzione](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Magazzino](inventory-manage-inventory.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Impostare le procedure ottimali: Pianificazione forniture](setup-best-practices-supply-planning.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


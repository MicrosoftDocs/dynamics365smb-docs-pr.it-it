---
title: Report e analisi delle vendite
description: Vedere quali report di vendita e analisi sono disponibili nella versione standard di Business Central in modo da poter tenere traccia della propria attività.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: a8ada1c8488e8c5dec581db98dccf02d89da21c3
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216374"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Report delle vendite e analisi in Business Central

Il report delle vendite in [!INCLUDE [prod_short](includes/prod_short.md)] consente ai professionisti delle vendite e aziendali di ottenere approfondimenti e statistiche sulle attività di vendita attuali e passate.  

## <a name="reports"></a>Report

La tabella seguente descrive alcuni dei report delle vendite chiave.

|Report |ID oggetto|Descrizione  |
|---------|---------|---------|
|**Cliente - Riepilogo ordine**|107| Viene visualizzato il dettaglio ordine con la quantità non ancora spedita per ogni cliente in tre periodi di 30 giorni ciascuno, a partire dalla data specificata. Vi sono inoltre colonne di ordini da spedire prima e dopo i tre periodi indicati e una colonna con il dettaglio ordine totale per ogni cliente. Usare il report per analizzare il volume di vendite di una compagnia. |
|**Clienti - Lista primi 10**|111| Visualizza informazioni su acquisti e saldi dei clienti per un determinato periodo. È possibile scegliere il numero di clienti da includere nel report. Vi verranno inclusi solamente i clienti con acquisti riguardanti il periodo o un saldo al suo termine.<br>I clienti sono ordinati secondo l'importo ed è possibile scegliere se ordinarli per importo vendita o saldo. Il report offre una panoramica dei clienti che acquistano di più o devono di più.|
|**Vendite cliente/articolo**|113|Mostra una lista delle vendite effettuate per ciascun cliente durante un determinato periodo di tempo. Il report contiene informazioni su quantità, importo vendita, profitto e possibili sconti. Può essere utilizzato, ad esempio, per analizzare i gruppi di clienti di una società.|
|**Magazzino - Vendita cliente**|713|Una panoramica dal punto di vista del magazzino. Questa è una visione diversa rispetto al report **Vendita cliente/oggetto** e mostra prima l'articolo e poi il cliente che ha acquistato questo prodotto.|
|**Cliente - Lista vendite**|119|Mostra le vendite clienti per un periodo. Il report viene utilizzato per la presentazione delle dichiarazioni alle autorità doganali e fiscali. È possibile scegliere di includere solo i clienti con un totale vendite che supera un importo minimo. È inoltre possibile specificare se includere nel report i dettagli relativi all'indirizzo di ogni cliente.<br>Il report si basa sulle vendite registrate (VL) dai movimenti contabili dei clienti. Nella parte inferiore del report, il totale vendite segnalato viene mostrato nella valuta locale. Il totale si basa sui clienti inclusi nel report, ovvero i clienti che rientrano nei filtri della Scheda dettaglio Cliente e che presentano un totale vendite superiore all'importo specificato nel campo **Importi superiori a (VL)** della Scheda dettaglio **Opzioni**.|
|**Cliente - Saldo alla data**|121|Visualizza un bilancio dettagliato per i clienti selezionati. Utilizzare ad esempio il report alla chiusura di un periodo contabile o di un anno fiscale.|
|**Clienti - Bilancio di verifica**|129|Visualizza un bilancio analitico per i clienti selezionati. Puoi utilizzare il report per verificare se il saldo di una categoria registrazione clienti è pari al saldo nel conto C/G corrispondente a una determinata data. Utilizzare ad esempio il report alla chiusura di un periodo contabile o di un anno fiscale. Se hai bisogno di una versione più dettagliata di questo tipo di rapporto, usa il rapporto **Bilancio di verifica dei dettagli del cliente** (104).|
|**Statistiche vendite**|112|Visualizza gli importi di vendita, margine, sconto in fattura e sconto di pagamento in valuta locale, nonché la percentuale di margine, per ogni cliente. I costi e i margini vengono indicati sia come originari che come rettificati. I costi e i margini originari sono quelli calcolati al momento della registrazione, mentre i costi e i profitti rettificati riflettono le modifiche apportate ai costi originari degli articoli nella vendita. L'importo rettifica costo visualizzato nel report rappresenta la differenza tra il costo originario e il costo rettificato.<br>Le cifre sono suddivise in tre periodi. La lunghezza del periodo può essere selezionata a partire da una data prescelta. Vi sono inoltre colonne di importi antecedenti o posteriori ai tre periodi. Ad esempio, utilizzare il report per analizzare profitti provenienti da un singolo cliente e andamenti di profitti. |
|**Disponibilità impegno vendita**|209|Visualizza la disponibilità di articoli da spedire sui documenti di vendita. Stabilire se nel report viene indicato lo stato di ciascun documento o di ciascuna riga vendita. Quando si stampa il report, la quantità disponibile per la spedizione può essere automaticamente immessa nel campo **Qtà da Spedire** delle righe vendita. Il report può quindi venire utilizzato per determinare quali documenti registrare.<br>C'è anche una capacità con cui puoi impostare la quantità di merce da spedire. **Nota** : questo report non è disponibile per la funzionalità di warehouse avanzata.|
|**Stato spedizione warehouse**|7313|Questo rapporto può essere utilizzato per tutte le località in cui è selezionato il campo **Richiedi spedizione**. Il report **Stato spedizione warehouse** Il report mostra tutti i documenti di spedizione di magazzino non registrati, incluse le ubicazioni, i codici collocazione, lo stato del documento, le quantità e così via. Questo rapporto è perfetto per avere una panoramica.|
|**Lista prelievi magazzino**|813|Visualizza una lista degli ordini vendita nei quali è incluso un determinato articolo. Per ogni articolo vengono visualizzate le seguenti informazioni: riga di ordine di vendita con il nome del cliente, codice variante, codice ubicazione, codice collocazione, data di spedizione, quantità da spedire e unità di misura. Per ciascun articolo viene calcolato il totale della quantità da spedire. Il report può essere utilizzato quando gli articoli vengono prelevati dal magazzino.<br>**Nota** : questo report non è disponibile per la funzionalità di warehouse avanzata.|
|**Ordini vendite arretrati magazzino**|718|Mostra una lista delle righe di ordine la cui data di spedizione è ormai superata. Per ogni singolo ordine vengono visualizzate le seguenti informazioni relative a ciascun articolo: numero, nome del cliente, numero di telefono del cliente, data di spedizione, quantità dell'ordine e quantità nell'ordine programmato. Vengono inoltre indicati eventuali altri articoli da spedire allo stesso cliente sulla base dell'ordine in ritardo.|



## <a name="tasks"></a>Attività

I seguenti articoli descrivono alcune delle attività chiave per analizzare lo stato del tuo business:

* [Creare report di analisi](bi-how-create-analysis-views-reports.md)  
* [Visualizzare la disponibilità di articoli](inventory-how-availability-overview.md)


## <a name="see-also"></a>Vedere anche

[Setup Vendite](sales-setup-sales.md)  
[Vendite](sales-manage-sales.md)  
[Prenotare articoli](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

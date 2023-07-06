---
title: Dettagli di progettazione - Struttura di registrazione di tracciabilità articolo
description: Informazioni su come utilizzare i movimenti contabili articoli come vettori principali dei numeri di tracciabilità articolo nella Struttura di registrazione di tracciabilità articolo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-posting-structure"></a><a name="design-details-item-tracking-posting-structure"></a><a name="design-details-item-tracking-posting-structure"></a>Dettagli di progettazione: Struttura di registrazione di tracciabilità articolo
Per conformità con la funzionalità di costing di magazzino e per ottenere una soluzione più semplice e più affidabile, i movimenti contabili articoli vengono utilizzati come principali vettori dei numeri di tracciabilità articolo.  
  
I numeri di tracciabilità articolo nelle entità di rete di ordini e nelle entità di rete diverse dagli ordini sono specificati nella tabella **Movimenti impegni** (T337). I numeri di tracciabilità articolo correlati a informazioni dello storico vengono recuperati direttamente dai movimenti contabili articoli correlati alla transazione in questione. Ciò significa che i movimenti contabili articoli riflettono la specifica di tracciabilità articolo della riga dell'ordine registrato.  
  
La pagina **Righe tracciabilità articolo** recupera le informazioni da T337 e dai movimenti contabili articoli e le mostra attraverso la tabella temporale denominata **Specifica tracciabilità** (T336). La tabella T336 contiene anche i dati temporanei nella pagina **Righe tracciabilità articolo** per le quantità di tracciabilità articolo che restano da fatturare.  
  
## <a name="one-to-many-relation"></a><a name="one-to-many-relation"></a><a name="one-to-many-relation"></a>Relazione uno-a-molti
La tabella **Relazione movimento articolo**, che viene utilizzata per collegare una riga di documento registrata con i relativi movimenti contabili articolo, è costituita da due parti principali:  
  
* Un puntatore alla riga di documento registrata, il campo **Nr. riga ordine**. .  
* Un numero di movimento che punta a un movimento contabile articolo, il campo **Nr. movimento articolo**.  
  
La funzionalità del campo **Nr. movimento**, che collega un movimento contabile articolo a una riga di documento registrato, gestisce la tipica relazione uno a uno quando non sono presenti numeri di tracciabilità articolo nella riga del documento registrato. Se sono presenti dei numeri di tracciabilità articolo, il campo **Nr. movimento** viene lasciato vuoto e la relazione uno a molti viene gestita dalla tabella **Relazione movimento articolo**. Se la riga del documento registrata contiene numeri di tracciabilità articolo ma si riferisce solo a un singolo movimento contabile articolo, il campo **Nr. movimento** gestisce la relazione e nella tabella **Relazione movimento articolo** non viene creato alcun record.  
  
## <a name="codeunits-80-and-90"></a><a name="codeunits-80-and-90"></a><a name="codeunits-80-and-90"></a>Codeunit 80 e 90
Per suddividere i movimenti contabili articoli durante la registrazione, il codice nella codeunit 80 e nella codeunit 90 è circondato di cicli che vengono eseguiti attraverso variabili di record temporanee globali. Questo codice chiama la codeunit 22 con una riga di registrazioni magazzino. Queste variabili vengono inizializzate quando sono presenti numeri di tracciabilità articolo per la riga del documento. Per mantenere il codice semplice, viene sempre utilizzata questa struttura ciclica. Se non sono presenti numeri di tracciabilità articolo per la riga del documento, verrà inserito un unico record e il ciclo verrà eseguito solo una volta.  
  
## <a name="posting-the-item-journal"></a><a name="posting-the-item-journal"></a><a name="posting-the-item-journal"></a>Contabilizzazione della registrazione magazzino
I numeri di tracciabilità articolo vengono trasferiti tramite i movimenti impegni che sono correlati al movimento contabile articolo e il loop attraverso i numeri di tracciabilità articolo si verifica nella codeunit 22. Questo concetto funziona in modo analogo sia quando una riga di registrazioni magazzino viene utilizzata indirettamente per registrare una vendita o un ordine di acquisto sia quando una riga di registrazioni magazzino viene utilizzata direttamente. Quando le registrazioni magazzino vengono utilizzate direttamente, il campo **ID riga origine** punta alla riga di registrazione magazzino stessa.  
  
## <a name="code-unit-22"></a><a name="code-unit-22"></a><a name="code-unit-22"></a>Codeunit 22
Le Codeunit 80 e 90 eseguono il ciclo della chiamata della codeunit 22 durante la registrazione della fattura dei numeri di tracciabilità articolo e durante la fatturazione delle spedizioni esistenti o dei carichi.  
  
Durante la registrazione della quantità dei numeri di tracciabilità articolo, la codeunit 22 richiama i numeri di tracciabilità articolo dai movimenti in T337 correlati alla registrazione. Questi movimenti vengono inseriti direttamente nella riga registrazioni magazzino.  
  
La Codeunit 22 esegue il ciclo tramite i numeri di tracciabilità articolo e suddivide la registrazione in rispettivi movimenti articolo collegati contabili che includono i numeri di tracciabilità articolo. Le informazioni sui movimenti contabili articoli che vengono creati vengono restituite a T337 utilizzando un record temporaneo T336, richiamato da una routine nella codeunit 22. Questa procedura viene avviata al termine dell'esecuzione della codeunit 22 perché, a quel punto, l'oggetto della codeunit 22 contiene le informazioni. Quando il record temporaneo T336 viene recuperato, le codeunit 80 e 90 creano dei record nella tabella **Relazione movimento articolo** per collegare i movimenti contabili articoli alla riga di spedizione o di carico creata. Le Codeunit 80 o la codeunit 90 converte quindi i record temporanei T336 in record effettivi T336 collegati alla riga in questione. Tuttavia, questa conversione si verifica solo se la riga del documento registrata non viene eliminata, perché è registrata solo in parte.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)   
[Dettagli di progettazione: Progettazione tracciabilità articolo](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

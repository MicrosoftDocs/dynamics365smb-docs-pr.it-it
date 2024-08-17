---
title: Dettagli di progettazione - Struttura di registrazione di tracciabilità articolo
description: Informazioni su come utilizzare i movimenti contabili articoli come vettori principali dei numeri di tracciabilità articolo nella Struttura di registrazione di tracciabilità articolo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Dettagli di progettazione: Struttura di registrazione di tracciabilità articolo
Per conformità con la funzionalità di costing di magazzino e per ottenere una soluzione più semplice e più affidabile, i movimenti contabili articoli vengono utilizzati come principali vettori dei numeri di tracciabilità articolo.  
  
I numeri di tracciabilità articolo nelle entità di rete di ordini e nelle entità di rete diverse dagli ordini sono specificati nella tabella **Movimenti impegni** (T337). I numeri di tracciabilità articolo correlati a informazioni dello storico vengono recuperati direttamente dai movimenti contabili articoli correlati alla transazione in questione. Ciò significa che i movimenti contabili articoli riflettono la specifica di tracciabilità articolo della riga dell'ordine registrato.  
  
La pagina **Righe tracciabilità articolo** recupera le informazioni da T337 e dai movimenti contabili articoli e le mostra attraverso la tabella temporale denominata **Specifica tracciabilità** (T336). La tabella T336 contiene anche i dati temporanei nella pagina **Righe tracciabilità articolo** per le quantità di tracciabilità articolo che restano da fatturare.  
  
## <a name="one-to-many-relation"></a>Relazione uno-a-molti
La tabella **Relazione movimento articolo**, che viene utilizzata per collegare una riga di documento registrata con i relativi movimenti contabili articolo, è costituita da due parti principali:  
  
* Un puntatore alla riga di documento registrata, il campo **Nr. riga ordine**. .  
* Un numero di movimento che punta a un movimento contabile articolo, il campo **Nr. movimento articolo**.  
  
La funzionalità del campo **Nr. movimento**, che collega un movimento contabile articolo a una riga di documento registrato, gestisce la tipica relazione uno a uno quando non sono presenti numeri di tracciabilità articolo nella riga del documento registrato. Se sono presenti dei numeri di tracciabilità articolo, il campo **Nr. movimento** viene lasciato vuoto e la relazione uno a molti viene gestita dalla tabella **Relazione movimento articolo**. Se la riga del documento registrata contiene numeri di tracciabilità articolo ma si riferisce solo a un singolo movimento contabile articolo, il campo **Nr. movimento** gestisce la relazione e nella tabella **Relazione movimento articolo** non viene creato alcun record.  
  
## <a name="codeunits-80-sales-post--and-90-purch-post"></a>Codeunits 80 (Vendita-Posta) e 90 (Acquisto-Posta)
Per suddividere i movimenti contabili articoli durante la registrazione, il codice nella codeunit 80 e nella codeunit 90 è circondato di cicli che vengono eseguiti attraverso variabili di record temporanee globali. Questo codice chiama la codeunit 22 con una riga di registrazioni magazzino. Queste variabili vengono inizializzate quando sono presenti numeri di tracciabilità articolo per la riga del documento. Per mantenere il codice semplice, viene sempre utilizzata questa struttura ciclica. Se non sono presenti numeri di tracciabilità articolo per la riga del documento, verrà inserito un unico record e il ciclo verrà eseguito solo una volta.  
  
## <a name="posting-the-item-journal"></a>Contabilizzazione della registrazione magazzino
I numeri di tracciamento degli articoli vengono trasferiti tramite le voci di prenotazione relative alla voce del registro articoli e il passaggio attraverso i numeri di tracciamento degli articoli avviene nell'unità di codice 22 (Riga di registrazione articoli-post). Questo concetto funziona in modo analogo sia quando una riga di registrazioni magazzino viene utilizzata indirettamente per registrare una vendita o un ordine di acquisto sia quando una riga di registrazioni magazzino viene utilizzata direttamente. Quando le registrazioni magazzino vengono utilizzate direttamente, il campo **ID riga origine** punta alla riga di registrazione magazzino stessa.  
  
## <a name="code-unit-22--item-jnl-post-line"></a>Codice Unità 22 (Articolo Jnl.-Post Line)
Le unità di codice 80 (Vendite-Posta) e 90 (Acquisto-Posta) eseguono il richiamo dell'unità di codice 22 (Riga articolo Jnl.-Posta) durante la registrazione della fattura dei numeri di tracciamento degli articoli e durante la fatturazione di spedizioni o ricevute esistenti.  
  
Durante la registrazione della quantità dei numeri di tracciabilità degli articoli, l'unità di codice 22 (Riga di registrazione degli articoli) recupera i numeri di tracciabilità degli articoli dalle voci in T337 (Voce di prenotazione) relative alla registrazione. Questi movimenti vengono inseriti direttamente nella riga registrazioni magazzino.  
  
Il codice unità 22 (articolo Jnl.-riga di registrazione) scorre i numeri di tracciabilità degli articoli e suddivide la registrazione nelle rispettive voci del registro articoli che riportano i numeri di tracciabilità degli articoli. Le informazioni sulle voci del registro articoli create vengono restituite a T337 (voce di prenotazione) utilizzando un record T336 temporaneo, che viene richiamato da una procedura nell'unità di codice 22. Questa procedura viene avviata al termine dell'esecuzione della codeunit 22 perché, a quel punto, l'oggetto della codeunit 22 contiene le informazioni. Quando viene recuperato il record temporaneo T336, le Codeunit 80 (Vendite-Registrazione) e 90 (Acquisto-Registrazione) creano record nella tabella  **Relazione immissione articolo** per collegare le voci contabili dell'articolo create nella riga di spedizione o ricezione creata. Le codeunit 80 (Sales-Post) e 90 (Purch-Post) convertono quindi i record temporanei T336 (Tracking Specification) in record T336 (Tracking Specification) reali correlati alla riga in questione. Tuttavia, questa conversione si verifica solo se la riga del documento registrata non viene eliminata, perché è registrata solo in parte.  
  
## <a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Tracciabilità articolo](design-details-item-tracking.md)   
[Dettagli di progettazione: Progettazione tracciabilità articolo](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

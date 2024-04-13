---
title: Mappare documenti elettronici a righe di ordini di acquisto con Copilot
description: Scopri come utilizzare Copilot per mappare documenti elettronici a righe di ordini di acquisto.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 02/23/2024
ms.custom: bap-template
---

# Mappare documenti elettronici per acquistare righe di ordini di acquisto con Copilot (anteprima)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Man mano che i processi di approvvigionamento diventano più digitali, la funzionalità dei documenti elettronici in Business Central svolge un ruolo chiave nell'automazione della ricezione e dell'elaborazione delle fatture fornitore. Copilot può assistere in questo processo migliorando il mapping e la corrispondenza delle fatture fornitore a ordini di acquisto. Ciò riduce le attività dispendiose in termini di tempo che normalmente includerebbero ricerche approfondite, ricerche e immissione di dati. Il vantaggio è dato dal fatto che le fatture fornitore spesso non si riferiscono esattamente agli ordini d'acquisto, nel qual caso Copilot è in una posizione migliore per identificare gli ordini d'acquisto corrispondenti. Le funzionalità di corrispondenza migliorate avvantaggiano in particolare le organizzazioni di piccole e medie dimensioni che necessitano di un tracciamento efficiente dei documenti per le righe di ordini di acquisto. Copilot è l'assistente per il lavoro basato sull'intelligenza artificiale che stimola la creatività e migliora la produttività per gli utenti di Business Central.

> [!IMPORTANT]
> - Questa è una funzionalità di Anteprima pronta per la produzione per ambienti di produzione e sandbox in qualsiasi localizzazione, ad eccezione del Canada.
> - Le anteprime pronte per la produzione sono soggette a condizioni per l'utilizzo supplementari. Ulteriori informazioni: [Condizioni di utilizzo supplementari per l'anteprima di Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - I contenuti generati dall'intelligenza artificiale potrebbero non essere corretti.

Nella versione iniziale dell'app **Documento elettronico**, abbiamo introdotto scenari fondamentali per documenti elettronici per l'intero processo di vendita. Tuttavia, sono necessari miglioramenti e automazione nella gestione dei documenti ricevuti, soprattutto nel contesto dei processi di acquisto. Copilot perfeziona il modo in cui gestisci i documenti elettronici nel processo di acquisto, in particolare per quanto riguarda gli ordini di acquisto. Il framework dei documenti elettronici ti consente di specificare il tipo di documento di acquisto da creare per ciascun fornitore quando ricevi fatture elettroniche da loro. In precedenza, l'unica opzione era creare una fattura di acquisto, come documento o registrazione COGE.

Ora puoi aggiornare un ordine di acquisto esistente in Business Central con le informazioni ricevute nella fattura elettronica.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->


## Identificare ordini di acquisto

Innanzitutto, puoi identificare gli ordini di acquisto per i quali puoi trovare automaticamente una corrispondenza.

## Mappare le righe

Copilot ti aiuta a trovare automaticamente una corrispondenza tra le righe della fattura elettronica e le righe di ordine di acquisto e offre informazioni aggiuntive sulla corrispondenza per migliorare le corrispondenze.

Una volta trovata la corrispondenza ed eseguito il mapping, Business Central aggiorna l'ordine di acquisto corrispondente con le informazioni sul carico pertinenti per garantire che nelle righe di ordine vengano ricevute le quantità corrette.

## Vedere anche

[Panoramica dei documenti elettronici](finance-edocuments-overview.md)  
[Utilizzare documenti elettronici nelle vendite e negli acquisti](finance-how-use-edocuments.md)  
[Risoluzione dei problemi relativi alle funzionalità di Copilot e IA](ai-copilot-troubleshooting.md)  
[Domande frequenti sull'intelligenza artificiale responsabile per l'assistenza per la riconciliazione dei conti correnti bancari](faqs-bank-reconciliation.md)  

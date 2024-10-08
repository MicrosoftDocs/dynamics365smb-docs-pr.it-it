---
title: Suggerire righe di vendita con Copilot
description: Scopri come suggerire righe in ordini vendita con Copilot.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# <a name="suggest-lines-on-sales-documents-with-copilot-preview"></a>Suggerire righe in documenti di vendita con Copilot (anteprima)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

In questo articolo viene descritto come creare documenti di vendita più velocemente consentendo a Copilot di suggerire gli articoli da aggiungere alle righe dei documenti di vendita per i clienti.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-sales-line-suggestions-with-copilot"></a>Informazioni sui suggerimenti per le righe di vendita con Copilot

I suggerimenti per righe di vendita con Copilot possono aiutare a creare righe in documenti di vendita come offerte di vendita, ordini e fatture basate su input strutturati o linguaggio naturale. La funzionalità non è una chat generica, ma un'esperienza altamente specifica e integrata che puoi utilizzare nei documenti di vendita. La funzionalità offre due capacità distinte che ti aiutano a trovare dati su singoli prodotti o interi documenti.

* Trovare prodotti

  Le informazioni che descrivono i prodotti sono archiviate in più aree in [!INCLUDE [prod_short](includes/prod_short.md)]. Ad esempio, i numeri e le descrizioni degli articoli sono memorizzati nella tabella **Articolo**, più codici a barre sono memorizzati nella tabella **Riferimento articolo** e le proprietà del prodotto sono archiviate nella tabella **Attributi articolo**. Sebbene sia possibile immettere *Bicicletta rossa*, il prodotto effettivo potrebbe essere *Tourer cremisi*, dove *Bicicletta* è una categoria di prodotto e *rosso* è un attributo.

* Trovare documenti per riferimento

  Gli utenti spesso ripetono un ordine precedente o almeno lo usano come punto di partenza. Ma potrebbe essere complicato trovare l'ordine appropriato in una pila di ordini. Potresti ricordare parte dell'ID dell'ordine, che può essere un numero assegnato dalla società o un numero di riferimento ricevuto da un cliente. La possibilità di utilizzare prompt come *Ho bisogno dell'ultima fattura di aprile* dovrebbe aiutarti a trovare un ordine più velocemente.

## <a name="available-languages"></a>Lingue disponibili

[!INCLUDE[sales-lines-suggestions-language-support](includes/sales-lines-suggestions-language-support.md)]

## <a name="prerequisites"></a>Prerequisiti

* Il suggerimento per le righe di vendita con Copilot è abilitato e attivato da un amministratore. Per ulteriori informazioni su come abilitare le funzionalità di IA, vedi [Configurare le funzionalità di Copilot e IA](enable-ai.md).
* Hai familiarità con la creazione di ordini di vendita.

## <a name="examples-of-prompts"></a>Esempi di prompt

I suggerimenti per le righe di vendita con Copilot sono in grado di gestire un'ampia varietà di input di prompt. Questa sezione offre alcuni esempi di prompt per vari scenari che abbiamo testato.

### <a name="sample-inquiry-to-repeat-the-past-document"></a>Richiesta di esempio per ripetere il documento precedente

Prompt: *Sono necessari tutti i prodotti della fattura 103031*

### <a name="during-phone-call-user-quickly-types-list-of-required-products-and-quantities-not-always-accurate-enough-or-using-internal-product-names"></a>Durante la telefonata l'utente digita rapidamente l'elenco dei prodotti e delle quantità necessari, che non sempre è sufficientemente accurato o utilizza nomi di prodotto interni

Prompt: *2 biiciclette rosse per bambini*

Tieni presente che il prompt funziona, anche con più errori di battitura.

### <a name="a-user-copies-an-inquiry-from-an-inbound-communication-and-pastes-it-to-the-sales-lines-suggestions-page"></a>Un utente copia una richiesta da una comunicazione in entrata e la incolla nella pagina Suggerimenti righe vendita

Prompt: *Salve, sono interessato all'acquisto di alcuni accessori per il mio laptop XXXX, ad esempio un mouse wireless, una cover per tastiera e una borsa per laptop. Mi chiedo se avete consigli o suggerimenti per questi articoli. Avete qualche offerta speciale o sconto per clienti fedeli come me? Cordiali saluti, M*

Tieni presente che laptop XXXX non è incluso nella ricerca.

## <a name="suggest-lines-on-a-sales-document"></a>Suggerire righe in un documento di vendita

Questo processo descrive come suggerire righe in un ordine di vendita. I passaggi sono uguali per le offerte di vendita e le fatture.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Ordine vendita**, quindi seleziona il collegamento correlato.
1. Aprire l'ordine di vendita.
1. Nella Scheda dettaglio **Righe** scegli l'azione **Ottieni suggerimento per righe**.
1. Nella finestra **Suggerisci righe con Copilot**, inserisci il prompt o selezionane uno dalle guide rapide.

## <a name="review-save-discard-or-regenerate-suggestions"></a>Esaminare, salvare, eliminare o rigenerare suggerimenti

Dopo che Copilot ha suggerito gli articoli da aggiungere alle righe, esaminane i suggerimenti e decidi se sono ciò che vuoi:

* Per eliminare una singola riga proposta, selezionala nell'elenco, quindi scegli l'azione **Elimina riga**.
* Per rimuovere tutte le righe proposte e chiudere la finestra Copilot, scegli il pulsante Rimuovi (cestino) accanto al pulsante **Mantieni**.
* Per trasferire le righe mostrate nella finestra Copilot, scegli **Mantieni**. 

È presente un campo **Affidabilità** che visualizza i punteggi **Alta (80+)**, **Media ( 60-80)** e **Bassa (60-)** e ti indirizza alle righe che richiedono attenzione.

Questo passaggio conferma che intendi trasferire le righe a un documento di vendita. Anche qui puoi eliminare o modificare le righe trasferite oppure eliminare l'intero documento.

## <a name="see-also"></a>Vedere anche

[Domande frequenti sui suggerimenti per le righe di vendita con Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Configurare le funzionalità di Copilot e IA](enable-ai.md)

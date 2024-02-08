---
title: DOMANDE FREQUENTI per dettagli tecnici
description: Dettagli di implementazione relativi al connetore Shopify.
ms.date: 01/24/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# DOMANDE FREQUENTI per dettagli tecnici

Questo articolo risponde alle domande frequenti relative al connettore Shopify.

## Che cos'è Shopify?

Shopify è un'applicazione basata su abbonamento che consente a chiunque di creare un negozio online e vendere i propri prodotti. La piattaforma Shopify offre ai rivenditori online una suite di servizi di pagamento, marketing, spedizione e coinvolgimento dei clienti.

## Cos'è il connettore Microsoft Dynamics 365 Business Central Shopify?

Con il connettore Shopify, le aziende possono connettere il loro negozio (o negozi) Shopify con [!INCLUDE[prod_short](../includes/prod_short.md)] per massimizzare la produttività dell'azienda. Con il connettore Shopify possono accedere e gestire le informazioni dettagliate dall'attività e dal negozio online Shopify come un'unica unità.

### Funzionalità

- Supporto per più di un punto vendita Shopify
  - Ogni negozio ha la propria configurazione, inclusa una raccolta dei prodotti e delle ubicazioni utilizzati per calcolare l'inventario e listini prezzi.  
- Sincronizzazione bidirezionale di articoli o prodotti
  - Il connettore sincronizza immagini, varianti articolo, codici a barre, numeri articolo fornitore, testi estesi e tag.  
  - Esoirta gli attributi articolo in Shopify.  
  - Utilizza gruppi di prezzi cliente e sconti selezionati per definire i prezzi esportati in Shopify.  
  - Decidi se gli articoli possono essere creati automaticamente o consenti solo gli aggiornamenti ai prodotti esistenti.  
- Sincronizzazione dei livelli di inventario
  - Scegli alcune o tutte le posizioni disponibili in [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Aggiorna i livelli di inventario in più posizioni in Shopify.  
- Sincronizzazione bidirezionale dei clienti
  - Mapping intelligente dei clienti per telefono ed e-mail.  
  - Utilizza modelli specifici per paese/aree geografiche durante la creazione dei clienti, il che aiuta a garantire che le impostazioni fiscali siano corrette.  
- Importare gli ordini da Shopify
  - Includi gli ordini creati in vari canali di vendita, ad esempio punto vendita online o **POS Shopify**.
  - Costi di spedizione, buoni regalo, mance, metodi di spedizione e pagamento, transazioni e rischio di frode.  
  - Durante l'importazione, puoi creare automaticamente clienti in [!INCLUDE [prod_short](../includes/prod_short.md)] o decidere di gestire i clienti in Shopify.  
  - Ricevi informazioni sul pagamento da Shopify Payments.
- Tracciabilità delle informazioni di evasione
  - Facoltativamente, scegli di trasferire le informazioni di tracciabilità dell'articolo da [!INCLUDE [prod_short](../includes/prod_short.md)] a Shopify.  

## Perché Microsoft e Shopify formano questa partnership?

[!INCLUDE[prod_short](../includes/prod_long.md)] sta collaborando con Shopify per aiutare i nostri clienti a creare una migliore esperienza di acquisto. Mentre Shopify fornisce ai commercianti una soluzione commerciale facile da usare, [!INCLUDE[prod_short](../includes/prod_short.md)] offre una soluzione di gestione aziendale completa per collegare i team dedicati a finanza, vendita, assistenza e operazioni. La perfetta connessione tra le applicazioni sincronizza ordini, scorte e informazioni sui clienti per garantire che possano evadere gli ordini più velocemente e servire meglio i clienti.

## Per quali prodotti Microsoft è disponibile il connettore Shopify?

Questa funzione è disponibile solo per [!INCLUDE[prod_short](../includes/prod_short.md)] online, a partire dalla versione 20.1. Non è disponibile nelle distribuzioni locali. Il connettore è preinstallato per i nuovi ambienti. Le organizzazioni con ambienti esistenti possono scaricare e installare il connettore da AppSource. L'organizzazione deve disporre sia di una licenza [!INCLUDE [prod_short](../includes/prod_short.md)] che di una licenza Shopify per usare il connettore. Per ulteriori informazioni sui paesi/aree geografiche, le lingue e le edizioni supportati di [!INCLUDE[prod_short](../includes/prod_short.md)], vedi [Connettore Shopify in AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Il connettore Shopify non funziona per l'[app Embed](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), dove l'URL del client ha il formato `https://[application name].bc.dynamics.com`.

## Quale supporto viene offerto per il connettore Shopify?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

I connettore Shopify è coperto dall'attuale modello di supporto. Per ulteriori informazioni, vedi [Supporto tecnico](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (solo in inglese).

Fatti aiutare da un consulente che conosce il connettore Shopify per [!INCLUDE[prod_short](../includes/prod_short.md)], per soddisfare i tuoi specifici requisiti aziendali. Cerca in [Servizi di consulenza](https://aka.ms/BCShopifyConsultant).

### Shopify

Ottieni aiuto con Shopify con il [Centro assistenza Generale Shopify](https://help.shopify.com/) o [Assistenza 24 ore su 24, 7 giorni su 7 per il tuo negozio come commerciante Shopify](https://help.shopify.com/questions#/).

Puoi anche visitare il [Marketplace degli esperti](https://experts.shopify.com/) per trovare gli specialisti adatti che offrono servizi ai commercianti Shopify.

## Funzionalità attualmente non supportate, tuttavia, le stiamo monitorando e potremmo considerare di aggiungerle

- Funzionalità B2B, tra cui aziende, listini prezzi aziendali e condizioni di pagamento
  - Il supporto esteso di B2B sarà disponibile nel primo ciclo di rilascio del 2024. Per ulteriori informazioni, vedi [Collegare Business Central a Shopify B2B](/dynamics365/release-plan/2023wave2/smb/dynamics365-business-central/connect-business-central-shopify-b2b)
- Mercati
  - Traduzioni multiple di dati master. Puoi scegliere una lingua che verrà utilizzata per l'esportazione delle informazioni sul prodotto.
  - Prezzi per paese/regione. È disponibile un listino prezzi per la valuta selezionata. Shopify gestisce la conversione in altre valute.
- Bozze di ordini

## Il connettore Shopify è estendibile?

Sì, il connettore Shopify è estendibile. Controlla GitHub per accedere all'[elenco dei punti di estendibilità](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) ed esplora alcuni [esempi](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md).

## Il connettore Shopify è aperto al contributo

Sì, questa estensione è aperta al contributo della nostra community. Puoi trovare il [codice sorgente](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) nel repository dei componenti aggiuntivi dell'applicazione Microsoft AL.

## Costruisci la tua versione del connettore Shopify

Secondo Shopify, se desideri creare e pubblicare un'app connettore sul marketplace Shopify che abbia lo scopo principale di trasferire o condividere i dati del commerciante a terzi ([!INCLUDE [prod_short](../includes/prod_short.md)]), è necessario avere il consenso scritto di Shopify. Nell'ambito di questo processo, è necessario ottenere il consenso di Microsoft nel "Modulo di riconoscimento dei dati del destinatario finale". Dobbiamo chiederti di gestire la questione con Shopify perché Microsoft non può firmare accordi con terze parti.

### Cosa fare

Controlla i requisiti Shopify perché potresti comunque essere in grado di avere un'app non elencata.

In alternativa, il connettore Shopify per [!INCLUDE [prod_short](../includes/prod_short.md)] ottiene costantemente nuove funzionalità e nuovi clienti. Se scopri una lacuna specifica, valuta la possibilità di inviare un suggerimento sul prodotto (https://aka.ms/bcideas) o un contributo in codice a [!INCLUDE [prod_short](../includes/prod_short.md)]. Per i requisiti che potrebbero non essere rilevanti per la maggior parte dei clienti e che non possono essere facilmente risolti dall'attuale modello di estensibilità, contatta il  [!INCLUDE [prod_short](../includes/prod_short.md)] team di sviluppo per discutere il caso d'uso. Dovremmo essere in grado di trovare una soluzione fattibile.

## Vedi anche

[Iniziare a usare il connettore per Shopify](get-started.md)  

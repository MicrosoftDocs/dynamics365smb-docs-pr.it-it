---
title: DOMANDE FREQUENTI per dettagli tecnici
description: Dettagli di implementazione relativi al connetore Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# DOMANDE FREQUENTI per dettagli tecnici

Questo articolo risponde alle domande frequenti relative al connettore Shopify.

## Che cos'è Shopify? 

Shopify è un software basato su abbonamento che consente a chiunque di creare un negozio online e vendere i propri prodotti. La piattaforma Shopify offre ai rivenditori online una suite di servizi tra cui strumenti di pagamento, marketing, spedizione e coinvolgimento dei clienti. 

## Cos'è il connettore Microsoft Dynamics 365 Business Central Shopify? 

Con il connettore Shopify, le aziende possono connettere il loro negozio (o negozi) Shopify con [!INCLUDE[prod_short](../includes/prod_short.md)] per massimizzare la produttività dell'azienda. Con il connettore Shopify possono gestire e visualizzare le informazioni dettagliate dall'attività e dal negozio online Shopify come un'unica unità. 

### Funzionalità

- Supporto per più di un punto vendita Shopify
  - Ogni negozio ha la propria configurazione, inclusa una raccolta di prodotti, posizioni utilizzate per calcolare l'inventario e listini prezzi.  
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
  - Utilizza modelli specifici per paese durante la creazione dei clienti, il che aiuta a garantire che le impostazioni fiscali siano corrette.  
- Importare gli ordini da Shopify
  - Includi gli ordini creati in vari canali di vendita, ad esempio punto vendita online o **POS Shopify**. 
  - Costi di spedizione, buoni regalo, mance, metodi di spedizione e pagamento, transazioni e rischio di frode.  
  - Durante l'importazione, puoi creare automaticamente clienti in [!INCLUDE [prod_short](../includes/prod_short.md)] o decidere di gestire i clienti in Shopify.  
  - Ricevi informazioni sul pagamento da Shopify Payments. 
- Tracciabilità delle informazioni di evasione
  - Facoltativamente, scegli di trasferire le informazioni di tracciabilità dell'articolo da [!INCLUDE [prod_short](../includes/prod_short.md)] a Shopify.  

## Perché Microsoft e Shopify formano questa partnership? 

[!INCLUDE[prod_short](../includes/prod_long.md)] sta collaborando con Shopify per aiutare i nostri clienti a creare una migliore esperienza di acquisto. Mentre Shopify fornisce ai commercianti una soluzione commerciale facile da usare, [!INCLUDE[prod_short](../includes/prod_short.md)] offre una soluzione di gestione aziendale completa per collegare i team dedicati a finanza, vendita, assistenza e operazioni in un'unica applicazione di facile utilizzo. La perfetta connessione tra i due sistemi sincronizza ordini, scorte e informazioni sui clienti per garantire che i commercianti possano evadere gli ordini più velocemente e servire meglio i clienti.

## Per quali prodotti Microsoft è disponibile il connettore Shopify?

Questa funzione è disponibile solo per [!INCLUDE[prod_short](../includes/prod_short.md)] online, a partire dalla versione 20.1. Non è disponibile nelle distribuzioni locali. L'app con il connettore è preinstallata per i nuovi ambienti. Le organizzazioni con ambienti esistenti possono scaricare e installare l'app da AppSource. L'organizzazione deve disporre sia di una licenza Business Central che di una licenza Shopify per usare il connettore. Per ulteriori informazioni sui paesi, le lingue e le edizioni supportati di [!INCLUDE[prod_short](../includes/prod_short.md)], vedi [Connettore Shopify in AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Il connettore Shopify non funziona per l'[app Embed](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), dove l'URL del client ha il formato: `https://[application name].bc.dynamics.com`. 

## Quale supporto viene offerto per il connettore Shopify?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

I connettore Shopify è coperto dall'attuale modello di supporto. Per ulteriori informazioni, vedi [Supporto tecnico](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (solo in inglese). 

Fatti aiutare da un consulente che conosce il connettore Shopify per [!INCLUDE[prod_short](../includes/prod_short.md)], per soddisfare i tuoi specifici requisiti aziendali.
 
Cerca in [Servizi di consulenza](https://aka.ms/BCShopifyConsultant).

### Shopify

Per ottenere aiuto con Shopify, inizia con [Centro assistenza Generale Shopify](https://help.shopify.com/) o [Assistenza 24 ore su 24, 7 giorni su 7 per il tuo negozio come commerciante Shopify](https://help.shopify.com/questions#/). 

Puoi anche visitare il [Marketplace degli esperti](https://experts.shopify.com/) per trovare gli specialisti adatti che offrono servizi ai commercianti Shopify.

## Funzionalità attualmente non supportate, tuttavia, le stiamo monitorando e potremmo considerare di aggiungerle in futuro:

- Funzionalità B2B, tra cui Aziende, listini prezzi aziendali, condizioni di pagamento
- Mercati
  - Traduzioni multiple di dati master. Puoi scegliere una lingua che verrà utilizzata per l'esportazione delle informazioni sul prodotto.
  - Prezzi per paese/regione. È disponibile un listino prezzi per la valuta selezionata. La conversione in altre valute sarà gestita da Shopify.

## Il connettore Shopify è estendibile?

Attualmente, questa app non è estensibile con piani per renderla estensibile nel 2023. 

## Il connettore Shopify è aperto al contributo

Sì, questa estensione è aperta al contributo della community. Puoi trovare il [codice sorgente](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) nel repository dei componenti aggiuntivi dell'applicazione Microsoft AL.


## Vedi anche

[Iniziare a usare il connettore per Shopify](get-started.md)  

---
title: Creazione e impostazione di un account Shopify
description: Scopri come ottenere un account Shopify in modo da poter dimostrare il flusso di lavoro per l'integrazione tra Shopify e Business Central.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Creazione e impostazione di un account Shopify

Se stai valutando se usare Shopify come soluzione di e-commerce e hai bisogno di un account Shopify per convalidare il flusso di lavoro integrato, hai le seguenti opzioni:

- Ottenere una versione di valutazione. Questo è il tipico punto di partenza per gli utenti finali.  
- Creare punti vendita di sviluppo. Questo approccio è per i partner che effettuano dimostrazioni ricorrenti, corsi di formazione e forniscono supporto.

## Valutazione (utente finale)

Vai al [sito Web Shopify](https://www.shopify.com) e utilizza il tuo account e-mail per l'account amministratore per registrarti per una versione di valutazione gratuita. Ulteriori informazioni su come creare e personalizzare il tuo punto vendita online in [Centro assistenza Shopify](https://help.shopify.com/).

In **Amministrazione Shopify** del punto vendita creato, applica le seguenti **Impostazioni**:

- Disattiva **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni [**Checkout**](https://www.shopify.com/admin/settings/checkout) nel tuo **Amministratore Shopify**.
- Prendi in considerazione l'abilitazione di *Mostra collegamento di accesso in punto vendita e alla cassa* nella sezione **Impostazioni account cliente** delle impostazioni di pagamento.
- Prendi in considerazione la possibilità di selezionare l'opzione *Nome azienda - Facoltativo* nella sezione **Informazioni cliente** delle impostazioni di pagamento.
- Abilita l'opzione **Mostra le opzioni per le mance al pagamento** nella sezione **Mance** delle impostazioni di pagamento, se hai intenzione di lasciare la mancia.
- Attiva i pagamenti di prova. Hai due opzioni. Inizia andando alle impostazioni dei [**pagamenti**](https://www.shopify.com/admin/settings/payments):  
  1. *(per test) Bogus Gateway*. Per ulteriori informazioni, vai ad [Attivare Bogus Gateway per il test](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* in modalità di test. Per ulteriori informazioni, vedi [Test Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Seleziona un piano nelle impostazioni del [**piano**](https://www.shopify.com/admin/settings/plan) per poter testare la procedura di pagamento.

> [!Important]  
> Per evitare pagamenti, ricorda di annullare la tua versione di valutazione di Shopify.

## Punto vendita per lo sviluppo

Inizia aderendo al [Programma per partner Shopify](https://help.shopify.com/partners/about). Successivamente, utilizza la **Dashboard partner** per creare il punto vendita per lo sviluppo. Per ulteriori informazioni, vedi [Creazione di punti vendita per lo sviluppo](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Dopo aver creato il punto vendita, in **Amministrazione Shopify** del punto vendita creato, applica le seguenti **Impostazioni**:

- Disattiva **Archivia automaticamente l'ordine** nella sezione **Elaborazione dell'ordine** delle impostazioni [**Checkout**](https://www.shopify.com/admin/settings/checkout) nel tuo **Amministratore Shopify**.
- Prendi in considerazione l'abilitazione di *Mostra collegamento di accesso in punto vendita e alla cassa* nella sezione **Impostazioni account cliente** delle impostazioni di pagamento.
- Prendi in considerazione la possibilità di selezionare l'opzione *Nome azienda - Facoltativo* nella sezione **Informazioni cliente** delle impostazioni di pagamento.
- Abilita l'opzione **Mostra le opzioni per le mance al pagamento** nella sezione **Mance** delle impostazioni di pagamento, se hai intenzione di lasciare la mancia.
- Attiva i pagamenti di prova. Hai due opzioni. Inizia andando alle impostazioni dei [**pagamenti**](https://www.shopify.com/admin/settings/payments):  
  1. *(per test) Bogus Gateway*. Per ulteriori informazioni, vai ad [Attivare Bogus Gateway per il test](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* in modalità di test. Ulteriori informazioni in [Test di Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> I punti vendita di sviluppo sono generalmente protetti da password. Quando provi ad aprire una pagina specifica nel tuo punto vendita online da [!INCLUDE [prod_short](../includes/prod_short.md)], ad esempio per accedere a un prodotto o un ordine specifico, dovrai inserire la tua password. Durante il test, per evitare di dover inserire la password, accedi all'amministrazione di Shopify e apri il tuo puntno vendita da lì. Non sarà necessario inserire la password del negozio fino a quando non si chiude il browser o la sessione scade.  

## Vedi anche

[Iniziare a usare il connettore Shopify](get-started.md)  
[Procedura dettagliata: Impostazione e utilizzo di un connettore Shopify](walkthrough-setting-up-and-using-shopify.md)

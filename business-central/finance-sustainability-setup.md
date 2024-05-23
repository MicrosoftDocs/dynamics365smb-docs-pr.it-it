---
title: Setup sostenibilità
description: Scopri come impostare funzionalità di sostenibilità.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Setup sostenibilità

Prima che il modulo Sostenibilità possa funzionare correttamente, devi impostare alcuni controlli di base e seguire istruzioni di base che sono correlati all'intera funzionalità.

Per impostare un modulo Sostenibilità, segui questi passaggi:

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), e immetti **Setup sostenibilità**, quindi seleziona il collegamento correlato.
2. Nella Scheda dettaglio **Generale**, configura i campi obbligatori che sono correlati al modulo Sostenibilità.

    | Campo | Descrizione |
    |-------|-------------|
    | **Codice unità di misura emissioni** | Specifica il codice dell'unità di misura utilizzato per registrare le emissioni. |
    | **Posizioni decimali emissioni** | Specifica il numero di posizioni decimali che vengono mostrate per gli importi delle emissioni. L'impostazione predefinita, *2:5*, indica che per tutti gli importi vengono mostrati un minimo di due posizioni decimali e un massimo di cinque posizioni decimali. Puoi anche immettere un numero fisso. Ad esempio, se immetti *2*, per tutti gli importi vengono mostrate due posizioni decimali. |
    | **Paese/area geografica obbligatorio** | Specifica se è obbligatorio indicare il paese o l'area geografica. Gli utenti possono impostare il campo Paese/area geografica nei giornali di registrazione anche se non selezioni questo campo. Tuttavia, se lo selezioni, gli utenti dovranno impostare il campo Paese/area geografica prima della registrazione. |
    | **Centro di responsabilità obbligatorio** | Specifica se è obbligatorio indicare il centro di responsabilità. Il centro di responsabilità può essere utilizzato come struttura, cosicché si possa misurare le emissioni basate sulla struttura. Gli utenti possono impostare il campo Centro di responsabilità nei giornali di registrazione anche se non selezioni questo campo. Tuttavia, se lo selezioni, gli utenti dovranno impostare il campo Centro di responsabilità prima della registrazione. |
    | **Modifica della base di calcolo dei blocchi se esistono movimenti contabili** | Specifica se le modifiche alla base di calcolo (formula) a livello di categoria di conto sono bloccate o meno al momento dell'immissione del movimento di sostenibilità, quando la formula è già stata applicata. |
    | **Abilita verifica errori in background** | Specifica se la verifica degli errori in background delle righe di registrazione della sostenibilità è abilitata o meno. |

    > [!NOTE]
    > Dopo che abiliti o disattivi la verifica degli errori in background nelle registrazioni, devi accedere di nuovo prima di avviare la nuova impostazione.

3. Nella Scheda dettaglio **Calcoli**, configura i campi obbligatori che sono correlati alle formule utilizzate per calcolare le emissioni.

    | Campo | Descrizione |
    |-------|-------------|
    | **Posizioni decimali combustibile/elettricità** | Specifica il numero di posizioni decimali che vengono mostrate per gli importi di combustibile/elettricità. L'impostazione predefinita, *2:5*, indica che per tutti gli importi vengono mostrati un minimo di due posizioni decimali e un massimo di cinque posizioni decimali. Puoi anche immettere un numero fisso. Ad esempio, se immetti *2*, per tutti gli importi vengono mostrate due posizioni decimali. |
    | **Posizioni decimali distanza** | Specifica il numero di posizioni decimali che vengono mostrate per le misurazioni della distanza. L'impostazione predefinita, *2:5*, indica che per tutti gli importi vengono mostrati un minimo di due posizioni decimali e un massimo di cinque posizioni decimali. Puoi anche immettere un numero fisso. Ad esempio, se immetti *2*, per tutti gli importi vengono mostrate due posizioni decimali. |
    | **Posizioni decimali importo personalizzato** | Specifica il numero di posizioni decimali che vengono mostrate per gli importi personalizzati. L'impostazione predefinita, *2:5*, indica che per tutti gli importi vengono mostrati un minimo di due posizioni decimali e un massimo di cinque posizioni decimali. Puoi anche immettere un numero fisso. Ad esempio, se immetti *2*, per tutti gli importi vengono mostrate due posizioni decimali. |

4. Nella Scheda dettaglio **Creazione di report**, completa l'impostazione configurando i campi che sono correlati alla creazione di report per le autorità.

    > [!NOTE]
    > Nella versione 24.0, [!INCLUDE[prod_short](includes/prod_short.md)] non supporta la creazione di report per alcuna autorità. Pertanto, i campi che sono correlati alla configurazione di questa funzionalità nella Scheda dettaglio **Creazione di report** sono destinati a funzionalità di reporting future. I partner possono comunque utilizzare questi campi anche nelle versioni localizzate.

    | Campo | Descrizione |
    |-------|-------------|
    | **Codice unità gerarchica di misura delle emissioni** | Specifica il codice dell'unità di misura utilizzato per creare report sulle emissioni, poiché puoi utilizzare un'unità di misura diversa quando crei i report per le autorità. Questo campo non è applicabile ai report standard. |
    | **Creazione report fattore UOM** | Specifica il fattore di unità di misura utilizzato per registrare le emissioni, se utilizzi un'unità di misura diversa quando crei i report per le autorità. |
    | **Approssimazione di arrotondamento delle emissioni** | Specifica le dimensioni dell'intervallo che viene utilizzato nell'arrotondamento degli importi delle emissioni quando crei i report per le autorità. |
    | **Tipo di arrotondamento delle emissioni** | Specifica in che modo il programma arrotonda gli importi delle emissioni quando crei i report per le autorità. Sono disponibili le opzioni seguenti: **Al più vicino**, **Per eccesso** e **Per difetto**. |

## Vedere anche

[Dati finanziari](finance.md)  
[Panoramica della gestione della sostenibilità](finance-manage-sustainability.md)  
[Contabilità generale e piano dei conti di sostenibilità](finance-sustainability-accounts-ledger.md)  
[Registrare movimenti di sostenibilità](finance-sustainability-journal.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Estensione dell'esperienza di base | Microsoft Docs
description: Questa estensione è un'alternativa moderna di Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 11/10/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# Estensione dell'esperienza di base

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Se è stato utilizzato Microsoft Dynamics C5, i partner Microsoft possono aiutare a passare a una soluzione più moderna basata su [!INCLUDE[prod_short](includes/prod_short.md)], in modo da poter continuare a godere delle stesse funzionalità semplificate di Dynamics C5.

Questa estensione è destinata alle piccole imprese e può supportare fino a tre utenti. Se sono necessari più utenti, eseguire l'aggiornamento a una licenza [!INCLUDE[prod_short](includes/prod_short.md)] e disinstallare questa estensione.

> [!NOTE]
> Al momento, questa estensione è disponibile solo per i clienti in Danimarca e Islanda.

## Funzionalità disponibili

La tabella seguente descrive le funzionalità disponibili se si installa l'estensione dell'esperienza di base.

|Ad area  |Funzionalità  |
|---------|---------|
|**Contabilità generale** |Finanza di base, report finanziari, cespiti, gestione bancaria, riconciliazione bancaria, pagamenti, addebito diretto, dimensioni, valute multiple, budget, flusso di lavoro, gestione documenti/OCR, consolidamento, numero illimitato di società|
|**Scadenzari clienti/Vendite** |Contabilità clienti di base, fatturazione di vendita, sconti di vendita, prezzi, IVA, gestione contatti |
|**Contabilità fornitori/Acquisti** |Contabilità fornitori di base, fatturazione degli acquisti |
|**Gestione progetti** |Commesse, prezzi delle commesse, fogli presenze, assegnazioni, task, risorse |
|**Magazzino** |Inventario di base, sostituzioni di articolo, cross reference dell'articolo |

## Introduzione

Questa estensione è leggermente diversa dalla maggior parte e sarà necessario l'aiuto di un partner Microsoft per installarla e configurarla. Per sapere cosa aspettarsi, ecco una visualizzazione ad alto livello di ciò che fa il partner Microsoft.

1. Creare un nuovo tenant [!INCLUDE[prod_short](includes/prod_short.md)]. Può essere una versione di valutazione o Cloud Solution Provider (CSP).
2. Aggiungere almeno un utente assegnato a una licenza dell'esperienza di base nell'account Microsoft Entra.
3. Rimuovere tutte le società, inclusa la società Cronus di esempio.
4. Creare una nuova società che non contenga dati o configurazioni di esempio.
5. Aggiungere il pacchetto **Demo RapidStart**. <!--what does the package contain?-->
6. Scaricare e installare l'estensione dell'esperienza di base da AppSource.

## Migrazione dei dati

Portare con sé i propri dati Dynamics C5. Dopo che il partner Microsoft avrà installato l'estensione dell'esperienza di base, sarà disponibile un'azienda vuota. Un modo semplice per spostare i dati da Dynamics C5 all'esperienza di base consiste nell'utilizzare l'estensione Migrazione dei dati C5, inclusa in [!INCLUDE[prod_short](includes/prod_short.md)]. L'estensione esegue la migrazione di clienti, fornitori, articoli, conti di contabilità generale e relativi movimenti.

## Vedere anche

[Estensione di migrazione dati C5](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

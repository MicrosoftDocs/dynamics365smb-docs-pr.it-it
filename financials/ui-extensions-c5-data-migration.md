---
title: Utilizzo dell'estensione di migrazione dati C5 | Documenti Microsoft
description: "Utilizzare questa estensione per migrare clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d3b8d3d01ce75da59c1cce873077955776963ce9
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---

# <a name="the-c5-data-migration-extension-for-finance-and-operations-business-edition"></a>Estensione di migrazione dati C5 per Finance and Operations, Business edition
Questa estensione consente di migrare facilmente clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)]. È inoltre possibile migrare lo storico dei movimenti per i conti di contabilità generale.

> [!Note]
> La società in [!INCLUDE[d365fin](includes/d365fin_md.md)] non deve contenere alcun dato. Inoltre, una volta avviata una migrazione, non creare clienti, fornitori, articoli o conti fino al termine della migrazione.

##<a name="what-data-is-migrated"></a>Quali dati vengono migrati?
I seguenti dati vengono migrati per ogni entità:

**Clienti**
* Località
* Paese
* Dimensioni clienti (reparto, centro, scopo)
* Metodo di spedizione
* Venditore
* Condizioni pagamento
* Metodo di pagamento
* Gruppo prezzi cliente
* Sconto fattura cliente

Se si migrano i conti, anche i seguenti dati vengono migrati:

* Setup registrazione cliente
* Batch registrazioni COGE
* Transazioni aperte(movimenti contabili clienti)

**Fornitori**
* Località
* Paese
* Dimensioni fornitori (reparto, centro, scopo)
* Sconto fattura
* Metodo di spedizione
* Add. acquisti
* Condizioni pagamento
* Metodo di pagamento
* Sconto fattura fornitore

Se si migrano i conti, anche i seguenti dati vengono migrati:

* Setup registrazione fornitori
* Batch registrazioni COGE
* Transazioni aperte(movimenti contabili fornitori)

**Articoli**
* Località
* Paese
* Dimensioni articoli (reparto, centro, scopo)
* Sconti riga vendita
* Categorie sconto clienti
* Gruppi sconto articolo
* Prezzo vendita
* Nomenclatura combinata
* Unità di misura
* Codice tracciabilità articolo
* Gruppo prezzi cliente

Se si migrano i conti, anche i seguenti dati vengono migrati:

* Setup registrazione magazzino
* Setup registrazioni COGE
* Batch registrazioni magazzino
* Transazioni aperte(movimenti contabili articoli)

> [!Note]
> Se esistono transazioni aperte che usano valute estere, vengono migrati anche i tassi di cambio per queste valute. Altri tassi di cambio non sono migrati.

## <a name="to-migrate-data"></a>Per migrare i dati
Sono necessari solo alcuni passaggi per esportare i dati da C5 e importarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. In C5, utilizzare la funzione **Esporta database** per esportare i dati. Quindi, inviare la cartella di esportazione a una cartella compressa (.zip).  
2. In [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report") e immettere **Migrazione dati**, quindi scegliere **Migrazione dati**.  
3. Completare i passaggi nella guida di setup assistito. Assicurarsi di scegliere **Importa da Microsoft Dynamcis C5 2012** come origine dati.  

> [!Note]
> Le aziende spesso aggiungono campi per personalizzare C5 per il proprio settore specifico. [!INCLUDE[d365fin](includes/d365fin_md.md)] non migra i dati dai campi personalizzati. Inoltre, la migrazione non avrà esito positivo se sono presenti più di 10 campi personalizzati.

## <a name="viewing-the-status-of-the-migration"></a>Visualizzazione dello stato della migrazione
Utilizzare la pagina **Sintesi migrazione dati** per monitorare il successo della migrazione. La pagina mostra informazioni quali il numero di entità che la migrazione includerà, lo stato della migrazione e il numero di articoli che sono stati migrati e se la migrazione ha avuto esito positivo. Mostra inoltre il numero di errori, consente di analizzare gli errori riscontrati e, se possibile, consente di passare facilmente all'entità per risolvere i problemi. Per ulteriori informazioni, vedere la sezione successiva in questo argomento.  

> [!Note]
> Mentre si attendono i risultati della migrazione, è necessario aggiornare la pagina per visualizzare i risultati.

## <a name="correcting-errors"></a>Correzione degli errori
Se si verifica un errore, il campo **Stato** mostrerà **Completato con errori**, quindi il campo **Numero di errori** mostrerà il numero degli errori. Per visualizzare un elenco degli errori, è possibile aprire la pagina **Errori di migrazione dati** scegliendo:  

* Il numero nel campo **Numero di errori** per l'entità.  
* L'entità, quindi l'azione **Mostra errori**.  

Nella pagina **Errori di migrazione dati**, per correggere un errore è possibile scegliere un messaggio di errore, quindi **Modifica record** per aprire una pagina che mostra i dati migrati per l'entità. Dopo aver corretto uno o più errori, è possibile scegliere **Esegui migrazione** per migrare solo le entità corrette, senza dover riavviare completamente la migrazione.  

> [!Tip]
> Se è stato corretto più di un errore, è possibile utilizzare la funzionalità **Seleziona più elementi** per selezionare più righe da migrare. In alternativa, se esistono errori che non è importante correggere, è possibile selezionarli, quindi scegliere **Ignora selezione**.

> [!Note]
> Se si dispone di articoli che sono inclusi in una distinta base, potrebbe essere necessario effettuare la migrazione più di una volta se l'articolo originale non viene creato prima delle varianti a cui è associato. Se una variante articolo viene creata per prima, il riferimento all'articolo originale può causare un messaggio di errore.  

## <a name="verifying-data-after-migrating"></a>Verifica dei dati dopo la migrazione
Un modo per verificare che i dati siano stati migrati correttamente consiste nell'esaminare le seguenti pagine in C5 e [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Movimenti clienti| Registrazioni COGE|
|Movimenti fornitori| Registrazioni COGE|
|Mov. Articoli| Registrazioni magazzino|

In [!INCLUDE[d365fin](includes/d365fin_md.md)], il batch per i dati migrati è denominato **C5MIGRATE**.

## <a name="stopping-data-migration"></a>Interruzione della migrazione dei dati
È possibile interrompere la migrazione dei dati scegliendo **Interrompi tutte le migrazioni**. In tal caso, tutte le migrazioni in sospeso vengono interrotte.

## <a name="see-also"></a>Vedi anche
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Benvenuto in [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  


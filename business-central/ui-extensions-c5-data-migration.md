---
title: Utilizzo dell'estensione di migrazione dati C5 | Documenti Microsoft
description: Utilizzare questa estensione per migrare clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a Business Central.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 23d2f6c950786bbd5eb8af0a79ea1351d4e8a3d0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250072"
---
# <a name="the-c5-data-migration-extension"></a>Estensione di migrazione dati C5
Questa estensione consente di migrare facilmente clienti, fornitori, articoli e conti di contabilità generale da Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)]. È inoltre possibile migrare lo storico dei movimenti per i conti di contabilità generale.

> [!Note]
> La società in [!INCLUDE[d365fin](includes/d365fin_md.md)] non deve contenere alcun dato. Inoltre, una volta avviata una migrazione, non creare clienti, fornitori, articoli o conti fino al termine della migrazione.

## <a name="what-data-is-migrated"></a>Quali dati vengono migrati?
I seguenti dati vengono migrati per ogni entità:

**Clienti**
* Contatti  
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
* Contatti
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
* DB assemblaggio

Se si migrano i conti, anche i seguenti dati vengono migrati:

* Setup registrazione magazzino
* Setup registrazioni COGE
* Batch registrazioni magazzino
* Transazioni aperte(movimenti contabili articoli)

> [!Note]
> Se esistono transazioni aperte che usano valute estere, vengono migrati anche i tassi di cambio per queste valute. Altri tassi di cambio non sono migrati.

**Piano dei conti**  
* Dimensioni standard: reparto, scopo e centro di costo  
* Transazioni storiche C/G  

> [!Note]
> Le transazioni storiche C/G vengono trattate in modo diverso. Quando si migrano i dati si imposta un parametro **Periodo corrente**. Questo parametro consente di elaborare le transazioni C/G. Le transazioni dopo questa data vengono migrate singolarmente. Le operazioni precedenti alla data vengono aggregate per conto e migrate come importo singolo. Ad esempio, sono presenti transazioni nel 2015, 2016, 2017, 2018 e si specifica il 1° gennaio 2017 nel campo Periodo corrente. Per ogni conto, gli importi per le transazioni il 31 dicembre 2106 o in data precedente verranno aggregate in un'unica riga del giornale di registrazione generale per ciascun conto C/G. Tutte le transazioni dopo questa data verranno migrate singolarmente.

## <a name="file-size-requirements"></a>Requisiti per le dimensioni di file
La dimensione di file più grande che è possibile caricare in [!INCLUDE[d365fin](includes/d365fin_md.md)] è 150 MB. Se il file esportato da C5 è più grande, considerare la migrazione dei dati in più file. Ad esempio, esportare uno o due tipo di entità da C5, quali clienti e fornitori, in un file quindi esportare gli articoli nell'altro file, e così via. È possibile importare file individualmente in [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-migrate-data"></a>Per migrare i dati
Sono necessari solo alcuni passaggi per esportare i dati da C5 e importarli in [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. In C5, utilizzare la funzione **Esporta database** per esportare i dati. Quindi, inviare la cartella di esportazione a una cartella compressa (.zip).  
2. In [!INCLUDE[d365fin](includes/d365fin_md.md)], scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Migrazione dati** e quindi scegliere **Migrazione dati**.  
3. Completare i passaggi nella guida di setup assistito. Assicurarsi di scegliere **Importa da Microsoft Dynamcis C5 2012** come origine dati.  

## <a name="viewing-the-status-of-the-migration"></a>Visualizzazione dello stato della migrazione
Utilizzare la pagina **Sintesi migrazione dati** per monitorare il successo della migrazione. La pagina mostra informazioni quali il numero di entità che la migrazione includerà, lo stato della migrazione e il numero di articoli che sono stati migrati e se la migrazione ha avuto esito positivo. Mostra inoltre il numero di errori, consente di analizzare gli errori riscontrati e, se possibile, consente di passare facilmente all'entità per risolvere i problemi. Per ulteriori informazioni, vedere la sezione successiva in questo argomento.  

> [!Note]
> Mentre si attendono i risultati della migrazione, è necessario aggiornare la pagina per visualizzare i risultati.

## <a name="how-to-avoid-double-posting"></a>Come evitare la doppia registrazione
Per evitare la doppia registrazione in contabilità generale, vengono utilizzati i seguenti conti di contropartita per le transazioni aperte:  

* Per i fornitori, si usa il conto v/fornitori della categoria di registrazione fornitori.  
* Per i clienti, si usa il conto v/clienti della categoria di registrazione clienti.  
* Per gli articoli, si crea una registrazione COGE dove il conto di rettifica è il conto specificato come conto relativo al magazzino nel setup della registrazione magazzino.  

## <a name="correcting-errors"></a>Correzione degli errori
Se si verifica un errore, il campo **Stato** mostrerà **Completato con errori**, quindi il campo **Numero di errori** mostrerà il numero degli errori. Per visualizzare un elenco degli errori, è possibile aprire la pagina **Errori di migrazione dati** scegliendo:  

* Il numero nel campo **Numero di errori** per l'entità.  
* L'entità, quindi l'azione **Mostra errori**.  

Nella pagina **Errori di migrazione dati**, per correggere un errore è possibile scegliere un messaggio di errore e **Modifica record** per visualizzare i dati migrati per l'entità. Se sono presenti più errori da correggere, è possibile scegliere **Correzione in blocco errori** per modificare le entità in un elenco. È comunque necessario aprire i singoli record se l'errore è stato causato da una voce correlata. Ad esempio, un fornitore non verrà migrato se un indirizzo e-mail di uno dei suoi contatti ha un formato non valido.

Dopo aver corretto uno o più errori, è possibile scegliere **Esegui migrazione** per migrare solo le entità corrette, senza dover riavviare completamente la migrazione.  

> [!Tip]
> Se è stato corretto più di un errore, è possibile utilizzare la funzionalità **Seleziona più elementi** per selezionare più righe da migrare. In alternativa, se esistono errori che non è importante correggere, è possibile selezionarli, quindi scegliere **Ignora selezione**.

> [!Note]
> Se si dispone di articoli che sono inclusi in una distinta base, potrebbe essere necessario effettuare la migrazione più di una volta se l'articolo originale non viene creato prima delle varianti a cui è associato. Se una variante articolo viene creata per prima, il riferimento all'articolo originale può causare un messaggio di errore.  

## <a name="verifying-data-after-migrating"></a>Verifica dei dati dopo la migrazione
Un modo per verificare che i dati siano stati migrati correttamente consiste nell'esaminare le seguenti pagine in C5 e [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Processo batch da usare |
|-----|-----|-----|
|Movimenti clienti| Registrazioni COGE| CUSTMIGR |
|Movimenti fornitori| Registrazioni COGE| VENDMIGR|
|Mov. Articoli| Registrazioni magazzino| ITEMMIGR |
|Movimenti C/G| Registrazioni COGE| GLACMIGR |

## <a name="stopping-data-migration"></a>Interruzione della migrazione dei dati
È possibile interrompere la migrazione dei dati scegliendo **Interrompi tutte le migrazioni**. In tal caso, tutte le migrazioni in sospeso vengono interrotte.

## <a name="see-also"></a>Vedi anche
[Personalizzazione di [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizzando le estensioni](ui-extensions.md)  
[Introduzione](product-get-started.md)

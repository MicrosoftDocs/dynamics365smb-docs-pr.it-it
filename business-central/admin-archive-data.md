---
title: L'estensione dell'archivio dati
description: L'archiviazione dei dati crea un backup a basso costo dei vostri dati.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 032c425f10bae29416cf8602d0c339f3ffaa3043
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589456"
---
# <a name="the-data-archive-extension"></a>L'estensione dell'archivio dati
Nel corso del tempo, la vostra azienda accumulerà una notevole quantità di dati, e come amministratore, è probabilmente una buona idea avere una strategia per l'archiviazione dei dati. Avere molti dati può rallentare le cose, per esempio, potrebbe richiedere un po' più tempo per generare i rapporti, o anche bloccare i record. Inoltre, grandi quantità di dati possono portare a un aumento dei costi di archiviazione.

L'estensione Data Archive fornisce un quadro di base per l'archiviazione e il backup dei dati come parte della compressione della data. Quando si usa la compressione delle date, le voci correlate vengono consolidate in una sola voce e gli originali vengono cancellati. Per ulteriori informazioni, vedere [Comprimere i dati con la compressione della data](admin-manage-documents.md#compress-data-with-date-compression). Tuttavia, potrebbe esserci un valore nel mantenere quei dati, quindi piuttosto che cancellarli, potete archiviarli per un uso successivo.

## <a name="start-archiving-data"></a>Iniziare l'archiviazione dei dati
L'estensione è preinstallata e disponibile nella **Gestione delle estensioni**, quindi non è necessario fare nulla per iniziare. L'estensione è disponibile anche su Microsoft AppSource. 

I tuoi archivi di dati sono elencati nella pagina **Elenco degli archivi di dati** . Ogni archivio può contenere dati da più tabelle e può contenere fino a 10.000 record. Se ci sono più di 10.000 record in una tabella, un secondo archivio sarà creato per i successivi 10.000 record, e così via. Per esempio, se archivi 10.100 voci G/L, Business Central crea un archivio "G/L Entry" per le prime 10.000 voci e poi un secondo archivio per le restanti 100 voci. 

Dopo aver archiviato i dati, puoi esplorarli usando Microsoft Excel o come file CSV.

* Se usi l'opzione Excel, la cartella di lavoro conterrà un foglio di lavoro per ogni tabella dell'archivio dati.
* Se usi l'opzione CSV otterrai un file ZIP con un file CSV per ogni tabella dell'archivio dati.

> [!TIP]
> Le opzioni Excel e CSV facilitano l'uso di un'altra app o servizio per spostare i dati in un'altra posizione, come Azure Blob storage, o strumento di analisi, come Microsoft Power BI.

Le estensioni dell'Archivio dati sono utilizzate dai seguenti lavori batch per la compressione della data.

|Lavori batch  |
|---------|
|Data Comp. Voce Voci di bilancio     |
|Data Compress Bank Acc. Ledger     |
|Data Comprimere il libro mastro dei clienti     |
|Data Comprimere FA Ledger     |
|Data Comprimere la contabilità generale     |
|Data Comprimere il libro mastro dell'assicurazione     |
|Data Compress Maint. Libro mastro     |
|Data Compress Maint. Libro mastro     |
|Data Comprimere il libro mastro delle risorse     |
|Comprimere la data delle voci IVA     |
|Data Comprimere il libro mastro dei fornitori     |
|Data Compress Whse. Movimenti     |
|Data Compr. Movimenti budget C/G     |

Per avviare l'archiviazione dei dati quando esegui uno dei lavori batch, attiva il toggle **Archivia le voci cancellate** .

## <a name="storage-considerations"></a>Considerazioni sullo stoccaggio
I dati archiviati sono memorizzati nella tabella **Elemento multimediale tenant** . Questa tabella non è inclusa nel calcolo delle dimensioni del database, secondo i termini della vostra licenza. Invece, conta come archiviazione di file. Tuttavia, si consiglia di esportare i vecchi archivi, per esempio, in un file CSV e poi cancellare i vecchi record dell'archivio.

## <a name="see-also"></a>Vedere anche
[Gestire l'archiviazione eliminando i documenti o comprimendo i dati](admin-manage-documents.md)

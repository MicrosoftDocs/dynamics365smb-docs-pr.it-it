---
title: Gestire l'archiviazione eliminando documenti o comprimendo i dati
description: Scopri come gestire l'accumulo di documenti storici (e ridurre la quantità di dati archiviati in un database) eliminandoli o comprimendoli.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 149f035dfd6b1abd2e00048bb1af4059e00c976f
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482172"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Gestire l'archiviazione eliminando documenti o comprimendo i dati

Un ruolo centrale, ad esempio l'amministratore dell'applicazione, deve occuparsi regolarmente dell'accumularsi dei documenti storici, eliminandoli o comprimendoli.  

> [!TIP]
> Per informazioni su altri modi di ridurre la quantità di dati archiviati in un database, vedi [Ridurre i dati archiviati nei database di Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) nella documentazione per sviluppatori e professionisti IT.

## <a name="delete-documents"></a>Eliminare documenti

In certe situazioni, si ha la necessità di eliminare degli ordini di acquisto fatturati. [!INCLUDE[prod_short](includes/prod_short.md)] verifica che gli ordini di acquisto eliminati siano stati completamente fatturati. Non è possibile eliminare ordini che non siano stati completamente fatturati e ricevuti.  

Gli ordini di reso sono in genere eliminati dopo la fatturazione. Quando si registra una fattura, viene trasferita nella pagina **Note credito acq. registrate** . Se si seleziona la casella di controllo **Spediz. resi in nota credito** nella pagina **Setup contabilità fornitori**, la fattura viene trasferita nella pagina **spedizione reso registrata**. È possibile eliminare i documenti mediante il processo batch **Rimuovi ordini resi acq. fatt.** . Prima di eliminarli, il processo batch verifica se gli ordini di reso acquisto sono completamente spediti e fatturati.  

Gli ordini di acquisto programmati non vengono eliminati dopo aver elaborato e fatturato tutti gli ordini di acquisto correlati. È possibile eliminare ordini programmati tramite il processo batch **Elimina ordini acq. progr. fatturati**.  

Gli ordini di assistenza fatturati vengono in genere eliminati automaticamente dopo che sono stati completamente fatturati. Quando si registra una fattura, viene creato un movimento corrispondente nella pagina **Fatture assistenza registrate**. Il documento registrato può essere visualizzato nella pagina **Fattura assistenza registrata**.  

Gli ordini di assistenza non vengono, tuttavia, eliminati automaticamente se la quantità totale indicata nell'ordine è stata registrata non dall'ordine stesso, ma dalla pagina **Fattura assistenza**. In questo caso può essere necessario eliminare ordini fatturati che non sono stati eliminati. Per eseguire questa operazione, utilizzare il processo batch **Elimina ordini assistenza fatturati**.  

## <a name="compress-data-with-date-compression"></a>Comprimere i dati con la compressione della data

È possibile comprimere i dati in [!INCLUDE [prod_short](includes/prod_short.md)] per risparmiare spazio nel database, che in [!INCLUDE [prod_short](includes/prod_short.md)] online può anche far risparmiare denaro. La compressione si basa sulle date e consiste nel combinare diversi movimenti vecchi in un unico movimento nuovo. 

È possibile comprimere le voci nelle seguenti condizioni:

* Sono relative ad anni fiscali chiusi
* Il campo **Apri** è impostato su **No** 
* Hanno almeno cinque anni. Se si intende comprimere dati che hanno meno di cinque anni, contattare il partner Microsoft.

Ad esempio, i movimenti di registro fornitori dell'ultimo anno fiscale trascorso possono essere compressi in modo da ottenere un solo valore di dare/avere per ogni mese. L'importo del nuovo movimento corrisponderà alla somma di tutti i movimenti compressi. La data assegnata sarà la data iniziale del periodo compresso, ad esempio il primo giorno del mese se i movimenti sono stati compressi per mese. In seguito alla compressione sarà comunque possibile visualizzare il saldo periodo per ogni conto dell'anno fiscale trascorso.

Il numero dei movimenti creati da una compressione data dipende dal numero di filtri impostati, dai campi che vengono associati e dalla durata del periodo. Il risultato del processo sarà sempre di almeno un movimento. Al termine del processo batch è possibile visualizzare il risultato nella pagina **Registri compressione data**.

È possibile comprimere i seguenti tipi di dati utilizzando i processi batch. C'è un lavoro batch per ogni tipo di dati.

* Movimenti finanziari - movimenti C/G, movimenti IVA, movimenti contabili conti bancari, movimenti budget C/G, movimenti contabili clienti, movimenti contabili fornitori.
* Movimenti warehouse 
* Movimenti risorse
* Movimenti budget articoli
* Cespiti - movimenti contabili cespiti, movimenti contabili di manutenzione cespiti, movimenti contabili di assicurazione cespiti.

Quando definisci i criteri per la compressione, puoi utilizzare le opzioni sotto **Mantieni contenuto campo** per mantenere il contenuto di determinati campi. I campi disponibili dipendono dai dati che stai comprimendo.

> [!NOTE]
> Prima di poter eseguire la compressione della data, le visualizzazioni dell'analisi devono essere aggiornate. Per ulteriori informazioni, vedi [Per aggiornare una vista di analisi](/dynamics365/business-central/bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

In seguito alla compressione verranno sempre mantenute le informazioni contenute nei seguenti campi: **Data di registrazione**, **Nr. fornitore**, **Tipo di documento**, **Codice valuta**, **Categoria registrazione**, **Importo**, **Importo residuo**, **Importo originario (VL)**, **Importo residuo (VL)**, **Importo (VL)**, **Acquisti (VL)**, **Sconto fattura (VL)**, **Sconto pagam. applicato (VL)** e **Colleg. sconto pag. possibile**.

## <a name="posting-compressed-entries"></a>Pubblicazione di voci compresse
Le voci compresse vengono pubblicate in modo leggermente diverso rispetto alla registrazione standard. Ciò serve a ridurre il numero di nuovi movimenti di contabilità generale creati dalla compressione della data ed è particolarmente importante quando si conservano informazioni quali dimensioni e numeri di documento. La compressione della data crea nuovi movimenti come segue:
* Nella pagina **Movimenti C/G** vengono creati nuovi movimenti con nuovi numeri per i movimenti compressi. Il campo **Descrizione** contiene **Data compressa** in modo da rendere i movimenti compressi facili da identificare. 
* Nelle pagine dei movimenti, ad esempio **Movimenti contabili clienti**, vengono creati uno o più movimenti con i nuovi numeri di movimento. 

Il processo di registrazione crea interruzioni nella numerazione per i movimenti nella pagina **Movimenti C/G**. Questi numeri vengono assegnati solo ai movimenti nelle pagine dei movimenti contabili. L'intervallo di numeri assegnato ai movimenti è disponibile nella pagina **Registro C/G**, nei campi **Dal nr. movimento** e **Al nr. movimento**. 

> [!NOTE]
> Dopo aver eseguito la compressione della data, tutti i conti nel libro mastro vengono bloccati. Ad esempio, non è possibile annullare l'applicazione di movimenti contabili bancari o fornitore per qualsiasi conto durante il periodo in cui le date sono compresse.

Il numero dei movimenti creati da una compressione data dipende dal numero di filtri impostati, dai campi che vengono associati e dalla durata del periodo. Il risultato del processo sarà sempre di almeno un movimento. 

> [!WARNING]
> Poiché la compressione data elimina del tutto i movimenti, è consigliabile eseguire sempre una copia di backup del database prima di eseguire questo processo batch.

### <a name="to-run-a-date-compression"></a>Per eseguire una compressione data
1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immetti **Amministrazione data**, quindi scegli il collegamento correlato.
2. Effettuare una delle seguenti operazioni:
    * Per utilizzare una guida alla configurazione assistita per impostare la compressione della data per uno o più tipi di dati, scegli **Guida all'amministrazione dei dati**.
    * Per impostare la compressione per un singolo tipo di dati, scegli **Compressione data**, **Comprimi voci**, quindi scegli i dati da comprimere.

   > [!NOTE]
   > Puoi comprimere solo i dati che hanno più di cinque anni. Se si intende comprimere dati che hanno meno di cinque anni, contattare il partner Microsoft.

## <a name="see-also"></a>Vedere anche

[Amministrazione](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
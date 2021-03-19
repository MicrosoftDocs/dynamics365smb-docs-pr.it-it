---
title: Gestire l'archiviazione eliminando documenti o comprimendo i dati
description: Informazioni su come conservare i dati storici comprimendo i movimenti contabili o eliminarli.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b17e4df039ef713bf5c0048d258aefd175157ba4
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493049"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Gestire l'archiviazione eliminando documenti o comprimendo i dati

Un ruolo centrale, ad esempio l'amministratore dell'applicazione, deve occuparsi regolarmente dell'accumularsi dei documenti storici, eliminandoli o comprimendoli.  

> [!TIP]
> Per informazioni su altri modi di ridurre la quantità di dati archiviati in un database, vedi [Ridurre i dati archiviati nei database di Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) nella guida per sviluppatori e professionisti IT.

## <a name="delete-documents"></a>Eliminare documenti

In certe situazioni, si ha la necessità di eliminare degli ordini di acquisto fatturati. [!INCLUDE[prod_short](includes/prod_short.md)] verifica che gli ordini di acquisto eliminati siano stati completamente fatturati. Non è possibile eliminare ordini che non siano stati completamente fatturati e ricevuti.  

Gli ordini di reso sono in genere eliminati dopo la fatturazione. Quando si registra una fattura, viene trasferita nella pagina **Note credito acq. registrate** . Se si seleziona la casella di controllo **Spediz. resi in nota credito** nella pagina **Setup contabilità fornitori**, la fattura viene trasferita nella pagina **spedizione reso registrata**. È possibile eliminare i documenti mediante il processo batch **Rimuovi ordini resi acq. fatt.** . Prima di eliminarli, il processo batch verifica se gli ordini di reso acquisto sono completamente spediti e fatturati.  

Gli ordini di acquisto programmati non vengono eliminati dopo aver elaborato e fatturato tutti gli ordini di acquisto correlati. È possibile eliminare ordini programmati tramite il processo batch **Elimina ordini acq. progr. fatturati**.  

Gli ordini di assistenza fatturati vengono in genere eliminati automaticamente dopo che sono stati completamente fatturati. Quando si registra una fattura, viene creato un movimento corrispondente nella pagina **Fatture assistenza registrate**. Il documento registrato può essere visualizzato nella pagina **Fattura assistenza registrata**.  

Gli ordini di assistenza non vengono, tuttavia, eliminati automaticamente se la quantità totale indicata nell'ordine è stata registrata non dall'ordine stesso, ma dalla pagina **Fattura assistenza**. In questo caso può essere necessario eliminare ordini fatturati che non sono stati eliminati. Per eseguire questa operazione, utilizzare il processo batch **Elimina ordini assistenza fatturati**.  

## <a name="compress-data-with-date-compression"></a>Comprimere i dati con la compressione della data

È possibile comprimere i dati in [!INCLUDE [prod_short](includes/prod_short.md)] in modo da risparmiare spazio nel database, che in [!INCLUDE [prod_short](includes/prod_short.md)] online può anche far risparmiare denaro. La compressione si basa sulle date e consiste nel combinare diversi movimenti vecchi in un unico movimento nuovo. È possibile comprimere soltanto movimenti appartenenti ad anni fiscali chiusi e movimenti contabili fornitori nel cui campo **Aperto** è impostato su *No*.  

Ad esempio, i movimenti di registro fornitori dell'ultimo anno fiscale trascorso possono essere compressi in modo da ottenere un solo valore di dare/avere per ogni mese. L'importo del nuovo movimento corrisponderà alla somma di tutti i movimenti compressi. La data assegnata sarà la data iniziale del periodo compresso, ad esempio il primo giorno del mese se i movimenti sono stati compressi per mese. In seguito alla compressione sarà comunque possibile visualizzare il saldo periodo per ogni conto dell'anno fiscale trascorso.

Il numero dei movimenti creati da una compressione data dipende dal numero di filtri impostati, dai campi che vengono associati e dalla durata del periodo. Il risultato del processo sarà sempre di almeno un movimento. Al termine del processo batch è possibile visualizzare il risultato nella pagina **Registri compressione data**.

È possibile comprimere i seguenti tipi di dati in [!INCLUDE [prod_short](includes/prod_short.md)] utilizzando i processi batch:

* Movimenti contabili C/C bancari

  In seguito alla compressione, tramite la funzione **Mantieni contenuto campo** è possibile mantenere le informazioni dei campi **Nr. Documento, Cod. Nostro Contatto**, **Cod. Dimens. Globale 1** e **Cod. Dimens. Globale 2**.
* Movimenti contabili fornitori

> [!NOTE]
> I movimenti compressi per clienti, fornitori, banca e registri secondari cespiti vengono registrati in modo leggermente diverso rispetto alla registrazione standard. Ciò serve a ridurre il numero di nuovi movimenti di contabilità generale creati dalla compressione della data ed è particolarmente importante quando si conservano informazioni quali dimensioni e numeri di documento. La compressione della data crea nuovi movimenti come segue:
>* Nella pagina **Movimenti C/G** vengono creati nuovi movimenti con nuovi numeri per i movimenti compressi. Il campo **Descrizione** contiene **Data compressa** in modo da rendere i movimenti compressi facili da identificare. 
>* Nelle pagine dei movimenti, ad esempio **Movimenti contabili clienti**, vengono creati uno o più movimenti con i nuovi numeri di movimento. 
> Il processo di registrazione crea interruzioni nella numerazione per i movimenti nella pagina **Movimenti C/G**. Questi numeri vengono assegnati solo ai movimenti nelle pagine dei movimenti contabili. L'intervallo di numeri assegnato ai movimenti è disponibile nella pagina **Registro C/G**, nei campi **Dal nr. movimento** e **Al nr. movimento**. 

In seguito alla compressione verranno sempre mantenute le informazioni contenute nei seguenti campi: **Data di registrazione**, **Nr. fornitore**, **Tipo di documento**, **Codice valuta**, **Categoria registrazione**, **Importo**, **Importo residuo**, **Importo originario (VL)**, **Importo residuo (VL)**, **Importo (VL)**, **Acquisti (VL)**, **Sconto fattura (VL)**, **Sconto pagam. applicato (VL)** e **Colleg. sconto pag. possibile**.

  Con la funzionalità **Mantieni contenuto campo** è inoltre possibile mantenere anche le informazioni contenute nei campi aggiuntivi seguenti: **Nr. documento**, **Acquistare da - Nr. for.**, **Cod. addetto acq.**, **Cod. dimens. globale 1** e **Cod. dimens. globale 2**.

> [!NOTE]
> Dopo aver eseguito la compressione della data, tutti i conti nel libro mastro vengono bloccati. Ad esempio, non è possibile annullare l'applicazione di movimenti contabili bancari o fornitore per qualsiasi conto durante il periodo in cui le date sono compresse.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Il numero dei movimenti creati da un processo batch di compressione data dipende dal numero di filtri impostati, dai campi che vengono associati e dalla durata del periodo. Il risultato del processo sarà sempre di almeno un movimento. 

> [!WARNING]
> Poiché la compressione data elimina del tutto i movimenti, è consigliabile eseguire sempre una copia di backup del database prima di eseguire questo processo batch.

La tabella seguente elenca i campi della scheda dettaglio **Opzioni** disponibili in tutti i processi batch. La sezione **Mantieni contenuto campo** include i campi aggiuntivi sono descritti sopra.

|Campo  |Descrizione  |
|-------|-------------|
|Data inizio     |Immettere in questo campo la data iniziale da includere nella compressione. La compressione comprenderà tutti i movimenti compresi fra questa data e la data finale.|
|Data fine     |Immettere in questo campo la data finale da includere nella compressione. La compressione comprenderà tutti i movimenti compresi fra la data iniziale e questa data.|
|Durata periodo |Scegliere la durata del periodo interessato dalla compressione. Per visualizzare le opzioni, selezionare il campo. Se la durata del periodo selezionata è *Trimestre*, *Mese* o *Settimana*, saranno compressi soltanto i movimenti che condividono uno stesso periodo contabile.|
|Mantieni contenuto campo     |Inserire un segno di spunta nelle caselle relative ai campi di cui si desidera mantenere le informazioni anche quando i movimenti siano stati compressi. Maggiore è il numero dei campi selezionati, più dettagliati saranno i movimenti compressi. Se nessuno di questi campi viene selezionato, verrà creato un solo movimento per ognuno dei periodi selezionati nel campo **Lunghezza periodo**. |

## <a name="see-also"></a>Vedere anche

[Amministrazione](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
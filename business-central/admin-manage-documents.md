---
title: Gestire l'archiviazione eliminando documenti o comprimendo i dati
description: Scopri come gestire l'accumulo di documenti storici (e ridurre la quantità di dati archiviati in un database) eliminandoli o comprimendoli.
author: edupont04
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: edupont
---
# Gestire l'archiviazione eliminando documenti o comprimendo i dati

Un ruolo centrale, ad esempio l'amministratore dell'applicazione, deve occuparsi regolarmente dell'accumularsi dei documenti storici, eliminandoli o comprimendoli.  

> [!TIP]
> Per ulteriori informazioni su altri modi di ridurre la quantità di dati archiviati in un database, vedi [Ridurre i dati archiviati nei database di Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) nella documentazione per sviluppatori e professionisti IT.

## Eliminare documenti.

In certe situazioni, si ha la necessità di eliminare degli ordini di acquisto fatturati. Tuttavia, non puoi eliminarli a meno che tu non abbia completamente fatturato e ricevuto gli articoli negli ordini di acquisto. [!INCLUDE[prod_short](includes/prod_short.md)] ti aiuta eseguendo i controlli.

Gli ordini di reso sono in genere eliminati dopo la fatturazione. Quando registri una fattura, viene trasferita nella pagina **Note credito acq. registrate** . Se selezioni la casella di controllo **Spediz. resi in nota credito** nella pagina **Setup contabilità fornitori**, la fattura viene trasferita nella pagina **spedizione reso registrata**. È possibile eliminare i documenti mediante il processo batch **Rimuovi ordini resi acq. fatt.** . Prima di eliminarli, il processo batch verifica se gli ordini di reso acquisto sono completamente spediti e fatturati.  

Gli ordini di acquisto programmati non vengono eliminati automaticamente dopo aver elaborato e fatturato tutti gli ordini di acquisto correlati. È possibile eliminarli tramite il processo batch **Elimina ordini acq. progr. fatturati**.  

Gli ordini di assistenza fatturati vengono in genere eliminati automaticamente dopo che sono stati completamente fatturati. Quando si registra una fattura, viene creato un movimento corrispondente che viene visualizzato nella pagina **Fatture assistenza registrate**.  

Gli ordini di assistenza non vengono, tuttavia, eliminati automaticamente se la quantità totale indicata nell'ordine è stata registrata dalla pagina **Fattura assistenza** anziché dall'ordine stesso. Potrebbe essere necessario eliminare manualmente tali ordini fatturati eseguendo il processo batch **Elimina ordini assistenza fatturati**.  

## Comprimere i dati con la compressione della data

È possibile comprimere i dati in [!INCLUDE [prod_short](includes/prod_short.md)] per risparmiare spazio nel database, che in [!INCLUDE [prod_short](includes/prod_short.md)] online può anche far risparmiare denaro. La compressione si basa sulle date e sulle funzioni, combinando diversi movimenti vecchi in un unico movimento nuovo.

È possibile comprimere i movimenti che soddisfano tutte le seguenti condizioni:

* Sono relativi ad anni fiscali chiusi.
* Il campo **Apri** è impostato su **No**.
* Hanno almeno cinque anni. Se intendi comprimere dati che hanno meno di cinque anni, contatta il partner Microsoft.

Ad esempio, i movimenti di registro fornitori dell'ultimo anno fiscale trascorso possono essere compressi in modo da ottenere un solo valore di dare/avere per ogni mese. L'importo del nuovo movimento è dato dalla somma di tutti i movimenti compressi. La data assegnata sarà la data iniziale del periodo compresso, ad esempio il primo giorno del mese se i movimenti vengono compressi in base ai mesi. In seguito alla compressione sarà comunque possibile visualizzare il saldo periodo per ogni conto dell'anno fiscale trascorso.

Il numero dei movimenti creati da una compressione data dipende dal numero di filtri impostati, dai campi che vengono associati e dalla durata del periodo. Il risultato del processo è sempre di almeno un movimento. Al termine del processo batch è possibile visualizzare il risultato nella pagina **Registri compressione data**.

Puoi comprimere i seguenti tipi di dati utilizzando i processi batch.

* Movimenti finanziari - movimenti di contabilità generale (C/G), movimenti IVA, movimenti contabili conti bancari, movimenti budget C/G, movimenti contabili clienti e movimenti contabili fornitori.
* Movimenti warehouse
* Movimenti risorse
* Movimenti budget articoli
* Cespiti - movimenti contabili cespiti, movimenti contabili di manutenzione cespiti e movimenti contabili di assicurazione cespiti.

Quando definisci i criteri per la compressione, puoi mantenere il contenuto di certi campi utilizzando le opzioni sotto **Mantieni contenuto campo**. I campi disponibili dipendono dai dati che stai comprimendo.

> [!NOTE]
> Prima di poter eseguire la compressione della data, le visualizzazioni dell'analisi devono essere aggiornate. Per ulteriori informazioni, vedi la sezione [Aggiornare una vista di analisi](bi-how-analyze-data-dimension.md#update-an-analysis-view).

In seguito alla compressione verranno sempre mantenute le informazioni contenute nei seguenti campi: **Data di registrazione**, **Nr. fornitore**, **Tipo di documento**, **Codice valuta**, **Categoria registrazione**, **Importo**, **Importo residuo**, **Importo originario (VL)**, **Importo residuo (VL)**, **Importo (VL)**, **Acquisti (VL)**, **Sconto fattura (VL)**, **Sconto pagam. applicato (VL)** e **Colleg. sconto pag. possibile**.

## Registrazione dei movimenti compressi

Le voci compresse vengono pubblicate in modo leggermente diverso rispetto alla registrazione standard. Ciò serve a ridurre il numero di nuovi movimenti di contabilità generale creati dalla compressione della data ed è particolarmente importante quando si conservano informazioni quali dimensioni e numeri di documento. La compressione della data crea nuovi movimenti come segue:

* Nella pagina **Movimenti C/G** vengono creati nuovi movimenti per i movimenti compressi. Il campo **Descrizione** contiene **Data compressa** in modo da rendere i movimenti compressi facili da identificare. 
* Nelle pagine dei movimenti, ad esempio **Movimenti contabili clienti**, vengono creati uno o più nuovi movimenti. 

Il processo di registrazione crea interruzioni nella numerazione per i movimenti nella pagina **Movimenti C/G**. Questi numeri vengono assegnati solo ai movimenti nelle pagine dei movimenti contabili. L'intervallo di numeri assegnato ai movimenti è disponibile nella pagina **Registro C/G**, nei campi **Dal nr. movimento** e **Al nr. movimento**. 

> [!NOTE]
> Dopo aver eseguito la compressione della data, tutti i conti nel libro mastro vengono bloccati. Ciò significa che non è possibile, ad esempio, stornare movimenti fornitori o contabili bancari per i conti interessati dalla compressione.

Il numero dei movimenti creati da una compressione data dipende dal numero di filtri impostati, dai campi che vengono associati e dalla durata del periodo di tempo. Il risultato del processo sarà sempre di almeno un movimento.

> [!WARNING]
> Poiché la compressione data elimina del tutto i movimenti, è consigliabile eseguire sempre una copia di backup del database prima di eseguire questo processo batch.

### Per eseguire una compressione data

1. Scegli l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Icona Cerca pagina o report"), immetti **Amministrazione data**, quindi scegli il collegamento correlato.
2. Effettuare una delle seguenti operazioni:
    * Per utilizzare una guida assistita per impostare la compressione della data per uno o più tipi di dati, scegli **Guida all'amministrazione dei dati**.
    * Per impostare la compressione per un singolo tipo di dati, scegli **Compressione data**, **Comprimi voci**, quindi scegli i dati da comprimere.

   > [!NOTE]
   > Puoi comprimere solo i dati che hanno più di cinque anni. Se intendi comprimere dati che hanno meno di cinque anni, contatta il partner Microsoft.

## Vedere anche

[Amministrazione](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

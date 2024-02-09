---
title: Allocare ricavi e costi a più conti CoGe
description: Scopri come allocare costi a uno o più conti nella contabilità generale.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Allocare ricavi e costi a più conti CoGe

In questo articolo viene descritto come utilizzare i conti di allocazione per distribuire importi in documenti di vendita e di acquisto e righe di registrazioni COGE in conti C/G diversi. Puoi allocare gli importi tramite una distribuzione fissa o variabile.  

L'allocazione suddivide una riga di registrazioni COGE nelle righe definite nella pagina **Conto allocazione**. Ad esempio, se dividi una spesa per l'affitto in tre modi utilizzando dimensioni, avrai tre righe da registrare per l'allocazione. Pertanto, avrai sei righe C/G (o forse di più se utilizzi l'IVA o l'imposta sulle vendite). Anche se in questo modo vengono registrati più movimenti C/G di quelli necessari, puoi stornare singole righe invece di stornare l'intera allocazione.

I conti di allocazione funzionano anche con i differimenti. Per ulteriori informazioni sui differimenti, vedi [Rateizzare le entrate e le uscite](finance-how-defer-revenue-expenses.md).

La tabella seguente presenta i metodi di allocazione che puoi utilizzare.

|Metodo di allocazione  |Descrizione  |
|---------|---------|
|Corretto     | Se desideri suddividere le spese in modo ripetuto per un periodo di tempo più lungo, puoi utilizzare un'allocazione fissa. Un'allocazione fissa ti consente di definire la suddivisione dell'allocazione. Questa suddivisione cambierà solo quando cambi l'impostazione nella pagina **Conto allocazione**.        |
|Variabile     | Per distribuire entrate o uscite in base a valori che cambiano nel tempo, utilizza il metodo di allocazione variabile. Le allocazioni variabili ti consentono di specificare le origini da utilizzare per calcolare le percentuali di allocazione. Questo metodo è utile, ad esempio, per suddividere i costi dei dipendenti in base al numero di dipendenti del reparto o delle divisioni. Un altro esempio è la distribuzione del costo dell'affitto in base alle riprese dell'impianto di produzione che potrebbero variare nel tempo in base alla linea di produzione. Le allocazioni variabili utilizzano una combinazione di dimensioni e conti statistici per determinare la modalità di distribuzione degli importi in un periodo di tempo. Per ulteriori informazioni sui conti statistici, vedi [Analizzare i dati con i conti statistici](bi-use-statistical-accounts.md). Per ulteriori informazioni sulle dimensioni, vedi [Usare le dimensioni](finance-dimensions.md).        |

## Utilizzare un metodo a quota fissa o percentuale per allocare gli importi

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Conto allocazione** e quindi scegli il collegamento correlato.  
1. Nella pagina **Conti allocazione** scegli l'azione **Nuovo**.
1. Compila i campi **Nr.** e **Nome**.
1. Nel campo **Tipo conto** scegli **Fisso**.
1. Nel campo **Tipo conto di destinazione**, scegli **Conto C/G** o **Conto bancario**.
1. Nel campo **Numero conto di destinazione** scegli il conto in cui registrare in valore.
1. Facoltativo: per registrare la riga, scegli l'azione **Dimensioni** e specifica le dimensioni.
1. Nei campi **Quota** e **Percentuale**, specifica come distribuire gli importi al conto di destinazione.
  
   > [!TIP]
   > Se inserisci l'importo effettivo da destinare a un'allocazione fissa nel campo **Quota**, il campo **Percentuale** mostra l'importo percentuale dell'importo totale.
1. Ripeti questo processo per ogni account da includere nell'allocazione.

## Utilizzare un metodo variabile per allocare importi

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Conto allocazione** e quindi scegli il collegamento correlato.  
1. Nella pagina **Conti allocazione** scegli l'azione **Nuovo**.
1. Compilare il campo **Nr.** e **Nome**.
1. Nel campo **Tipo conto** scegli **Variabile**.
1. Nel campo **Tipo di conto di destinazione** scegli **Conto C/G**.
1. Nel campo **Numero conto di destinazione** scegli il conto in cui registrare in valore.
1. Nel campo **Tipo di conto di ripartizione** scegli **Conto statistico**.
1. Nel campo **Periodo di calcolo** scegli il periodo per il quale distribuire gli importi.
1. Facoltativo: per filtrare in base a valori di dimensione globale specifici, scegli l'azione **Filtri per saldo conto di ripartizione** e quindi specifica i valori di filtro.
1. Facoltativo: per registrare la riga, scegli l'azione **Dimensioni** e specifica le dimensioni.

## Allocare importi immediatamente

Si creano conti di allocazione per suddividere ricavi e costi per conti C/G e conti bancari. L'automatizzazione dell'allocazione può farti risparmiare molto tempo. Tuttavia, se desideri utilizzare conti di allocazione, ma non desideri crearli per ogni conto C/G, puoi risparmiare ancora più tempo.

L'opzione Eredita da conto padre ti consente di utilizzare il conto di allocazione per suddividere gli importi per qualsiasi conto C/G su una riga di un documento o giornale di registrazioni. Nel campo **Tipo di account** di un documento o una riga di registrazione, scegli un conto C/G, quindi scegli il conto di allocazione nel campo **Nr. conto di allocazione**. L'importo della riga viene suddiviso per il conto C/G in base all'impostazione nel conto di allocazione. È un modo di allocazione meno trasparente, ma non devi creare un conto di allocazione specificatamente per il conto C/G.

Le allocazioni ad hoc sono facili da impostare. Anziché specificare un conto bancario o C/G nel campo **Tipo di conto di destinazione** nella pagina **Conto allocazione**, scegli l'opzione **Eredita da conto padre**. Lascia vuoto il campo **Numero conto di destinazione**. Quando scegli il conto C/G nel documento o nella riga di registrazione, tale conto viene utilizzato per allocare importi.

## Verificare che gli importi siano distribuiti correttamente prima di registrarli

Esistono un paio di modi per verificare che gli importi vengano distribuiti correttamente:

* Nella pagina **Conto allocazione** scegli l'azione **Allocazione test**. Usa il campo **Importo da allocare** per testare importi diversi.
* Nella pagina **Giornali di contabilità generale**, scegli il giornale e usa l'azione **Anteprima registrazione**.

## Rettificare la distribuzione

Se trovi qualcosa in un'allocazione che desideri modificare, puoi rettificare l'allocazione prima di registrarla.  

1. Apri il documento o il giornale a cui è associata l'allocazione che vuoi modificare.
1. Selezionare la riga e quindi l'azione **Ridistribuisci allocazioni conto**.
1. Nella pagina **Modifica allocazioni**, esegui la rettifica.

## Registrare una transazione di allocazione

I passaggi seguenti descrivono come registrare una transazione di allocazione da una registrazione COGE. I passaggi sono uguali per tutti i documenti di acquisto e vendita.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni COGE** e quindi scegliere il collegamento correlato.  
1. Creare una nuova riga. Compila i campi come faresti per qualsiasi altro tipo di registrazione COGE.
1. Se utilizzi un'allocazione fissa o variabile, compila i seguenti campi:
    1. Nel campo **Tipo conto** scegli **Conto allocazione**.
    1. Nel campo **Nr. conto** scegli il conto di allocazione.
1. Se stai utilizzando un'allocazione che utilizza l'opzione Eredita da conto padre, procedi come segue:
    1. Nel campo **Tipo conto** scegli **Conto C/G**.
    1. Nel campo **Nr. conto** scegli il conto C/G.
    1. Nel campo **Nr. conto di allocazione**, scegli il conto di allocazione configurato per utilizzare l'opzione Eredita da conto padre. 
1. Scegli **Registra**.

## Vedi anche

[Usare le registrazioni COGE](ui-work-general-journals.md)  
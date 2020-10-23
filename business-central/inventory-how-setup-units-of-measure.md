---
title: 'Procedura: Impostare unità di misura articolo | Documenti Microsoft'
description: È possibile impostare più unità di misura per un articolo in modo da poter assegnare le unità di misura all'articolo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e6a9465f13e272d653ec9a0544618b243928af03
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923722"
---
# <a name="set-up-units-of-measure"></a>Impostare unità di misura

Come parte del setup di [!INCLUDE [prodshort](includes/prodshort.md)], sono state impostate le unità di misura generali nella pagina **Unità di misura**. Quindi, quando si registrano nuovi articoli si specifica l'unità di misura base nella **Scheda articolo**. Ma è anche possibile aggiungere le unità di misura in un secondo momento.  

È possibile impostare più unità di misura per un articolo in modo da poter assegnare le unità di misura all'articolo per i seguenti scopi:

- Assegnare un'unità di misura base sulla scheda articolo per definire come viene memorizzata nel magazzino e per essere utilizzata come base di conversione per le unità di misura alternative.
- Assegnare unità di misura alternative ai documenti di acquisto, produzione, o vendita per indicare quante unità dell'unità di misura di base alla volta gestire nei processi. Ad esempio, è possibile acquistare l'articolo in pallet e utilizzare solo i pezzi singoli nella produzione.

Se un articolo viene inserito in stock utilizzando un'unità di misura ma viene prodotto in un'altra, viene creato un ordine di produzione che utilizza un'unità di misura batch di produzione per calcolare la quantità corretta di componenti durante il processo batch **Aggiorna ordine produzione**. Un esempio di calcolo di un'unità di misura è il caso in cui un articolo prodotto viene inserito in stock in pezzi, ma viene prodotto in tonnellate. Per ulteriori informazioni, vedere [Utilizzare le unità di misura batch di produzione](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

## <a name="to-set-up-units-of-measure"></a>Per impostare le unità di misura

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Unità di misura** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo**. Una nuova riga vuota viene inserita.  
3. Compilare i campi. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Se l'organizzazione venderà gli articoli con questa unità di misura a clienti di altri paesi, è possibile aggiungere le traduzioni.  
    1. Selezionare il codice per cui si intendono impostare le traduzioni e scegliere l'azione **Traduzioni**.
    2. Nel campo **Cod. lingua** selezionare la freccia a discesa per visualizzare una lista dei codici lingua disponibili. Selezionare il codice lingua per il quale si intende immettere la traduzione, quindi fare clic su OK per copiare il codice nel campo.
    3. Nel campo **Descrizione**, immettere il testo adeguato.
5. Ripetere i passaggi precedenti per tutte le unità di misura aggiuntive che si desidera aggiungere.  

Quando si registra un nuovo articolo è possibile scegliere l'unità di misura di base dall'elenco delle unità di misura impostato ora. È anche possibile impostare più unità di misura per un articolo.  

## <a name="to-set-up-multiple-item-units-of-measure"></a>Per impostare più unità di misura per l'articolo

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda dell'articolo per la quale si intende impostare unità di misura alternative.
3. Scegliere l'azione **Unità di misura**. Verrà visualizzata la pagina **Unità di misura articoli**.
4. Se il campo **Unità di misura base** nella scheda articolo è compilato, allora tale unità di misura è già impostata.
5. Scegliere l'azione **Nuovo**. Una nuova riga vuota viene inserita.
6. Nel campo **Codice** immettere il nome dell'unità di misura. In alternativa, selezionare il campo per selezionare i codici di unità di misura che sono nel database.
7. Nel campo **Qtà per unità di misura** immettere il numero dell'unità di misura di base che la nuova unità di misura contiene.
8. Facoltativamente nei campi **Altezza**, **Larghezza**, **Lunghezza** e **Peso** è possibile inserite informazioni precise relative alle dimensioni di un'unità di misura che consenta a [!INCLUDE [prodshort](includes/prodshort.md)] di calcolare automaticamente quante unità articolo possono essere inserite in una determinata collocazione. Il campo **Cubatura** viene calcolato automaticamente in base ad **Altezza**, **Larghezza** e **Lunghezza**.

    Se uno di questi campi contiene un valore diverso da 0, la misura viene utilizzata durante tutti i processi che comportano l'inserimento di articoli in una collocazione: immagazzinamento, movimenti, ricevute, spedizioni, prelievi e rettifiche. [!INCLUDE [prodshort](includes/prodshort.md)] controlla la somma di ogni misura fisica degli articoli in fase di stoccaggio e degli articoli già presenti nella collocazione rispetto alla dimensiona massima o ad altra misura supportata da una collocazione, in base ai criteri di capacità della collocazione presenti nella scheda della collocazione per questo articolo. In altre parole, è necessario utilizzare la stessa unità di misura per ogni dimensione in tutte le unità di misura dell'articolo: ad esempio, utilizzare chilogrammi o libbre per il peso, ma con coerenza.
9. Ripetere i passaggi da 5 a 7 per impostare tutte le unità di misura alternative da utilizzare nei processi diversi per questo articolo.

    Nella parte inferiore della finestra del campo **Unità di misura base** è possibile visualizzare o modificare l'unità di misura di base dell'articolo. È inoltre possibile modificare l'unità di misura di base nel campo **Unità di misura base** nella scheda articolo. Nella pagina **Unità di misura articolo**, l'unità di misura di base deve avere il valore **1** nel campo **Quantità per unità di misura**.

Ora è possibile utilizzare le unità di misura alternative nei documenti di acquisto, produzione e vendita come descritto nella sezione [Inserire un codice unità di misura predefinito per le transazioni di vendita e acquisto](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## <a name="to-set-up-unit-of-measure-translations"></a>Per impostare traduzioni di unità di misura

Se si vendono articoli a clienti stranieri, potrebbe essere necessario indicare l'unità di misura nella lingua del cliente. Questa operazione può essere eseguita impostando le necessarie traduzioni delle unità di misura.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Unità di misura** e quindi scegliere il collegamento correlato.
2. Selezionare il codice per cui si intendono impostare le traduzioni e scegliere l'azione **Traduzioni**.
3. Nel campo **Cod. lingua** selezionare la freccia a discesa per visualizzare una lista dei codici lingua disponibili. Selezionare il codice lingua per il quale si intende immettere la traduzione, quindi fare clic su OK per copiare il codice nel campo.
4. Nel campo **Descrizione**, immettere il testo adeguato.
5. Ripetere i passaggi da 2 a 4 per i codici delle unità di misura e per le lingue per le quali si intendono inserire le traduzioni.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Per immettere codici di unità di misura di default per transazioni di vendita e acquisto

Se si è soliti effettuare acquisti o vendite utilizzando unità di misura diverse dall'unità di misura di base, è possibile definire unità di misura distinte per gli acquisti e per le vendite. A tal fine, le relative unità di misura devono essere impostate nella pagina **Unità di Misura Articoli**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda articolo pertinente per la quale si intende specificare un codice di unità di misura di vendita o acquisto di default.
3. Per le vendite, nella Scheda dettaglio **Fatturazione**, nel campo **Unità di misura vendita** , aprire la pagina **Unità di misura articoli** .
4. Per gli acquisti, nella Scheda dettaglio **Rifornimento**, nel campo **Unità di misura acquisto** , aprire la pagina **Unità di misura articoli** .
5. Selezionare il codice che si intende impostare come unità di misura di default per le vendite o gli acquisti rispettivamente quindi scegliere il pulsante **OK**.

## <a name="see-also"></a>Vedere anche

[Utilizzare le unità di misura batch di produzione](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Gestione dei costi del magazzino](inventory-manage-inventory.md)  
[Gestione acquisti](purchasing-manage-purchasing.md)  
[Gestione vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

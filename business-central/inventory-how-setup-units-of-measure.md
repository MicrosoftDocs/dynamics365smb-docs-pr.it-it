---
title: 'Procedura: Impostare unità di misura articolo | Documenti Microsoft'
description: È possibile impostare più unità di misura per un articolo in modo da poter assegnare le unità di misura all'articolo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 672ddb851b14accf4df3f88bbc0badd775319a68
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309798"
---
# <a name="set-up-item-units-of-measure"></a>Impostare unità di misura articolo
È possibile impostare più unità di misura per un articolo in modo da poter assegnare le unità di misura all'articolo per i seguenti scopi:

- Assegnare un'unità di misura base sulla scheda articolo per definire come viene memorizzata nel magazzino e per essere utilizzata come base di conversione per le unità di misura alternative.
- Assegnare unità di misura alternative ai documenti di acquisto, produzione, o vendita per indicare quante unità dell'unità di misura di base alla volta gestire nei processi. Ad esempio, è possibile acquistare l'articolo in pallet e utilizzare solo i pezzi singoli nella produzione.

Se un articolo viene inserito in stock utilizzando un'unità di misura ma viene prodotto in un'altra, viene creato un ordine di produzione che utilizza un'unità di misura batch di produzione per calcolare la quantità corretta di componenti durante il processo batch **Aggiorna ordine produzione**. Un esempio di calcolo di un'unità di misura è il caso in cui un articolo prodotto viene inserito in stock in pezzi, ma viene prodotto in tonnellate. Per ulteriori informazioni, vedere [Utilizzare le unità di misura batch di produzione](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Per impostare un'unità di misura
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Articoli** e quindi scegliere il collegamento correlato.
2. Aprire la scheda dell'articolo per la quale si intende impostare unità di misura alternative.
3. Scegliere l'azione **Unità di misura**. Verrà visualizzata la pagina **Unità di misura articoli**.
4. Se il campo **Unità di misura base** nella scheda articolo è compilato, allora tale unità di misura è già impostata.
5. Scegliere l'azione **Nuovo**. Una nuova riga vuota viene inserita.
6. Nel campo **Codice** immettere il nome dell'unità di misura. In alternativa, selezionare il campo per selezionare i codici di unità di misura che sono nel database.
7. Nel campo **Qtà per unità di misura** immettere il numero dell'unità di misura di base che la nuova unità di misura contiene.
8. Ripetere i passaggi da 5 a 7 per impostare tutte le unità di misura alternative da utilizzare nei processi diversi per questo articolo.

È ora possibile utilizzare le unità di misura alternative nei documenti di acquisto, produzione e vendita. Per ulteriori informazioni, vedere Immettere codici di unità di misura di default per transazioni di acquisto e di vendita o Utilizzare l'unità di misura batch di produzione.

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

## <a name="see-also"></a>Vedi anche
[Utilizzare le unità di misura batch di produzione](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Gestione dei costi del magazzino](inventory-manage-inventory.md)  
[Gestione acquisti](purchasing-manage-purchasing.md)  
[Gestione vendite](sales-manage-sales.md)    
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

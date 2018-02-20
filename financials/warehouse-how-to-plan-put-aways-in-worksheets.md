---
title: 'Procedura: Pianificare stoccaggi nei prospetti | Documenti Microsoft'
description: "Se l'ubicazione richiede sia l'elaborazione degli stoccaggi che dei carichi e si desidera pianificare le istruzioni di stoccaggio per una serie di carichi, evitando in tal modo che gli addetti seguano le istruzioni create automaticamente per carichi registrati distinti, è possibile utilizzare il prospetto stoccaggi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f1ced6c90333c1da9cbd148f199debdc70ed5a46
ms.contentlocale: it-it
ms.lasthandoff: 01/30/2018

---
# <a name="plan-put-aways-in-worksheets"></a>Pianificare stoccaggi nei prospetti
Se l'ubicazione richiede sia l'elaborazione degli stoccaggi che dei carichi e si desidera pianificare le istruzioni di stoccaggio per una serie di carichi, evitando in tal modo che gli addetti seguano le istruzioni create automaticamente per carichi registrati distinti, è possibile utilizzare il prospetto stoccaggi.  

Per impostare la warehouse in modo che le righe di carico siano rese disponibili nel prospetto stoccaggi non appena vengono registrate, selezionare il campo **Usa prospetto stoccaggi** nella Scheda dettaglio **Warehouse** della scheda ubicazione. Per ulteriori informazioni, vedere [Impostazione gestione warehouse](warehouse-setup-warehouse.md).  

Se non si seleziona questo campo, le istruzioni di stoccaggio per i carichi vengono create automaticamente non appena questi vengono registrati.  

> [!NOTE]  
>  Indipendentemente dallo stato del campo **Usa prospetto stoccaggi** nella scheda ubicazione, è possibile rendere disponibili in qualsiasi momento le righe delle istruzioni di stoccaggio, ovvero le righe dei carichi registrati, nel prospetto di stoccaggio effettuando le seguenti operazioni:  
>   
>  1.  Nella finestra **Stoccaggio warehouse** premere CTRL+D per eliminare l'intera istruzione di stoccaggio oppure selezionare le righe che si desidera elaborare nel prospetto ed eliminarle.  
> 2.  Ripetere il processo per tutti gli stoccaggi di interesse fino a completa eliminazione di tutte le righe che si desidera gestire nel prospetto. A questo punto, scegliere **Prospetti stoccaggio** e procedere alla pianificazione.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Per pianificare le istruzioni nel prospetto di stoccaggio  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "Cerca pagina o report"), immettere **Prospetto stoccaggio**, quindi scegliere il collegamento correlato.  
2.  Scegliere l'azione **Prendi documenti warehouse**. Verrà visualizzata la finestra **Selezione stoccaggio**.  

    In questa finestra vengono visualizzati tutti i carichi registrati e gli stoccaggi interni registrati inoltrati alla funzione di stoccaggio, inclusi quelli per cui sono già state create istruzioni di stoccaggio. I documenti contenenti righe di stoccaggio per le quali lo stoccaggio è stato eseguito per intero e registrato non vengono visualizzati in questa lista.  

3. Selezionare i documenti da gestire nel prospetto. È possibile gestire contemporaneamente righe appartenenti a più documenti.  

    > [!NOTE]  
    >  se si tenta di selezionare un documento di carico o stoccaggio interno per cui sono già state create istruzioni relative a tutte le righe, viene visualizzato un messaggio per informare che non esiste alcun elemento da gestire.  

4. Compilare il campo **Metodo di Sort** per ordinare le righe nel modo desiderato.  

    > [!NOTE]  
    >  La modalità di ordinamento delle righe nel prospetto non viene applicata automaticamente alle istruzioni di stoccaggio, tuttavia esistono le stesse possibilità di ordinamento, unitamente alla valutazione collocazione. L'ordine delle righe pianificato nel prospetto può pertanto essere facilmente riprodotto durante la creazione delle istruzioni di stoccaggio o quando si esegue direttamente l'ordinamento nelle istruzioni di stoccaggio.  

5.  Compilare il campo **Qtà da gestire**. Scegliere l'azione **Autocompil. qtà da gestire** oppure compilare i campi manualmente.  
6.  Se necessario, modificare le righe manualmente. È possibile eliminare righe nel caso in cui, ad esempio, sia necessario stoccare alcuni articoli in una collocazione distante dalle collocazioni per altri tipi di articoli.  

    > [!NOTE]  
    >  le righe vengono eliminate solo da questo prospetto e non dalla lista di selezione degli stoccaggi.  

7.  Selezionare l'azione **Crea stoccaggio**. Verrà visualizzata la finestra **Crea documento** in cui è possibile aggiungere ulteriori informazioni relative allo stoccaggio che si sta creando, come descritto di seguito.  

    -   È possibile assegnare lo stoccaggio a un addetto al magazzino specifico.  
    -   È possibile ordinare le righe delle istruzioni di stoccaggio in base agli stessi criteri di ordinamento utilizzati nel prospetto o in base alla valutazione collocazione. Quando si esegue un ordinamento in base alla valutazione collocazione, le righe Prendere vengono visualizzate per prime, in quanto alla maggior parte delle collocazioni carichi è associata una valutazione pari a 0, mentre le righe Mettere vengono visualizzate per ultime a partire dalle collocazioni con valutazione più bassa. Se la warehouse è stata strutturata in modo che le collocazioni con valutazione simile siano posizionate l'una accanto all'altra, questa modalità di ordinamento delle righe comporta una semplificazione delle operazioni che gli impiegati warehouse dovranno eseguire.  
    -   È possibile scegliere di non visualizzare le righe intermedie create durante la conversione automatica di un'unità di misura più grande in unità di misura più piccole selezionando il campo **Impostare filtro breakbulk**. Per ulteriori informazioni, vedere [Abilitare breakbulk automatico con stoccaggi e prelievi guidati] (warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   È possibile scegliere che il campo **Qtà da gestire** non venga compilato automaticamente nelle istruzioni di stoccaggio.  
    -   È possibile scegliere di stampare il documento immediatamente.  

8.  Scegliere **OK** e lo stoccaggio verrà automaticamente creato in base alle selezioni effettuate.  

## <a name="see-also"></a>Vedi anche  
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


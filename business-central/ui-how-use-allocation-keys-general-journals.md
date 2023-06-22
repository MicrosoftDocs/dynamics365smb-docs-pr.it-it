---
title: Utilizzare le chiavi di allocazione nelle registrazioni COGE
description: 'È possibile assegnare un movimento in una registrazione generale a più conti diversi, quando tale registrazione viene contabilizzata.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.search.form: '283, 284'
ms.date: 06/29/2021
ms.author: edupont
---
# <a name="use-allocation-keys-in-general-journals" />Utilizzare le chiavi di allocazione nelle registrazioni COGE
È possibile assegnare un movimento in una registrazione generale a più conti diversi, quando tale registrazione viene contabilizzata. L'allocazione può essere effettuata per quantità, percentuale o importo.

## <a name="to-set-up-allocation-keys" />Per impostare le chiavi di allocazione
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni periodiche generali**, quindi scegli il collegamento correlato.
2. Scegliere il campo **Nome batch** per aprire la pagina **Batch registrazioni COGE**.
3. È possibile modificare le allocazioni in un batch esistente nell'elenco o creare un nuovo batch con le allocazioni.
   * Per creare un nuovo batch, scegliere l'azione **Nuovo** e andare al passaggio successivo.
   * Per modificare le allocazioni di registrazioni esistenti, selezionare le registrazioni e andare al passaggio 7.    
4. Nel campo **Nome** immettere un nome per il batch, ad esempio PULIZIE. Nel campo **Descrizione** immettere una descrizione, ad esempio Registrazioni spese pulizie.
5. Al termine, chiudere la pagina. Verrà visualizzata una nuova registrazione periodica vuota.
6. Compilare i campi nella riga.
7. Scegliere l'azione **Allocazioni**.
8. Aggiungere una riga per ciascuna allocazione. È necessario compilare il campo **Allocazione %**, **Quantità allocazione** o **Importo**. È necessario compilare anche il campo **Nr. conto** e, se si sta allocando la transazione tra dimensioni globali, anche i campi delle dimensioni globali.
9. Se in una riga è stata immessa una percentuale, il valore del campo **Importo** viene calcolato automaticamente. Questi importi hanno il segno opposto rispetto all'importo totale nel campo **Importo** delle registrazioni periodiche.
10. Dopo aver immesso le righe di allocazione, scegliere **OK** per tornare alla pagina **Reg. periodiche generali**. Il campo **Importo allocato (VL)** viene compilato e corrisponde al campo **Importo**.
11. Effettuare la registrazione.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up" />Per modificare una chiave di allocazione già impostata
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Registrazioni periodiche generali**, quindi scegli il collegamento correlato.
2. Nella pagina **Registrazioni periodiche generali** selezionare le registrazioni con l'allocazione.
3. Selezionare la riga con l'allocazione e scegliere l'azione **Allocazioni**.
4. Cambia i campi pertinenti e quindi scegli **OK**.

## <a name="see-also" />Vedere anche
[Utilizzare le registrazioni COGE](ui-work-general-journals.md)  
[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

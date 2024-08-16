---
title: Panoramica delle attività per l'allocazione di costi e ricavi
description: 'Descrive i task per allocare un movimento in una registrazione COGE periodica a più conti diversi, quando tale registrazione viene contabilizzata.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 08/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="allocate-recurring-costs-and-income"></a>Allocare costi e ricavi periodici

Puoi allocare un movimento in una registrazione COGE periodica a più conti diversi, quando tale registrazione viene contabilizzata. Per ulteriori informazioni sulle registrazioni COGE periodiche, vedi [Utilizzare le registrazioni periodiche](ui-work-general-journals.md#work-with-recurring-journals). 

L'allocazione può essere effettuata in base a tre diversi metodi:

* Quantità
* Percentuale (%)
* Importo

Le funzionalità di allocazione sono utilizzate con le registrazioni COGE periodiche e le registrazioni cespiti.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Di seguito viene descritto come preparare l'allocazione dei costi in una registrazione COGE periodica definendo le chiavi di allocazione. Quando le chiavi di allocazione sono definite, è possibile completare e contabilizzare le registrazioni come qualsiasi altra registrazione COGE periodica. Per ulteriori informazioni, vedere [Utilizzare le registrazioni COGE](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Per impostare le chiavi di allocazione

È possibile allocare un movimento in una registrazione COGE periodica a più conti diversi, quando tale registrazione viene contabilizzata. L'allocazione può essere effettuata per quantità, percentuale o importo.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") Icona, immettere **Giornali generali ricorrenti**, quindi selezionare il relativo collegare.
2. Scegliere il campo **Nome batch** per aprire la pagina **Batch registrazioni COGE**.
3. È possibile modificare le allocazioni in un batch esistente nell'elenco o creare un nuovo batch con le allocazioni.
   * Per creare un nuovo batch, scegliere l'azione **Nuovo** e andare al passaggio successivo.
   * Per modificare le allocazioni di registrazioni esistenti, selezionare le registrazioni e andare al passaggio 7.    
4. Nel campo **Nome** immettere un nome per il batch, ad esempio PULIZIE. Nel campo **Descrizione** immettere una descrizione, ad esempio Registrazioni spese pulizie.
5. Quando sei Fatto, Chiudi nella pagina. Verrà visualizzata una nuova registrazione periodica vuota.
6. Compilare i campi nella riga.
7. Scegliere l'azione **Allocazioni**.
8. Aggiungere una riga per ciascuna allocazione. È necessario compilare il campo **Allocazione %**, **Quantità allocazione** o **Importo**. È inoltre necessario compilare il campo  **Numero di conto** e, se si sta assegnando la transazione tra dimensioni globali, i campi dimensione globale.
9. Se in una riga è stata immessa una percentuale, il valore del campo **Importo** viene calcolato automaticamente. Questi importi hanno il segno opposto rispetto all'importo totale nel campo **Importo** delle registrazioni periodiche.
10. Dopo aver immesso le righe di allocazione, scegliere **OK** per tornare alla pagina **Registrazioni COGE periodiche**. Il campo **Importo allocato (VL)** viene compilato e corrisponde al campo **Importo**.
11. Effettuare la registrazione.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Per modificare una chiave di allocazione già impostata

1. Scegli l'icona ![lampadina che apre la funzionalità Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") Icona, immettere **Giornali generali ricorrenti**, quindi selezionare il relativo collegare.
2. Nella pagina  **Giornali generali ricorrenti**, Seleziona il giornale con l'allocazione.
3. Selezionare la riga con l'allocazione e scegliere l'azione **Allocazioni**.
4. Cambia i campi pertinenti e quindi scegli **OK**.

## <a name="see-also"></a>Vedere anche

[Anni e periodi di chiusura](year-close-years-periods.md)    
[Elaborazione delle registrazioni COGE](ui-work-general-journals.md)    
[Contabilizzazione dei documenti e delle registrazioni](ui-post-documents-journals.md)    
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

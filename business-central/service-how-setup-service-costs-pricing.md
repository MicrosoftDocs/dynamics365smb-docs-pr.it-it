---
title: Impostare prezzi e costi per servizi assistenza
description: 'Scopri come utilizzare le funzionalità di definizione dei prezzi per impostare e personalizzare l''applicazione in modo da poter applicare e rettificare i prezzi per articoli in assistenza, riparazioni e ordini.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/25/2021
ms.author: bholtorf
---

# <a name="set-up-pricing-and-additional-costs-for-services"></a>Impostare prezzi e costi aggiuntivi per i servizi assistenza
È possibile utilizzare le funzionalità di definizione dei prezzi di [!INCLUDE[prod_short](includes/prod_short.md)] per impostare e personalizzare l'applicazione in modo da poter applicare e rettificare i prezzi per articoli in assistenza, riparazioni e ordini. Queste decisioni relative ai prezzi potranno essere in seguito agevolmente trasmesse al processo di fatturazione.  
  
Come previsto dall'implementazione, si possono impostare gruppi di prezzi associandoli a specifici periodi di tempo, clienti o valute. È anche possibile impostare prezzi fissi, minimi o massimi, a seconda dei contratti di assistenza in atto con i vari clienti. Infine, in fase di rettifica dei prezzi, è possibile visualizzare e approvare le modifiche prima di applicarle alla contabilità.  

## <a name="to-set-up-a-service-price-group"></a>Per impostare un gruppo di prezzi in assistenza
È possibile impostare gruppi contenenti articoli in assistenza a cui si desidera vengano applicate le stesse definizioni speciali del prezzo di assistenza. I gruppi dei prezzi di assistenza vengono assegnati ad articoli in assistenza nelle righe di articoli in assistenza. È inoltre possibile assegnare gruppi di prezzi di assistenza ai gruppi di articoli in assistenza.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi prezzo assistenza**, quindi scegli il collegamento correlato.  
2. Creare un nuovo gruppo di prezzi di assistenza.  
3. Compilare i campi **Codice** e **Descrizione**.  
4. Scegliere l'azione **Setup**.  
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Con i campi **Tipo rettifica** e **Importo**, è possibile specificare se una rettifica riguarderà un importo fisso oppure verrà applicata esclusivamente ai prezzi totali di assistenza che supereranno o saranno inferiori all'importo specificato nel campo **Importo**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Per impostare un gruppo di rettifica dei prezzi di assistenza
È possibile impostare i gruppi di rettifica del prezzo per rettificare il prezzo di assistenza degli articoli in assistenza. Ad esempio, è possibile impostare gruppi di rettifica del prezzo per modificare il costo di spedizione o dei pezzi di ricambio.  
  
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Gruppi rettifica prezzo assistenza**, quindi scegli il collegamento correlato.  
2. Creare un nuovo gruppo di rettifica dei prezzi di assistenza.  
3. Compilare i campi **Codice** e **Descrizione**.  
4. Nel campo **Tipo** immettere il tipo del movimento da rettificare.  
  
    * Per rettificare un solo movimento specifico, immettere il numero di tale movimento nel campo **Nr.**   Se questo campo viene lasciato vuoto, il gruppo di rettifica andrà a rettificare tutti i movimenti del tipo definito nel campo **Tipo**.  
    * Per rettificare i prezzi di assistenza in base a un determinato servizio di assistenza, compilare il campo **Tipo di lavoro**. Se questo campo viene lasciato vuoto, l'impostazione verrà ignorata.  
  
5. Nel campo **Descrizione** immettere una breve descrizione della rettifica dei prezzi di assistenza.  
6. Per rettificare i prezzi di assistenza relativi a una determinata categoria di registrazione articoli/servizi, compilare il campo **Cat. reg. articolo/servizio**.

> [!Tip]
> È possibile scegliere **Dettagli** per aggiungere altre informazioni relative al gruppo di rettifica. Ad esempio, specificare quale articolo appartiene al gruppo di rettifica dei prezzi di assistenza e se si tratta di un articolo, una risorsa, un gruppo di risorse o un addebito di assistenza.  

## <a name="to-set-up-additional-costs-for-services"></a>Per impostare costi aggiuntivi per i servizi assistenza
Quando si utilizzano articoli in assistenza e ordini di assistenza, potrebbe essere necessario registrare costi aggiuntivi, quali le spese di viaggio in determinate zone di assistenza o le spese iniziali. Quando si crea un ordine di assistenza, è possibile inserire tali costi e verrà aggiunta una riga con il tipo **Costo**. In alternativa, se si desidera applicare il costo a tutti gli ordini di assistenza, è possibile impostare un costo di default. Ad esempio, se si desidera applicare sempre una spesa iniziale.
  
### <a name="to-set-up-service-costs"></a>Per impostare i costi di assistenza
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Costi assistenza**, quindi scegli il collegamento correlato. 
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Per specificare un costo di default per gli ordini di assistenza
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup assistenza**, quindi scegli il collegamento correlato. 
2. Nel campo **Tariffa iniziale ordine assistenza** selezionare il costo di assistenza appropriato.

## <a name="see-also"></a>Vedere anche
[Impostazione della gestione assistenza](service-setup-service.md)  
[Gestione assistenza](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

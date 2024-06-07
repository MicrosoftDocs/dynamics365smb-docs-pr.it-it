---
title: Creare fatture o note di credito per servizi di assistenza
description: Scopri come creare fatture e note di credito per i servizi di assistenza.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-service-invoices-or-credit-memos"></a>Creare fatture o note di credito di assistenza

La facilità di fatturazione degli ordini di assistenza è una caratteristica chiave di [!INCLUDE[prod_short](includes/prod_short.md)]. È possibile impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo che un tecnico dell'assistenza possa creare una fattura di assistenza non collegata ad alcun contratto o ordine esistente. In alternativa, impostare [!INCLUDE[prod_short](includes/prod_short.md)] in modo da fatturare periodicamente i contratti di assistenza. Il periodo di fatturazione di ogni contratto definisce con quale frequenza avviene la fatturazione.

## <a name="to-invoice-several-service-contracts"></a>Per fatturare più contratti di assistenza

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Crea fatture contratto assistenza**, quindi seleziona il collegamento correlato.  
2. Impostare i filtri che si desidera applicare.  
3. Nel campo **Data di registrazione** inserire la data che si intende utilizzare come data di registrazione nelle fatture di assistenza.  
4. Nel campo **Fattura Alla Data** immettere la data fino a cui si intendono fatturare contratti. Il processo batch includerà i contratti con le date di fatturazione successive fino a tale data.  
5. Nel campo **Azione** scegliere **Crea fatture**.  
6. Scegliere **OK** per creare le fatture di assistenza.  
  
È anche possibile fatturare un contratto di assistenza direttamente dalla pagina **Contratto di Assistenza** se la data della prossima fatturazione nel contratto risulta precedente alla data di lavoro.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Per fatturare un contratto di assistenza dalla pagina Contratto assistenza

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Contratti assistenza**, quindi scegli il collegamento correlato.  
2. Scegliere il contratto di assistenza da fatturare e aprire la scheda contratto.  
3. Scegliere l'azione **Crea fattura assistenza**. 
4. Scegliere **Sì** per creare le fatture di assistenza.  
  
  > [!NOTE]  
  > Non è possibile creare fatture di assistenza per il contratto di assistenza quando il valore del campo **Modifica stato** è impostato su **Aperto**.  

## <a name="to-post-an-invoice-from-a-service-order"></a>Per registrare una fattura da un ordine di assistenza

La procedura seguente indica le modalità di definizione della parte dei servizi di assistenza da addebitare al cliente.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ordini assistenza**, quindi scegli il collegamento correlato.  
2. Scegliere l'ordine di assistenza da fatturare e aprire la scheda ordine.  
3. Scegliere l'azione **Righe assistenza**.  
4. Individuare i movimenti necessari, quindi specificare le quantità da addebitare al cliente nel campo **Qtà da fatturare**.  
  
   > [!NOTE]  
   > È possibile emettere una fattura relativa all'assistenza registrata totale o parziale. Se la fattura è totale, il valore del campo **Qtà da fatturare** deve corrispondere a quello del campo **Quantità**. È possibile registrare una fattura totale con una spedizione completa ed è possibile registrare una fattura totale per una spedizione completa già registrata non fatturata né consumata.  
   >  
   > Quando si registra una fattura parziale, è possibile specificare la quantità da fatturare in due modi diversi. Se l'assistenza viene registrata mediante l'opzione **Spedisci e fattura**, il valore del campo **Qtà da fatturare** deve corrispondere al valore del campo **Qtà da spedire**. Se si desidera fatturare una spedizione già registrata, la quantità da fatturare non deve superare il valore specificato nel campo **Quantità spedita**.  
  
5. Scegliere **Registra**, quindi **Fattura** o **Spedisci e fattura**. Per ulteriori informazioni, vedi [Registrazione in Gestione assistenza](service-service-posting.md).  
  
 La riga di assistenza selezionata viene registrata. È possibile registrare diverse righe di assistenza contemporaneamente selezionandole e scegliendo **Registra**. Se si esegue questa operazione, verificare di immettere tutte le informazioni necessarie nelle righe.  
  
 Se si registra l'ordine mediante l'opzione **Fattura**, verrà creata una fattura di assistenza registrata con i movimenti contabili corrispondenti e verranno aggiornati i campi relativi nelle righe di assistenza dell'ordine. Inoltre, vengono aggiornati i documenti di spedizione registrati in precedenza con le quantità fatturate. Se si seleziona l'opzione di registrazione **Spedisci e fattura**, verrà creata una spedizione registrata.

## <a name="to-create-a-service-invoice-manually"></a>Per creare una fattura di assistenza manualmente

In genere, dopo la registrazione di un ordine di assistenza mediante l'opzione **Fattura** o **Spedisci e fattura**, verrà registrata automaticamente una fattura di assistenza. Può essere tuttavia necessario emettere una fattura che non è collegata a un contratto di assistenza o a un ordine di assistenza. Di seguito vengono descritte le modalità di emissione di una fattura nel momento in cui il cliente riceve l'assistenza.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture assistenza**, quindi scegli il collegamento correlato.  
2. Creare una nuova fattura di assistenza.  
3. Compilare debitamente i campi **Nr.**    
  
    > [!NOTE]  
    >  Se hai impostato una numerazione per le fatture di assistenza nella pagina **Setup gest. assist.**, puoi selezionare **INVIO** per selezionare il numero successivo di fattura di assistenza disponibile.  
  
4. Nel campo **Nr. cliente** immettere il numero di un cliente. Selezionare il cliente appropriato dalla lista.  
  
    I campi del cliente vengono compilati con le informazioni della scheda **Cliente**.  
  
5. Immettere una data nel campo **Data di registrazione**. Tale data verrà visualizzata sui movimenti registrati. Questo campo mostra la data del lavoro corrente, che può essere modificata.  
6. Nel campo **Data documento** immettere una data che verrà visualizzata nella fattura stampata e utilizzata per calcolare la data di scadenza.  
7. Compilare le righe di assistenza della fattura. Compilare i campi **Tipo**, **Nr.** e **Quantità** per registrare articoli, risorse e costi utilizzati durante le operazioni di assistenza.

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders"></a>Per creare una fattura che combina le righe di spedizione registrate da uno o più ordini di assistenza

Può essere necessario creare una fattura relativa a un'assistenza che è già stata spedita da uno o più ordini, ma non ancora fatturata o consumata. È possibile compilare automaticamente le righe della fattura con le righe di spedizione registrate e selezionate relative a un cliente specifico.  

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Fatture assistenza**, quindi scegli il collegamento correlato.  
2. Compilare i campi della riga in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Creare righe di fattura per servizi di assistenza spediti, ma non fatturati. In alternativa, è possibile utilizzare l'azione **Prendi righe di spedizione** per aggiungere righe di spedizione registrate alla fattura.  
4. Registrare la fattura di assistenza.  
  
 Verranno creati la fattura di assistenza registrata e i movimenti contabili corrispondenti. I documenti di spedizione registrati in precedenza vengono aggiornati con le quantità fatturate e le quantità nelle righe di assistenza degli ordini di origine.  

## <a name="to-create-a-service-credit-memo"></a>Per creare una nota di credito di assistenza

In genere si utilizza un documento di nota di credito di assistenza quando un cliente restituisce un articolo. Puoi però utilizzarli anche per rimborsare un cliente o per correggere una fattura errata.  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Note credito assistenza**, quindi scegli il collegamento correlato.  
2. Compilare i campi della riga come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nei campi **Data di registrazione** e **Data documento** viene visualizzata la data di lavoro. Se necessario, è possibile modificarla.    
4. Nelle righe della nota di credito immettere le informazioni relative agli articoli resi o rimossi oppure al risarcimento concesso al cliente.  

## <a name="correct-errors-in-service-invoices"></a>Correggere gli errori nelle fatture di assistenza

È possibile eliminare le fatture di assistenza a cui sono associati movimenti contabili di assistenza. Ciò significa che puoi correggere errori o apportare modifiche alle fatture di assistenza senza rimanere bloccato o perdere dati. Ad esempio, se si dimentica di assegnare una categoria di registrazione prodotto a un conto C/G, è possibile aggiungerla in un secondo momento e ricreare la fattura di assistenza.

Usa l'azione :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="Elimina icona azione"::: per eliminare una fattura di assistenza. 

Quando elimini una fattura di assistenza, si verifica quanto segue:

* Registrazione di un movimento contabile di assistenza correttivo
* Ripristino della data e del periodo di fatturazione nel contratto, in modo da poter creare nuovamente la fattura.

> [!NOTE]
> Puoi annullare più fatture, ma devi farlo in sequenza, a partire dall'ultima fattura.
>
> Non è possibile eliminare una fattura di assistenza se i relativi dettagli, come il periodo di fatturazione o l'interruttore **Prepagato** sono stati modificati nel relativo contratto di assistenza. Assicurati di eliminare le fatture prima di modificare le impostazioni del contratto di assistenza.

## <a name="see-also"></a>Vedere anche

[Registrare le fatture di assistenza](service-how-to-post-service-orders.md)  
[Impostazione della gestione assistenza](service-setup-service.md)  
[Registrazione di assistenza](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

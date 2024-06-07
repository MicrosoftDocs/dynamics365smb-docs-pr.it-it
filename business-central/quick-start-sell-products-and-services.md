---
title: Inizio rapido delle vendite (video)
description: Impara come riempire i primi campi critici su prodotti e clienti in Business Central in modo da poter iniziare i tuoi processi di vendita.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="sales-quick-start"></a>Inizio rapido delle vendite

Per essere in grado di vendere prodotti e servizi, devi prima impostare articoli e clienti. Una volta fatto questo, si può iniziare a registrare gli ordini di vendita e inviare le fatture.

## <a name="set-up-items-to-sell"></a>Impostare gli articoli da vendere

Questo video mostra come impostare un oggetto da vendere in [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### <a name="set-up-a-new-item"></a>Impostare un nuovo elemento

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Per maggiori informazioni e ulteriori cose che puoi fare quando imposti gli articoli, vedi [Registrare nuovi articoli](inventory-how-register-new-items.md).  

## <a name="set-up-customers"></a>Impostare i clienti

Questo video mostra come impostare un nuovo cliente in [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### <a name="set-up-a-new-customer"></a>Impostare un nuovo cliente

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Per maggiori informazioni e ulteriori cose che puoi fare quando imposti i clienti, vedi [Registrare nuovi clienti](sales-how-register-new-customers.md)

## <a name="create-a-sales-order"></a>Creare un ordine di vendita

Quando si vende qualcosa a un cliente, si hanno due opzioni. Il primo, e più semplice, è quello di creare semplicemente una fattura di vendita. Tuttavia, se il vostro processo di vendita è più complesso, per esempio se avete situazioni in cui spedite solo parti di una quantità d'ordine, usate un ordine di vendita.

### <a name="to-create-a-sales-order"></a>Per creare un ordine di vendita

1. Scegli la ![lampadina che apre la funzione Dimmi 10](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Ordini vendita**, quindi seleziona il collegamento correlato.
2. Selezionare **Nuovo** per creare una nuova voce.
3. Nel campo **Cliente** immettere il nome di un cliente esistente.

    Altri campi nella pagina **Ordine di vendita** vengono compilati con le informazioni standard del cliente selezionato.  

4. Compilare i restanti campi della pagina **Ordine di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Nella Scheda dettaglio **Righe** nel campo **Tipo** selezionare il tipo di prodotto, addebito o transazione per cui si effettuerà la registrazione per il cliente con la riga di vendita.

6. Nel campo **Nr.** immettere il numero di un'assistenza o di un articolo di magazzino.

7. Nel campo **Quantità** immettere il numero di articoli da vendere.

8. Nel campo **% sconto riga** immettere una percentuale se si intende concedere al cliente uno sconto sul prodotto.

9. Per aggiungere un commento sulla riga dell'ordine che il cliente può vedere sull'ordine di vendita stampato, scrivi un commento nel campo **Descrizione** su una riga vuota.

10. Ripeti i passi da 5 a 9 per ogni articolo che vuoi vendere al cliente.

11. Per spedire solo una parte della quantità ordinata, immettere la quantità desiderata nel campo **Qtà da spedire**. Il valore viene copiato nel campo **Qtà da fatturare**.

12. Per fatturare solo una parte della quantità spedita, immettere la quantità desiderata nel campo **Qtà da fatturare**. La quantità deve essere inferiore al valore presente nel campo **Qtà da spedire**.

13. Una volta completate le righe dell'ordine di vendita, scegliere l'azione **Registra e invia**.

Per maggiori informazioni e ulteriori cose che puoi fare quando crei ordini di vendita al cliente, vedi [Vendere prodotti con un ordine di vendita al cliente](sales-how-sell-products.md).  

## <a name="create-a-sales-invoice"></a>Creare una fattura di vendita

Quando crei e posti una fattura di vendita, non solo crei il documento della fattura che invii al cliente, ma crei anche le relative voci di quantità e valore in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="to-create-and-post-a-sales-invoice"></a>Per creare e pubblicare una fattura di vendita

1. Scegli la ![lampadina che apre la funzione Dimmi 20](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Fatture vendite**, quindi seleziona il collegamento correlato.  

2. Selezionare **Nuovo** per creare una nuova voce.

3. Nel campo **Cliente** immettere il nome di un cliente esistente.

4. Compilare i restanti campi della pagina **Fattura di vendita** in base alle proprie esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Nella FastTab **Righe**, nel campo **Tipo**, selezionare il tipo di prodotto, addebito o transazione che si vuole registrare per il cliente con la linea di vendita.

6. Nel campo **Nr.** selezionare un record per effettuare la registrazione in base al valore nel campo **Tipo**.

7. Nel campo **Quantità** immettere qui il numero di unità di articoli, addebiti o transazioni che la riga registrerà per il cliente.  

8. Se si desidera assegnare uno sconto, immettere una percentuale nel campo **% sconto riga**. Il valore nel campo **Importo riga** viene aggiornato di conseguenza.  

9. Ripetere i passaggi da 5 a 8 per ogni prodotto o addebito che si desidera fatturare al cliente.  

10. Nel campo **Importo sconto fattura** immettere un importo che deve essere dedotto dal valore indicato nel campo **Totale IVA incl.**.

11. Una volta completate le righe della fattura di vendita, scegliere l'azione **Registra e invia**.  

Per maggiori informazioni e ulteriori cose che puoi fare quando crei fatture di vendita per i clienti, vedi [Fattura di vendita](sales-how-invoice-sales.md)

## <a name="see-also"></a>Vedere anche

[Avviamento rapido di Business Central](quick-start-business-central.md)  
[Panoramica delle vendite](sales-manage-sales.md)  
[Vendere prodotti con un ordine di vendita al cliente](sales-how-sell-products.md)  
[Fatturare le vendite](sales-how-invoice-sales.md)  

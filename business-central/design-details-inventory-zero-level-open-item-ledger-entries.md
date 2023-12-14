---
title: Movimenti contabili articoli aperti con inventario zero
description: In questo articolo viene discusso un problema in cui il livello di scorte è pari a zero sebbene vi siano movimenti contabili articoli aperti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="design-details-known-item-application-issue"></a>Dettagli di progettazione: Problema noto di collegamento articoli
In questo articolo viene discusso un problema in cui il livello di magazzino è pari a zero sebbene vi siano movimenti contabili articoli aperti in [!INCLUDE[prod_short](includes/prod_short.md)].  

L'articolo inizia elencando gli indizi tipici del problema, seguiti dai concetti di base del collegamento articoli per supportare i motivi descritti per tale problema. Alla fine dell'articolo viene fornita una soluzione alternativa per gestire tali movimenti contabili articoli aperti.  

## <a name="symptoms-of-the-issue"></a>Indizi del problema
 Gli indizi tipici del problema con magazzino zero anche se esistono movimenti contabili articoli aperti sono i seguenti:  

-   Il seguente messaggio quando si tenta di chiudere un periodo di magazzino: "The inventory cannot be closed because there is negative inventory for one or more items.".  

-   Una situazione di movimento contabile articolo in cui un movimento contabile articolo in uscita e il relativo movimento contabile articolo in entrata sono entrambi aperti.  

     Vedere il seguente esempio di una situazione con movimento contabile articolo.  

     |Nr. movimento|Data di registrazione|Tipo movimento|Tipo di documento|Nr. documento|Nr. articolo|Cod. ubicazione|Quantità|Importo costo (effettivo)|Quantità fatturata|Quantità residua|Apri|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|28/01/2018|Vendita|Spedizioni vendita|102043|TEST|BLU|-1|-10|-1|-1|Sì|  
     |334|28/01/2018|Vendita|Spedizioni vendita|102043|TEST|BLU|1|10|1|1|Sì|  

## <a name="basics-of-item-application"></a>Nozioni di base del collegamento articoli
 Un movimento di collegamento articoli viene creato per ogni transazione di magazzino per collegare il destinatario di costo alla relativa origine del costo in modo da poter trasferire il costo in base al metodo di costing. Per ulteriori informazioni, vedere [Dettagli di progettazione: Collegamento articoli](design-details-item-application.md).  

-   Per un movimento contabile articolo in entrata, il movimento di collegamento articoli viene creato alla creazione del movimento contabile articolo.  

-   Per un movimento contabile articolo in uscita, il movimento di collegamento articoli viene creato alla registrazione del movimento contabile di articolo, SE esiste un movimento contabile articolo in entrata aperto con la quantità disponibile a cui può essere collegato. Se non è presente un movimento contabile articolo in entrata aperto a cui eseguire il collegamento, il movimento contabile articolo in uscita rimane aperto fino alla registrazione del movimento contabile articolo in entrata a cui può essere collegato.  

 Vi sono due tipi di collegamento articoli:  

-   Collegamento della quantità  

-   Collegamento costo  

### <a name="quantity-application"></a>Collegamento della quantità
 I collegamenti quantità vengono eseguiti per tutte le transazioni di magazzino e sono creati automaticamente, oppure manualmente in processi speciali. Quando creati manualmente, i collegamenti quantità sono denominati collegamenti fissi.  

 L'illustrazione seguente mostra come vengono eseguiti i collegamenti quantità.  

![Flusso di rettifica dei costi dall'acquisto alla vendita.](media/helene/TechArticleInventoryZero2.png "Flusso di rettifica dei costi dall'acquisto alla vendita")

 Da notare che il movimento contabile articolo 1 (Acquisto) è il fornitore dell'articolo e l'origine del costo per il movimento contabile articolo collegato, movimento contabile articolo 2 (Vendita).  

> [!NOTE]  
>  Se il movimento contabile articolo in uscita viene valutato per costo medio, il movimento contabile articolo in entrata collegato non è l'origine del costo univoca. Svolge semplicemente un ruolo nel calcolo del costo medio del periodo.  

### <a name="cost-application"></a>Collegamento costo
I collegamenti costo sono creati solo per le transazioni in entrata dove il campo **Collega-da mov. art.** viene compilato per fornire un collegamento fisso. Questo avviene in genere in relazione a una nota di credito di vendita oppure a uno scenario con eliminazione della spedizione. Il collegamento costo garantisce che l'articolo viene immesso di nuovo in magazzino con lo stesso costo di quando è stato spedito.  

Il diagramma seguente mostra come vengono eseguiti i collegamenti costo.  

|Nr. movimento|Data di registrazione|Tipo movimento|Tipo di documento|Nr. documento|Nr. articolo|Cod. ubicazione|Quantità|Importo costo (effettivo)|Quantità fatturata|Quantità residua|Apri|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|28/01/2018|Vendita|Spedizioni vendita|102043|TEST|BLU|-1|-10|-1|-1|Sì|  
|334|28/01/2018|Vendita|Spedizioni vendita|102043|TEST|BLU|1|10|1|1|Sì|  

 Da notare che il movimento contabile articolo in entrata 3 (Reso vendita) è un destinatario di costo per il movimento contabile articolo in uscita 2 (Vendita).  

## <a name="illustration-of-a-basic-cost-flow"></a>Illustrazione di un flusso dei costi di base
 Si supponga un flusso dei costi completo in cui un articolo viene ricevuto, spedito e fatturato, reso con lo storno del costo\-esatto e spedito nuovamente.  

 Il seguente diagramma illustra il flusso dei costi.  

![Flusso di rettifica dei costi dalla vendita al reso di vendita.](media/helene/TechArticleInventoryZero4.png "Flusso di rettifica dei costi dalla vendita al reso di vendita")

 Da notare che il costo viene trasferito al movimento contabile articolo 2 (Vendita), quindi al movimento contabile articolo 3 (Reso vendita) e infine al movimento contabile articolo 4 (Vendita 2).  

## <a name="reasons-for-the-issue"></a>Motivi del problema
 Il problema con magazzino zero sebbene esistano movimenti contabili articolo aperti può essere causato dai seguenti scenari:  

-   Scenario 1: Una spedizione e una fattura vengono registrati anche se l'articolo non è disponibile. La registrazione viene quindi stornata del costo esatto con una nota di credito di vendita.  

-   Scenario 2: Una spedizione viene registrata anche se l'articolo non è disponibile. La registrazione viene quindi annullata con la funzione Elimina spedizione.  

 L'illustrazione seguente mostra come vengono eseguiti i collegamenti articolo in entrambi gli scenari  

![Il flusso di rettifica dei costi va in entrambe le direzioni.](media/helene/TechArticleInventoryZero6.png "Il flusso di rettifica dei costi va in entrambe le direzioni")  

 Da notare che un collegamento costo viene eseguito (frecce blu) per garantire che al movimento contabile articolo 2 (Reso vendita) siano assegnati gli stessi costi del movimento contabile articolo stornato, movimento contabile articolo 1 (Vendita). Tuttavia, un collegamento quantità (frecce rosse) non viene eseguito.  

 Il movimento contabile articolo 2 (Reso vendita) non può essere un destinatario di costo del movimento contabile articolo originale e allo stesso tempo un fornitore degli articoli e la relativa origine dei costi. Di conseguenza, il movimento contabile articolo originale 1 (Vendita 1) rimane aperto fino a che non si ha un origine valida.  

## <a name="identifying-the-issue"></a>Identificazione del problema
 Per determinare se i movimenti contabili articolo aperti sono stati creati, procedere nel modo seguente:  

 Per lo scenario 1, identificare il problema nel modo seguente:  

-   Nella pagina **Nota cred. di vend. reg.** o **Carico da reso registrato**, verificare se il campo **Collega\-da mov. art.** è compilato e in tal caso a quale movimento contabile articolo il carico da reso è collegato al costo.  

 Per lo scenario 2, identificare il problema in uno dei due seguenti modi:  

-   Cercare un movimento contabile articolo in uscita aperto e un movimento contabile articolo in entrata con lo stesso numero nel campo **Nr. documento** e Sì nel campo **Correzione**. Vedere il seguente esempio di tale situazione con movimento contabile articolo.  

|Nr. movimento|Data di registrazione|Tipo movimento|Tipo di documento|Nr. documento|Nr. articolo|Cod. ubicazione|Quantità|Importo costo (effettivo)|Quantità fatturata|Quantità residua|Apri|Correzione|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|28/01/2018|Vendita|Spedizioni vendita|102043|TEST|BLU|-1|-10|-1|-1|Sì|No|  
|334|28/01/2018|Vendita|Spedizioni vendita|102043|TEST|BLU|1|10|1|1|Sì|**Sì**|  

-   Nella pagina **Spedizioni vendita registrate**, verificare se il campo **Collega-da mov. art.** è compilato e in tal caso a quale movimento contabile articolo il carico da reso è collegato al costo.  

> [!NOTE]  
>  I collegamenti costo non possono essere identificati nella pagina **Mov. articoli collegati** perché quella pagina visualizza solo i collegamenti quantità.  

 Per entrambi gli scenari, identificare il collegamento costo interessato nel modo seguente:  

1.  Aprire la tabella **Mov. collegamento articoli**.  

2.  Filtrare in base al campo **Nr. movimento cont. articolo** utilizzando il numero del movimento contabile articolo Reso vendita.  

3.  Analizzare il movimento di collegamento articoli, prendendo nota di quanto segue:  

     Se il campo **Nr. movimento articolo in uscita** viene compilato per un movimento contabile articolo in entrata (quantità positiva), significa che il movimento contabile articolo in entrata è il destinatario di costo del movimento contabile articolo in uscita.  

     Vedere il seguente esempio di un movimento di collegamento articoli.  

     |Nr. movimento|Nr. movimento cont. articolo|Nr. movimento articolo in entrata|Nr. movimento articolo in uscita|Quantità|Data di registrazione|Collegamento costo|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|28/01/2018|Sì|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Da notare che il movimento contabile articolo in entrata 334 è collegato al costo al movimento contabile articolo in uscita 333.  

## <a name="workaround-for-the-issue"></a>Soluzione alternativa per il problema
 Nella pagina **Registrazioni magazzino**, registrare le seguenti righe per l'articolo in questione:  

-   Una rettifica positiva per chiudere il movimento contabile articolo in uscita aperto.  

-   Una rettifica negativa con la stessa quantità.  

     Questa rettifica compensa l'aumento di magazzino causato da quella positiva e chiude il movimento contabile articolo in entrata aperto.  

 Il risultato è un magazzino pari a zero e tutti i movimenti contabili articolo sono chiusi.  

## <a name="see-also"></a>Vedi anche
[Dettagli di progettazione: Collegamento articoli](design-details-item-application.md)   
[Dettagli di progettazione: Costing di magazzino](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

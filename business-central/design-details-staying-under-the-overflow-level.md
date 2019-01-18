---
title: 'Dettagli di progettazione: Al di sotto del livello di overflow | Microsoft Docs'
description: "Quando si utilizzano i campo Qtà Massima e Qtà Riordino Fissa, il sistema di pianificazione si concentra solo sulle giacenze previste nell'intervallo di tempo specificato. Ciò significa che il sistema di pianificazione può suggerire un approvvigionamento superfluo quando si verificano dei cambiamenti nella domanda negativa o nell'approvvigionamento positivo al di fuori dell'intervallo di tempo specificato."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: a4a35cec571f1a0c7644fe937553d87007a9567e
ms.contentlocale: it-it
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a>Dettagli di progettazione: Al di sotto del livello di overflow
Quando si utilizzano i metodi Qtà Massima e Qtà Riordino Fissa, il sistema di pianificazione si concentra solo sulle giacenze previste nell'intervallo di tempo specificato. Ciò significa che il sistema di pianificazione può suggerire un approvvigionamento superfluo quando si verificano dei cambiamenti nella domanda negativa o nell'approvvigionamento positivo al di fuori dell'intervallo di tempo specificato. Se, per questo motivo, viene suggerito un approvvigionamento inutile, il sistema di pianificazione calcola la quantità alla quale l'approvvigionamento dovrebbe essere ridotto (o eliminato) per evitare l'approvvigionamento superfluo. Questa quantità è denominata “livello di overflow”. L'overflow viene comunicato come una riga di pianificazione con un'azione **Cambia Qtà (riduzione)** o **Annulla** e il seguente messaggio di avviso:  

*Attenzione: La giacenza disponibile [xx] è superiore al livello di overflow [xx] alla data di scadenza [xx].*  

![Livello di overflow del magazzino](media/supplyplanning_2_overflow1_new.png "Livello di overflow del magazzino")  

##  <a name="calculating-the-overflow-level"></a>Calcolo del livello di overflow  
Il livello di overflow viene calcolato in modi diversi a seconda dell'impostazione della pianificazione.  

### <a name="maximum-qty-reordering-policy"></a>Metodo di riordino di Qtà Massima  
Livello di overflow = giacenza massima  

> [!NOTE]  
>  Se è presente una quantità ordine minima, verrà aggiunta come segue: Livello di overflow = giacenza massima + quantità ordine minima.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Metodo di riordino Qtà Riordino Fissa  
Livello di overflow = quantità di riordino + punto di riordino  

> [!NOTE]  
>  Se la quantità di ordine minima è superiore al punto di riordino, sarà sostituita come segue: Livello di overflow = quantità di riordino + quantità ordine minima  

### <a name="order-multiple"></a>Molteplicità ordine  
In presenza di una molteplicità di ordini, verrà rettificato il livello di overflow per i metodi di riordino sia Quantità massima che Quantità riordino fissa.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Creazione della riga di pianificazione con avviso di overflow  
Quando un approvvigionamento esistente determina un aumento della giacenza disponibile oltre il livello di overflow alla fine di un intervallo di tempo, viene creata una riga di pianificazione. Per avvisare del potenziale approvvigionamento superfluo, la riga di pianificazione contiene un messaggio di avviso, il campo **Accetta messaggio azione** non è selezionato e il messaggio di azione è Annulla o Cambia Qtà.  

### <a name="calculating-the-planning-line-quantity"></a>Calcolo della quantità della riga di pianificazione  
Quantità della riga di pianificazione = quantità dell'approvvigionamento corrente - (scorte previste - livello di overflow)  

> [!NOTE]  
>  Analogamente a tutte le righe di avviso, tutte le quantità ordine minime e massime o di ordine multiplo verranno ignorate.  

### <a name="defining-the-action-message-type"></a>Definizione del tipo di messaggio di azione  

-   Se la quantità della riga di pianificazione è uguale o superiore a 0, il messaggio di azione sarà Cambia qtà.  
-   Se la quantità della riga di pianificazione è uguale o inferiore a 0, il messaggio di azione sarà pari ad Annulla  

### <a name="composing-the-warning-message"></a>Composizione del messaggio di avviso  
In caso di overflow, nella pagina **Elementi di pianificazione non tracciati** viene visualizzato un messaggio di avviso con le informazioni seguenti:  

-   Livello di giacenza disponibile che ha attivato l'avviso  
-   Livello di overflow calcolato  
-   Data di scadenza dell'evento di approvvigionamento.  

Esempio: "La giacenza disponibile 120 è superiore al livello di overflow 60 in 28-01-11”  

## <a name="scenario"></a>Scenario  
In questo scenario, un cliente modifica un ordine di vendita da 70 a 40 pezzi tra due esecuzioni di pianificazione. La funzionalità di overflow consente di ridurre l'acquisto che è stato suggerito per la quantità di vendita iniziale.  

### <a name="item-setup"></a>Impostazione articolo  

|Metodo di riordino|Qtà Massima|  
|-----------------------|------------------|  
|Quantità massima ordine|100|  
|Punto riordino|50|  
|Magazzino|80|  

### <a name="situation-before-sales-decrease"></a>Situazione prima della riduzione della vendita  

|Evento|Cambia Qtà|Quantità scorte previste|  
|-----------|-----------------|-------------------------|  
|Giorno uno|Nessuno|80|  
|Vendite|-70|10|  
|Fine dell'intervallo di tempo|Nessuno|10|  
|Suggerire nuovo ordine di acquisto|+90|100|  

### <a name="situation-after-sales-decrease"></a>Situazione dopo la riduzione della vendita  

|Cambia|Cambia Qtà|Quantità scorte previste|  
|------------|-----------------|-------------------------|  
|Giorno uno|Nessuno|80|  
|Vendite|-40|40|  
|Acquisti|+90|130|  
|Fine dell'intervallo di tempo|Nessuno|130|  
|Suggerire di ridurre l'acquisto<br /><br /> ordine di acquisto da 90 a 60|-30|100|  

### <a name="resulting-planning-lines"></a>Righe pianificazione risultanti  
 Una riga di pianificazione (avviso) viene creata per ridurre l'acquisto di 30 da 90 a 60 per mantenere la giacenza disponibile su 100 in base al livello di overflow.  

![Pianificazione in base al livello di overflow](media/nav_app_supply_planning_2_overflow2.png "Pianificazione in base al livello di overflow")  

> [!NOTE]  
>  Senza la funzionalità di overflow, nessun avviso viene creato se il livello di giacenza disponibile è superiore alla giacenza massima. Potrebbe verificarsi un approvvigionamento superfluo di 30.  

## <a name="see-also"></a>Vedi anche  
[Dettagli di progettazione: Metodi di riordino](design-details-reordering-policies.md)   
[Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
[Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
[Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)


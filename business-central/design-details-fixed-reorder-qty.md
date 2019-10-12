---
title: 'Dettagli di progettazione: Qtà riordino fissa | Microsoft Docs'
description: Il criterio Qtà Riordino Fissa è correlato alla pianificazione di magazzino dei tipici articoli C (costo di magazzino basso, basso rischio di obsolescenza e/o molti articoli). Questo metodo viene in genere utilizzato in connessione con un punto di riordino che riflette la domanda anticipata durante il lead time dell'articolo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: dd8c4b8cdae3e004e30551798e5a68058b5c38fe
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307225"
---
# <a name="design-details-fixed-reorder-qty"></a>Dettagli di progettazione: Qtà riordino fissa
Il criterio Qtà Riordino Fissa è correlato alla pianificazione di magazzino dei tipici articoli C (costo di magazzino basso, basso rischio di obsolescenza e/o molti articoli). Questo metodo viene in genere utilizzato in connessione con un punto di riordino che riflette la domanda anticipata durante il lead time dell'articolo.  

## <a name="calculated-per-time-bucket"></a>Calcolato per intervallo di tempo  
 Se il sistema di pianificazione rileva che il punto di riordino è stato raggiunto o superato in un intervallo di tempo specificato (ciclo di riordino) - sopra o in corrispondenza del punto di riordino all'inizio del periodo e sotto o in corrispondenza del punto di riordino alla fine del periodo - verrà suggerito di creare un nuovo ordine di approvvigionamento della quantità di riordino specificata e di programmarlo dalla prima data successiva alla fine dell'intervallo di tempo.  

 Il concetto di punto di riordino programmato riduce il numero di suggerimenti di approvvigionamento. Ciò riflette un processo manuale di entrare nella warehouse spesso per controllare i contenuti effettivi nelle varie collocazioni.  

## <a name="creates-only-necessary-supply"></a>Crea solo l'approvvigionamento necessario  
 Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione controlla se l'approvvigionamento è già stato ordinato per essere ricevuto entro il lead time di un articolo. Se un ordine di approvvigionamento esistente risolverà il problema portando la giacenza disponibile al punto di riordino o oltre nel lead time, il sistema non suggerirà un nuovo ordine di approvvigionamento.  

 Gli ordini di approvvigionamento che vengono creati specificamente per soddisfare un punto di riordino sono esclusi dal bilanciamento dell'approvvigionamento ordinario e non verranno in alcun modo modificati in seguito. Di conseguenza, se un articolo che utilizza il punto di riordino deve essere eliminato (non compilato), è consigliabile verificare gli ordini di approvvigionamento inevasi manualmente o modificare il metodo di riordino lotto-per-Lotto con cui il sistema ridurrà o annullerà l'approvvigionamento superfluo.  

## <a name="combines-with-order-modifiers"></a>Combina con i modificatori di ordine  
 I modificatori di ordini, Quantità minima ordine, Quantità massima ordine e Molteplicità ordine, non devono svolgere un grande ruolo quando vengono utilizzati i criteri di quantità riordino fissa. Tuttavia, il sistema di pianificazione prende ancora in considerazione questi modificatori e diminuirà la quantità alle quantità di ordine massime specificate (e creerà due o più approvvigionamenti per raggiungere la quantità di ordine totale), aumenterà la quantità di ordine minima o arrotonderà la quantità di ordine fino a soddisfare la molteplicità ordine specificata.  

## <a name="combines-with-calendars"></a>Associazioni con i calendari  
 Prima di suggerire un nuovo ordine di approvvigionamento per soddisfare un punto di riordino, il sistema di pianificazione verifica che l'ordine sia programmato per un giorno non lavorativo, in base ai calendari definiti nel campo **Codice calendario base** delle pagine **Informazioni società** e **Scheda Ubicazione**.  

 Se la data prevista è un giorno non lavorativo, il sistema di pianificazione sposta l'ordine al giorno lavorativo più vicino. In questo modo, potrebbe verificarsi che un ordine soddisfi un punto di riordino ma non una richiesta specifica. Per tale richiesta non bilanciata, il sistema di pianificazione crea un approvvigionamento aggiuntivo.  

## <a name="should-not-be-used-with-forecast"></a>Non deve essere utilizzato con la previsione  
 Poiché la domanda prevista è già espressa nel livello del punto di riordino non è necessario includere una previsione nella pianificazione di un articolo utilizzando un punto di riordino. Se è necessario basare il piano su una previsione, utilizzare il metodo lotto per lotto.  

## <a name="must-not-be-used-with-reservations"></a>Non deve essere utilizzato con gli impegni  
 Se l'utente ha impegnato una quantità, ad esempio una quantità in magazzino, per una domanda remota, la struttura della pianificazione rimarrà alterata. Anche se il livello della quantità scorte previste è ammesso relativamente al punto di riordino, le quantità potrebbero non essere disponibili. Il sistema può provare a compensare creando ordini di eccezione; tuttavia, è consigliabile che il campo Impegno sia impostato su Mai negli articoli che sono pianificati utilizzando un punto di riordino.  

## <a name="see-also"></a>Vedi anche  
 [Dettagli di progettazione: Criteri di riordino](design-details-reordering-policies.md)   
 [Dettagli di progettazione: Qtà Massima](design-details-maximum-qty.md)   
 [Dettagli di progettazione: Parametri di pianificazione](design-details-planning-parameters.md)   
 [Dettagli di progettazione: Gestione dei metodi di riordino](design-details-handling-reordering-policies.md)   
 [Dettagli di progettazione: Pianificazione approvvigionamento](design-details-supply-planning.md)

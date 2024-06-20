---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!IMPORTANT]
> Quando modifichi l'evento per una fase workflow, cambiano anche le risposte. A volte, le risposte di altri eventi si riferiscono a queste risposte come fase successiva nel workflow. Dopo aver modificato un evento, verifica che le fasi successive per gli eventi siano corretti.  
>
> Ad esempio, il modello di workflow **Workflow di approvazione fornitore** ha un evento primario **Approvazione fornitore necessaria**. Questo evento ha una risposta **Inviare la richiesta di approvazione per il record e creare una notifica**, a cui fanno riferimento altre risposte. Se cambi l'evento **Approvazione fornitore necessaria** in, ad esempio, **Record fornitore cambiato**, la risposta viene cancellata insieme ai riferimenti.
>
> Le risposte per gli eventi **Richiesta approvazione delegata** e **Richiesta approvazione approvata** (con **Condizione** di **Approvazioni in sospeso >0**) sono esempi di casi in cui la modifica di un evento primario può causare problemi. Le relative risposte hanno una fase successiva che fa riferimento alla risposta **Inviare la richiesta di approvazione per il record e creare una notifica** dell'evento **Approvazione fornitore necessaria**. Poiché la risposta per l'evento **Approvazione fornitore necessaria** non è più disponibile, gli eventi indentati non funzioneranno come previsto.
>
> Dovrai specificare le fasi successive per le risposte per gli eventi che facevano riferimento all'evento modificato.
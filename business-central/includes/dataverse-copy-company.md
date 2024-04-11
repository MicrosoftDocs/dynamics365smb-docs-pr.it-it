---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!NOTE]
> Quando copi una società in un ambiente in cui è abilitata l'integrazione di Dataverse o di Sales, [!INCLUDE [prod_short](prod_short.md)] annulla le seguenti impostazioni durante la copia nella società di destinazione:
>
> * Impostazioni di connessione Dataverse e Dynamics per garantire che l'integrazione venga riavviata correttamente nella società di destinazione.
> * Record di integrazione per garantire che la società di destinazione non punti a record accoppiati nella società di origine.
> * Processi di sincronizzazione di integrazione per interrompere i processi di sincronizzazione in background.
> * Errori di sincronizzazione, se esistono, perché indicano errori nella società di origine e sarebbero considerati solo dettagli poco significativi nella società di destinazione.
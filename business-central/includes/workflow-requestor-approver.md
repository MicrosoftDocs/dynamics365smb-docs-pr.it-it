---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Quando imposti gli utenti per i workflow di approvazione, è importante che lo stesso utente non sia simultaneamente un richiedente e un responsabile dell'approvazione in un gruppo utenti del workflow. Quando un utente è nello stesso tempo un richiedente e un responsabile dell'approvazione, le approvazioni funzionano come segue:

* Le loro richieste vengono sempre approvate automaticamente.
* Se sono presenti più responsabili dell'approvazione, solo quelli con un numero di sequenza più elevato nel gruppo utenti del workflow possono modificare lo stato di una richiesta in Approvata. I responsabili dell'approvazione con un numero di sequenza inferiore possono approvare le richieste, tuttavia le loro approvazioni non influiranno sullo stato di una richiesta.
---
author: edupont04
ms.topic: include
ms.date: 04/01/2022
ms.author: edupont
---
Gli utenti [!INCLUDE[prod_short](prod_short.md)] a volte supportano più di un reparto o una sottoorganizzazione all'interno di una business unit. Ad esempio, un'azienda potrebbe avere uffici di vendita in diverse città e in più paesi/aree geografiche, quindi ha creato una business unit separata per ciascun ufficio. Gli uffici che si trovano nello stesso paese/area geografica sono istituiti come *società* separate in un *ambiente* condiviso. Altri uffici vengono creati come aziende in ambienti separati perché sono geograficamente in altri paesi/aree geografiche.

- Cos'è un'azienda?

  Una *società* è come contenitore che contiene informazioni su una persona giuridica. Usando l'esempio sopra, l'azienda ha un ufficio vendite a Seattle e un altro a New York, quindi crea una società in [!INCLUDE[prod_short](prod_short.md)] per ogni ufficio in modo che possa gestire le operazioni separatamente per ogni ufficio.

- Che cos'è un ambiente?

  Le aziende in [!INCLUDE[prod_short](prod_short.md)] online esistono in ciò che viene indicato come *ambiente*. Esistono due tipi di ambienti, **produzione** e **sandbox**. In breve, gli ambienti di produzione contengono dati aziendali in tempo reale e gli ambienti sandbox vengono utilizzati come luogo sicuro per testare operazioni come nuovi processi o funzionalità aziendali. Per ulteriori informazioni, vedi [Tipi di ambiente](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (solo in inglese). Se è disponibile l'accesso a un'azienda, è disponibile l'accesso all'ambiente in cui si trova. Se si ha accesso a più di una società e tali società si trovano in ambienti diversi, quando si accede a [!INCLUDE[prod_short](prod_short.md)] è necessario specificare l'ambiente in cui si desidera lavorare. Gli ambienti sono specifici di un determinato paese/area geografica, quindi se l'organizzazione lavora in più paesi/aree geografiche, sono necessari ambienti separati per ciascun paese/area geografica. Per ulteriori informazioni, vedi [Ambienti e società](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (solo in inglese).

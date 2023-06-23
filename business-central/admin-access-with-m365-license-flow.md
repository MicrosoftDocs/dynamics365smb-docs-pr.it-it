---
title: Flusso di accessi utente per licenze Microsoft 365
description: Ottieni una panoramica di ciò che accade quando un utente accede ai dati di Business Central utilizzando la propria licenza Microsoft 365 per la prima volta.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses" />Flusso di accessi utente per licenze Microsoft 365

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Questo articolo descrive ciò che accade quando un utente accede ai dati di Business Central utilizzando la propria licenza Microsoft 365 per la prima volta. La comprensione di questo flusso consente agli amministratori di pianificare l'approccio e configurare Business Central in base alle proprie esigenze aziendali.

1. Innanzitutto, l'identità dell'utente viene autenticata 
2. Business Central verifica che tutti i [requisiti minimi](admin-access-with-m365-license.md#minimum-requirements) siano soddisfatti.
3. Business Central verifica che questo utente non disponga di una licenza superiore, ad esempio una licenza Business Central, o di un ruolo amministrativo come un ruolo di amministratore delegato. 
4. Business Central verifica se l'utente sta accedendo ai dati che appartengono a un ambiente con cui è abilitato l'accesso con licenze Microsoft 365. 
5. Il record utente viene fornito in Business Central, assegnando il gruppo utente, il profilo e gli insiemi di autorizzazioni definiti nella pagina di configurazione della licenza Microsoft 365. Per impostazione predefinita, viene assegnato il gruppo utenti Utenti di Teams, viene assegnato il profilo Dipendente e viene assegnato solo il set di autorizzazioni di accesso. Viene applicata anche qualsiasi altra impostazione predefinita per l'utente, come un utente Business Central con licenza. 
6. Viene applicato il modello di sicurezza completo di Business Central per determinare se l'utente deve essere in grado di accedere al record, alla pagina, nell'azienda e nell'ambiente specificati. 

Se tutti i passaggi hanno esito positivo, l'utente può ora visualizzare questi dati di Business Central in Teams. Il servizio Business Central garantisce automaticamente l'accesso in sola lettura e semplifica l'interfaccia utente. 

L'account utente è ora registrato in Business Central e può essere gestito come qualsiasi utente di Business Central.

> [!NOTE]
> I passaggi possono variare a seconda di qualsiasi configurazione di sicurezza aggiuntiva specificata in Microsoft 365 o Business Central.

## <a name="see-also" />Vedere anche

[Accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurare l'accesso con licenze Microsoft 365](admin-access-with-m365-license-setup.md)  

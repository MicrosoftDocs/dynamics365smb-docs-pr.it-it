---
title: Risoluzione dei problemi di accesso con licenze Microsoft 365
description: Scopri come risolvere i problemi di accesso a Business Central solo con una licenza Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Risoluzione dei problemi di accesso con licenze Microsoft 365

## Sintomi

Quando accedi a un record in Teams, ti viene mostrato un messaggio di errore in una scheda o nei dettagli della scheda simile a:

"Questa pagina utilizza i dati delle tabelle correlate a cui non hai accesso. Per utilizzare tutte le funzionalità di questa pagina, contatta il tuo amministratore".

## Causa

Molto probabilmente mancano le autorizzazioni per gli oggetti per le tabelle a cui si collega la pagina o il record corrente.

## Sintomi

L'accesso è stato abilitato, ma gli utenti ricevono un errore di autorizzazione quando accedono a qualsiasi record.

## Causa

Se si abilita l'accesso nell'interfaccia di amministrazione di Business Central, ma non si assegnano le autorizzazioni nella pagina Configurazione licenza, chiunque tenti di accedere ai record di Business Central in Teams avrà il proprio record utente fornito senza autorizzazione per alcun oggetto. Business Central è sicuro per impostazione predefinita: gli amministratori devono prima configurare a quali dati è possibile accedere in Teams. 

## Risoluzione

La personalizzazione delle autorizzazioni nella pagina Configurazione licenza influirà solo sugli utenti appena creati. È inoltre necessario assegnare le autorizzazioni mancanti agli utenti che sono già stati creati tramite la pagina Elenco utenti. 

## Sintomi

Quando condivido un collegamento in Teams, altri ricevono l'errore "Quando si accede a Business Central con una licenza Microsoft 365, puoi solo visualizzare i dati in Microsoft Teams".

## Causa

Quando si condivide un collegamento di Business Central a una chat o a un canale di Teams, il raggiungimento di un collegamento uscirà sempre da Microsoft Teams qualora i dati non diventino più accessibili a un utente che dispone di una licenza Microsoft 365.

## Risoluzione

Quando condividi pagine o record, includi l'anteprima del collegamento come scheda o condividi i dati come scheda nella chat o nel canale.

## Vedere anche

[Accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurare l'accesso con licenze Microsoft 365](admin-access-with-m365-license-setup.md)  
[Integrazione tra Business Central e Microsoft Teams](across-teams-overview.md)
[Condivisione di record di Business Central e collegamenti di pagina in Microsoft Teams](across-working-with-teams.md)  
[Risoluzione dei problemi di integrazione di Teams](admin-teams-troubleshooting.md)  
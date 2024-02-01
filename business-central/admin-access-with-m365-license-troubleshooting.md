---
title: Risoluzione dei problemi di accesso con licenze Microsoft 365
description: Scopri come risolvere i problemi di accesso a Business Central solo con una licenza Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.service: dynamics-365-business-central
---

# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Risoluzione dei problemi di accesso con licenze Microsoft 365

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message"></a>Messaggio di errore "Questa pagina utilizza i dati delle tabelle correlate a cui non hai accesso"

### <a name="symptoms"></a>Sintomi

Quando accedi a un record in Teams, ti viene mostrato un messaggio di errore in una scheda o nei dettagli della scheda simile a:

"Questa pagina utilizza i dati delle tabelle correlate a cui non hai accesso. Per utilizzare tutte le funzionalità di questa pagina, contatta il tuo amministratore".

### <a name="cause"></a>Causa

Molto probabilmente mancano le autorizzazioni per gli oggetti per le tabelle a cui si collega la pagina o il record corrente.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error"></a>L'accesso Microsoft 365 è stato abilitato, ma gli utenti ricevono un errore di autorizzazione

### <a name="symptoms-1"></a>Sintomi

L'accesso con Microsoft 365 è stato abilitato nell'interfaccia di amministrazione di Business Central, ma gli utenti ricevono un errore di autorizzazione quando accedono a qualsiasi record.

### <a name="cause-1"></a>Causa

Se si abilita l'accesso nell'interfaccia di amministrazione di Business Central, ma non si assegnano le autorizzazioni nella pagina **Configurazione licenza**, chiunque tenti di accedere ai record di Business Central in Teams avrà il proprio record utente fornito senza autorizzazione per alcun oggetto. Business Central è sicuro per impostazione predefinita: gli amministratori devono prima configurare a quali dati è possibile accedere in Teams. 

### <a name="resolution"></a>Risoluzione

La personalizzazione delle autorizzazioni nella pagina Configurazione licenza influirà solo sugli utenti appena creati. È inoltre necessario assegnare le autorizzazioni mancanti agli utenti che sono già stati creati tramite la pagina Elenco utenti. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data"></a>Hai condiviso un collegamento in Teams, ma gli utenti ricevono un messaggio che li informa che possono solo visualizzare i dati

### <a name="symptoms-2"></a>Sintomi

Quando condividi un collegamento in Teams come utente Business Central, altri ricevono l'errore "Quando si accede a Business Central con una licenza Microsoft 365, puoi solo visualizzare i dati in Microsoft Teams".

### <a name="cause-2"></a>Causa

Quando si condivide un collegamento di Business Central a una chat o a un canale di Teams, il raggiungimento di un collegamento uscirà sempre da Microsoft Teams qualora i dati non diventino più accessibili a un utente che dispone di una licenza Microsoft 365.

### <a name="resolution-1"></a>Risoluzione

Quando condividi pagine o record, includi l'anteprima del collegamento come scheda o condividi i dati come scheda nella chat o nel canale.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button"></a>La scheda dal collegamento condiviso è ridotta al minimo e non include il pulsante Dettagli

### <a name="symptoms-3"></a>Sintomi

Quando un titolare della licenza Microsoft 365 senza licenza Business Central condivide un collegamento Business Central in Teams, si espande automaticamente in una scheda che non contiene informazioni utili e mostra solo Business Central senza il pulsante **Dettagli**.

### <a name="cause-3"></a>Causa

Gli utenti che dispongono di una licenza Microsoft 365 ma non di una licenza Business Central non sono autorizzati a condividere collegamenti come schede. Se l'utente ha installato l'app Business Central per Teams e incolla un collegamento nell'area di composizione, viene visualizzata solo una scheda ridotta al minimo. 

## <a name="see-also"></a>Vedere anche

[Accesso a Business Central con licenze Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurare l'accesso con licenze Microsoft 365](admin-access-with-m365-license-setup.md)  
[Integrazione tra Business Central e Microsoft Teams](across-teams-overview.md)
[Condivisione di record di Business Central e collegamenti di pagina in Microsoft Teams](across-working-with-teams.md)  
[Risoluzione dei problemi di integrazione di Teams](admin-teams-troubleshooting.md)  

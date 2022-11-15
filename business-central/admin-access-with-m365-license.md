---
title: Accesso a Business Central con licenze Microsoft 365
description: Scopri come gli utenti possono accedere ai dati di Business Central, ad esempio nelle chat e nei canali di Microsoft Teams, con una sola licenza Microsoft 365, ma nessuna licenza Business Central.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: 84cd78b2e87f51dead2ce8a2d0340da76eb59e38
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744988"
---
# <a name="business-central-access-with-microsoft-365-licenses"></a>Accesso a Business Central con licenze Microsoft 365

Agli utenti di Business Central viene assegnata una licenza Dynamics 365 Business Central che consente loro di visualizzare, modificare e agire sui propri dati aziendali da qualsiasi interfaccia utente. Per tutti gli altri dipendenti dell'organizzazione che necessitano di visualizzare i dati solo occasionalmente, Business Central offre l'accesso tramite Microsoft 365.  

Quando un'organizzazione ha entrambi gli abbonamenti Dynamics 365 Business Central e Microsoft 365, gli amministratori possono configurare gli ambienti per abilitare l'accesso alle licenze Microsoft 365 e scegliere esattamente a quali tabelle e altri oggetti avrà accesso questa categoria di utenti. Una volta configurati, i dipendenti che dispongono di una licenza Microsoft 365 ma no hanno licenze Business Central possono visualizzare i record di Business Central che sono condivisi con loro tramite chat e canali Microsoft Teams.

## <a name="why-enable-access-with-microsoft-365-licenses"></a>Perché abilitare l'accesso con le licenze Microsoft 365  

- Sblocca l'anagrafica a cui ogni dipendente dell'organizzazione dovrebbe avere accesso.

- Consenti ai reparti che non funzionano su Business Central di essere self-service, accedendo ai dati principali necessari per svolgere con successo le proprie attività, eliminando la necessità di richiedere continuamente dati ad altri. 

- Aumenta l'efficacia della collaborazione in modo che le attività e i progetti che si estendono tra i reparti vengano completati in tempo, eliminando l'attrito tipicamente associato agli errori di accesso negato a causa delle licenze. 

- Aumenta le prestazioni del team in modo che le persone possano prendere decisioni basate sui dati che includono tutti i membri del gruppo, anche se non lavorano in Business Central. 

- Soddisfa gli obiettivi di budget delle licenze, assegnando licenze che corrispondono progressivamente alle esigenze dei dipendenti, con licenze Microsoft 365 per l'accesso in sola lettura, licenze Dynamics 365 Business Central dei membri del team per accesso in scrittura limitato e Dynamics 365 Business Central Essentials o Premium per l'accesso in scrittura completo.

- Migliora la sicurezza dei dati riducendo la necessità di incollare frammenti di schermo dei dati aziendali al di fuori dei limiti di conformità alla governance dei dati.

## <a name="use-rights"></a>Diritti di utilizzo

Quando una persona accede a Business Central con una licenza Microsoft 365, questa licenza autorizza l'utente a leggere (ma non a scrivere) i dati di Business Central attraverso un'interfaccia utente semplificata in formato Microsoft Teams. Questa sezione spiega questi diritti di utilizzo e limitazioni che aiutano a pianificare come configurare e sfruttare al massimo questa capacità. Per ulteriori informazioni su questo tipo di licenza rispetto ad altre licenze di Business Central, consulta la [Guida alle licenze di Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access"></a>Accesso client

Gli utenti hanno il diritto di accedere ai dati di Business Central in Microsoft Teams. La tabella seguente riassume quali dei diversi metodi di accesso al servizio Business Central sono consentiti con questa licenza. 

|Cliente che accede al servizio Business Central |Accedi|
|-|-|
|App Business Central per Microsoft Teams|![Sì](media/check.png)|
|Client Web Business Central |![Nr.](media/x-icon.png ) |
|App per dispositivi mobili Business Central|![Nr.](media/x-icon.png )|
|API Business Central|![Nr.](media/x-icon.png )|
|Integrazioni di Business Central con altre applicazioni di Office|![Nr.](media/x-icon.png )|
|Business Central integrato in altre applicazioni |![Nr.](media/x-icon.png )|

### <a name="data-access"></a>Accesso ai dati 

Gli utenti hanno il diritto di leggere i dati delle tabelle ma non possono modificare, creare o eliminare record. La piattaforma Business Central impedisce automaticamente la scrittura su tabelle di dati.  

### <a name="use-of-objects"></a>Uso di oggetti 

Gli accessi tramite licenze Microsoft 365 non limitano gli oggetti o gli intervalli di oggetti di Business Central a cui è possibile accedere. Gli utenti hanno il diritto di accedere all'applicazione di base Microsoft e a eventuali estensioni come personalizzazioni e app aggiuntive. 

## <a name="simplified-ui"></a>Interfaccia utente semplificata 

Gli utenti hanno diritto a un insieme ridotto di caratteristiche e funzioni fornite da Business Central in Microsoft Teams. Le tabelle seguenti indicano caratteristiche degne di nota. Questo non è un elenco esaustivo ed è soggetto a modifiche.

Funzionalità dell'app Business Central per Teams:

|Funzionalità  |Disponibile|
|-|-|
|Visualizza le schede Business Central|![Sì](media/check.png)|
|Visualizzare i dettagli della scheda |![Sì](media/check.png) |
|Aggiungere i dettagli come scheda |![Sì](media/check.png)|
|Visualizza le schede Business Central|![Sì](media/check.png)|
|Aggiungere una scheda Business Central|![No_](media/x-icon.png )|
|Cerca contatti aziendali |![Nr.](media/x-icon.png )|
|Incollare e condividere un'anteprima del collegamento come scheda|![Nr.](media/x-icon.png )|

Funzioni del client Business Central integrato in Teams:

|Funzione |Disponibile|Esempi di funzioni|
|-|-|-|
|Azioni del sistema di manipolazione dei dati |![Nr.](media/x-icon.png )|Modifica, crea, elimina|
|Funzioni di base negli elenchi|![Sì](media/check.png)|Cerca, ordina, modifica layout|
|Funzioni avanzate negli elenchi|![Nr.](media/x-icon.png )|Riquadro filtri, viste|
|Scorri dall'elenco alla scheda |![Sì](media/check.png)||
|Accessi ai dati da tabelle correlate|![Nr.](media/x-icon.png )|Riquadro Dettaglio informazioni, drilldown campo, visualizzare, cercare |
|Azioni|![Nr.](media/x-icon.png )|Barra delle azioni, menu delle azioni, azioni di notifica della pagina|
|Scelte rapide a livello di sistema|![Nr.](media/x-icon.png )|Impostazioni personali, Esplora ruoli, ricerca Dimmi  |
|Copia|![Sì](media/check.png)|Copia le righe, copia il valore del campo, copia il collegamento alla pagina|
|Personalizzazione interfaccia utente|![Nr.](media/x-icon.png )|Personalizza| 
|Personalizzazione incorporata|![Sì](media/check.png)|Ridimensiona colonna, Espandi/Comprimi, Mostra di più |
|Condivisione dei dati |![Nr.](media/x-icon.png )|Apri o Modifica in Excel, Condividi in Teams|
|Assistenza utente incorporata|![Sì](media/check.png) |Suggerimenti, collegamenti alla documentazione|
|Assistenza utente avanzata |![Nr.](media/x-icon.png )|Suggerimenti didattici relativi a pagine e campi, riquadro della Guida|

## <a name="minimum-requirements"></a>Requisiti minimi

Questa sezione descrive i requisiti minimi che devono essere soddisfatti affinché l'organizzazione abiliti l'accesso con licenze Microsoft 365 e per gli utenti privati di Microsoft Teams per accedere ai dati di Business Central senza una licenza Business Central.

### <a name="requirements-to-enable-access"></a>Requisiti per abilitare l'accesso

- Business Central Online (SaaS).

- Gli ambienti devono essere della piattaforma versione 21.1 o successiva.

### <a name="requirements-for-individual-users-to-access-data-in-teams"></a>Requisiti per i singoli utenti per accedere ai dati in Teams

- È necessario accedere ai dati utilizzando l'app Business Central per Teams. Gli utenti devono avere l'app Business Central per Teams installata e devono usare uno dei client Teams supportati. Per un elenco di client Teams supportati da Business Central, vedi [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md#teams).

- Gli utenti devono essere interni all'organizzazione, il che significa che un'identità utente proviene dallo stesso tenant principale in cui è distribuito Business Central e in cui è abilitato l'accesso. Le identità esterne non sono supportate. Business Central impedisce automaticamente l'accesso agli utenti guest.

- Agli utenti deve essere assegnata una licenza Microsoft 365 da uno dei seguenti piani.
  
  |Piano supportato|ID prodotto |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |<!--??--> Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |<!--??--> Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Microsoft Teams Essentials (Azure AD Identity) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  |<!--??--> Microsoft 365 E1 ||

  > [!NOTE]
  > Non riesci a trovare il tuo piano nell'elenco? Microsoft è continuamente alla ricerca di commenti su come possiamo migliorare il nostro servizio ed espandere la nostra offerta in modo che più clienti possano trarre vantaggio da questa funzionalità. Condividi la tua idea per quali piani dovremmo supportare in futuro in [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Agli utenti deve essere assegnata una licenza Microsoft 365 che ha l'app Microsoft Teams abilitata nell'elenco delle app per quella licenza. 

  |App supportate|ID piano di servizio|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- L'organizzazione deve avere almeno un altro utente assegnato alla licenza Dynamics 365 Business Central.

## <a name="next-steps"></a>Passaggi successivi

- Ottieni ulteriori informazioni sul flusso di accesso degli utenti per pianificare il tuo approccio e la configurazione di Business Central per soddisfare le esigenze aziendali. Vedi [Flusso di accessi utente](admin-access-with-m365-license-flow.md).
- Configura il tuo ambiente e gli utenti per l'accesso con le licenze Microsoft 365. Vedi [Configurare gli accessi con licenze Microsoft 365](admin-access-with-m365-license-setup.md).

## <a name="see-also"></a>Vedere anche

[Business Central e integrazione Microsoft Teams](across-teams-overview.md)  

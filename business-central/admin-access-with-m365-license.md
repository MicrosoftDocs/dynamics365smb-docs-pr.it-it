---
title: Accesso a Business Central con licenze Microsoft 365
description: 'Scopri come gli utenti possono accedere ai dati di Business Central, ad esempio nelle chat e nei canali di Microsoft Teams, con una sola licenza Microsoft 365, ma nessuna licenza Business Central.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Accesso a Business Central con licenze Microsoft 365

Agli utenti di [!INCLUDE[prod_short](includes/prod_short.md)] viene assegnata una licenza Dynamics 365 Business Central che consente loro di visualizzare, modificare e agire sui propri dati aziendali da qualsiasi interfaccia utente. Per tutti gli altri dipendenti dell'organizzazione che necessitano di visualizzare i dati solo occasionalmente, Business Central offre l'accesso tramite Microsoft 365.  

Quando un'organizzazione ha entrambi gli abbonamenti Dynamics 365 Business Central e Microsoft 365, gli amministratori possono configurare gli ambienti per abilitare l'accesso alle licenze Microsoft 365 e scegliere esattamente a quali tabelle e altri oggetti avrà accesso questa categoria di utenti. Una volta configurati, i dipendenti che dispongono di una licenza Microsoft 365 ma no hanno licenze [!INCLUDE [prod_short](includes/prod_short.md)] possono visualizzare i record di [!INCLUDE [prod_short](includes/prod_short.md)] che sono condivisi con loro tramite chat e canali Microsoft Teams.

## Perché abilitare l'accesso con le licenze Microsoft 365  

- Sblocca l'anagrafica a cui ogni dipendente dell'organizzazione dovrebbe avere accesso.

- Consenti ai reparti che non funzionano su [!INCLUDE [prod_short](includes/prod_short.md)] di essere self-service, accedendo ai dati principali necessari per svolgere con successo le proprie attività, eliminando la necessità di richiedere continuamente dati ad altri.

- Aumenta l'efficacia della collaborazione in modo che le attività e i progetti che si estendono tra i reparti vengano completati in tempo, eliminando l'attrito tipicamente associato agli errori di accesso negato a causa delle licenze.

- Aumenta le prestazioni del team in modo che le persone possano prendere decisioni basate sui dati che includono tutti i membri del gruppo, anche se non lavorano in [!INCLUDE [prod_short](includes/prod_short.md)].

- Soddisfa gli obiettivi di budget delle licenze, assegnando licenze che corrispondono progressivamente alle esigenze dei dipendenti, con licenze Microsoft 365 per l'accesso in sola lettura, licenze Dynamics 365 Business Central dei membri del team per accesso in scrittura limitato e Dynamics 365 Business Central Essentials o Premium per l'accesso in scrittura completo.

- Migliora la sicurezza dei dati riducendo la necessità di incollare frammenti di schermo dei dati aziendali al di fuori dei limiti di conformità alla governance dei dati.

## Diritti di utilizzo

Quando una persona accede a [!INCLUDE [prod_short](includes/prod_short.md)] con una licenza Microsoft 365, questa licenza autorizza l'utente a leggere (ma non a scrivere) i dati di [!INCLUDE [prod_short](includes/prod_short.md)] attraverso un'interfaccia utente semplificata in Microsoft Teams. Questa sezione spiega questi diritti di utilizzo e limitazioni che aiutano a pianificare come configurare e sfruttare al massimo questa capacità. Per ulteriori informazioni su questo tipo di licenza rispetto ad altre licenze di [!INCLUDE [prod_short](includes/prod_short.md)], consulta la [Guida alle licenze di Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### Accesso client

Gli utenti hanno il diritto di accedere ai dati di [!INCLUDE [prod_short](includes/prod_short.md)] in Microsoft Teams. La tabella seguente riassume quali dei diversi metodi di accesso al servizio [!INCLUDE [prod_short](includes/prod_short.md)] sono consentiti con questa licenza.

|Cliente che accede al servizio Business Central |Accedi|
|-|-|
|App Business Central per Microsoft Teams|![Sì](media/check.png)|
|Client Web Business Central |![Nr.](media/x-icon.png ) |
|App per dispositivi mobili Business Central|![Nr.](media/x-icon.png )|
|API Business Central|![Nr.](media/x-icon.png )|
|Integrazioni di Business Central con altre applicazioni di Office|![Nr.](media/x-icon.png )|
|Business Central integrato in altre applicazioni |![Nr.](media/x-icon.png )|

### Accesso ai dati

Gli utenti hanno il diritto di leggere i dati delle tabelle ma non possono modificare, creare o eliminare record. La piattaforma [!INCLUDE [prod_short](includes/prod_short.md)] impedisce automaticamente la scrittura su tabelle di dati.  

### Uso di oggetti

Gli accessi tramite licenze Microsoft 365 non limitano gli oggetti o gli intervalli di oggetti di Business Central a cui è possibile accedere. Gli utenti hanno il diritto di accedere all'applicazione di base Microsoft e a eventuali estensioni come personalizzazioni e app aggiuntive.

## Interfaccia utente semplificata

Gli utenti hanno diritto a un insieme ridotto di caratteristiche e funzioni fornite da [!INCLUDE [prod_short](includes/prod_short.md)] in Microsoft Teams. Le tabelle seguenti indicano caratteristiche degne di nota. Questo non è un elenco esaustivo ed è soggetto a modifiche.

Funzionalità dell'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams:

|Funzionalità  |Disponibile|
|-|-|
|Visualizzare le schede di [!INCLUDE [prod_short](includes/prod_short.md)]|![Sì](media/check.png)|
|Visualizzare i dettagli della scheda |![Sì](media/check.png) |
|Aggiungere i dettagli come scheda |![Sì](media/check.png)|
|Visualizzare le schede di [!INCLUDE [prod_short](includes/prod_short.md)]|![Sì](media/check.png)|
|Aggiungere una scheda di [!INCLUDE [prod_short](includes/prod_short.md)]|![No_](media/x-icon.png )|
|Cerca contatti aziendali |![Nr.](media/x-icon.png )|
|Incollare e condividere un'anteprima del collegamento come scheda|![Nr.](media/x-icon.png )|

Funzioni del client [!INCLUDE [prod_short](includes/prod_short.md)] integrato in Teams:

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

## Requisiti minimi

Questa sezione descrive i requisiti minimi che devono essere soddisfatti affinché l'organizzazione abiliti l'accesso con licenze Microsoft 365 e per gli utenti privati di Microsoft Teams per accedere ai dati di [!INCLUDE [prod_short](includes/prod_short.md)] senza una licenza [!INCLUDE [prod_short](includes/prod_short.md)].

### Requisiti per abilitare l'accesso

- [!INCLUDE [prod_short](includes/prod_short.md)] online (SaaS).

- Gli ambienti devono essere della piattaforma versione 21.1 o successiva.

### Requisiti per i singoli utenti per accedere ai dati in Teams

- È necessario accedere ai dati utilizzando l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams. Gli utenti devono avere l'app [!INCLUDE [prod_short](includes/prod_short.md)] per Teams installata e devono usare uno dei client Teams supportati. Per un elenco di client Teams supportati da [!INCLUDE [prod_short](includes/prod_short.md)], vedi [Requisiti minimi per l'utilizzo di Business Central](product-requirements.md#teams).

- Gli utenti devono essere interni all'organizzazione, il che significa che un'identità utente proviene dallo stesso tenant principale in cui è distribuito [!INCLUDE [prod_short](includes/prod_short.md)] e in cui è abilitato l'accesso. Le identità esterne non sono supportate. [!INCLUDE [prod_short](includes/prod_short.md)] impedisce automaticamente l'accesso agli utenti guest.

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
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Microsoft Entra Identity) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  Sono supportate anche la maggior parte delle offerte basate su questi piani. Ad esempio, se ti abboni a Microsoft 365 Business Premium (Prezzo staff Nonprofit), è un'offerta specifica per le organizzazioni no profit basata sul piano Microsoft 365 Business Premium ed è quindi supportato.

  > [!NOTE]
  > Non riesci a trovare il tuo piano nell'elenco? Microsoft è continuamente alla ricerca di commenti su come possiamo migliorare il nostro servizio ed espandere la nostra offerta in modo che più clienti possano trarre vantaggio da questa funzionalità. Condividi la tua idea per quali piani dovremmo supportare in futuro in [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Agli utenti deve essere assegnata una licenza Microsoft 365 che ha l'app Microsoft Teams abilitata nell'elenco delle app per quella licenza.

  |App supportate|ID piano di servizio|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- L'organizzazione deve avere almeno un altro utente assegnato alla licenza Dynamics 365 Business Central.

## Passaggi successivi

- Ottieni ulteriori informazioni sul flusso di accesso degli utenti per pianificare il tuo approccio e la configurazione di Business Central per soddisfare le esigenze aziendali. Vedi [Flusso di accessi utente](admin-access-with-m365-license-flow.md).
- Configura il tuo ambiente e gli utenti per l'accesso con le licenze Microsoft 365. Vedi [Configurare gli accessi con licenze Microsoft 365](admin-access-with-m365-license-setup.md).

## Vedere anche

[Business Central e integrazione Microsoft Teams](across-teams-overview.md)  

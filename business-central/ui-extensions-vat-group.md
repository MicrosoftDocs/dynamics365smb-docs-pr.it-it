---
title: L'estensione della gestione del gruppo IVA per il Regno Unito
description: Puoi impegnarti con altre aziende per formare un gruppo IVA in cui tutti i membri dichiarano l'IVA in un'unica dichiarazione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841922"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>L'estensione della gestione del gruppo IVA per il Regno Unito

È possibile connettere una o più aziende nel paese per combinare la dichiarazione IVA con un unico numero di registrazione. Questo tipo di modalità è noto come *gruppo IVA*. È possibile interagire con il gruppo come membro o rappresentante del gruppo.

## <a name="forming-a-vat-group"></a>Formazione di un gruppo IVA
I membri del gruppo IVA e il rappresentante del gruppo possono utilizzare la guida al setup assistito **Impostare Gestione gruppo IVA** per definire il coinvolgimento con il gruppo e creare una connessione tra i tenant [!INCLUDE[prod_short](includes/prod_short.md)]. I membri del gruppo utilizzeranno la connessione per presentare le loro dichiarazioni IVA al rappresentante del gruppo. Il rappresentante invierà una singola dichiarazione IVA alle autorità fiscali per il gruppo. 

## <a name="license-requirements"></a>Requisiti di licenza
I partecipanti al gruppo devono avere la licenza per l'uso di [!INCLUDE[prod_short](includes/prod_short.md)]. Non puoi utilizzare account guest nei gruppi IVA. 

* Per calcolare e inviare le dichiarazioni IVA, un utente deve essere un utente completo di Business Central.
* Per accedere ed eseguire attività di base, come creare account, puoi avere la licenza di membro del team Dynamics 365 Business Central.

## <a name="vat-group-constellations"></a>Costellazioni del gruppo IVA
La comunicazione avviene dai membri del gruppo al rappresentante. Il rappresentante del gruppo espone un URL di API che consente ai membri di presentare le dichiarazioni IVA al rappresentante del gruppo IVA. 
[!INCLUDE[prod_short](includes/prod_short.md)] supporta le dichiarazioni IVA tra gruppi per le aziende che utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] in locale o online e in qualsiasi combinazione. L'impostazione della comunicazione dipende dalla costellazione. Questo articolo descrive varie costellazioni di gruppi.

Il seguente elenco mostra l'ordine consigliato dei passaggi per impostare un gruppo IVA:

1. Creare il setup in Azure Active Directory. Per ulteriori informazioni, vedere [Requisiti per l'autenticazione](ui-extensions-vat-group.md#requirements-for-authentication).
2. Condividere le informazioni tecniche necessarie ai membri del gruppo IVA e al rappresentante per collegare i tenant [!INCLUDE[prod_short](includes/prod_short.md)]. Di solito, il rappresentante del gruppo IVA dispone di queste informazioni, come il nome dell'ambiente del rappresentante del gruppo IVA a cui i membri del gruppo IVA invieranno l'IVA.
3. Crea gli utenti che i membri del gruppo IVA possono utilizzare per autenticarsi quando si connettono a [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. Gli utenti devono disporre di una licenza utente completa per [!INCLUDE[prod_short](includes/prod_short.md)].
4. Esegui la guida al setup assistito **Impostare Gestione gruppo IVA** per collegare i membri del gruppo IVA.

  La guida richiede alcune informazioni dal rappresentante del gruppo IVA. Per ulteriori informazioni, vedi [Impostare i membri del gruppo IVA](#set-up-vat-group-members). Prendere nota dell'**ID membro del gruppo** per ogni membro del gruppo IVA. Il rappresentante ha bisogno di questi ID per aggiungere le società al gruppo IVA.
5. Imposta l'estensione Gestione gruppo IVA nel [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA utilizzando la guida al setup assistito **Impostare Gestione gruppo IVA**. 

> [!NOTE]
> Per connettersi al rappresentante del gruppo IVA, i membri del gruppo devono avere un account utente con accesso al [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. Il rappresentante del gruppo IVA deve creare almeno un utente per questo scopo, tuttavia, per motivi di sicurezza, si consiglia di creare un utente per ogni membro del gruppo IVA. Assicurarsi di distribuire le credenziali di questi utenti ai membri del gruppo IVA in modo sicuro. Questo è un account utente di sistema che non è correlato a una persona reale.

## <a name="about-the-vat-group-management-setup"></a>Informazioni sull'impostazione di Gestione gruppo IVA

Il rappresentante del gruppo IVA espone un'API ai membri del gruppo. I membri utilizzano l'API per connettersi al tenant [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante e presentare le dichiarazioni IVA. I membri del gruppo IVA usano spesso [!INCLUDE[prod_short](includes/prod_short.md)] in tenant Azure Active Directory separati. Pertanto, sono necessarie ulteriori impostazioni per connettere il membro del gruppo IVA e il [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante. 
  
I membri del gruppo IVA si connettono al rappresentante chiamando un servizio Web sul tenant del rappresentante del gruppo IVA. Il chiamante deve essere autenticato utilizzando OAuth2. Quando l'estensione Gestione gruppo IVA è impostata, ti verrà richiesto di autenticarti presso il rappresentante del gruppo IVA per ottenere e salvare un token di accesso. Questo token di accesso viene utilizzato quando si inviano dichiarazioni IVA al rappresentante del gruppo IVA. 

## <a name="construct-the-api-url"></a>Costruire l'URL dell'API
1. Nell'interfaccia di amministrazione di Business Central per il tenant del rappresentante, scegli la scheda **Ambienti**.
2. Nella sezione **Dettagli** copia l'**URL**.
3. Apri Blocco note e incolla l'URL. Sostituisci **https://businesscentral.dynamics.com** con **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Requisiti per l'autenticazione 
> [!NOTE]
> Ciò richiede le credenziali per un account amministratore che dispone di una licenza utente completa per [!INCLUDE[prod_short](includes/prod_short.md)].

Quando il rappresentante del gruppo IVA utilizza [!INCLUDE[prod_short](includes/prod_short.md)] online o in locale, i membri del gruppo IVA devono utilizzare Azure Active Directory per autenticare gli utenti quando presentano le dichiarazioni IVA al rappresentante del gruppo IVA. Per [!INCLUDE[prod_short](includes/prod_short.md)] locale, i membri devono configurare il Single Sign-On. Per ulteriori informazioni, vedi [Configurare l'autenticazione Azure Active Directory con WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Se anche i membri del gruppo IVA utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] online, il membro del gruppo IVA può autenticarsi utilizzando le credenziali dell'utente designato e le informazioni sull'endpoint. Per ulteriori informazioni, vedi [Impostare i membri del gruppo IVA](ui-extensions-vat-group.md#set-up-vat-group-members).

I membri del gruppo IVA che hanno [!INCLUDE[prod_short](includes/prod_short.md)] in locale devono configurare una registrazione dell'app in Azure Active Directory per il tenant [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. La registrazione dell'app abilita [!INCLUDE[prod_short](includes/prod_short.md)] online del rappresentante del gruppo IVA per autenticare il membro del gruppo. Per ulteriori informazioni, vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app).

Quando crei la registrazione dell'app in Azure Active Directory, devi specificare le seguenti informazioni.

* Nella sezione **Autenticazione** aggiungere **Web** come piattaforma e utilizzare il seguente **URL di reindirizzamento**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Nella sezione **Autenticazione**, nell'opzione per selezionare **Tipi di account supportati**, selezionare **Account in qualsiasi directory dell'organizzazione (qualsiasi directory Azure AD - Multitenant)**.
* Nella sezione **Certificati e segreti** creare un nuovo segreto client e prendere nota del valore. I membri del gruppo IVA utilizzeranno il segreto quando impostano la connessione al rappresentante del gruppo.
* Nella sezione **Autorizzazioni API** aggiungere le autorizzazioni in [!INCLUDE[prod_short](includes/prod_short.md)]. Abilitare l'accesso delegato a **Financials.ReadWrite.All** e **user_impersonation**.
* Nella sezione **Sintesi** notare l'**ID applicazione (client)**. I membri del gruppo IVA utilizzeranno l'ID quando impostano la connessione al rappresentante del gruppo. 

## <a name="set-up-vat-group-members"></a>Impostare i membri del gruppo IVA
> [!IMPORTANT]
> Le società membri del gruppo IVA non devono connettersi a HMRC perché dichiarano tramite il rappresentante del gruppo.

Prima di iniziare, contattare il rappresentante del gruppo IVA per le seguenti informazioni sul tenant [!INCLUDE[prod_short](includes/prod_short.md)]:

* URL dell'API
* Nome della società 
* ID client
* Segreto client
* Credenziali di accesso per l'utente dedicato 

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup gestione gruppo IVA**, quindi scegli il collegamento correlato.
2. Nel campo **Ruolo gurppo IVA** specifica se sei membro del gruppo o rappresentante del gruppo. Scegli **Membro** per agire da membro del gruppo e inviare l'IVA dichiarata ai rappresentanti del gruppo anziché all'autorità tributaria, quindi scegli **Avanti**.
3. Copiare il valore del campo **ID membro del gruppo** e condividerlo con il rappresentante del gruppo IVA in modo che possa aggiungere la società come membro approvato del gruppo.
4. Nel campo **Versione del prodotto rappresentante del gruppo**, specifica la versione di [!INCLUDE[prod_short](includes/prod_short.md)] che il rappresentante sta utilizzando.
5. Nel campo **Società di rappresentanza del gruppo** inserisci la ragione sociale del rappresentante del gruppo IVA. Per esempio, **CRONUS UK Ltd**.
6. Nel campo **Tipo di autenticazione** scegli l'opzione **OAuth2**. Se il rappresentante del gruppo IVA sta utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] online, specifica che il **Rappresentante del gruppo utilizza Business Central Online**, quindi scegli **Avanti**. A seconda che il rappresentante stia utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] online o locale, segui i passaggi nella sezione [Il rappresentante del gruppo IVA utilizza Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) o [Il rappresentante del gruppo IVA utilizza Business Central locale](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Il rappresentante del gruppo IVA usa Business Central Online
1. Immetti le credenziali utente fornite dal rappresentante del gruppo IVA e aggiungi le autorizzazioni richieste.
2. Scegli la configurazione della dichiarazione IVA attualmente utilizzata per inviare dichiarazioni IVA alle autorità fiscali. Dopo aver completato il setup, [!INCLUDE[prod_short](includes/prod_short.md)] creerà una nuova configurazione in base a questa scelta e utilizzerà la configurazione per presentare le dichiarazioni IVA al rappresentante del gruppo IVA.  
3. Aggiungere l'**URL API** del rappresentante del gruppo IVA. In genere, l'URL è nel seguente formato: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Ad esempio, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Il rappresentante del gruppo IVA usa Business Central locale
1. Nel campo **ID client**, inserisci l'ID client dalla registrazione dell'app in Azure Active Directory.
2. Nel campo **Segreto client**, inserisci il segreto client dalla registrazione dell'app in Azure Active Directory.
3. Nel campo **Endpoint dell'autorità OAuth 2.0** immetti `https://login.microsoftonline.com/common/oauth2`.
4. Nel campo **URL risorsa OAuth 2.0** immetti `https://api.businesscentral.dynamics.com/`.
5. Nel campo **URL di reindirizzamento OAuth 2.0** immetti `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Dopo aver specificato i vari campi, scegli **Avanti**, quindi immetti le credenziali utente fornite dal rappresentante del gruppo IVA.
7. Scegliere la configurazione del report IVA da utilizzare per dichiarare l'IVA alle autorità del paese.

## <a name="set-up-the-vat-group-representative"></a>Impostare il rappresentante del gruppo IVA
> [!NOTE]
> Per i sistemi locali, supportiamo solo una singola istanza del tenant del rappresentante del gruppo.

> [!IMPORTANT]
> La società rappresentante deve abilitare la connessione del servizio **Setup IVA HMRC** nella pagina **Connessioni del servizio**. I rappresentanti devono anche scaricare i periodi di dichiarazione IVA da HMRC.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup gestione gruppo IVA**, quindi scegli il collegamento correlato.
2. Nel campo **Ruolo gurppo IVA** specifica se sei membro del gruppo o rappresentante del gruppo. Scegli **Rappresentante** per agire da rappresentante del gruppo IVA e inviare le dichiarazioni IVA alle autorità fiscali per il gruppo, quindi scegli **Avanti**.
3. Nel campo **Conto liquidazione IVA** specifica il conto utilizzato per le liquidazioni IVA.
4. Nel campo **Nr. riquadro IVA dovuta** specifica la casella che rappresenta l'importo IVA totale dovuto da un invio del gruppo IVA.
5. Nel campo **Definizione registrazioni COGE per liquidazione gruppo**, specifica la definizione registrazioni COGE per liquidazione gruppo utilizzata per il documento per registrare l'IVA del gruppo nel conto di liquidazione.
6. Il campo **Membri approvati** mostra il numero di membri del gruppo che sono impostati per presentare le dichiarazioni IVA al rappresentante. Per aggiungere nuovi membri, scegli il numero per aprire la pagina **Membri approvati**.
7. Per aggiungere nuovi membri, aggiungi le seguenti informazioni sulla pagina **Membri approvati dal gruppo IVA**:
    1. Nel campo **ID membro del gruppo** immetti un identificatore per il membro del gruppo.
    2. Nel campo **Nome del membro del gruppo** specifica il nome del membro del gruppo. 
    3. Nel campo **Società**, specifica la società da cui il membro del gruppo invia le dichiarazioni IVA in [!INCLUDE[prod_short](includes/prod_short.md)]. Per esempio, **CRONUS UK Ltd**.
    4. Specifica i dettagli relativi ai contatti della società.

## <a name="use-the-vat-group-management-features"></a>Utilizzare le funzionalità di gestione del gruppo IVA
I membri del gruppo IVA utilizzano le procedure standard per preparare le dichiarazioni IVA. L'unica differenza sta nello scegliere la versione del report **VATGROUP** che presenta la dichiarazione IVA al rappresentante del gruppo IVA anziché alle autorità. Per ulteriori informazioni, vedi [Informazioni sul report Dichiarazione IVA](finance-how-report-vat.md#vatreturn).

Le sezioni seguenti descrivono i task che i rappresentanti di un gruppo IVA devono svolgere.

### <a name="vat-group-submissions"></a>Invii gruppo IVA

La pagina **Invii gruppo IVA** elenca le dichiarazioni IVA presentate dai membri. La pagina funge da posizione di bozza per le presentazioni fino a quando il rappresentante del gruppo IVA non le include in una dichiarazione IVA per il gruppo. È possibile aprire gli invii per rivedere l'IVA per le singole caselle segnalate dal membro del gruppo IVA. 

> [!TIP]
> Sulla pagina **Periodi dichiarazione IVA**, il campo **Invii dei membri del gruppo** mostra quante dichiarazioni i membri hanno inviato. Per assicurarti che questo numero sia aggiornato, scegli l'azione **Ottieni dichiarazioni IVA**.

### <a name="creating-a-group-vat-return"></a>Creazione di una dichiarazione IVA di gruppo

Per dichiarare l'IVA per il gruppo, nella pagina **Dichiarazioni IVA** crea una dichiarazione IVA solo per l'azienda. Successivamente, includere gli invii IVA più recenti dai membri del gruppo IVA scegliendo l'azione **Includi IVA di gruppo**.  

Quando la dichiarazione IVA del rappresentante del gruppo IVA è stata presentata alle autorità per l'intero gruppo, normalmente si esegue l'azione **Calcola e registra liquidazione IVA**. Questa azione chiude i movimenti IVA aperti e trasferisce importi nel conto di liquidazione dell'IVA. Attualmente, questa azione non tiene conto degli invii di gruppo. <!--Has this changed?--> Verranno registrati solo i movimenti IVA della società rappresentante del gruppo IVA. Gli importi di presentazione dei membri del gruppo IVA devono essere registrati manualmente nell'importo di liquidazione IVA, in modo che il conto di liquidazione IVA del rappresentante del gruppo IVA rifletta la passività di quanto segnalato alle autorità. Questo comportamento cambierà in un prossimo aggiornamento di [!INCLUDE[prod_short](includes/prod_short.md)], in questo modo verrà liquidata l'intera IVA del gruppo (l'importo totale nelle righe del report nella dichiarazione IVA). <!--Has this behavior changed?-->

> [!NOTE]
> I membri del gruppo IVA possono correggere le dichiarazioni IVA presentate purché il rappresentante del gruppo non abbia rilasciato la dichiarazione IVA per il gruppo. Per apportare una correzione, il membro del gruppo IVA deve creare una nuova dichiarazione IVA per il periodo di dichiarazione IVA e presentarla al rappresentante del gruppo IVA. Dal lato del rappresentante del gruppo IVA, l'ultima dichiarazione IVA sarà inclusa nella pagina **Dichiarazioni IVA**. 

> [!IMPORTANT]
> La funzionalità del gruppo IVA è supportata solo nei mercati in cui [!INCLUDE[prod_short](includes/prod_short.md)] utilizza un quadro IVA che consiste in dichiarazioni IVA e periodi di dichiarazione IVA. Non è possibile utilizzare gruppi IVA in altri mercati che hanno altre implementazioni della dichiarazione IVA locale, come Austria, Germania, Italia, Spagna e Svizzera. 

## <a name="see-also"></a>Vedi anche
[Funzionalità locale del Regno Unito nella versione britannica](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Digitalizzazione delle imposte nel Regno Unito](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

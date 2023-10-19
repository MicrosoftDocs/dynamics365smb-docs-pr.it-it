---
title: L'estensione della gestione del gruppo IVA per il Regno Unito
description: Puoi impegnarti con altre aziende per formare un gruppo IVA in cui tutti i membri dichiarano l'IVA in un'unica dichiarazione.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: soalex
ms.topic: conceptual
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 09/18/2023
---

# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>L'estensione della gestione del gruppo IVA per il Regno Unito

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

È possibile connettere una o più aziende nel Regno Unito per combinare la dichiarazione IVA (imposta sul valore aggiunto) con un unico numero di registrazione. Questo tipo di modalità è noto come *gruppo IVA*. È possibile interagire con il gruppo come membro o rappresentante del gruppo.

## <a name="forming-a-vat-group"></a>Formazione di un gruppo IVA

I membri del gruppo IVA e il rappresentante del gruppo possono utilizzare la guida al setup assistito **Setup gestione gruppo IVA** per definire il coinvolgimento con il gruppo e creare una connessione tra i tenant [!INCLUDE[prod_short](includes/prod_short.md)]. I membri del gruppo utilizzeranno questa connessione per presentare le loro dichiarazioni IVA al rappresentante del gruppo. Il rappresentante del gruppo usa quindi una singola dichiarazione IVA del gruppo per le autorità fiscali.

[!INCLUDE[prod_short](includes/prod_short.md)] supporta le dichiarazioni IVA intragruppo per le aziende che utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] in locale oppure online, in qualsiasi combinazione, che influenza l'impostazione della comunicazione tra le aziende. Questo articolo descrive varie configurazioni dei gruppi.

### <a name="license-requirements"></a>Requisiti di licenza

I partecipanti al gruppo devono avere la licenza per l'uso di [!INCLUDE[prod_short](includes/prod_short.md)]. Non puoi utilizzare account guest nei gruppi IVA.

* Per calcolare e inviare le dichiarazioni IVA, un utente deve essere un utente completo di [!INCLUDE[prod_short](includes/prod_short.md)].
* Per accedere ed eseguire attività di base, come creare account, devi avere la licenza di membro del team [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="set-up-a-vat-group"></a>Impostare un gruppo IVA

Di seguito l'ordine consigliato dei passaggi utilizzati da un amministratore per configurare un gruppo IVA:

1. Crea la configurazione in [Configurazione di Microsoft Entra ID per i membri del gruppo](#microsoft-entra-id-setup-for-group-members).
2. Condividere le informazioni tecniche necessarie ai membri del gruppo IVA e al rappresentante per collegare i tenant [!INCLUDE[prod_short](includes/prod_short.md)]. Di solito, il rappresentante del gruppo IVA dispone di queste informazioni, come l'[URL API](#group-api-setup) e il nome dell'ambiente del rappresentante del gruppo IVA a cui i membri del gruppo IVA invieranno l'IVA.
3. Crea gli utenti che i membri del gruppo IVA utilizzeranno per autenticarsi quando si connettono a [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. Gli utenti devono disporre di una licenza utente completa per [!INCLUDE[prod_short](includes/prod_short.md)].
4. Esegui la guida al setup assistito **Impostare Gestione gruppo IVA** per collegare i membri del gruppo IVA.

   Il rappresentante del gruppo IVA deve fornire determinate informazioni ai membri del gruppo per completare la loro configurazione. Scopri di più nella sezione [Impostare i membri del gruppo IVA](#set-up-vat-group-members) seguente. Prendere nota dell'**ID membro del gruppo** per ciascun membro del gruppo IVA. Il rappresentante del gruppo ha bisogno di questi ID per aggiungere le società al gruppo IVA.
5. Imposta l'estensione della gestione del gruppo IVA nel [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA utilizzando la guida al setup assistito **Impostare Gestione gruppo IVA**.

> [!NOTE]
> Per connettersi al rappresentante del gruppo IVA, i membri del gruppo devono avere un account utente con accesso al [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. Il rappresentante del gruppo IVA deve creare almeno un utente per questo. Tuttavia, per motivi di sicurezza, si consiglia di creare un utente per ogni membro del gruppo IVA, che può essere un account utente di sistema non correlato a una persona reale. Assicurarsi di distribuire le credenziali utente dei membri del gruppo IVA in modo sicuro.

### <a name="microsoft-entra-id-setup-for-group-members"></a>Configurazione di Microsoft Entra ID per i membri del gruppo

Quando il rappresentante del gruppo IVA utilizza [!INCLUDE[prod_short](includes/prod_short.md)] online o locale, i membri del gruppo IVA devono utilizzare Microsoft Entra ID per autenticare gli utenti quando presentano le dichiarazioni IVA al rappresentante del gruppo IVA. Per [!INCLUDE[prod_short](includes/prod_short.md)] locale, i membri devono configurare il Single Sign-On. Per ulteriori informazioni, vedi [Configurare l'autenticazione Microsoft Entra con WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Se anche i membri del gruppo IVA utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] online, il membro può autenticarsi utilizzando le credenziali dell'utente designato e le informazioni di accesso fornite dal rappresentante del gruppo. Ulteriori informazioni nella sezione [Impostare i membri del gruppo IVA](#set-up-vat-group-members) riportata di seguito.

I membri del gruppo IVA che hanno [!INCLUDE[prod_short](includes/prod_short.md)] in locale devono configurare una registrazione dell'app in Microsoft Entra ID per il tenant [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. La registrazione dell'app abilita [!INCLUDE[prod_short](includes/prod_short.md)] online del rappresentante del gruppo IVA per autenticare il membro del gruppo. Ulteriori informazioni in [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app).

Quando l'amministratore dei membri del gruppo IVA crea la registrazione dell'app in Microsoft Entra, ID deve specificare le seguenti informazioni.

* Nella sezione **Autenticazione**, aggiungi **Web** come piattaforma e utilizza il seguente **URL di reindirizzamento**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* Nella sezione **Autenticazione**, nell'opzione per selezionare **Tipi di account supportati**, selezionare **Account in qualsiasi directory dell'organizzazione (qualsiasi directory Microsoft Entra - Multitenant)**.
* Nella sezione **Certificati e segreti** creare un nuovo segreto client e prendere nota del valore. I membri del gruppo IVA utilizzeranno il segreto quando impostano la connessione al rappresentante del gruppo.
* Nella sezione **Autorizzazioni API** aggiungere le autorizzazioni in [!INCLUDE[prod_short](includes/prod_short.md)]. Abilitare l'accesso delegato a **Financials.ReadWrite.All** e **user_impersonation**.
* Nella sezione **Sintesi** notare l'**ID applicazione (client)**. I membri del gruppo IVA utilizzeranno l'ID quando impostano la connessione al rappresentante del gruppo.

### <a name="group-api-setup"></a>Configurazione del gruppo API

Il rappresentante del gruppo IVA crea e fornisce un'API ai membri del gruppo. I membri utilizzano questa API per connettersi al tenant [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante e presentare le dichiarazioni IVA. I membri del gruppo IVA usano spesso [!INCLUDE[prod_short](includes/prod_short.md)] in tenant Microsoft Entra separati. Pertanto, sono necessarie ulteriori impostazioni per connettere il membro del gruppo IVA e il [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante.

> [!NOTE]
> Questa configurazione richiede le credenziali per un account amministratore che dispone di una licenza utente completa per [!INCLUDE[prod_short](includes/prod_short.md)].

1. Nell'interfaccia di amministrazione di Business Central per il tenant del rappresentante, scegli la scheda **Ambienti**.
1. Scegli l'ambiente del rappresentante.
1. Nella sezione **Dettagli** copia l'**URL**.
1. Apri Blocco note e incolla l'URL. Sostituisci `https://businesscentral.dynamics.com` con `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a>Impostare i membri del gruppo IVA

I membri del gruppo IVA si connettono al rappresentante chiamando un servizio Web sul tenant del rappresentante del gruppo IVA. Il chiamante deve essere autenticato utilizzando OAuth2. Quando l'estensione della gestione del gruppo IVA è impostata, ai membri viene richiesto di autenticarsi presso il rappresentante del gruppo IVA per ottenere e salvare un token di accesso. Questo token di accesso viene utilizzato quando si inviano dichiarazioni IVA al rappresentante del gruppo IVA.

> [!IMPORTANT]
> Le società membri del gruppo IVA non devono connettersi a HMRC perché dichiarano tramite il rappresentante del gruppo.

Prima che i membri del gruppo IVA avviino la configurazione (elencata di seguito), devono contattare il rappresentante del gruppo IVA per le seguenti informazioni sul tenant [!INCLUDE[prod_short](includes/prod_short.md)]:

* URL dell'API
* Nome della società
* Credenziali di accesso per l'utente dedicato

1. Nell'angolo superiore destro, scegliere **Impostazioni** icona ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente") e quindi l'azione **Setup assistito**.
2. Scegliere l'azione **Setup gestione gruppo IVA**.
3. Nel campo **Ruolo gruppo IVA**, scegli **Membro**, quindi **Avanti**.
4. Copiare il valore del campo **ID membro del gruppo** e condividerlo con il rappresentante del gruppo IVA in modo che possa aggiungere la società come membro approvato del gruppo.
5. Nel campo **Versione del prodotto rappresentante del gruppo**, specifica la versione di [!INCLUDE[prod_short](includes/prod_short.md)] che il rappresentante sta utilizzando.
6. Nel campo **URL API** immettere l'URL API fornito dal rappresentante del gruppo IVA. In genere, l'URL è nel seguente formato: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Ad esempio, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`
7. Nel campo **Società di rappresentanza del gruppo** inserisci la ragione sociale del rappresentante del gruppo IVA, ad esempio **CRONUS UK Ltd**.
8. Nel campo **Tipo di autenticazione** scegli l'opzione **OAuth2**. Se il rappresentante del gruppo IVA sta utilizzando [!INCLUDE[prod_short](includes/prod_short.md)] online, abilita l'opzione **Rappresentante del gruppo utilizza Business Central Online**, quindi scegli **Avanti**.

   Quindi, segui i passaggi nella sezione [Il rappresentante del gruppo IVA usa Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) o [Il rappresentante del gruppo IVA utilizza Business Central locale](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) riportata di seguito.

### <a name="vat-group-representative-uses-business-central-online"></a>Il rappresentante del gruppo IVA usa Business Central Online

1. Immetti le credenziali utente fornite dal rappresentante del gruppo IVA e aggiungi le autorizzazioni richieste per generare il token di accesso.
2. Scegli la configurazione della dichiarazione IVA attualmente utilizzata per inviare dichiarazioni IVA alle autorità fiscali del Regno Unito. 

Dopo aver completato il setup, [!INCLUDE[prod_short](includes/prod_short.md)] creerà una nuova configurazione in base a questa scelta e ti consentirà di presentare le dichiarazioni IVA al rappresentante del gruppo IVA.

### <a name="vat-group-representative-uses-business-central-on-premises"></a>Il rappresentante del gruppo IVA usa Business Central locale

1. Inserisci le credenziali utente fornite dal rappresentante del gruppo IVA e scegli **Avanti**.
2. Nel campo **ID client**, inserisci l'ID client dalla registrazione dell'app in [Configurazione di Microsoft Entra ID per i membri del gruppo](#microsoft-entra-id-setup-for-group-members).
3. Nel campo **Segreto client**, inserisci il segreto client dalla registrazione dell'app in Microsoft Entra ID.
4. Nel campo **Endpoint dell'autorità OAuth 2.0** immetti `https://login.microsoftonline.com/common/oauth2`.
5. Nel campo **URL risorsa OAuth 2.0** immetti `https://api.businesscentral.dynamics.com/`.
6. Nel campo **URL di reindirizzamento OAuth 2.0** immetti `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Dopo aver specificato i vari campi, scegli **Avanti** e quindi conferma la connessione di autenticazione per generare il token di accesso.
8. Scegli la configurazione della dichiarazione IVA attualmente utilizzata per inviare dichiarazioni IVA alle autorità fiscali del Regno Unito.

## <a name="set-up-the-vat-group-representative"></a>Impostare il rappresentante del gruppo IVA

> [!NOTE]
> Per i sistemi locali, [!INCLUDE[prod_short](includes/prod_short.md)] supporta solo una singola istanza del tenant del rappresentante del gruppo.

> [!IMPORTANT]
> La società rappresentante deve abilitare la connessione del servizio **Setup IVA HMRC** nella pagina **Connessioni del servizio**. I rappresentanti devono anche scaricare i periodi di dichiarazione IVA da HMRC.

1. Nell'angolo superiore destro scegli l'icona **Impostazioni** ![Impostazioni.](media/ui-experience/settings_icon_small.png "Icona Impostazioni per Gestione ruolo utente"), quindi scegli l'azione **Setup assistito**.
2. Scegliere l'azione **Setup gestione gruppo IVA**.
3. Nel campo **Ruolo gruppo IVA**, scegli **Rappresentante** per agire come rappresentante del gruppo IVA, quindi scegli **Avanti**.
4. Nel campo **Conto liquidazione gruppo**, specifica il conto di liquidazione utilizzato per gli importi IVA dei membri del gruppo. Questo account deve avere **Cespiti** come **Categoria conto**.
5. Nel campo **Conto liquidazione IVA** specifica il conto utilizzato per le liquidazioni IVA. Questo account deve avere **Passività** come **Categoria conto**.
6. Nel campo **Nr. riquadro IVA dovuta** specifica la casella che rappresenta l'importo IVA totale dovuto da un invio del gruppo IVA.
7. Nel campo **Definizione registrazioni COGE per liquidazione gruppo**, specifica la definizione registrazioni COGE per creare il documento con cui il rappresentante del gruppo registra il gruppo IVA nel conto di liquidazione.
8. Il campo **Membri approvati** mostra il numero di membri del gruppo che sono impostati per presentare le dichiarazioni IVA al rappresentante del gruppo. Per aggiungere nuovi membri, scegli il numero per aprire la pagina **Membri approvati gruppo IVA** e aggiungere le seguenti informazioni:
    1. Nel campo **ID membro del gruppo**, inserisci un identificatore per il membro del gruppo, come visualizzato durante la configurazione del membro del gruppo (ulteriori informazioni nella sezione [Impostazione del membro del gruppo IVA](#set-up-vat-group-members) precedente).
    2. Nel campo **Nome del membro del gruppo** specifica il nome del membro del gruppo.
    3. Nel campo **Società**, specifica la società da cui il membro del gruppo invia le dichiarazioni IVA in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio, **CRONUS UK Ltd**.
    4. Specifica i dettagli relativi ai contatti della società.

## <a name="use-the-vat-group-management-features"></a>Utilizzare le funzionalità di gestione del gruppo IVA

I membri del gruppo IVA utilizzano le procedure standard per preparare le dichiarazioni IVA. L'unica differenza sta nel fatto che i membri devono scegliere la versione del report **VATGROUP** nella pagina **Dichiarazione IVA** per inoltrare la dichiarazione al rappresentante del gruppo IVA anziché alle autorità. Ulteriori informazioni in [Informazioni sul report Dichiarazione IVA](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> I membri del gruppo IVA possono correggere le dichiarazioni IVA presentate purché il rappresentante del gruppo non abbia rilasciato la dichiarazione IVA per il gruppo. Per apportare una correzione, il membro del gruppo IVA deve creare una nuova dichiarazione IVA per il periodo di dichiarazione IVA e presentarla al rappresentante del gruppo IVA. Dal lato del rappresentante del gruppo IVA, l'ultima dichiarazione IVA del membro sostituirà la precedente e sarà inclusa nella pagina **Dichiarazioni IVA**.

Le sezioni seguenti descrivono i task che i rappresentanti di un gruppo IVA devono svolgere per compilare la dichiarazione IVA del gruppo.

### <a name="review-vat-member-submissions"></a>Revisione degli invii dei membri del gruppo IVA

La pagina **Invii gruppo IVA** elenca le dichiarazioni IVA presentate dai membri. La pagina funge da posizione di bozza per le presentazioni fino a quando il rappresentante del gruppo IVA non le include in una dichiarazione IVA per il gruppo. Il rappresentante può aprire gli invii per rivedere le singole caselle contenenti gli importi segnalate da ciascun membro del gruppo IVA.

> [!TIP]
> Nella pagina **Periodi di dichiarazione IVA**, il campo **Invii membri del gruppo** mostra quante dichiarazioni i membri hanno inviato. Per assicurarti che questo numero sia aggiornato, scegli l'azione **Ottieni dichiarazioni IVA**.

### <a name="create-a-group-vat-return"></a>Creare una dichiarazione IVA di gruppo

Per dichiarare l'IVA per il gruppo, nella pagina **Dichiarazioni IVA** crea una dichiarazione IVA solo per l'azienda. Successivamente, includere gli invii IVA più recenti dai membri del gruppo IVA scegliendo l'azione **Includi IVA di gruppo**.  

Quando il rappresentante del gruppo ha presentato la dichiarazione IVA del gruppo alle autorità, normalmente il rappresentante esegue l'azione **Calcola e registra liquidazione IVA**. Questa azione chiude i movimenti IVA aperti e trasferisce importi nel conto di liquidazione dell'IVA. Attualmente, questa azione non tiene conto degli invii di gruppo. Verranno registrati solo i movimenti IVA della società rappresentante del gruppo IVA. Gli importi di presentazione dei membri del gruppo IVA devono essere registrati manualmente nell'importo di liquidazione IVA, in modo che il conto di liquidazione IVA del rappresentante del gruppo IVA rifletta la passività di quanto segnalato alle autorità. Questo comportamento cambierà in un prossimo aggiornamento di [!INCLUDE[prod_short](includes/prod_short.md)], in questo modo verrà liquidata l'intera IVA del gruppo (l'importo totale nelle righe del report nella dichiarazione IVA).

> [!IMPORTANT]
> La funzionalità del gruppo IVA è supportata solo nei mercati in cui [!INCLUDE[prod_short](includes/prod_short.md)] utilizza un quadro IVA che consiste in dichiarazioni IVA e periodi di dichiarazione IVA. Non è possibile utilizzare gruppi IVA in mercati che hanno altre implementazioni della dichiarazione IVA locale, come Austria, Germania, Italia, Spagna e Svizzera.

## <a name="see-also"></a>Vedere anche

[Funzionalità locale del Regno Unito nella versione britannica](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Digitalizzazione delle imposte nel Regno Unito](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Consolidare dati finanziari di molteplici società](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

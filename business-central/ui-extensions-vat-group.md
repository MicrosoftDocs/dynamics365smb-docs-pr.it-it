---
title: Estensione della gestione del gruppo IVA
description: È possibile impegnarsi con altre aziende per formare un gruppo IVA e agire come membro o rappresentante del gruppo quando si dichiara l'IVA.
author: bholtorf
manager: annbe
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 470b8af1322fa0f3b295f566244af44c3183c2fe
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132448"
---
# <a name="the-vat-group-management-extension"></a>Estensione della gestione del gruppo IVA

È possibile unirsi a una o più aziende nel paese dell'utente per consolidare la dichiarazione IVA con un unico numero di registrazione. Questo tipo di modalità è noto come *gruppo IVA*. È possibile interagire con il gruppo come membro o rappresentante del gruppo.

## <a name="forming-a-vat-group"></a>Formazione di un gruppo IVA
I membri del gruppo IVA e il rappresentante del gruppo possono utilizzare la guida al setup assistito **Impostare Gestione gruppo IVA** per definire il coinvolgimento con il gruppo e creare una connessione tra i tenant [!INCLUDE[prod_short](includes/prod_short.md)]. I membri del gruppo utilizzeranno la connessione per presentare le loro dichiarazioni IVA al rappresentante del gruppo. Il rappresentante presenterà l'IVA alle autorità fiscali per conto del gruppo utilizzando un'unica dichiarazione IVA. 

## <a name="vat-group-constellations"></a>Costellazioni del gruppo IVA
La comunicazione avviene dai membri del gruppo al rappresentante. Il rappresentante del gruppo espone un'API che consente ai membri di presentare le loro dichiarazioni IVA al rappresentante del gruppo IVA. 
[!INCLUDE[prod_short](includes/prod_short.md)] supporta le dichiarazioni IVA tra gruppi per le aziende che utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] in locale o online e in qualsiasi combinazione. L'impostazione della comunicazione dipende dalla costellazione. Le sezioni seguenti descrivono come impostare le varie costellazioni del gruppo.

Il seguente elenco mostra l'ordine consigliato dei passaggi per impostare un gruppo IVA:

1. Creare il setup in Azure Active Directory. Per ulteriori informazioni, vedere [Requisiti per l'autenticazione](ui-extensions-vat-group.md#requirements-for-authentication).
2. Condividere le informazioni tecniche necessarie ai membri del gruppo IVA e al rappresentante per collegare i tenant [!INCLUDE[prod_short](includes/prod_short.md)]. Di solito, il rappresentante del gruppo IVA dispone di queste informazioni, come il nome dell'ambiente del rappresentante del gruppo IVA a cui i membri del gruppo IVA invieranno l'IVA.
3. Creare gli utenti nel [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA che i membri del gruppo IVA possono utilizzare per autenticarsi e connettersi.
4. Eseguire la guida al setup assistito **Impostare Gestione gruppo IVA** per collegare i membri del gruppo IVA.

  La guida richiede alcune informazioni dal rappresentante del gruppo IVA. Per ulteriori informazioni, vedere la sezione [Impostazione del membro del gruppo IVA](#vat-group-member-setup). Prendere nota dell'**ID membro del gruppo** per ogni membro del gruppo IVA. Il rappresentante ha bisogno di questi ID per aggiungere le società al gruppo IVA.
5. Impostare l'estensione Gestione gruppo IVA nel [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA utilizzando la guida al setup assistito **Impostare Gestione gruppo IVA**. 

> [!NOTE]
> Per connettersi al rappresentante del gruppo IVA, i membri del gruppo necessitano di un utente con accesso al [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. Il rappresentante del gruppo IVA deve creare almeno un utente per questo scopo, tuttavia, per motivi di sicurezza, si consiglia di creare un utente per ogni membro del gruppo IVA. Assicurarsi di distribuire le credenziali di questi utenti ai membri del gruppo IVA in modo sicuro.

## <a name="understanding-the-vat-group-management-setup"></a>Informazioni sull'impostazione di Gestione gruppo IVA

Il rappresentante del gruppo IVA espone un'API che i membri del gruppo IVA possono utilizzare per connettersi al tenant [!INCLUDE[prod_short](includes/prod_short.md)] e presentare le dichiarazioni IVA. I membri del gruppo IVA useranno spesso [!INCLUDE[prod_short](includes/prod_short.md)] in tenant Azure Active Directory separati. Pertanto, sono necessarie ulteriori impostazioni per stabilire una connessione tra il membro del gruppo IVA e il [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante. 
  
I membri del gruppo IVA si connettono al rappresentante chiamando un servizio Web sul tenant del rappresentante del gruppo IVA. Il chiamante deve essere autenticato utilizzando OAuth. Quando l'estensione Gestione gruppo IVA è impostata, verrà richiesto di autenticarsi presso il rappresentante del gruppo IVA per ottenere e salvare un token di accesso. Questo token di accesso viene utilizzato quando si inviano dichiarazioni IVA al rappresentante del gruppo IVA. 

L'autenticazione è gestita da Azure Active Directory, quindi la configurazione deve essere effettuata in Azure Active Directory del rappresentante del gruppo IVA per consentire le connessioni. Una registrazione dell'app Azure Active Directory deve essere configurata con l'accesso al [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. Questo vale anche se il rappresentante del gruppo IVA utilizza [!INCLUDE[prod_short](includes/prod_short.md)] in locale. Inoltre, è necessario configurare Single Sign-On se il rappresentante del gruppo IVA utilizza [!INCLUDE[prod_short](includes/prod_short.md)] in locale.

> [!NOTE]
> Per un periodo di tempo limitato, è supportata anche l'autenticazione mediante una chiave di accesso al servizio Web. Per ulteriori informazioni, vedere [Funzionalità deprecate nel primo ciclo di rilascio 2021](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Requisiti per l'autenticazione 
Quando il rappresentante del gruppo IVA utilizza [!INCLUDE[prod_short](includes/prod_short.md)] online o in locale, i membri del gruppo IVA utilizzano Azure Active Directory per autenticarsi quando presentano le dichiarazioni IVA al rappresentante del gruppo IVA. Se anche i membri del gruppo IVA utilizzano [!INCLUDE[prod_short](includes/prod_short.md)] online, il membro del gruppo IVA può autenticarsi utilizzando le credenziali dell'utente designato e le informazioni sull'endpoint. Per ulteriori informazioni, vedere [Impostazione del membro del gruppo IVA](ui-extensions-vat-group.md#vat-group-member-setup).

I membri del gruppo IVA che hanno [!INCLUDE[prod_short](includes/prod_short.md)] in locale devono configurare una registrazione dell'app in Azure Active Directory per il tenant [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA. La registrazione dell'app abiliterà [!INCLUDE[prod_short](includes/prod_short.md)] online del rappresentante del gruppo IVA per autenticare il membro del gruppo. Per ulteriori informazioni, vedere [Avvio rapido: registrare un'applicazione con la piattaforma di identità Microsoft](/azure/active-directory/develop/quickstart-register-app).

Quando si crea la registrazione dell'app in Azure Active Directory, è necessario specificare quanto segue.

* Nella sezione **Autenticazione** aggiungere **Web** come piattaforma e utilizzare il seguente **URL di reindirizzamento**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Nella sezione **Autenticazione**, nell'opzione per selezionare **Tipi di account supportati**, selezionare **Account in qualsiasi directory dell'organizzazione (qualsiasi directory Azure AD - Multitenant)**.
* Nella sezione **Certificati e segreti** creare un nuovo segreto client e prendere nota del valore. I membri del gruppo IVA utilizzeranno il segreto quando impostano la connessione al rappresentante del gruppo.
* Nella sezione **Autorizzazioni API** aggiungere le autorizzazioni in [!INCLUDE[prod_short](includes/prod_short.md)]. Abilitare l'accesso delegato a **Financials.ReadWrite.All** e **user_impersonation**.
* Nella sezione **Sintesi** notare l'**ID applicazione (client)**. I membri del gruppo IVA utilizzeranno l'ID quando impostano la connessione al rappresentante del gruppo. 

## <a name="vat-group-member-setup"></a>Impostazione del membro del gruppo IVA
Impostare il membro del gruppo IVA avviando la guida al setup assistito **Impostare Gestione gruppo IVA**. 

> [!NOTE]
> Prima di iniziare, contattare il rappresentante del gruppo IVA per le seguenti informazioni sul tenant [!INCLUDE[prod_short](includes/prod_short.md)]:
>
> * URL dell'API
> * Nome della società 
> * ID client
> * Segreto client
> * Credenziali di accesso per l'utente dedicato 

1. Per definire il ruolo del gruppo IVA della società, scegliere **Membro** e quindi scegliere **Avanti**.
2. Copiare il valore del campo **ID membro del gruppo** e condividerlo con il rappresentante del gruppo IVA in modo che possa aggiungere la società come membro approvato del gruppo.
3. Aggiungere l'**URL API** del rappresentante del gruppo IVA. In genere, l'URL è nel seguente formato: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Ad esempio, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative` 
4. Aggiungere il nome della società [!INCLUDE[prod_short](includes/prod_short.md)] del rappresentante del gruppo IVA, ad esempio *CRONUS UK Ltd*.
5. Scegliere **Tipo di autenticazione**, scegliere **OAuth2** e quindi scegliere **Avanti**.
6. Nel campo **ID cliente** immettere l'ID fornito dal rappresentante del gruppo IVA.
7. Nel campo **Segreto cliente fornito dal rappresentante del gruppo IVA** inserire il segreto fornito dal rappresentante del gruppo IVA.
8. Nel campo **Endpoint dell'autorità OAuth 2.0** immettere *https://login.microsoftonline.com/common/oauth2*.
9. Nel campo **URL risorsa OAuth 2.0** immettere *https://api.businesscentral.dynamics.com/*.
10. Nel campo **URL di reindirizzamento OAuth 2.0** immettere *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
11. Dopo aver specificato i vari campi, scegliere **Avanti**, quindi immettere le credenziali utente fornite dal rappresentante del gruppo IVA.
12. Scegliere la configurazione del report IVA da utilizzare per dichiarare l'IVA alle autorità del paese.

  Ad esempio, nel Regno Unito, la configurazione del report IVA sarebbe impostata per dichiarare l'IVA a HMRC. L'estensione Gestione gruppo IVA copia questa impostazione, ma sostituisce la codeunit di invio con una che supporta la presentazione al rappresentante del gruppo IVA anziché alle autorità fiscali. La codeunit è fornita da Microsoft. Al termine, selezionare **Avanti**.

## <a name="using-the-vat-group-management-features"></a>Utilizzo delle funzionalità di gestione del gruppo IVA

I membri del gruppo IVA utilizzano le procedure standard per preparare le dichiarazioni IVA. L'unica differenza sta nello scegliere la versione del report **VATGROUP** che presenta la dichiarazione IVA al rappresentante del gruppo IVA anziché alle autorità. Per ulteriori informazioni, vedere [Informazioni sul report Dichiarazione IVA](finance-how-report-vat.md#about-the-vat-return-report).

Le sezioni seguenti descrivono i task che i rappresentanti di un gruppo IVA devono svolgere.

### <a name="vat-group-submissions"></a>Invii del gruppo IVA

La pagina **Invii gruppo IVA** elenca le dichiarazioni IVA presentate dai membri. La pagina funge da posizione di bozza per le presentazioni fino a quando il rappresentante del gruppo IVA non le include in una dichiarazione IVA per il gruppo. È possibile aprire gli invii per rivedere l'IVA per le singole caselle segnalate dal membro del gruppo IVA.

### <a name="creating-a-group-vat-return"></a>Creazione di una dichiarazione IVA di gruppo

Per dichiarare l'IVA a nome del gruppo, nella pagina **Dichiarazioni IVA** creare una dichiarazione IVA solo per l'azienda. Successivamente, includere gli invii IVA più recenti dai membri del gruppo IVA scegliendo l'azione **Includi IVA di gruppo**.  

Quando la dichiarazione IVA del rappresentante del gruppo IVA è stata presentata alle autorità per conto dell'intero gruppo, normalmente si esegue l'azione **Calcola e registra liquidazione IVA**. Questa azione chiude i movimenti IVA aperti e trasferisce importi nel conto di liquidazione dell'IVA. Attualmente, questa azione non tiene conto degli invii di gruppo. Ciò significa che verranno registrate solo i movimenti IVA della società rappresentante del gruppo IVA. Gli importi di presentazione dei membri del gruppo IVA devono essere registrati manualmente nell'importo di liquidazione IVA, in modo che il conto di liquidazione IVA del rappresentante del gruppo IVA rifletta la passività di quanto segnalato alle autorità. Questo comportamento cambierà in un prossimo aggiornamento di [!INCLUDE[prod_short](includes/prod_short.md)], in questo modo verrà liquidata l'intera IVA del gruppo (l'importo totale nelle righe del report nella dichiarazione IVA). 

> [!NOTE]
> I membri del gruppo IVA possono correggere le dichiarazioni IVA presentate purché il rappresentante del gruppo non abbia rilasciato la dichiarazione IVA per il gruppo. Per apportare una correzione, il membro del gruppo IVA deve creare una nuova dichiarazione IVA per il periodo di dichiarazione IVA e presentarla al rappresentante del gruppo IVA. Dal lato del rappresentante del gruppo IVA, l'ultima dichiarazione IVA sarà inclusa nella pagina **Dichiarazioni IVA**. 

> [!IMPORTANT]
> La funzionalità del gruppo IVA è supportata solo nei mercati in cui [!INCLUDE[prod_short](includes/prod_short.md)] utilizza un quadro IVA che consiste in dichiarazioni IVA e periodi di dichiarazione IVA. Non è possibile utilizzare gruppi IVA in altri mercati che hanno altre implementazioni della dichiarazione IVA locale, come Austria, Germania, Italia, Spagna e Svizzera. 

## <a name="see-also"></a>Vedere anche

[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Impostare l'IVA (imposta sul valore aggiunto)](finance-setup-vat.md)  
[Utilizzare l'IVA nelle vendite e negli acquisti](finance-work-with-vat.md)  
[Digitalizzazione delle imposte nel Regno Unito](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Report IVA norvegese nella versione norvegese](LocalFunctionality/Norway/norwegian-vat-reporting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

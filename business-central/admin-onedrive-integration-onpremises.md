---
title: Configurazione dell'integrazione di OneDrive con Business Central in locale
description: Scopri come configurare Business Central in locale per l'integrazione di OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 09/28/2023
ms.author: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a>Configurazione dell'integrazione di OneDrive con Business Central in locale

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Questo articolo spiega come configurare l'integrazione di OneDrive con Business Central in locale. A differenza di [!INCLUDE[prod_short](includes/prod_short.md)] online, il collegamento tra Business Central e OneDrive for Business non viene impostato automaticamente. Se la connessione non è configurata, gli utenti non possono usare le funzioni di OneDrive.

Ci sono due attività che devono essere eseguite per configurare l'integrazione di OneDrive.

- La prima attività prevede la registrazione di un'applicazione (app) nel tenant di Microsoft Entra del tuo piano Microsoft 365. L'app registrata viene utilizzata per scopi di autenticazione. Questa attività viene in genere eseguita nel portale di Azure e nel client Web Business Central.
- La seconda attività prevede l'impostazione della connessione all'URL di OneDrive e l'attivazione delle funzionalità OneDrive in Business Central. Questa attività viene eseguita nel client Web Business Central. È diversa per la versione 21 rispetto alle versioni 19 e 20. La versione 21 introduce una nuova **Impostazione di OneDrive** che sostituisce **Setup connessione SharePoint**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] on-premises può essere collegato solo a OneDrive ospitato da Microsoft nel cloud. La connessione di [!INCLUDE[prod_short](includes/prod_short.md)] on premises al repository My Sites di SharePoint Server non è supportata.

## <a name="register-an-app-in-microsoft-entra-id-for-onedrive-integration"></a><a name="registerapp"></a>Registrare un'app in Microsoft Entra ID per l'integrazione OneDrive

In questa attività aggiungi un'app registrata per Business Central nel tenant Microsoft Entra del tuo piano Microsoft 365. Come altri servizi Azure che lavorano con Business Central, OneDrive richiede un'app registrata in Microsoft Entra ID. L'app registrata fornisce servizi di autenticazione e autorizzazione tra Business Central e SharePoint, utilizzato da OneDrive.

Per passaggi dettagliati per completare questa attività, vedi [Registrare un'applicazione in Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) nella guida per sviluppatori e professionisti IT.

Per la registrazione dell'applicazione, considera i seguenti punti:

- Se hai già registrato un'applicazione come parte di un'integrazione con un altro prodotto Microsoft, come Power BI, allora puoi riutilizzare l'app registrata. In questo caso, devi solo impostare le autorizzazioni di SharePoint per l'app registrata esistente.

- Assicurati di configurare l'app registrata con le seguenti autorizzazioni delegate all'API SharePoint :

    - AllSites.FullControl
    - User.ReadWrite.All
    
    Per il secondo ciclo di rilascio di Business Central 2021 (versione 19), imposta queste autorizzazioni:
    
    - TuttiSiti.Write
    - Scrivere i miei file
    - Utente.Read.All 

- Se utilizzi Business Central versione 19 o 20, copia **l'ID applicazione (client).** e il **segreto client** utilizzati dall'app registrata. Avrai bisogno di queste informazioni nel prossimo compito.

## <a name="get-your-onedrive-url"></a><a name="url"></a>Ottenere l'URL OneDrive

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>Impostare la connessione OneDrive nella versione 21 e successive

Utilizza questa procedura se usi il secondo ciclo di rilascio di Business Central 2022 (versione 21) o successive.

### <a name="prerequisites"></a>Prerequisiti

- Autorizzazione indiretta, modifica ed eliminazione (imd) sulla tabella **Scenario di servizio documenti** come minimo

### <a name="run-onedrive-setup"></a>Eseguire Setup OneDrive

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup OneDrive**, quindi scegli il collegamento correlato.
2. La prima volta che esegui il setup assistito, vedrai il collegamento **Privacy**. Leggi le informazioni della pagina e, se sei d'accordo con le condizioni, seleziona **Accetto** e continua.
3. Sulla pagina **Configura gestione file** hai le seguenti opzioni tra cui scegliere:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. Sulla pagina **Configura Business Central** immetti l'URL OneDrive nel campo **URL OneDrive**.

   [Come si trova l'URL OneDrive?](#url)
5. Scegli **Test della connessione** e aspetta i risultati.
   - Se il test ha esito positivo, scegli **Fatto**, e sei pronto per iniziare.
   - Se il test non riesce, riceverai un messaggio che descrive il problema. In genere il problema ha a che fare con l'URL che hai fornito. Scegli **OK** per tornare alla pagina **Configura Business Central**, verifica l'URL e riprova.
   - Se non hai già impostato l'app registrata in Microsoft Entra ID, si apre la guida **Impostare Microsoft Entra ID**.
6. Una volta completata, l'informativa sulla privacy per l'integrazione OneDrive è concordata per tutti gli utenti. Se vuoi cambiarla in modo che gli utenti debbano essere d'accordo o non essere d'accordo per se stessi, allora vai alla pagina **Stato informative sulla privacy** e seleziona **Consenti all'utente di decidere** per l'integrazione OneDrive. Agli utenti verrà quindi richiesto di accettare o meno l'informativa sulla privacy la prima volta che utilizzano le funzionalità OneDrive. Per maggiori informazioni, vedi [Informative sulla privacy](privacy-notices-status.md).

## <a name="set-up-the-connection-in--version-19-and-20"></a>Impostare la connessione in [!INCLUDE[prod_short](includes/prod_short.md)] nella versione 19 e 20

Utilizza questa procedura se usi il primo ciclo di rilascio di Business Central 2022 (versione 20) o il secondo ciclo di rilascio 2021 (versione 19).
> [!IMPORTANT]
> Configurando questa funzione, si abilitano anche le funzioni legacy che inviano file a OneDrive.  
>
>* La funzione Apri in Excel copierà automaticamente il file Excel su OneDrive, quindi lo aprirà in Excel Online. 
>* Esportando qualsiasi rapporto in un file, il file verrà automaticamente copiato in OneDrive, quindi aperto in Excel Online, Word Online o OneDrive. 
>* Altre funzioni possono anche aprirsi automaticamente in OneDrive.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , entrare in **Microsoft SharePoint - Configurazione connessione**, e poi scegliere il link relativo.
2. Nel campo **Descrizione**, inserisci una descrizione per la connessione, come **OneDrive**.
3. Nel campo **Cartella**, inserisci **Business Central**.
4. Nel campo **Posizione**, inserisci l'URL del tuo OneDrive.

   [Come si trova l'URL OneDrive?](#url)
5. Nel campo **ID** cliente, inserisci l'ID client dell'app registrata.
6. Nel campo **Segreto client**, inserisci il segreto dell'app registrata. 

> [!IMPORTANT]
> La pagina **Setup connessione SharePoint** è usata per configurare diverse funzioni legacy. La sezione **Generale** configura la connessione a OneDrive, e la sezione **Documenti condivisi** reindirizza invece i file a SharePoint . Il **Setup connessione SharePoint** è stato deprecato e verrà rimosso nella prossima versione. Si consiglia di non configurare la sezione **Documenti condivisi** . Per ulteriori informazioni, vedi [Funzionalità deprecate nell'app di base](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-21"></a>Dopo l'aggiornamento alla versione 21

Quando esegui l'aggiornamento alla versione 21 o successiva, la connessione esistente a OneDrive che è configurata nella pagina **Setup connessione SharePoint** funzionerà ancora. Ma poiché la pagina **Setup connessione SharePoint** pagina verrà rimossa nella versione 23, ti consigliamo di passare alla nuova integrazione OneDrive, come descritto nella sezione successiva. Fare questo passaggio ora renderà le cose più facili quando il **Setup connessione SharePoint** viene infine rimosso. Inoltre, ti consentirà di utilizzare la guida al setup assistito **Setup OneDrive** per gestire le funzionalità OneDrive accessibili agli utenti.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Passaggio da SharePoint legacy alla nuova integrazione OneDrive

Per passare alla nuova integrazione OneDrive, esegui la guida al setup assistito **Setup OneDrive** che puoi aprire direttamente o dalla pagina legacy **Setup connessione SharePoint**. Il setup assistito **Setup OneDrive** ti guiderà attraverso la transizione, fornendo informazioni sulle modifiche apportate lungo il percorso.

Prima di iniziare con il passaggio o mentre lo stai facendo, fai riferimento alla sezione successiva per conoscere alcuni aspetti e considerazioni sul processo. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a>Informazioni sul passaggio alla nuova integrazione OneDrive

Oltre all'integrazione OneDrive, Business Central può anche integrarsi con altri servizi, come Power BI e Stampa universale. L'integrazione con questi altri servizi richiede anche un'app Microsoft Entra registrata per l'autenticazione. L'app Microsoft Entra utilizzata da questi altri servizi è configurata nel setup assistito **Impostazione account Microsoft Entra**. Quando passi dalla configurazione della connessione SharePoint legacy, il nuovo setup assistito cambierà **Setup OneDrive** cambierà l'integrazione OneDrive per utilizzare anche il setup assistito **Impostazione account Microsoft Entra**, quindi tutte le integrazioni usano la stessa app Microsoft Entra.

Questa modifica ha implicazioni quando si passa alla nuova integrazione OneDrive, a seconda che sia già presente un'app Microsoft configurata nel setup assistito **Impostazione account Microsoft Entra**. 

> [!IMPORTANT]
> Dopo essere passato al nuovo setup OneDrive, non è più possibile utilizzare la pagina **Setup connessione SharePoint** per configurare l'integrazione OneDrive.

#### <a name="how-the-changes-affect-the-integration"></a>Come le modifiche influiscono sull'integrazione

Il setup assistito **Setup OneDrive** utilizzerà sempre l'app configurata nel setup assistito **Impostazione account Microsoft Entra**, se presente. Quando esegui il setup assistito **Setup OneDrive**, confronterà l'app configurata in **Impostazione account Microsoft Entra** con l'app corrente configurata in **Setup connessione SharePoint**.

> [!TIP]
> Nella pagina **Setup connessione SharePoint** e nel setup assistito **Impostazione account Microsoft Entra**, l'app Microsoft Entra è identificata dall'**ID client**.

- Se l'app in **Impostazione account Microsoft Entra** è diversa dall'app in **Setup connessione SharePoint**, l'integrazione OneDrive utilizza l'app in **Impostazione account Microsoft Entra**.

   In **Setup OneDrive** mentre effettui il passaggio, riceverai un messaggio simile al seguente testo: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` rappresenta l'ID client dell'app in **Impostazione account Microsoft Entra** che è utilizzata dall'integrazione OneDrive. 

  > [!IMPORTANT]
  > Per utilizzare la nuova integrazione OneDrive dopo aver effettuato il passaggio, è necessario concedere l'autorizzazione dell'app all'API SharePoint nel portale di Azure. Puoi eseguire questo passaggio prima o dopo il passaggio al nuovo setup OneDrive. Per ulteriori informazioni, vedi la sezione [Registrare un'app in Microsoft Entra ID per l'integrazione OneDrive](#registerapp).

- Se l'app in **Impostazione account Microsoft Entra** è la stesso app in **Setup connessione SharePoint**, l'integrazione OneDrive utilizzerà la stessa app di prima, ad eccezione della configurazione nel setup **Impostazione account Microsoft Entra**.

   In **Setup OneDrive** mentre effettui il passaggio, riceverai un messaggio simile al seguente testo:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Se non ci sono app configurate nel setup **Impostazione account Microsoft Entra** l'integrazione OneDrive utilizzerà la stessa app di prima.

   Il setup assistito **Setup OneDrive** copierà la configurazione dell'app nel setup **Impostazione account Microsoft Entra**, quindi verrà utilizzato per altre integrazioni che potrebbero essere configurate in seguito.

   In **Setup OneDrive** mentre effettui il passaggio, riceverai un messaggio simile al seguente testo:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Eseguire il setup OneDrive per passare alla nuova integrazione OneDrive

1. Apri la pagina **Setup OneDrive** o la pagina **Setup connessione SharePoint**.
2. Se usi la pagina **Setup connessione SharePoint** scegli **Vai al nuovo setup di OneDrive** nella notifica nella parte superiore della pagina.
3. Segui la guida di setup assistito **Setup OneDrive**.
4. Quando arrivi alla pagina **Configura gestione file** scegli una delle seguenti opzioni per attivare le funzioni:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. La pagina **Configura Business Central** mostra lo stesso URL utilizzato dall'esistente integrazione OneDrive. Se necessario, puoi modificare l'URL.
6. Seleziona **Test della connessione** e segui le istruzioni.

   Se il test ha esito positivo, seleziona **Fatto**, e sei pronto per iniziare. In caso contrario, utilizza i messaggi nella pagina per aiutarti a risolvere il problema.

## <a name="see-also"></a>Vedi anche
[Business Central e OneDrive per l'integrazione del business](across-onedrive-overview.md)  
[Apertura dei file di Business Central in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)


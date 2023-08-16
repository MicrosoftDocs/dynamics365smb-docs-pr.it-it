---
title: Risoluzione dei problemi di connettività
description: Descrive come utilizzare la pagina Risoluzione dei problemi di connettività per identificare e risolvere i problemi di connessione a Business Central online.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
---
# Risoluzione dei problemi di connettività per Business Central

> **SI APPLICA A:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Questa funzionalità è attualmente disponibile solo in anteprima. La funzionalità e la documentazione potrebbero cambiare nelle versioni successive. Se desideri contribuire alla documentazione in base alle tue scoperte, seleziona ![Modifica articolo in GitHub.](media/github-edit-pencil.png) **Modifica** e proponi le modifiche. Quindi ci daremo un'occhiata!

[!INCLUDE[prod_short](includes/prod_short.md)] Online include la pagina **Risoluzione dei problemi di connettività** che è possibile utilizzare per identificare problemi con la connessione al servizio online. Ci sono diversi fattori che influiscono sulla connettività a Business Central, come le impostazioni del firewall della rete o la configurazione del servizio del nome di dominio. La pagina consente di eseguire un elenco di controlli che diagnosticano i problemi di connettività comuni di Business Central. È possibile utilizzare le informazioni per provare a risolvere i problemi da soli o trasmetterle al rappresentante dell'assistenza.

> [!NOTE]
> La pagina **Risoluzione dei problemi di connettività** non esegue il test delle prestazioni o dell'affidabilità della rete, come la velocità della connessione. Verifica solo la connettività a risorse diverse.

## Avviare il controllo della connettività 

1. Apri un browser Internet.
2. Nell'indirizzo, inserisci l'URL che utilizzi per aprire Business Central e aggiungi `/connectivity` alla fine. 

    Ad esempio, se usi `https://businesscentral.dynamics.com`, inserisci:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Oppure, se l'URL include l'ID tenant, come `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, inserisci:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. Nella pagina **Risoluzione dei problemi di connettività** scegli **Inizia controllo**.

    Viene eseguita una serie di controlli e viene mostrato il risultato di ogni controllo:

    - ![Controllo della connettività riuscito.](media/connectivity-check.png) Indica che il controllo è riuscito.
    - ![Controllo della connettività non riuscito.](media/connectivity-failed.png) Indica che il controllo non è riuscito. Rivedi il messaggio sotto il controllo per maggiori dettagli.
    - ![Il controllo della connettività non è stato eseguito.](media/connectivity-blocked.png) Indica che il controllo non è stato eseguito, in genere a causa di un errore di un controllo precedente. Rivedi il messaggio sotto il controllo per maggiori dettagli.

4. Per eseguire nuovamente il controllo, scegli **Riavvia controllo**.

Le sezioni seguenti spiegano i controlli eseguiti e forniscono alcuni suggerimenti per risolvere eventuali problemi.

## Connettività Internet di base

Controlla la tua connessione Internet verificando che tu possa accedere a un dominio pubblico noto, come www.bing.com.

|Problema|Cose da provare|
|-------|-------------|
|Il tuo browser non supporta questo controllo|Apri la pagina in un browser supportato e riprova. Per un elenco di browser supportati, vedi [Requisiti minimi per l'utilizzo di Business Central - Browser](product-requirements.md#browsers)|
|Impossibile eseguire il ping del server al seguente URL: {url}|Verifica le impostazioni del firewall.|

## Caricamento delle risorse CDN (Content Delivery Network)

[!INCLUDE[prod_short](includes/prod_short.md)] usa Azure Content Delivery Network (CDN) per fornire le risorse necessarie per eseguire il client Web di Business Central. Questo controllo verifica che le risorse richieste siano disponibili e accessibili eseguendo il ping dell'istanza di Business Central in CDN.

|Problema|Cose da provare|
|-------|-------------|
|Il tuo browser non supporta questo controllo|Vedi il controllo **Connettività Internet di base**.|
|Impossibile eseguire il ping del server al seguente URL: {url}|Verifica le impostazioni del firewall.|

## Autenticazione utente

Verifica che l'utente corrente abbia effettuato l'accesso con un account Business Central valido.

|Problema|Cose da provare|
|-------|-------------|
|Nessun utente è attualmente autenticato|Accedi a Business Central con nome utente e password validi.|

## Individuazione degli ambienti di Business Central

Verifica gli ambienti Business Central disponibili per un utente autenticato, quindi verifica se l'utente può essere autenticato nell'ambiente.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problema|Cose da provare|
|-------|-------------|
|Nessun utente autenticato di cui eseguire questo controllo|Vedi il controllo **Autenticazione utente**.|
|Impossibile recuperare gli ambienti disponibili per il tuo account.|Controllare l'elenco degli ambienti disponibili nell'interfaccia di amministrazione di Business Central.|
|Il nome utente o la password non sono corretti oppure non si dispone di un account valido.| Verifica di aver effettuato l'accesso utilizzando il nome utente e la password corretti.|

## Connettività del servizio applicativo

Verifica che l'utente autenticato possa connettersi a un ambiente rilevato, in genere a partire dall'ambiente di produzione.

|Problema|Cose da provare|
|-------|-------------|
|Nessun utente autenticato di cui eseguire questo controllo|Vedi il controllo **Autenticazione utente**.|
|Impossibile recuperare gli ambienti disponibili per il tuo account.|Vedi **Individuazione degli ambienti di Business Central**.|
|Nessun indirizzo di cluster di cui eseguire questo controllo|Controllare l'elenco degli ambienti disponibili nell'interfaccia di amministrazione di Business Central.|
|L'endpoint della versione non esiste|Controllare l'elenco degli ambienti disponibili nell'interfaccia di amministrazione di Business Central.|

## Connettività server Web

Verifica che l'utente autenticato riesca a stabilire correttamente le connessioni con il server Web.

|Problema|Cose da provare|
|-------|-------------|
|Nessun utente autenticato per cui eseguire questo controllo|Vedi il controllo **Autenticazione utente**.|
|Impossibile recuperare gli ambienti disponibili per il tuo account.|Vedi **Individuazione degli ambienti di Business Central**.|
|Nessun indirizzo di cluster di cui eseguire questo controllo|Controllare l'elenco degli ambienti disponibili nell'interfaccia di amministrazione di Business Central.|
|Impossibile stabilire una connessione con il server Web|Svuota la cache e ricarica la pagina.|

## Stato di integrità del servizio

Segnala lo stato di integrità del servizio Business Central controllando le interruzioni dichiarate.

|Problema|Cose da provare|
|-------|-------------|
|Nessun utente autenticato per cui eseguire questo controllo|Vedi il controllo **Autenticazione utente**.|
|Business Central è temporaneamente non disponibile. Prego riprovare più tardi.|Riprovare.|

## Vedi anche

[Risorse per guida e supporto](product-help-and-support.md)  
[Panoramica dei task per impostare Business Central](setup.md)  
[Domande frequenti sull'utilizzo di Business Central](across-faq.yml)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Interfaccia di amministrazione di Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]

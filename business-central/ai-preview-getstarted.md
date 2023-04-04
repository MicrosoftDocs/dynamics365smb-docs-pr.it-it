---
title: Ottenere l'accesso all'anteprima di Business Central - Edizione Copilot
description: Spiega come ottenere un ambiente Business Central con la nuova funzionalità IA per la generazione di suggerimenti di testo per le descrizioni di articoli/prodotti.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# Iniziare a usare la versione di anteprima di Business Central - Edizione Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Puoi provare il testo di marketing degli articoli basato sull'intelligenza artificiale con Copilot indipendentemente dal fatto che tu sia un cliente Business Central esistente o un potenziale cliente, ovvero qualcuno che è solo interessato a esplorare Business Central e provare la nuova funzionalità. Per iniziare, devi ottenere l'accesso a una versione di anteprima di Business Central che supporti la nuova funzionalità. Completa la sezione sottostante che ti riguarda.

## L'organizzazione già usa Business Central

Come cliente o partner esistente, avrai bisogno di un amministratore con accesso all'interfaccia di amministrazione di Business Central per configurare un *ambiente sandbox* che esegua la versione di anteprima che include Copilot. Una volta che l'ambiente sandbox è attivo e funzionante, gli utenti possono provare la nuova funzionalità.

Se sei un amministratore dell'ambiente, completa i seguenti passaggi:

1. Accedi all'interfaccia di amministrazione di Business Central.
2. Seleziona **Ambienti** > **Nuovo**.
3. Nel riquadro **Crea ambiente** , specifica un nome per il nuovo ambiente nel campo **Nome ambiente**.
4. Imposta **Tipo di ambiente** su **Sandbox**.
5. Imposta **Paese** su **Stati Uniti**.

   > [!IMPORTANT]
   > L'anteprima è disponibile solo per gli Stati Uniti. Le organizzazioni in qualsiasi altro paese o regione possono comunque creare un'anteprima nell'ambiente sandbox per gli Stati Uniti per provare Copilot.

6. Nella casella **Versione** , scegli una versione **22.0.54157.54311 (Anteprima - Edizione Copilot)**.

   > [!IMPORTANT]
   > Devi utilizzare **22.0.54157.54311 (Anteprima - Edizione Copilot)** per provare Copilot.

7. Selezionare **Crea**.  

Per ulteriori informazioni su come creare gli ambienti sandbox, vai a [Creare un ambiente](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Gli ambienti sandbox di anteprima sono disponibili solo fino al 1° maggio 2023. Dopo questa data, dovrai eseguire il provisioning di un nuovo ambiente o aggiornare uno qualsiasi dei tuoi altri ambienti alla versione 22.0 o successiva per continuare a provare l'anteprima del testo di marketing degli articoli basato sull'intelligenza artificiale.

## L'organizzazione non usa Business Central

Se non sei un cliente di Business Central, registrati per una versione di valutazione gratuita per provare le nuove funzionalità di intelligenza artificiale. Iscriversi alla versione di valutazione è semplice. Verrai guidato attraverso alcuni passaggi in cui dovrai fornire alcune informazioni, come il tuo indirizzo e-mail, numero di telefono e nome. Per ottenere la versione di valutazione, completa i seguenti passaggi:

1. Vai a [questo sito di valutazione](https://go.microsoft.com/fwlink/?linkid=2227167) per iniziare la procedura di registrazione.
2. Segui le istruzioni visualizzate.

   Ti viene chiesto di fornire informazioni come il tuo indirizzo e-mail, nome e numero di telefono. L'esperienza esatta può variare, a seconda delle informazioni fornite. Ma qui ci sono un paio di punti importanti da tenere presente durante il processo di registrazione:

   - Per l'indirizzo e-mail, usa il tuo indirizzo e-mail di lavoro o della scuola. Stabiliremo la tua versione di prova sull'account della tua organizzazione. Non è possibile utilizzare gli indirizzi e-mail forniti dai servizi di posta elettronica consumer o dai provider di telecomunicazioni, come outlook.com, hotmail.com, gmail.com, e altri.
   - Quando arrivi all'opzione per **Paese o area geografica** assicurati di impostare **Stati Uniti**.

      > [!IMPORTANT]
      > Devi impostare **Paese o area geografica** su **Stati Uniti**; in caso contrario, il testo di marketing degli articoli basato sull'intelligenza artificiale con Copilot non sarà disponibile in Business Central.  
3. Quando arrivi al passaggio **Dettagli di conferma** sei pronto per iniziare la versione di valutazione.

   - Per andare direttamente a Business Central, seleziona **Ignora e vai a Dynamics 365 Business Central** > **Inizia**.
   - Hai anche la possibilità di invitare altri membri della tua organizzazione alla versione di valutazione gratuita. Basta inserire gli indirizzi e-mail di ogni persona, quindi selezionare **Invia inviti**. Seleziona **Inizia** per passare a Business Central.  

   Verrà eseguito il reindirizzamento alla versione di valutazione all'indirizzo [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Possono essere necessari diversi minuti per preparare la versione di valutazione la prima volta che accedi.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Una volta effettuato l'accesso, verrà visualizzata la home page di Business Central, chiamata Gestione ruolo utente, simile alla figura seguente:

   [![Mostra Gestione ruolo utente di Business Central e l'elenco di controllo per Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Per ottenere un'introduzione guidata alla creazione di testo di marketing basato sull'intelligenza artificiale con Copilot, in **Elenco di controllo personale** nella parte superiore della pagina, seleziona **Crea con Copilota** > **Inizia presentazione**. Quindi segui le istruzioni sullo schermo.

   > [!TIP]
   > Se non vedi **Elenco di controllo personale**, seleziona prima il pulsante **Mostra presentazioni dimostrative**.

## Passaggi successivi

Le funzionalità IA fornite da Copilot devono essere abilitate prima che tu o chiunque altro possiate utilizzare Copilot. Per abilitare le funzionalità IA, un amministratore deve accettare le condizioni dell'[anteprima](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) e l'[Informativa sulla privacy di Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) per conto dell'organizzazione.

> [!NOTE]
> Se stai utilizzando una versione di prova, sei l'amministratore. Se durante la registrazione hai invitato altre persone della tua organizzazione alla versione di prova, queste non potranno utilizzare Copilot finché non accetti i termini e le condizioni.

Ci sono due modi per acconsentire come amministratore:

- Il modo più semplice è utilizzare Copilot. La prima volta che utilizzi Copilot come amministratore, ti viene chiesto di rivedere i termini e le condizioni, quindi accettare o meno. Per informazioni su come utilizzare Copilot, vai a [Aggiungere testo di marketing agli articoli](item-marketing-text.md).  

- L'altro modo consiste nell'utilizzare la pagina **Stato avvisi sulla privacy** in Business Central e accettare l'integrazione di **Azure OpenAI** per tutti gli utenti. Per saperne di più, vai a [Consenso ai termini e condizioni](enable-ai.md#consent-to-or-reject-the-preview-and-privacy-terms-and-conditions-for-all-users).

## Vedere anche

[Panoramica del testo di marketing dell'articolo basato su intelligenza artificiale con Copilot](ai-overview.md)  
[Configurare testo del marketing articolo basato su intelligenza artificiale con Copilot come amministratore](enable-ai.md)  
[Creare un testo di marketing per gli articoli utilizzando Copilot](item-marketing-text.md)  
[Domande frequenti sul testo di marketing per l'articolo basato sull'intelligenza artificiale (anteprima) con Copilot](ai-faq.md)  
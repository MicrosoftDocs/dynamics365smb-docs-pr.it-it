---
title: Ottieni il componente aggiuntivo Business Central per Outlook
description: Scopri come installare l'add-in Business Central per Outlook per la tua organizzazione o per uso personale.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, Outlook'
ms.search.form: '1831, 1832'
ms.date: 04/27/2022
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-outlook" />Ottieni il componente aggiuntivo Business Central per Outlook

Con [!INCLUDE[prod_short](includes/prod_short.md)], puoi gestire le interazioni commerciali con i tuoi clienti e fornitori, direttamente in Microsoft Outlook. Con il componente aggiuntivo [!INCLUDE[prod_short](includes/prod_short.md)] Outlook, è possibile vedere i dati finanziari relativi a clienti e fornitori. È anche possibile creare e inviare documenti finanziari, come preventivi e fatture.  

Ci sono due modi per installare l'add-in di Business Central per Outlook, a seconda del tuo ruolo nell'organizzazione:

- Come amministratore di Microsoft 365, usa la *Distribuzione centralizzata* per installare automaticamente il componente aggiuntivo per l'intera organizzazione, per gruppi o per utenti specifici.

- Come qualsiasi utente, installa l'add-in per il tuo uso personale, se il tuo amministratore non l'ha già distribuito per te.

## <a name="about-the-business-central-add-in-for-outlook" />Informazioni sul componente aggiuntivo Business Central per Outlook

L'add-in Business Central per Outlook consiste in due add-in più piccoli:

- Approfondimenti di contatto

    Questo add-in fornisce agli utenti [!INCLUDE[prod_short](includes/prod_short.md)] informazioni sul cliente o sul venditore nelle e-mail di Outlook e negli appuntamenti del calendario. Permette anche di creare e inviare documenti aziendali [!INCLUDE[prod_short](includes/prod_short.md)], come preventivi di vendita e fatture a un contatto. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Vista del documento

    Quando un'email fa riferimento a un numero di documento aziendale nel corpo dell'email, questo add-in fornisce un collegamento diretto e in linea dal corpo dell'email al documento aziendale effettivo in [!INCLUDE[prod_short](includes/prod_short.md)].

Per ulteriori informazioni su ciò che si fa con i componenti aggiuntivi, vedi [Utilizzare Business Central come casella di posta elettronica aziendale in Outlook](work-outlook-addin.md).

Ogni add-in è fornito come un file XML, chiamato *manifest*, che deve essere installato in Outlook da chiunque voglia questa funzionalità. Questi file descrivono come attivare gli add-in e connettersi a Business Central quando sono usati in Outlook. Lavorare con questi file è tipicamente fatto da un amministratore. Come utente normale, nella maggior parte dei casi, non avrete a che fare direttamente con questi file. O il tuo amministratore imposterà l'add-in per installarlo automaticamente per te o userai il setup assistito integrato per gestire l'installazione.

> [!IMPORTANT]
> Lavorare con più ambienti Il componente aggiuntivo Business Central per Outlook è progettato per funzionare con un unico ambiente Business Central. Quando il componente aggiuntivo viene installato, il nome dell'ambiente viene incluso nel manifesto del componente aggiuntivo. Questa configurazione significa che il componente aggiuntivo si connette solo all'ambiente da cui è stato installato. Per utilizzare il componente aggiuntivo con un ambiente diverso, devi aprire l'ambiente e installare nuovamente il componente aggiuntivo.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin" />Distribuire il componente aggiuntivo utilizzando la distribuzione centralizzata come amministratore

La distribuzione centralizzata è una funzione nel centro amministrativo di Microsoft 365 che si usa per installare automaticamente i componenti aggiuntivi nelle applicazioni Office degli utenti, come Outlook. È il modo raccomandato per gli amministratori di distribuire i componenti aggiuntivi di Office agli utenti e ai gruppi all'interno dell'organizzazione.

> [!NOTE]
> Per Business Central on-premises, vedi [Impostazione dell'Add-In per l'integrazione di Outlook con Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) nel contenuto dell'amministrazione (solo in inglese).

### <a name="prerequisites" />Prerequisiti

- Una sottoscrizione Microsoft 365  
- Agli utenti viene assegnata una licenza Microsoft 365  
- Il tuo account Microsoft 365 ha il ruolo di *Amministratore globale* o *Amministratore di Exchange*

### <a name="deploy-the-add-in" />Distribuire il componente aggiuntivo

1. In Business Central, scegli la ![lampadina che apre la funzione Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). , entrare in **Setup assistito**e poi scegliere il link relativo.
2. scegli **Outlook Add-in Centralized Deployment** per avviare la guida alla configurazione assistita.
3. Esamina la prima pagina e scegli **Avanti** per aprire la pagina per scaricare i componenti aggiuntivi.
4. Nella colonna **Distribuisci**, seleziona la casella di controllo per i componenti aggiuntivi che vuoi distribuire, quindi scegli **Scarica e continua**.

    Un file con il nome *OutlookAddins.zip* viene scaricato sul tuo dispositivo.

5. A questo punto, hai finito il lavoro che devi fare in Business Central, quindi puoi scegliere **Fatto**.

   >[!TIP]
   > Prima di scegliere **Avanti**, seleziona il collegamento **Vai a Microsoft 365 (si apre in una nuova finestra)** per aprire e accedere all'interfaccia amministrativa di Microsoft 365 in una nuova finestra del browser. Dovrete comunque andare all'interfaccia di amministrazione di Microsoft 365 in un passo successivo.

6. Vai nella cartella dove è stato scaricato OutlookAddins.zip ed estrai i file **Contact Insights.xml** e **Document View.xml** dallo zip in una cartella di tua scelta.

    Per maggiori informazioni, vedi [Zip e Unzip di file e cartelle](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Accedi all'interfaccia amministrativa di Microsoft 365, quindi vai ad [App integrate](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Scegliere **Carica applicazioni personalizzate**.
9. Nella pagina **Carica app da distribuire**, scegli **Carica manifest file (.xml) dal dispositivo** > **Scegli file**.
10. Seleziona uno dei file di aggiunta che hai estratto prima, per esempio, **Contact Insights.xml**.
11. Segui le istruzioni per assegnare gli utenti e distribuire l'add-in.
12. Ripeti i passi da 9 a 11 per l'altro file aggiuntivo, se vuoi.

> [!IMPORTANT]
> Un segno di spunta verde appare quando l'add-in viene distribuito nel centro amministrativo. Tuttavia, possono essere necessarie fino a 24 ore prima che gli utenti vedano l'add-in nell'app Outlook. Gli utenti potrebbero dover riavviare anche Outlook.

Quando hai finito, puoi sempre cambiare la distribuzione nell'interfaccia di amministrazione di Microsoft 365, come assegnare più utenti. Per ulteriori informazioni sulla distribuzione dei componenti aggiuntivi nel centro amministrativo, vedi [Distribuzione di componenti aggiuntivi nel centro amministrativo](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true).

## <a name="a-nameinstallainstall-the-add-in-for-your-own-use" /><a name="install"></a>Installare l'add-in per uso personale

Se la tua organizzazione lo permette, puoi installare l'add-in Business Central solo per te stesso. Contatta il tuo amministratore se non sei sicuro.

1. In Business Central, vai alla ![lampadina che apre la funzione Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). , inserire **Ottieni l’Add-in Outlook**, poi scegliere il link relativo.
2. Leggi la pagina e scegli **Avanti** quando sei pronto.
3. Se vuoi ricevere un messaggio e-mail di benvenuto da Business Central con una panoramica sull'utilizzo del componente aggiuntivo, attiva **Invia messaggio e-mail di esempio**.
4. scegli **Fine** per completare l'installazione.

Business Central si collegherà al tuo server di posta elettronica e installerà l'add-in nel tuo Outlook. Non ci vorrà molto tempo. Ora sei pronto per iniziare ad usare l'add-in in Outlook.

### <a name="a-nameonpremafor-business-central-on-premises" /><a name="onprem"></a>Per Business Central on-premises

Se stai usando Business Central on-premises, l'installazione dell'add-in potrebbe essere leggermente diversa.

1. In Business Central, vai alla ![lampadina che apre la funzione Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). , inserire **Ottieni l’Add-in Outlook**, poi scegliere il link relativo.
2. Leggi la pagina e scegli **Avanti** quando sei pronto.
3. Fai uno dei seguenti passi, a seconda della pagina che vedi:

    - Se vedete il pulsante **Installa sul mio Outlook**, sceglilo e il gioco è fatto.
    - Se vedi il pulsante **Avanti**, sceglilo. Nella pagina successiva, se vuoi ricevere un messaggio email di benvenuto da Business Central con una panoramica sull'uso dell'add-in, attiva **Invia messaggio email campione**. Poi, scegli **Fine** e avete finito.
    - Se vedi il pulsante **Scarica add-in**, sceglilo, poi vai al passo successivo.
4. Quando scegli **Scarica add-in**, un file con il nome *OutlookAddins.zip* viene scaricato sul vostro dispositivo. Dovresti vedere il file nella parte superiore del browser.

   Vai nella cartella dove è stato scaricato OutlookAddins.zip ed estrai i file **Contact Insights.xml** e **Document View.xml** dallo zip in una cartella di tua scelta. Per maggiori informazioni su come estrarre i file, vedi [Zip e Unzip di file e cartelle](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Aprire Outlook e scegliere **Get Add-ins** dalla barra multifunzione. Oppure, se stai usando Outlook sul web, seleziona il menu a discesa su qualsiasi messaggio di posta elettronica nuovo o esistente, quindi seleziona **Get Add-ins**.
6. scegli **I miei add-in** > **Aggiungere un add-in personalizzato** > **Aggiungere da un file**.
7. Scegli uno dei file .xml che hai estratto, come **Contact Insights.xml**, poi scegli **Open** > **Install**.
8. Ripeti i passi 6 e 7 per l'altro file .xml, se ne hai scaricato uno.

Ora sei pronto per iniziare ad usare l'add-in in Outlook.

## <a name="see-related-microsoft-trainingtrainingmodulesalternative-interfaces-dynamics--business-centralindex" />Vedi il relativo [training Microsoft](/training/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also" />Vedi anche

[Prepararsi a fare affari](ui-get-ready-business.md)  
[Scaricare Business Central sul dispositivo mobile](install-mobile-app.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Finanze](finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Requisiti minimi per Outlook](product-requirements.md#outlook)  
[Utilizzare i componenti aggiuntivi in Outlook sul Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

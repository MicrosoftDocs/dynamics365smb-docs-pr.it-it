---
title: Creare una nuova società utilizzando una guida al setup assistito
description: Creare una nuova società vuota in Business Central è facile. Una guida al setup assistito fornisce le istruzioni nei vari passaggi e consente di importare i dati aziendali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/14/2023
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
---
# Creare nuove società in [!INCLUDE[prod_short](includes/prod_short.md)]

In [!INCLUDE[prod_short](includes/prod_short.md)] il contenitore per i dati aziendali che appartiene alla Business Unit o alla persona giuridica viene indicato con il termine *società*. Quando ti iscrivi a [!INCLUDE[prod_short](includes/prod_short.md)], vengono fornite una società dimostrativa e una società vuota denominata *La mia azienda*. Il passaggio tra le società è facile: basta accedere a **Impostazioni personali** e passare all'altra società. È tuttavia possibile anche creare nuove società in [!INCLUDE[prod_short](includes/prod_short.md)] in base alle esigenze aziendali.  

> [!NOTE]
> Per creare una nuova società, devi essere assegnato al set di autorizzazioni **Super** .

Quando si crea una nuova azienda una guida al setup assistito aiuta ad applicare le nozioni di base. Successivamente è possibile importare i dati rilevanti dal sistema legacy o un'altra azienda in [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Scegliere il modello giusto

Se decidi di aggiungere una società a [!INCLUDE[prod_short](includes/prod_short.md)], puoi utilizzare la guida al setup assistito **Crea nuova società** per iniziare. La guida al setup è disponibile nella pagina **Società** e tramite la ricerca nel campo **Società** nella pagina **Impostazioni personali**.  

La guida al setupoffre due modelli e un'opzione vuota:

- **Valutazione - Dati campione**  
    Crea una società che è simile alla società di dimostrazione con i dati di esempio e i dati di setup. Questo tipo di società è a tua disposizione senza passare a un periodo di valutazione di 30 giorni, come fanno gli altri tipi.  
- **Produzione - Solo dati setup**  
    Crea una società che è simile a **La mia società** con i dati di setup ma senza i dati di esempio. Puoi utilizzare questa società per un periodo di valutazione di 30 giorni.  
- **Crea nuovo - Senza dati**  
    Crea una società vuota senza dati di setup. Puoi utilizzare questa società per un periodo di valutazione di 30 giorni.  

Se si desidera iniziare in modo semplice con una società nuova, scegliere **Produzione - Solo dati setup** e quindi importare i dati della propria azienda, ad esempio i clienti, gli articoli e i fornitori. Scegli il modello **Nuovo** se vuoi impostare tutto da zero. È possibile in tal caso utilizzare la guida al setup assistito **Setup società** per istruzioni su come iniziare con i dati di setup di base.  

> [!NOTE]  
> La creazione di una nuova società richiede alcuni minuti prima che sia possibile accedervi in [!INCLUDE[prod_short](includes/prod_short.md)]. Lo stato del setup nella pagina **Società** mostra quando la nuova società è pronta. È quindi possibile passare alla nuova società utilizzando **Impostazioni personali**.  

Nella versione di valutazione di 30 giorni è possibile creare un numero qualsiasi di nuove società, ma saranno disponibili solo nel periodo di valutazione. Per altre informazioni, contattare il partner [!INCLUDE[prod_short](includes/prod_short.md)]. Vedi anche l'articolo [Domande frequenti sulla versione di valutazione di Dynamics 365 Business Central](trial-faq.md).  

L'amministratore può ottenere ulteriori informazioni su versioni di valutazione e sottoscrizioni [qui](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## Copiare una società

Nella pagina **Società** è possibile utilizzare l'azione **Copia** per creare una seconda società in base al contenuto di una società esistente. Ciò è utile ad esempio quando si desidera testare una società senza interrompere i dati di produzione.

> [!Important]
> Non utilizzare l'azione Copia per eseguire un backup di un'azienda. Per eseguire un backup, esporta il database come file con estensione BACPAC. Per ulteriori informazioni, vedere [Esportazione dei database](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) nella Guida per sviluppatori e amministratori.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## Impostare la società

Quando si accede a una nuova società, la procedura guidata **Setup società** si avvia automaticamente e fornisce le istruzioni per iniziare. Verranno richieste le informazioni sulla società, ad esempio l'indirizzo, i dati bancari e il metodo di calcolo dei costi di magazzino. Queste informazioni servono da base per molte aree di [!INCLUDE[prod_short](includes/prod_short.md)] che non dovranno quindi più essere impostate manualmente un momento successivo.  

Ad esempio, [!INCLUDE [prod_short](includes/prod_short.md)] include l'indirizzo della tua società nelle fatture e in altri documenti e le tue informazioni bancarie nei pagamenti. Il metodo di valutazione dei costi vieneutilizzato per il calcolo peri prezzi e della valutazione del magazzino.  

Dopo che sono state impostate le informazioni di base, è possibile impostare le restanti aree fondamentali. A questo punto puoi aggiungere i dati aziendali, ad esempio i clienti e i fornitori. Per ulteriori informazioni, vedi [Impostare [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## Società e ambienti

[!INCLUDE [company_environment](includes/company_environment.md)]

Per ulteriori informazioni, vedere [Passare a un'altra società o ambiente](ui-organization-switch.md). Per ulteriori informazioni sugli ambienti, vedi [Informazioni sull'infrastruttura di Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (solo in inglese).  

## Modificare il nome di una società

Una volta creata una società, non puoi modificarne il nome. Puoi tuttavia modificarne il **Nome visualizzato**, ovvero il testo che verrà visualizzato per la società nell'applicazione.  

> [!TIP]
> Puoi rinominare una società se utilizzi [!INCLUDE[prod_short](includes/prod_short.md)] locale.

## Aggiungere Contoso Coffee

L'app Contoso Coffee fornisce dati dimostrativi per aiutarti a esplorare le funzionalità avanzate di [!INCLUDE [prod_short](includes/prod_short.md)]. Trova l'app in AppSource e installala in una società vuota, ad esempio un'azienda in un ambiente sandbox. Per ulteriori informazioni, vedi [Introduzione ai dati dimostrativi di Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## Vedi il relativo [training Microsoft](/training/modules/create-new-companies-dynamics-365-business-central/)

## Vedere anche

[Personalizzazione di Business Central](ui-customizing-overview.md)  
[Impostazione di [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Informazioni sull'infrastruttura di Business Central Online (solo in inglese)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

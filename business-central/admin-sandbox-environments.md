---
title: Ambienti sandbox
description: 'Scopri come un ambiente dedicato può aiutarti a esplorare, imparare, dimostrare, sviluppare, risolvere i problemi e testare Business Central in sicurezza.'
author: brentholtorf
ms.topic: conceptual
ms.reviewer: bholtorf
ms.devlang: al
ms.search.keywords: 'sandbox, demo, develop'
ms.date: 12/20/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="sandbox-environments-in-"></a>Ambienti sandbox in [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)] online è possibile ottenere facilmente un ambiente sicuro in cui testare, istruire o risolvere i problemi senza disturbare i processi di lavoro o i dati aziendali della società. Tale ambiente non di produzione è denominato *sandbox*. Isolato dalla produzione, un ambiente sandbox consente di esplorare, apprendere, dimostrare, sviluppare e testare in sicurezza il servizio senza il rischio di compromettere i dati e le impostazioni dell'ambiente di produzione.  

> [!TIP]
> Sei arrivato a questo articolo dopo aver scelto il nome del tuo ambiente [!INCLUDE [prod_short](includes/prod_short.md)] nella barra in alto? Attualmente, non è possibile modificare il nome o l'ambiente in questo modo. Invece, devi chiedere al tuo amministratore di cambiare il nome o di condividere il collegamento di un altro ambiente.

L'amministratore gestisce gli ambienti sandbox nell'[interfaccia di amministrazione](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Ad esempio, se si desidera creare un sandbox per il benchmarking, l'amministratore può creare un ambiente dedicato nell'interfaccia di amministrazione. Per ulteriori informazioni, vedere [Ambienti di produzione e sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types) nel contenuto per sviluppatori e amministratori.  

Puoi anche utilizzare in sicurezza le sandbox per la formazione, ad esempio per seguire un percorso di apprendimento da [training Microsoft](/training/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), perché è un ambiente sicuro con cui sperimentare. Se qualcosa va storto, basta eliminare la sandbox e ricominciare da capo.  

Una volta terminato, puoi rimuovere la sandbox, utilizzando il centro di amministrazione.  

> [!NOTE]
> Tecnicamente, gli ambienti sandbox sono molto diversi dagli ambienti di produzione. L'amministratore può creare una sandbox che include i dati di produzione, ma è sempre una sandbox e non è possibile richiedere l'esportazione del database, ad esempio. Per ulteriori informazioni, vedere [Ambienti sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) nel contenuto per sviluppatori e amministratori.

L'ambiente sandbox non è meno utile perché include un paio di funzioni utili:

* [Esperienza utente avanzata](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Designer](#designer)  

## <a name="advanced-user-experience"></a>Esperienza utente avanzata

È possibile abilitare e provare la funzionalità completa della versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] in un tenant sandbox impostando il campo **Esperienza** nella pagina **Informazioni società** su *Premium*. Trova la pagina **Informazioni società** nel menu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Icona impostazioni."::: .  

Dopo aver abilitato l'esperienza utente *Premium*, si ottiene l'accesso a tutti i profili standard (ruoli) e alla Gestione ruolo utente nella versione standard. In alternativa, contattare un partner di rivendita per una dimostrazione delle funzionalità. Per ulteriori informazioni, vedi [Come trovo un partner di rivendita?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Dati di esempio completi

Per situazioni in cui hai bisogno di dati di esempio aggiuntivi, parla con il tuo partner di rivendita.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Designer

In un ambiente sandbox, la **funzionalità di progettazione** è abilitata. Puoi attivare la funzionalità di progettazione selezionando l'icona di progettazione ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) su una pagina, o scegliendo la voce di menu **Progettazione** nel menu Impostazioni ![Impostazioni](media/ui-experience/settings_icon_small.png).  

Per ulteriori informazioni, vedi [Utilizzare la finestra di progettazione](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) nel contenuto per sviluppatori e amministratori (solo in inglese).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Vedere anche

[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
Versioni di valutazione e sottoscrizioni di [[!INCLUDE[prod_long](includes/prod_long.md)]](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions)  
[Gestione di ambienti nell'interfaccia di amministrazione di Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Ambienti di produzione e sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

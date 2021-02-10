---
title: Creare un ambiente sandbox | Microsoft Docs
description: Creare un ambiente per l'esplorazione, l'apprendimento, le dimostrazioni, lo sviluppo e i test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 43442680578eca60fabdc620e1f8bd04036d214c
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024439"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Creazione di un ambiente sandbox in [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)], è possibile creare facilmente un ambiente sicuro in cui testare, istruire o risolvere i problemi senza disturbare i processi di lavoro o i dati aziendali della società. Tale ambiente non di produzione è denominato *sandbox*. Isolato dalla produzione, un ambiente sandbox consente di esplorare, apprendere, dimostrare, sviluppare e testare in sicurezza il servizio senza il rischio di compromettere i dati e le impostazioni dell'ambiente di produzione.  

L'amministratore può creare ambienti sandbox nell'[interfaccia di amministrazione](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), ma se si desidera testare rapidamente qualcosa, è possibile creare un ambiente sandbox da [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> Tecnicamente, gli ambienti sandbox sono molto diversi dagli ambienti di produzione, anche se l'amministratore crea un sandbox che include dati di produzione. Non è possibile utilizzare un sandbox per il benchmarking e, ad esempio, non è possibile richiedere un'esportazione del database. Se si desidera creare un sandbox per il benchmarking, l'amministratore può creare un ambiente di produzione dedicato nell'interfaccia di amministrazione. Per ulteriori informazioni, vedere [Tipi di ambienti](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Per creare un ambiente sandbox in [!INCLUDE[prod_short](includes/prod_short.md)]

1. Accedere all'istanza di produzione di [!INCLUDE[prod_short](includes/prod_short.md)].

2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ambiente sandbox** e quindi scegliere il collegamento correlato.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Fare clic sul pulsante **Crea**.  

    Viene visualizzata un'altra scheda con [!INCLUDE[prod_short](includes/prod_short.md)] dove è possibile completare la configurazione del proprio ambiente sandbox.

    > [!NOTE]  
    >  Se la funzione Blocco popup del browser è abilitata, modificarne l'impostazione per consentire la visualizzazione degli URL dall'indirizzo *.businesscentral.dynamics.com.

Quando l'ambiente sandbox è pronto, si verrà reindirizzati all'introduzione guidata dell'ambiente sandbox.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

È possibile scegliere il pulsante **Ulteriori informazioni** per informazioni sugli scenari per sviluppatori che è possibile provare in un ambiente sandbox o scegliere il pulsante **Chiudi** per passare a Gestione ruolo utente dell'istanza sandbox di [!INCLUDE[prod_short](includes/prod_short.md)].

Nella parte superiore di Gestione ruolo utente viene visualizzato un avviso che informa che ci si trova in un ambiente sandbox. È possibile vedere il tipo di ambiente anche nella barra del titolo del client.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Un ambiente sandbox creato in questo modo contiene solo i dati di dimostrazione predefiniti per l'azienda CRONUS. Nessun dato viene copiato o altrimenti trasferito dall'ambiente di produzione.<br /><br />
> È inoltre possibile creare un ambiente sandbox contenente i dati di produzione. Questa operazione deve essere eseguita mediante l'Interfaccia di amministrazione. Per ulteriori informazioni, vedere [Gestione di ambienti](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in Guida per sviluppatori e professionisti IT.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Un amministratore può limitare o persino bloccare l'accesso di alcuni utenti all'ambiente sandbox. Questa operazione può essere effettuata utilizzando le funzionalità di sicurezza standard del prodotto, ad esempio la scheda Utente, gruppi di utenti e set di autorizzazioni. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Funzionalità avanzata nell'ambiente sandbox

L'ambiente sandbox non è meno utile perché include un paio di funzioni utili.

### <a name="to-enable-the-advanced-user-experience"></a>Per abilitare l'esperienza utente avanzata

È possibile abilitare e provare la funzionalità completa della versione standard di [!INCLUDE[prod_short](includes/prod_short.md)] in un tenant sandbox impostando il campo **Esperienza** nella pagina **Informazioni società** su *Premium*. Trovare la pagina **Informazioni società** nel menu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Icona impostazioni":::.  

Dopo aver abilitato l'esperienza utente *Premium*, si ottiene l'accesso a tutti i profili standard (ruoli) e alla Gestione ruolo utente nella versione standard. È inoltre possibile creare una società di valutazione completamente configurata, inclusiva dei dati di esempio e dell'accesso alle aree avanzate del prodotto. In alternativa, contattare un partner di rivendita per una dimostrazione delle funzionalità. Per ulteriori informazioni, vedere [Come trovare un partner di rivendita?](across-faq.md#findpartner)  

### <a name="to-enable-complete-sample-data"></a>Per abilitare i dati di esempio completi

Nell'ambiente sandbox, è anche possibile creare una nuova società con l'opzione **Valutazione avanzata: dati di esempio completi** in modo da poter seguire la formazione o usare le procedure dettagliate che richiedono dati di esempio aggiuntivi, ad esempio [Procedura dettagliata: ricezione e stoccaggio nelle configurazioni di warehouse di base](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).  

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Per creare una società con dati di esempio completi in una sandbox

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Società** e quindi scegliere il collegamento correlato.  
2. Selezionare l'azione **Nuovo** quindi selezionare **Crea nuova società**.  
3. Nella pagina **Setup assistito per la creazione di una società** scegliere **Avanti**.  
4. Specificare un nome per la nuova società, quindi nel campo **Selezionare la data e il setup per iniziare** scegliere **Valutazione avanzata - Dati di esempio completi**.  
5. Completare il resto della guida di setup assistito.  

Al termine della guida di setup assistita, è possibile iniziare a esplorare la nuova società con i dati di esempio completi. Per ulteriori informazioni, vedere [Creazione di nuove società in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Designer

In un ambiente sandbox, la **funzionalità di progettazione** è abilitata. È possibile attivare la funzionalità di progettazione selezionando l'icona ![progettazione](./media/across-sandbox/sandbox-inclient-design-icon.png) in una pagina o selezionando **Design** nel menu ![Impostazioni](media/ui-experience/settings_icon_small.png) Impostazioni.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Vedere anche

[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
Versioni di valutazione e sottoscrizioni di [[!INCLUDE[prod_long](includes/prod_long.md)]](across-preview.md)  
[Gestione di ambienti nell'interfaccia di amministrazione di Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  

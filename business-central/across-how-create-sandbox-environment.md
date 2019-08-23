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
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 10ccbc7546aa5d03c3837997a721c63c3ce465da
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796667"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Creazione di un ambiente sandbox
Un ambiente sandbox (anteprima) è un'istanza di non produzione di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isolato dalla produzione, un ambiente sandbox consente di esplorare, apprendere, dimostrare, sviluppare e testare in sicurezza il servizio senza il rischio di compromettere i dati e le impostazioni dell'ambiente di produzione.

## <a name="to-create-a-sandbox-environment"></a>Per creare un ambiente sandbox
Per poter creare un ambiente sandbox, è necessario possedere una sottoscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Può esistere un solo ambiente sandbox per sottoscrizione.

1. Accedere all'istanza di produzione del servizio [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ambiente sandbox** e quindi scegliere il collegamento correlato.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Fare clic sul pulsante **Crea**.  

    Viene visualizzata un'altra scheda con [!INCLUDE[d365fin](includes/d365fin_md.md)] dove è possibile completare la configurazione del proprio ambiente sandbox.

    > [!NOTE]  
    >  Se la funzione Blocco popup del browser è abilitata, modificarne l'impostazione per consentire la visualizzazione degli URL dall'indirizzo *.businesscentral.dynamics.com.

4. Quando l'ambiente sandbox è pronto, si verrà reindirizzati all'introduzione guidata dell'ambiente sandbox.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Scegliere il pulsante **Ulteriori informazioni**per informazioni sugli scenari che è possibile provare in un ambiente sandbox o scegliere il pulsante **Chiudi** per passare a Gestione ruolo utente dell'istanza sandbox di [!INCLUDE[d365fin](includes/d365fin_md.md)].

    Nella parte superiore di Gestione ruolo utente viene visualizzato un avviso che informa che ci si trova in un ambiente sandbox. È possibile vedere il tipo di ambiente anche nella barra del titolo del client.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > Un ambiente sandbox creato in questo modo contiene solo i dati di dimostrazione predefiniti per l'azienda CRONUS. Nessun dato viene copiato o altrimenti trasferito dall'ambiente di produzione.<br /><br />
    > È inoltre possibile creare un ambiente sandbox contenente i dati di produzione. Questa operazione deve essere eseguita mediante l'Interfaccia di amministrazione. Per ulteriori informazioni, vedere [Gestione di ambienti](/business-central/dev-itpro/administration/tenant-admin-center-environments) in Guida per sviluppatori e professionisti IT.

6. È possibile tornare in qualsiasi momento nella pagina **Ambiente sandbox** e reimpostare l'ambiente sandbox.
    > [!NOTE]  
    >  La reimpostazione dell'ambiente sandbox ne determinerà la rimozione completa e la successiva creazione di un nuovo ambiente sandbox con i dati dimostrativi di default.  

7. Per passare tra gli ambienti di produzione e sandbox, è possibile utilizzare l'utilità di avvio dell'app Business Central.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. È possibile per un amministratore o un altro utente limitare o persino bloccare l'accesso da parte di alcuni utenti all'ambiente sandbox. Questa operazione può essere effettuata utilizzando le funzionalità di sicurezza standard del prodotto, ad esempio la scheda Utente, gruppi di utenti e set di autorizzazioni.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Funzionalità avanzata nell'ambiente sandbox
### <a name="designer"></a>Designer
In un ambiente sandbox la funzionalità di **progettazione** è abilitata. È possibile attivarla selezionando l'icona di progettazione ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) in una pagina.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Per abilitare l'esperienza utente avanzata
È possibile abilitare e provare la funzionalità completa avanzata di [!INCLUDE[d365fin](includes/d365fin_md.md)] in un tenant sandbox impostando il campo **Esperienza** nella pagina **Informazioni società**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Dopo avere abilitato la funzionalità avanzata in un tenant sandbox, si ottiene l'accesso a tutti i profili (ruoli) e i servizi Gestione ruolo utente standard. È inoltre possibile creare una società di valutazione completamente configurata, inclusiva dei dati di esempio e dell'accesso alle aree avanzate del prodotto.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

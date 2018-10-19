---
title: Ottenere un'anteprima dei nuovi mercati
description: Informazioni su come accedere alle anteprime di Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 50d1429a58b878766c76ed97f65936db78191ee0
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>Accedere all'anteprima di [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
A partire dalla primavera 2018, [!INCLUDE[d365fin](includes/d365fin_md.md)] diventerà disponibile in nuovi paesi. Per essere certi che [!INCLUDE[d365fin](includes/d365fin_md.md)] è la soluzione adeguata per quei clienti, stiamo offrendo una versione di anteprima del servizio prima del lancio a primavera. L'anteprima per la Danimarca è diventata disponibile nel gennaio 2018 e altri mercati seguiranno.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Introduzione a anteprime e sandbox
Anteprime e sandbox sono un'ottima soluzione per iniziare a utilizzare [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un istanza di anteprima contiene funzionalità non disponibili nella versione corrente. Le anteprime forniscono a partner e clienti l'opportunità di provare le funzionalità che intendiamo rilasciare e di fornire feedback sulle stesse. Sebbene le anteprime siano soprattutto destinate ai partner, anche i clienti sono invitati a utilizzarle per un tempo limitato. L'anteprima corrente di [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene la maggior parte delle funzionalità disponibili in Dynamics NAV 2018, la cui configurazione in genere richiede l'assistenza di un partner.

Per iniziare con un anteprima, accedere a [questa pagina](https://go.microsoft.com/fwlink/?linkid=866045) e immettere il proprio indirizzo e-mail di lavoro. Per ulteriori informazioni su [!INCLUDE[d365fin](includes/d365fin_md.md)] e le funzionalità che offre, fare riferimento alla documentazione disponibile in questo sito.

È possibile considerare una sandbox come un ambiente non di produzione utilizzabile a monte dell'istanza di produzione o anteprima di [!INCLUDE[d365fin](includes/d365fin_md.md)]. Una sandbox consente di creare e verificare in modo sicuro le estensioni e di sviluppare nuove funzionalità per personalizzare l'assistenza senza influire sui dati e sulle impostazioni della istanze di produzione o anteprima. Attualmente, tutti i clienti con una versione di produzione o di anteprima possono utilizzare una sandbox.

Per informazioni su come iniziare a utilizzare una sandbox, vedere le istruzioni riportate di seguito.

## <a name="creating-a-sandbox-environment"></a>Creazione di un ambiente sandbox
Per poter utilizzare un ambiente sandbox, è necessario avere una sottoscrizione a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Può esistere una sola sandbox per sottoscrizione.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Funzionalità avanzate disponibili nell'ambiente sandbox
Le sandbox contengono una funzionalità di progettazione nel client che consente di pianificare pagine utilizzando un'interfaccia di trascinamento e creare estensioni nel client stesso aggiungendo e riorganizzando campi.

Per ulteriori informazioni, vedere [Utilizzo di Designer](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Per creare un ambiente sandbox
1.  Accedere all'istanza di produzione o di anteprima di [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Ambiente sandbox** e quindi scegliere il collegamento correlato.
3.  Selezionare **Crea**. Viene visualizzata una scheda in cui è possibile completare la configurazione della sandbox.

    > [!Note]
    > Se la funzione Blocco popup del browser è abilitata, modificarne l'impostazione per consentire la visualizzazione degli URL dall'indirizzo *.businesscentral.dynamics.com*.  

4.  Quando la sandbox è pronta,viene visualizzata una pagina di benvenuto.  
5.  Per leggere informazioni sugli scenari che è possibile provare in una sandbox, ad esempio come sviluppare estensioni, scegliere il collegamento **Ulteriori informazioni**. In alternativa scegliere **Chiudi** per passare al servizio Gestione ruolo utente dell'istanza sandbox di [!INCLUDE[d365fin](includes/d365fin_md.md)].  
6.  Nella parte superiore di Gestione ruolo utente viene visualizzato un avviso che informa che ci si trova in una sandbox. È possibile vedere il tipo di ambiente anche nella barra del titolo del client.

    > [!Note]
    > La sandbox contenente dati dimostrativi per la società fittizia CRONUS. Nessun dato viene copiato o altrimenti trasferito dall'ambiente di produzione.  

7.  È possibile tornare alla pagina Ambiente sandbox in qualsiasi momento e reimpostare la sandbox.

    > [!Note]
    > La reimpostazione di una sandbox ne determinerà la rimozione completa e la successiva creazione con i dati dimostrativi di default.  

8.  Per passare dall'ambiente di produzione alla sandbox e viceversa, utilizzare il menu di Dynamics 365 o la home page di Dynamics.

    > [!Note]
    > Un amministratore o un altro utente può limitare o persino bloccare l'accesso degli utenti alla sandbox utilizzando le funzioni di sicurezza standard di [!INCLUDE[d365fin](includes/d365fin_md.md)], quali la scheda Utente, i gruppi utente e i set di autorizzazioni.  

### <a name="building-new-solutions-and-intellectual-property"></a>Creazione di nuove soluzioni e proprietà intellettuale
[!INCLUDE[d365fin](includes/d365fin_md.md)] offre una serie di strumenti di sviluppo e una piattaforma moderna per la creazione di app add-on e l'integrazione di soluzioni per la connessione o l'estensione di [!INCLUDE[d365fin](includes/d365fin_md.md)].

[!INCLUDE[d365fin](includes/d365fin_md.md)] fornisce strumenti utilizzabili per implementare componenti aggiuntivi e integrare funzionalità allo scopo di aggiungere nuove esperienze end-to-end specifiche del settore o di integrare soluzioni di terze parti. Ad esempio, è possibile utilizzare un'API per creare un app allo scopo di scambiare dati tra [!INCLUDE[d365fin](includes/d365fin_md.md)] l'app per le retribuzioni. Le app di connessione*** possono inoltre utilizzare estensioni per creare pagine da utilizzare per setup, configurazione o per supportare le funzionalità specifiche delle app. Per ulteriori informazioni, vedere [Sviluppo di app per [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://aka.ms/getstartedwithapps).

## <a name="see-also"></a>Vedi anche
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


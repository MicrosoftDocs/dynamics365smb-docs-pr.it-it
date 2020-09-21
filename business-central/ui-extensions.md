---
title: Installare le estensioni per personalizzare Business Central | Documenti Microsoft
description: Informazioni sull'aggiunta di funzionalità e la personalizzazione di Business Central tramite l'installazione delle estensioni.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765923"
---
# <a name="customizing-business-central-using-extensions"></a>Personalizzazione di Business Central con le estensioni

È possibile modificare [!INCLUDE[d365fin](includes/d365fin_md.md)] installando estensioni che, ad esempio, aggiungano funzionalità, modifichino il comportamento o permettano di accedere a nuovi servizi online.

> [!NOTE]
> Per installare le estensioni da AppSource o aggiungere estensioni per tenant, è necessario avere le autorizzazioni giuste. È necessario essere membri del gruppo utenti D365 EXTENSION MGMT oppure disporre dell'autorizzazione D365 EXTENSION MGMT impostata. Se si è un amministratore, è possibile assegnare gruppi di utenti e autorizzazioni ad altri utenti della tua azienda.<br /><br />
Per utilizzare la funzionalità fornita da un'estensione, come l'apertura di pagine, l'esecuzione di report, la selezione di azioni e così via, è necessario assegnare i set di autorizzazioni installati come parte dell'estensione.

> [!IMPORTANT]  
> Il caricamento di estensioni per tenant e l'installazione di estensioni AppSource non sono supportati tramite la pagina **Gestione delle estensioni** per installazioni locali.

La prima volta che si avvia [!INCLUDE[d365fin](includes/d365fin_md.md)], alcune estensioni risultano già installate. Con il tempo verranno rese disponibili altre estensioni e sarà possibile scegliere se installarle o meno.

Ad esempio, Microsoft fornisce un'estensione che consente l'integrazione con PayPal Payments Standard. Questa estensione è installata per impostazione di default.
Se tuttavia diventa disponibile un'altra estensione che offre l'integrazione con un altro servizio di pagamento, è possibile installare la nuova estensione e scegliere quale dei due servizi utilizzare.  

Le estensioni vengono gestite nella pagina **Gestione estensioni**. È possibile accedere a questa pagina dalla home page. In alternativa, scegliere l'icona **Cerca pagina o report** ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") nell'angolo superiore destro, immettere **Estensione**, quindi scegliere il collegamento correlato. Per ulteriori informazioni, vedere [Installazione e disinstallazione delle estensioni](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Se si prevede di dover accedere a un'estensione, ma non è possibile individuare la relativa funzionalità, controllare la pagina **Gestione estensioni**, se l'estensione non è elencata, è possibile installarla come descritto nella sezione seguente.  

> [!NOTE]  
> Le nuove estensioni non saranno subito disponibili in AppSource dopo l'annuncio di un aggiornamento. Seguire gli aggiornamenti sulla disponibilità delle estensioni tramite il sito Web [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="see-also"></a>Vedi anche

[Estensione di Dynamics 365 Business Central](about-develop-extensions.md)  
[Estensioni per Business Central fornite da altri provider](ui-extensions-other.md)  
[Impostare il servizio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Abilitare i pagamenti clienti attraverso PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Impostazione dell'estensione dei codici postali GetAddress.io per il Regno Unito](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Estensioni per [!INCLUDE[d365fin](includes/d365fin_md.md)] fornite da altri provider](ui-extensions-other.md)  
[Introduzione](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

---
title: Funzionalità multilingue e localizzazione
description: Informazioni su come lingua e area geografica influenzano l'esperienza utente in Business Central. Modifica la lingua dell'interfaccia utente in Impostazioni personali.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture, region, regional settings
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5187d4f98360d7cf43300f86eda9e99dcbda4063
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323138"
---
# <a name="changing-language-and-region"></a>Modifica di lingua e area geografica

[!INCLUDE[prod_short](includes/prod_short.md)] è disponibile in numerosi mercati e lingue in tutto il mondo. Nei mercati dove [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile, è offerta una serie di funzioni normative per assistere le aziende con gli oneri normativi. [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile in diverse lingue ed è possibile modificare la lingua utilizzata per visualizzare testi e la modifica viene applicata dopo la procedura di disconnessione e connessione automatica. L'impostazione è valida solo per l'utente corrente e non per gli altri utenti nella società.  

Ad esempio, se si utilizza la versione canadese di [!INCLUDE[prod_short](includes/prod_short.md)], è possibile visualizzare l'interfaccia utente in inglese, tedesco, francese e un'altra lingua ma rimane una versione canadese di [!INCLUDE[prod_short](includes/prod_short.md)] in tutti gli altri aspetti. È quindi diversa, ad esempio, dalla versione di [!INCLUDE[prod_short](includes/prod_short.md)] per il Regno Unito, dove la funzionalità è stata adattata alle esigenze del mercato.  

Per modificare la lingua dell'interfaccia utente, accedere alla pagina **Impostazioni personali**. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md#language). 

> [!NOTE]  
> La scelta delle lingue verrà ripristinata sulle impostazioni del profilo di Microsoft 365 se l'amministratore sincronizza gli utenti da Microsoft 365 a [!INCLUDE[prod_short](includes/prod_short.md)].

La modifica dei testi memorizzati come dati dell'applicazione non è invece supportata dalla funzionalità multilingue. Tale modifica rientra nell'ambito della progettazione dell'applicazione. Tra gli esempi di questo tipo di testi rientrano i nomi degli articoli in magazzino o i commenti relativi a un cliente. In altre parole, questi testi non vengono tradotti.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] supporta solo un unico set di caratteri per i dati. Alcuni caratteri, pertanto, potrebbero non essere supportati nell'ambiente ed è possibile che si verifichino problemi durante il recupero di dati immessi utilizzando un set di caratteri diverso. Ad esempio, l'ambiente potrebbe supportare solo caratteri inglesi e russi e se si immettono i dati in una lingua diversa, potrebbero non essere archiviati correttamente. Per verificare di avere individuato correttamente le lingue supportate per [!INCLUDE[prod_short](includes/prod_short.md)], rivolgersi all'amministratore di sistema.  

## <a name="changing-your-region-setting"></a>Cambiare l'impostazione della regione
L'area geografica differisce dalla lingua e dai requisiti legali nei mercati locali. L'area geografica determina la visualizzazione dei dati in termini di separatore, allineamento a sinistra o a destra ed alcune altre impostazioni. L'area geografica determina anche alcuni degli elementi di sistema nel browser, ad esempio l'azione per creare un nuovo elemento in un elenco.  

È possibile modificare l'area geografica nella scheda del browser utilizzato in [!INCLUDE[prod_short](includes/prod_short.md)]. La modifica è valida solo per l'utente corrente e non per gli altri utenti nella società.  La scelta dell'area geografica verrà ripristinata sulle impostazioni del profilo di Microsoft 365 se l'amministratore sincronizza gli utenti da Microsoft 365 in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]  
> Quando si modifica l'area geografica viene visualizzato un lungo elenco di lingue e aree geografiche. Tuttavia, la lingua non è influenzata dalla scelta dell'area geografica.  

Per modificare l'area geografica accedere alla pagina **Impostazioni personali**. Per ulteriori informazioni, vedere [Modificare le impostazioni di base](ui-change-basic-settings.md).  

## <a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a>Cambiare l'impostazione della regione per clienti, contatti e fornitori
Alcune aziende usano un servizio esterno che convalida le informazioni dell'indirizzo nel loro paese o regione. Tuttavia, quando avete bisogno di aggiornare le informazioni sull'indirizzo, l'approccio strutturato che questi servizi utilizzano potrebbe non essere sempre quello giusto per alcuni scenari. Business Central offre un mezzo più flessibile per inserire i dettagli dell'indirizzo.

Nella pagina **Setup contabilità generale**, se si attiva l'opzione **Richiedi il codice paese/regione nel toggle dell'indirizzo**, le modifiche al campo **Codice paese/regione** negli indirizzi di clienti, contatti o fornitori resetteranno i valori negli altri campi indirizzo.

## <a name="application-version"></a>Versione applicazione

Nella pagina **Guida e supporto** è possibile visualizzare la versione di [!INCLUDE[prod_short](includes/prod_short.md)] su cui si basa la società. Se si desidera basare una società su una versione diversa, l'amministratore può creare un nuovo ambiente di produzione. Per ulteriori informazioni, vedere [Creare un nuovo ambiente di produzione](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) nel contenuto per sviluppatori e professionisti IT.  

## <a name="languages-of-the-prod_short-help"></a>Lingue della Guida di [!INCLUDE[prod_short](includes/prod_short.md)]

Il contenuto della Guida relativo alle funzionalità di base di [!INCLUDE[prod_short](includes/prod_short.md)] è pubblicato nel sito Microsoft Docs ed è disponibile in varie lingue. Se si accede ai documenti dall'interno di [!INCLUDE[prod_short](includes/prod_short.md)], il contenuto verrà visualizzato nella lingua in uso. Se una pagina specifica non è disponibile nella lingua in uso, verrà visualizzata in inglese.

### <a name="how-do-i-change-the-language-of-the-microsoft-docs-site"></a>Come cambio la lingua del sito di Microsoft Docs?

È semplice. Basta scorrere in fondo alla pagina del browser e scegliere il simbolo del globo nell'angolo inferiore sinistro.

> [!NOTE]  
> Verrà visualizzato un elenco delle lingue supportate dal sito Microsoft Docs. [!INCLUDE[prod_short](includes/prod_short.md)] è disponibile in un numero limitato di paesi/regioni e il contenuto della Guida di [!INCLUDE [prod_short](includes/prod_short.md)] non è disponibile in tutte le lingue supportate dal sito Microsoft Docs.

## <a name="see-also"></a>Vedere anche

[Risorse per Guida e supporto](product-help-and-support.md)  
[Modificare le impostazioni di base](ui-change-basic-settings.md)  
[Preparazione al business](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
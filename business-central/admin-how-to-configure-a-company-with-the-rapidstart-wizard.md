---
title: "Configurare una società con la procedura guidata RapidStart Services | Microsoft Docs"
description: "È possibile configurare rapidamente una nuova società creata utilizzando la procedura guidata RapidStart Services."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4dd595fabbf8e4cd2a3eef73a934922dfea92858
ms.contentlocale: it-it
ms.lasthandoff: 11/22/2018

---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Configurare una società con la procedura guidata RapidStart Services
È possibile configurare rapidamente una nuova società creata utilizzando la procedura guidata RapidStart Services.

Nella procedura riportata di seguito, al cliente è stato fornito un pacchetto di configurazione che verrà successivamente installato su un computer. Il cliente apre la nuova società, che non contiene dati relativi ai clienti. L'utente o la società del cliente esegue quindi i passaggi descritti nella procedura guidata RapidStart Services per inserire informazioni di base sulla società. La procedura guidata consente di importare il pacchetto di configurazione e di collegarlo alla società.  

## <a name="to-configure-a-new-company"></a>Per configurare una nuova società  
1. Nella Gestione ruolo utente Implementatore di RapidStart Services, scegliere l'azione **Procedura guidata RapidStart Services**.  
2. Espandere la Scheda dettaglio **Passaggio 1** che contiene informazioni generali sulla nuova società. Compilare i campi con le informazioni appropriate sulla nuova società. Soltanto il campo **Nome** è obbligatorio. I campi restanti sono facoltativi.  
3. Espandere la Scheda dettaglio **Passaggio 2** che contiene le informazioni di contatto e sulla comunicazione relative alla nuova società. Compilare i campi con le informazioni appropriate sulla nuova società.
4. Espandere la Scheda dettaglio **Passaggio 3** che contiene il conto corrente bancario e informazioni di pagamento relative alla nuova società. Compilare i campi con le informazioni appropriate sulla nuova società.  
5. Espandere la Scheda dettaglio **Passaggio 4**. Selezionare il pulsante **AssistEdit** per selezionare il pacchetto di configurazione che si desidera collegare. Viene visualizzato il nome del pacchetto di configurazione. È possibile eseguire le seguenti azioni, nell'ordine elencato:  

    1. Collegare la configurazione scegliendo l'azione **Collega pacchetto**. Questa operazione consente di importare il pacchetto di configurazione e di collegare tutti i dati del database del pacchetto contemporaneamente.  

    2. Esaminare la configurazione dopo che è stata collegata. Questa opzione consente di esaminare i dettagli e i questionari relativi alla configurazione forniti dai partner, nonché di importare alcuni dati master necessari per la società. Scegliere l'azione **Foglio di lavoro configurazione**. Per ulteriori informazioni, vedere la sezione “Completare il questionario di configurazione" in [Raggruppare i valori di setup del cliente](admin-gather-customer-setup-values.md).  

6. Espandere la Scheda dettaglio **Passaggio 5**. Specificare la Gestione ruolo utente predefinita per la nuova società.  

    > [!IMPORTANT]  
    >  Modificare la Gestione ruolo utente solo dopo avere completato la configurazione della società. Se sono presenti più dettagli di setup da analizzare e modificare, utilizzare innanzitutto il foglio di lavoro configurazione per continuare il proprio lavoro. Quindi, tornare alla procedura guidata per aggiornare il proprio profilo di Gestione ruolo utente, oppure scegliere l'azione **Completa setup**.

7. Scegliere il pulsante **OK**.  
8. Per verificare che le informazioni sulla configurazione siano state collegate alla nuova società, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere le **informazioni sulla società**, quindi scegliere il collegamento correlato.

La pagina **Informazioni società** contiene le informazioni precedentemente specificate.   

La società risulta ora configurata e collegata ai dati.  

## <a name="see-also"></a>Vedi anche  
[Applicazione della configurazione a nuove società](admin-apply-configuration-to-new-companies.md)  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)


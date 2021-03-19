---
title: Condividere contatti tra Business Central e Outlook| Microsoft Docs
description: Questo servizio è completamente integrato con Microsoft 365 pertanto è possibile condividere i contatti tra Outlook e Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7c9d267df2fb58da3b4a7aa1505030c9510bdf4f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386101"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Sincronizzare i contatti di Business Central con i contatti di Microsoft Outlook
È possibile visualizzare gli stessi contatti in [!INCLUDE[prod_short](includes/prod_short.md)] come visualizzati in Outlook se si imposta la sincronizzazione dei contatti. Ad esempio, un addetto alle vendite potrebbe svolgere parte del lavoro in Outlook e parte del tuo lavoro in [!INCLUDE[prod_short](includes/prod_short.md)]. Se i contatti sono uguali in entrambi i programmi, il lavoro è più semplice.  

Una cartella dedicata in Outlook rende i contatti facili da trovare ed è possibile impostare un filtro per sincronizzare solo i contatti di [!INCLUDE[prod_short](includes/prod_short.md)] che si desidera visualizzare in Outlook. Una volta impostata la sincronizzazione dei contatti, è possibile avviare la sincronizzazione manualmente o impostare una sincronizzazione automatica che manterrà i contatti sincronizzati su base pianificata.  

## <a name="set-up-synchronization"></a>Impostare la sincronizzazione
È possibile definire come sincronizzare i contatti con Outlook nella pagina **Setup sincronizzazione con Exchange** in [!INCLUDE[prod_short](includes/prod_short.md)]. Come prerequisito, il profilo utente in [!INCLUDE[prod_short](includes/prod_short.md)] deve specificare l'account e-mail di Microsoft 365. È possibile controllare questo valore nella sezione di **autenticazione Microsoft 365** del profilo utente nell'elenco **Utenti**.  

Quindi, nella pagina **Setup sincronizzazione con Exchange** è possibile verificare che la connessione a Exchange funzioni e quindi configurare la sincronizzazione dei contatti. Aprire la pagina **Setup sincronizzazione contatti** e avviare la sincronizzazione. Facoltativamente, impostare un filtro per i contatti da sincronizzare tra [!INCLUDE[prod_short](includes/prod_short.md)] e Outlook. Ad esempio, è possibile impostare un filtro in base a nome, tipo, azienda o simile. È inoltre possibile modificare il nome predefinito della cartella in cui verranno sincronizzati i contatti in Outlook. Il nome predefinito è *Business Central*.  

Una volta impostata la sincronizzazione, qualsiasi modifica apportata al contatto in Outlook o in [!INCLUDE[prod_short](includes/prod_short.md)] viene sincronizzata tra i programmi.  

Ogni collega può anche configurare la propria sincronizzazione di Exchange e impostare il proprio filtro sui contatti da sincronizzare.  

## <a name="synchronize-contacts"></a>Sincronizzare i contatti
Se si è abituati a utilizzare i contatti in [!INCLUDE[prod_short](includes/prod_short.md)], sarà semplice avviare la sincronizzazione manualmente ogni volta che si desidera dall'elenco **Contatti**. È sufficiente scegliere l'azione **Sincronizza con Office 365** e quindi decidere se si desidera modificare il filtro che si è impostato. Scegliendo il pulsante OK, la sincronizzazione viene avviata immediatamente e le modifiche più recenti vengono applicate ai contatti in Outlook.  

Nell'elenco **Contatti** è possibile sincronizzare i contatti in due modi:

* **Sincronizza con Office 365**

  Questa azione sincronizza tutte le modifiche di [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft 365 a partire dalla sincronizzazione precedente, in base all'ultima data di modifica. Tutti i nuovi contatti di Microsoft 365 verranno sincronizzati di nuovo anche in [!INCLUDE[prod_short](includes/prod_short.md)]. Questo è in genere più veloce di una sincronizzazione completa.  

* **Sincronizzazione completa con Office 365**

  Questa azione sincronizza tutti i contatti in entrambe le direzioni indipendentemente dall'ultima data di sincronizzazione e dall'ultima data di modifica.  

In entrambi i casi, i contatti vengono sincronizzati solo da Outlook se i campi richiesti sono compilati. I campi obbligatori per la sincronizzazione con Microsoft 365 sono **Nome**, **Indirizzo e-mail** e devono essere di tipo Persona. [!INCLUDE[prod_short](includes/prod_short.md)] è il master delle informazioni di contatto, quindi in caso di duplicati verranno salvate le informazioni di contatto di [!INCLUDE[prod_short](includes/prod_short.md)].  

In Outlook, i contatti di [!INCLUDE[prod_short](includes/prod_short.md)] vengono visualizzati in una cartella in **Altri contatti** nella visualizzazione **Persone**. Se non si ha familiarità con la vista Persone in Outlook, è possibile accedervi dalle opzioni di spostamento nell'angolo in basso a sinistra di Outlook.  

## <a name="see-also"></a>Vedi anche
[Introduzione](product-get-started.md)  
[Finanze](finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzo dei contatti (Persone) in Outlook sul Web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
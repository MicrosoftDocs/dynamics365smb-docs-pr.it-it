---
title: Visualizzazione e modifica delle impostazioni di base in Financials | Documenti Microsoft
description: "Informazioni su come modificare alcune impostazioni di base in Financials, ad esempio, la Gestione ruolo utente, la società o la data di lavoro."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: c7f07bd3cee8d52cccf171dfd229265d65e99cba
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="changing-basic-settings"></a>Modifica delle impostazioni di base
Nella finestra **Impostazioni personali** è possibile vedere e modificare le impostazioni di base per [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Gestione ruolo utente
Gestione ruolo utente rappresenta la pagina iniziale ed è progettata per le esigenze del ruolo. La Gestione ruolo utente fornisce una panoramica dell'azienda e riflette informazioni, task e priorità del ruolo.

Nella parte superiore della Gestione ruolo utente, è visualizzata una barra di spostamento che consente di accedere facilmente alle entità tipiche per il ruolo, ad esempio clienti, fornitori, articoli e così via.

Il contenuto visualizzato nell'area di contenuto principale dipenderà dalla Gestione ruolo utente specifica. Ad esempio, nella maggior parte delle Gestioni ruolo utente, vi sono dei riquadri Attività che mostrano i dati correnti. È possibile fare clic su di essi o toccarli per accedere facilmente al documento selezionato. È possibile impostare degli indicatori delle prestazioni chiave (KPI) per visualizzare un determinato grafico per rappresentare visivamente i flussi di cassa o le spese e i ricavi. Alcune Gestioni ruolo utente consentono di creare un elenco di entità preferite, come clienti e fornitori, o mostrano Report elaborati.

### <a name="to-change-role-center"></a>Per modificare una Gestione ruolo utente
La Gestione ruolo utente di default è **Manager aziendale**, ma è possibile selezionare un altro Centro ruolo utente più adatto alle proprie esigenze.
1. Nell'angolo superiore destro scegliere l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente"), quindi scegliere **Impostazioni personali**.
2. Nella fienstra **Impostazioni personali** nel campo **Gestione ruolo utenter** selezionare la Gestione ruolo utente che si desidera impostare come standard. Ad esempio, selezionare **Contabile**.
3. Scegliere il pulsante **OK**.

## <a name="company"></a>Società
Una società funziona da contenitore dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Possono essere presenti più società in un database, ma è possibile selezionarne solo una alla volta.

La società di default è detta CRONUS e contiene solo i dati di esempio.

> [!TIP]  
>   Se si desidera visualizzare un nome diverso per la società nell'applicazione (ad esempio in Gestione ruolo utente), impostare il campo **Nome** nella pagina **Informazioni società** o **Nome visualizzato** nella pagina **Società**.  

## <a name="work-date"></a>Work Date
La data di lavoro di default in genere è la data odierna. Per poter eseguire task quali il completamento delle transazioni per una data che non corrisponde alla data corrente, può essere necessario modificare temporaneamente la data di lavoro.

> [!TIP]  
>   Digitare **w** per immettere rapidamente la data di lavoro in un campo di data. Scrivere **t** per immettere rapidamente la data corrente nel campo della data.

> [!IMPORTANT]  
>   La data di lavoro verrà modificata solo finché non si chiude la società o finché non vengono modificate le date. Se viene aperta una società differente oppure quando viene aperta la stessa società il giorno successivo ed è ancora necessario utilizzare una data di lavoro diversa, occorre reimpostare la data di lavoro.

## <a name="region"></a>Area geografica
L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.   

## <a name="changing-when-i-receive-notifications"></a>Modifica del momento in cui ricevere le notifiche
Scegliere questo collegamento per visualizzare o modificare le notifiche ricevute in merito a determinati eventi o modifiche dello stato, come, ad esempio, quando si sta per fatturare a un cliente che ha un saldo scaduto o la giacenza disponibile è inferiore alla quantità che si intende vendere. Per ulteriori informazioni, vedere [Notifiche smart](ui-smart-notifications.md).

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizzazione dell'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  


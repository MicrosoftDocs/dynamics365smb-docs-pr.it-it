---
title: Visualizzazione e modifica delle impostazioni di base in Financials | Documenti Microsoft
description: "Informazioni su come modificare alcune impostazioni di base in Financials, ad esempio, la Gestione ruolo utente, la società o la data di lavoro."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7c9dec3bcb000be958acec3f0d88abbab9946bf8
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="changing-basic-settings"></a>Modifica delle impostazioni di base
Nella finestra **Impostazioni personali** è possibile vedere e modificare le impostazioni di base per [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Gestione ruolo utente
Gestione ruolo utente rappresenta la home page, una pagina iniziale che è progettata per le esigenze del ruolo. Nella home page è disponibile una panoramica dell'azienda. A sinistra è presente una barra di spostamento che consente di accedere rapidamente a clienti, fornitori, articoli e così via.

Al centro si trovano i riquadri Attività. I riquadri Attività mostrano i dati correnti ed è possibile fare clic su di essi o toccarli per accedere al documento selezionato. È possibile impostare degli indicatori delle prestazioni chiave (KPI) per visualizzare un determinato grafico per rappresentare visivamente i flussi di cassa o le spese e i ricavi.

È inoltre possibile creare una lista di Clienti preferiti nella home page per gli account con cui si intrattengono affari spesso o a cui è importante prestare un'attenzione speciale. Utilizzare le frecce per comprimere parte della pagina e per creare più spazio dove visualizzare i dati specifici. Nella parte superiore della home page si trovano tutte le azioni applicabili al contenuto corrente. Anche questa parte può essere compressa. È sufficiente scegliere l'area compressa per visualizzarla di nuovo.

### <a name="to-change-role-center"></a>Per modificare una Gestione ruolo utente
La Gestione ruolo utente di default è **Manager aziendale**, ma è possibile selezionare un altro Centro ruolo utente più adatto alle proprie esigenze.
1. Nell'angolo superiore destro scegliere l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente"), quindi scegliere **Impostazioni personali**.
2. Nella fienstra **Impostazioni personali** nel campo **Gestione ruolo utenter** selezionare la Gestione ruolo utente che si desidera impostare come standard. Ad esempio, selezionare **Contabile**.
3. Scegliere il pulsante **OK**.

## <a name="company"></a>Società
Una società funziona da contenitore dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Possono essere presenti più società in un database, ma è possibile selezionarne solo una alla volta.

La società di default è detta CRONUS e contiene solo i dati di esempio.

> [!TIP]  
>   Se si desidera visualizzare un nome diverso per la società nell'applicazione (ad esempio nella home page), impostare il campo **Nome** nella pagina **Informazioni società** o **Nome visualizzato** nella pagina **Società**.  

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


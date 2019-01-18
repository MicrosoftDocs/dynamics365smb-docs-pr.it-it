---
title: Visualizzazione e modifica delle impostazioni di base | Microsoft Docs
description: "Informazioni su come modificare alcune impostazioni di base, ad esempio, la Gestione ruolo utente, la società o la data di lavoro."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 11/19/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 353662322e36a564f30bc911f056817cafa7440c
ms.contentlocale: it-it
ms.lasthandoff: 11/26/2018

---
# <a name="changing-basic-settings"></a>Modifica delle impostazioni di base
Nella pagina [**Impostazioni personali**](https://businesscentral.dynamics.com?page=9176 "Passare direttamente alla pagina impostazioni utente in Business Central"), è possibile visualizzare e modificare le impostazioni di base per [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le modifiche apportate interesseranno solo l'area di lavoro dell'utente, non quello di altri utenti.  

## <a name="role-center"></a> Gestione ruolo utente
Gestione ruolo utente rappresenta la home page, una schermata iniziale che è progettata per le esigenze di un ruolo specifico dell'organizzazione. A seconda del ruolo, Gestione ruolo utente offre una panoramica del business, del reparto o dei task personali. Agevola anche l'esplorazione dei task quotidiane e la ricerca del lavoro assegnato.

-   Nella parte superiore, lo spostamento consente di esplorare clienti, fornitori, articoli e altri importanti elenchi di informazioni. In modo simile, le azioni consentono di avviare task, come creare una nuova fattura di vendita, direttamente da Gestione ruolo utente.

-   Al centro si trova **Attività**. Le attività mostrano i dati correnti e possono essere selezionate o toccate per visualizzare informazioni più dettagliate. È possibile impostare degli indicatori delle prestazioni chiave (KPI) per visualizzare un determinato grafico per rappresentare visivamente i flussi di cassa o le spese e i ricavi. È inoltre possibile creare una lista di Clienti preferiti nella home page per gli account con cui si intrattengono affari spesso o a cui è importante prestare un'attenzione speciale.

### <a name="to-change-role-center"></a>Per modificare una Gestione ruolo utente
La Gestione ruolo utente di default è **Manager aziendale**, ma è possibile selezionare un altro Centro ruolo utente più adatto alle proprie esigenze.
1. Nell'angolo superiore destro scegliere l'icona **Impostazioni** ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente"), quindi scegliere **Impostazioni personali**.
2. Nella pagina **Impostazioni personali** nel campo **Gestione ruolo utenter** selezionare la Gestione ruolo utente che si desidera impostare come standard. Ad esempio, selezionare **Contabile**.
3. Scegliere il pulsante **OK**.

## <a name="company"></a>Società
Una società funziona da contenitore dei dati in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Possono essere presenti più società in un database, ma è possibile selezionarne solo una alla volta.

La società di default è detta CRONUS e contiene solo i dati di esempio.

> [!TIP]  
>   Se si desidera visualizzare un nome diverso per la società nell'applicazione (ad esempio in Gestione ruolo utente), impostare il campo **Nome** nella pagina **Informazioni società** o **Nome visualizzato** nella pagina **Società**.  

## <a name="work-date"></a>Data lavoro
La data di lavoro di default in genere è la data odierna. Per poter eseguire task quali il completamento delle transazioni per una data che non corrisponde alla data corrente, può essere necessario modificare temporaneamente la data di lavoro.

> [!TIP]  
>   Digitare **w** per immettere rapidamente la data di lavoro in un campo di data. Scrivere **t** per immettere rapidamente la data corrente nel campo della data.

> [!IMPORTANT]  
>   La data di lavoro verrà modificata solo finché non si chiude la società o finché non vengono modificate le date. Se viene aperta una società differente oppure quando viene aperta la stessa società il giorno successivo ed è ancora necessario utilizzare una data di lavoro diversa, occorre reimpostare la data di lavoro.

## <a name="region"></a> Area geografica
L'impostazione **Area geografica** determina il modo in cui date, ore, numeri e valute vengono visualizzati o formattati.   


## <a name="language"></a> Lingua
Cambia la lingua di visualizzazione. Questo campo viene visualizzato solo quando c'è più di una lingua tra cui scegliere. 

La lingua iniziale è determinata dall'amministratore o dalle impostazioni del browser quando ci si registri per [!INCLUDE[d365fin](includes/d365fin_md.md)]. La lingua impostata verrà utilizzata su tutti i dispositivi dai quali si accede, ad esempio da telefono o tablet.

## <a name="changing-when-i-receive-notifications"></a>Modifica del momento in cui ricevere le notifiche
Scegliere questo collegamento per visualizzare o modificare le notifiche ricevute in merito a determinati eventi o modifiche dello stato, come, ad esempio, quando si sta per fatturare a un cliente che ha un saldo scaduto o la giacenza disponibile è inferiore alla quantità che si intende vendere. Per ulteriori informazioni, vedere [Notifiche smart](ui-smart-notifications.md).

## <a name="see-also"></a>Vedi anche
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  


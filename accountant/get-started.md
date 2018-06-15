---
title: "Esperienza di contabilità in Dynamics 365 | Microsoft Docs"
description: Ottenere informazioni su Accountant Hub per Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/09/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8901216a843440e922ae4df9d7508b543a6c1322
ms.contentlocale: it-it
ms.lasthandoff: 05/15/2018

---
# <a name="get-started-with-include-d365acclongincludesd365acclongmdmd"></a>Introduzione a [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Qualsiasi attività deve avere i suoi libri e firmare la contabilità. Alcuni aziende hanno un contabile esterno e altre hanno un contabile interno. Se si è un contabile con vari client, è possibile utilizzare [!INCLUDE [d365acc](includes/d365acc_md.md)] come dashboard per avere una panoramica più precisa dei client.  

È possibile accedere a [!INCLUDE [d365acc](includes/d365acc_md.md)] iscrivendosi da [Dynamics 365 - Accountant Hub su Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]
>  Quando ci si iscrive a [!INCLUDE [d365acc](includes/d365acc_md.md)], è necessario specificare l'indirizzo di posta elettronica di lavoro, ad esempio <em>me@accountant.com</em>. È consigliabile utilizzare lo stesso indirizzo di posta elettronica quando si lavora con [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] dei client in modo che sia facile passare tra i client. L'indirizzo e-mail deve essere un indirizzo di lavoro che si basa su Active Directory.

## <a name="working-with-individual-clients"></a>Utilizzo dei singoli client
Il dashboard visualizza la maggior parte delle informazioni importanti relative a ogni client.  
![Accountant Hub](./media/accountant-get-started/accountant-dashboard-tasks.png)

Nella colonna **Nome client** sono riportati i nomi dei client e nella colonna **Nome società** sono elencate tutte le società se il client ha più società in [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]. Sono inoltre disponibili campi per mostrare i task assegnati a te nella società del cliente, inclusi i task in ritardo.  

È possibile personalizzare il dashboard per indicare le informazioni sui dati che si desidera visualizzare aggiungendo o rimovendo le colonne. Ad esempio, è possibile visualizzare le imposte in scadenza, il numero di documenti di vendita aperti in ogni client o il numero delle fatture di acquisto che sono in scadenza la settimana prossima. È possibile configurare la visualizzazione in base alle proprie esigenze. Se si dispone di molti client, è possibile utilizzare i filtri per ordinare la visualizzazione.  

Accanto al nome del cliente, i tre puntini (...) indicano un menu breve:

- Aggiornare la società corrente e ottenere i dati più recenti per il client  
- Andare a [!INCLUDE [d365fin](includes/d365fin_md.md)] del client  
- Selezionare più client  

Analogamente, è possibile utilizzare il menu a discesa **Riepilogo client** per aggiornare tutte le società, ad esempio.  

> [!TIP]
>  Per accedere a [!INCLUDE [d365fin](includes/d365fin_md.md)] di un client, scegliere la voce di menu **Vai al client**, si viene connessi automaticamente.

## <a name="company-details"></a>Dettagli Società
Per visualizzare ulteriori informazioni sui dati dei clienti, scegliere il nome della società su cui si desidera ottenere ulteriori informazioni. Verrà aperto il riquadro **Dettagli Società**, nel quale sarà possibile visualizzare informazioni aggiuntive, ad esempio:  

* Saldi conto di cassa  
* Previsione flusso di cassa  
* Fatture di acquisto scadute  
* Fatture di vendita scadute  

![Dettagli della società cliente nel dashboard contabile](./media/accountant-get-started/accountant-company-details.png)

Teoricamente si è connessi a [!INCLUDE [d365fin](includes/d365fin_md.md)] del proprio client e i dati che si vedono sono di dati reali. Se si desidera analizzare i dati, ad esempio una fattura di acquisto scaduta, selezionare il collegamento. si verrà reindirizzati alla società del client.  

> [!TIP]
>  È possibile aprire cartelle di lavoro di Excel predefinite dalla scheda **Report** nella barra multifunzione. Queste cartelle di lavoro di Excel sono concepite come report e rendiconti finanziari pronti per la stampa, ma sono anche modificabili in base alle esigenze. Per ulteriori informazioni, vedi [Analisi dei rendiconti finanziari in Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) della guida per [!INCLUDE [d365fin](includes/d365fin_md.md)].  

In caso contrario, chiudere il riquadro Dettagli e passare al client successivo.  

## <a name="assigned-tasks"></a>Task assegnati
Nel [!INCLUDE [d365fin](includes/d365fin_md.md)] del cliente, è possibile assegnare task a se stessi e ad altri, altri utenti possono assegnate task a te. Il dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] offre una panoramica dei task assegnati per ogni cliente ed è inoltre possibile accedere a una lista di tutti i task assegnati scegliendo **Task personali dell'utente** nel riquadro di spostamento sinistro.  

Nella società cliente, sono inoltre presenti delle pile con i task assegnati per un cliente specifico.

![Task assegnati al contabile nella società cliente](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Task personali dell'utente
L'elenco **Task personali dell'utente** in [!INCLUDE [d365acc](includes/d365acc_md.md)] consente di assegnare la priorità al giorno mostrando ulteriori informazioni sui task assegnati per tutti i clienti.  

![Elenco dei task personali come contabile esterno](./media/accountant-get-started/accountant-tasklist.png)

È possibile ordinare per data di scadenza, ad esempio, o per qualsiasi altro tipo di dati che consente di assegnare priorità per la giornata. Per impostazione predefinita, nell'elenco sono visualizzati tutti i task allocati a te, ma puoi impostare i filtri per visualizzare solo i task prioritari, ad esempio.

Per selezionare un task, sceglierlo dall'elenco dei task in sospeso dell'utente. Nella barra multifunzione, il collegamento **Vai a elemento task** apre la finestra in cui è possibile svolgere l'attività.  

Una volta completato il task, contrassegnarlo come completato.  

## <a name="see-also"></a>Vedi anche
[Aggiungere clienti al dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
[Benvenuto in [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Analisi dei rendiconti finanziari in Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)   
[Esperienze di contabile in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365 - Accountant Hub su Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  


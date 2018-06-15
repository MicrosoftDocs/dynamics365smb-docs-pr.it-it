---
title: Rispondere a richieste relative a dati personali
description: "È necessario rispondere alle richieste di oggetti dati."
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 05/25/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: 400b4710bd4e9a26db3b392646581f5225a2d245
ms.contentlocale: it-it
ms.lasthandoff: 05/28/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Rispondere a richieste relative a dati personali  
Gli oggetti dati possono richiedere diversi tipi di azioni riguardanti i relativi dati personali. Ad esempio, ai sensi del regolamento generale sulla protezione dei dati (GDPR), i residenti dell'UE hanno il diritto di chiedere l'esportazione, la cancellazione e la modifica dei loro dati personali. Questo è noto come *richiesta dell'interessato*. Se i dati riservati sono stati classificati e si è certi della correttezza dell'operazione, un amministratore può rispondere alle richieste utilizzando le opzioni in **Privacy dati** nella Gestione ruolo utente **Amministrazione di utenti, gruppi di utenti e autorizzazioni** oppure, se si sta utilizzando il client Windows, nella Gestione ruolo utente **Manager IT**. Per ulteriori informazioni sulla classificazione dei dati e sulla classificazione di dati riservati in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], vedere [Classificazione di dati](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) e [Classificazione di dati riservati](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Tipi di richieste

Nella tabella seguente vengono forniti esempi dei tipi di richieste a cui è possibile rispondere.

> [!Note]
> Sebbene forniamo le funzionalità per rispondere a questi tipi di richieste e quindi per accedere a dati personali, è responsabilità dell'utente assicurare la corretta archiviazione e classificazione dei dati personali e riservati.

|Tipo richiesta|Descrizione e risposta suggerita|
|-----|-----|
|Richieste di trasferibilità|Un oggetto dati può eseguire una richiesta di trasferibilità dei dati, di conseguenza è necessario esportare i dati personali dell'oggetto dati dai sistemi e fornirli in un formato strutturato comune. Per rispondere a queste richieste, è possibile utilizzare **Utilità privacy dei dati** per esportare dati personali in un file di Excel o in un pacchetto di configurazione di RapidStart. Con Excel, è possibile modificare i dati personali e salvarli in un formato comune leggibile da computer, ad esempio .csv o .xml. Per i pacchetti di configurazione di RapidStart è possibile configurare le tabelle di dati master e le relative tabelle che contengono dati personali. <br><br> **Nota**: quando si esportano i dati, si specifica un livello minimo di sensibilità. L'esportazione includerà il livello minimo e tutti i livelli di sensibilità sopra di esso. Ad esempio, se si sceglie di esportare dati classificati come Personali, l'esportazione includerà anche dati classificati come Sensibili. <br><br>Quando si esportano dati relativi a una persona interessata, l'**Utilità privacy dei dati** cerca relazioni dirette tra l'interessato e i dati relativi all'interessato. Le relazioni indirette tra i dati relativi alla persona interessata e gli altri dati non vengono esportate automaticamente dall'**Utilità privacy dei dati**. Ad esempio, la tabella Contatto ha messo in correlazione diretta i dati di Risposte profilo contatto e la tabella Risposte profilo contatto è collegata a sua volta ai dati di Domande profilo. Se si desidera esportare anche Domande profilo, è necessario aggiungere questa tabella manualmente come una riga con i filtri appropriati nel pacchetto di configurazione creato dall'**Utilità privacy dei dati**.|
|Richieste di eliminazione|Un oggetto dati può richiedere di eliminare i relativi dati personali. Esistono svariati metodi per eliminare dati personali utilizzando le funzionalità di personalizzazione, ma la decisione e l'implementazione sono di responsabilità dell'utente. In alcuni casi, è possibile scegliere di modificare direttamente i dati, ad esempio eliminando un contatto e quindi eseguendo il processo batch relativo all'eliminazione di interazioni annullate per il contatto. <br><br> **Nota:** se è stata specificata una data nel campo **Consenti eliminazione documenti anteriori a** nelle pagine **Setup contabilità clienti e vendite** o **Setup contabilità fornitori e acquisti**, potrebbe essere necessario modificare la data in modo da eliminare i documenti di acquisto e vendita registrati che sono stati stampati e le cui date di registrazione sono uguali o antecedenti a quella data.|
|Richieste di correzione|Un oggetto dati può richiedere di correggere dati personali inaccurati. Questa operazione può essere effettuata in vari modi. In alcuni casi, si potrebbero esportare liste in Excel per modificare in blocco più record e quindi importare i dati aggiornati. Per ulteriori informazioni, vedere [Esportazione dei dati aziendali in Excel](about-export-data.md). È inoltre possibile modificare manualmente i campi contenenti dati personali, ad esempio modificare informazioni relative a un cliente nella scheda cliente. Tuttavia, i record delle transazioni quali movimenti contabili generali, clienti e fiscali sono essenziali per l'integrità del sistema di pianificazione delle risorse aziendali. Se si archiviano dati personali nei record delle transazioni commerciali, si deve prendere in considerazione l'utilizzo delle funzionalità di personalizzazione per modificare tali dati personali.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Limitazione dell'elaborazione dei dati per un oggetto dati
Un oggetto dati può richiedere di interrompere temporaneamente l'elaborazione dei relativi dati personali. Per soddisfare tali richieste, è possibile contrassegnare i record come bloccati a causa della privacy. Quando un record viene contrassegnato come bloccato, non è possibile creare nuove transazioni che utilizzano quel record. Ad esempio, non è possibile creare una nuova fattura per un cliente quando il cliente o il venditore è bloccato. Per contrassegnare un oggetto dati come bloccato, aprire la scheda per l'oggetto dati, ad esempio le schede cliente, fornitore o contatto, e scegliere la casella du controllo **Bloccato dalla privacy**. Potrebbe essere necessario scegliere **Mostra di più** per visualizzare il campo.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Gestione delle richieste dell'interessato in una versione di valutazione
Alcuni tipi di dati personali fanno parte dell'account Office 365 e richiedono l'accesso amministrativo per l'esportazione, se si riceve una richiesta da parte di un utente in merito a questo tipo di dati personali ai sensi del Regolamento generale sulla protezione dei dati (GDPR). Il processo per la gestione delle richieste degli interessati è diverso in base al tipo di tenant di [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Se si dispone di un abbonamento a pagamento per [!INCLUDE[d365fin](includes/d365fin_md.md)], è necessario contattare l'amministratore del tenant della propria organizzazione per inoltrare una richiesta dell'interessato. L'amministratore ha i diritti e gli strumenti amministrativi per soddisfare tale richiesta.  

Se ci si è registrati a [!INCLUDE[d365fin](includes/d365fin_md.md)] tramite la pagina [Trial](https://trials.dynamics.com/) e si sta ancora utilizzando la versione di prova tramite un abbonamento a pagamento dall'amministratore del tenant dell'organizzazione, è possibile inoltrare la richiesta tramite la pagina dedicata alla [privacy dell'utente nel Portale di Azure](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Qui è possibile esportare e scaricare i dati personali.

Nella pagina sulla privacy per la privacy, è anche possibile chiudere il proprio account. Tuttavia, si consiglia di assicurarsi di aver esportato e cancellato tutti i dati prima, poiché l'eliminazione dell'account comporta la perdita dell'accesso a [!INCLUDE[d365fin](includes/d365fin_md.md)].  

È comunque possibile contrassegnare le persone come bloccate in base alla privacy ed esportare, modificare o eliminare le transazioni come spiegato in altre sezioni di questo articolo.  

## <a name="handling-data-about-minors"></a>Gestione di dati relativi ai minori
Se l'età di una persona di contatto è inferiore all'età legale stabilita dalle leggi nella propria area geografica, è possibile indicare tale condizione selezionando la casella di controllo **Minorenne** nella scheda **Contatto**. Quando si seleziona tale casella, la casella di controllo **Bloccato dalla privacy** viene selezionata automaticamente. Quando si riceve il consenso dal genitore o dal tutore legale, è possibile scegliere la casella di controllo **Consenso dei genitori ricevuto** per sbloccare il contatto. Sebbene sia possibile elaborare i dati personali dei minori, non è possibile utilizzare la funzione di profiling in Microsoft Dynamics 365 for Sales.

> [!Note]
> Il log modifiche consente di registrare informazioni dettagliate, ad esempio quando e da chi la casella di controllo **Consenso dei genitori ricevuto** è stata selezionata. Un amministratore può eseguire tale impostazione utilizzando la guida **Setup log modifiche** e anche scegliendo la casella di controllo **Log Modification for Parental Consent Received** nella scheda **Contatto**. Per ulteriori informazioni, vedere [Registrazione di modifiche](across-log-changes.md).  

## <a name="see-also"></a>Vedi anche
[Classificazione di dati](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classificazione di dati riservati](admin-classifying-data-sensitivity.md)  
[Esportazione dei dati aziendali in Excel](about-export-data.md)  
[Registrazione di modifiche](across-log-changes.md)  
[Richieste degli interessati correlate al GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)  


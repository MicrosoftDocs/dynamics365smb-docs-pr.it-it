---
title: Rispondere a richieste relative a dati personali
description: "È necessario rispondere alle richieste di oggetti dati."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Rispondere a richieste relative a dati personali  
Gli oggetti dati possono richiedere diversi tipi di azioni riguardanti i relativi dati personali. Se i dati riservati sono stati classificati e si è certi della correttezza dell'operazione, un amministratore può rispondere alle richieste utilizzando il foglio di lavoro di classificazione dati nella Gestione ruolo utente **Amministrazione di utenti, gruppi di utenti e autorizzazioni** oppure, se si sta utilizzando il client Windows, nella Gestione ruolo utente **Manager IT**. Per ulteriori informazioni sulla classificazione dei dati e sulla classificazione di dati riservati, vedere [Classificazione di dati](/dynamics-nav/classifying-data) e [Classificazione di dati riservati](admin-classifying-data-sensitivity.md).

Nella tabella seguente vengono forniti esempi dei tipi di richieste a cui è possibile rispondere.

> [!Note]
> Sebbene forniamo le funzionalità per rispondere a questi tipi di richieste e quindi per accedere a dati personali, è responsabilità dell'utente assicurare la corretta archiviazione e classificazione dei dati personali e riservati.

|Tipo richiesta|Descrizione e risposta suggerita|
|-----|-----|
|Richieste di trasferibilità|Un oggetto dati può eseguire una richiesta di trasferibilità dei dati, di conseguenza è necessario esportare i dati personali dell'oggetto dati dai sistemi e fornirli in un formato strutturato comune. Per rispondere a queste richieste, utilizzare Utilità privacy dei dati per esportare dati personali in un file di Excel. Con Excel, è possibile modificare i dati personali e salvarli in un formato comune leggibile da computer, ad esempio .csv o .xml. Gli amministratori possono anche esportare i dati utilizzando pacchetti di configurazione di RapidStart e quindi configurare le tabelle di dati master e le relative tabelle che contengono dati personali. |
|Richieste di eliminazione|Un oggetto dati può richiedere di eliminare i relativi dati personali. Esistono svariati metodi per eliminare dati personali utilizzando le funzionalità di personalizzazione, ma la decisione e l'implementazione sono di responsabilità dell'utente. In alcuni casi, è possibile scegliere di modificare direttamente i dati, ad esempio eliminando un contatto e quindi eseguendo il processo batch relativo all'eliminazione di interazioni annullate per il contatto. <br><br> **Nota:** se è stata specificata una data nel campo **Consenti eliminazione documenti anteriori a** nelle pagine **Setup contabilità clienti e vendite** o **Setup contabilità fornitori e acquisti**, potrebbe essere necessario modificare la data in modo da eliminare i documenti di acquisto e vendita registrati che sono stati stampati e le cui date di registrazione sono uguali o antecedenti a quella data.|
|Richieste di correzione|Un oggetto dati può richiedere di correggere dati personali inaccurati. Questa operazione può essere effettuata in vari modi. In alcuni casi, si potrebbero esportare liste in Excel per modificare in blocco più record e quindi importare i dati aggiornati. Per ulteriori informazioni, vedere [Esportazione dei dati aziendali in Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). È inoltre possibile modificare manualmente i campi contenenti dati personali, ad esempio modificare informazioni relative a un cliente nella scheda cliente. Tuttavia, i record delle transazioni quali movimenti contabili generali, clienti e fiscali sono essenziali per l'integrità del sistema di pianificazione delle risorse aziendali. Se si archiviano dati personali nei record delle transazioni commerciali, si deve prendere in considerazione l'utilizzo delle funzionalità di personalizzazione per modificare tali dati personali.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Limitazione dell'elaborazione dei dati per un oggetto dati
Un oggetto dati può richiedere di interrompere temporaneamente l'elaborazione dei relativi dati personali. Per soddisfare tali richieste, è possibile contrassegnare i record come bloccati a causa della privacy. Quando un record viene contrassegnato come bloccato, non è possibile creare nuove transazioni che utilizzano quel record. Ad esempio, non è possibile creare una nuova fattura per un cliente quando il cliente o il venditore è bloccato. Per contrassegnare un oggetto dati come bloccato, aprire la scheda per l'oggetto dati, ad esempio le schede cliente, fornitore o contatto, e scegliere la casella du controllo **Bloccato dalla privacy**. Potrebbe essere necessario scegliere **Mostra di più** per visualizzare il campo.

## <a name="handling-data-about-minors"></a>Gestione di dati relativi ai minori
Se l'età di una persona di contatto è inferiore all'età legale stabilita dalle leggi nella propria area geografica, è possibile indicare tale condizione selezionando la casella di controllo **Minorenne** nella scheda **Contatto**. Quando si seleziona tale casella, la casella di controllo **Bloccato dalla privacy** viene selezionata automaticamente. Quando si riceve il consenso dal genitore o dal tutore legale, è possibile scegliere la casella di controllo **Consenso dei genitori ricevuto** per sbloccare il contatto. Sebbene sia possibile elaborare i dati personali dei minori, non è possibile utilizzare la funzione di profiling in Microsoft Dynamics 365 for Sales.

> [!Note]
> Il log modifiche consente di registrare informazioni dettagliate, ad esempio quando e da chi la casella di controllo **Consenso dei genitori ricevuto** è stata selezionata. Un amministratore può eseguire tale impostazione utilizzando la guida **Setup log modifiche** e anche scegliendo la casella di controllo **Log Modification for Parental Consent Received** nella scheda **Contatto**. Per ulteriori informazioni, vedere [Registrazione di modifiche](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Vedi anche
[Classificazione di dati](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Classificazione di dati riservati](admin-classifying-data-sensitivity.md)  
[Esportazione dei dati aziendali in Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  


---
title: Classificazione di dati riservati
description: È necessario specificare quale tipo di dati sulle persone memorizzare in modo da rispondere alle richieste dell'oggetto dati.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.search.form: 1752
ms.date: 06/14/2021
ms.service: dynamics-365-business-central
---

# <a name="classifying-data-sensitivity-fields"></a>Campi Classificazione di dati riservati

Per classificare i campi che contengono dati riservati o personali, un partner Microsoft può impostare la proprietà ```DataClassification``` nei campi. Per eseguire questa operazione è necessario l'accesso alle tabelle del database, tramite l'ambiente di sviluppo oppure eseguendo uno script Windows PowerShell. Per ulteriori informazioni, vedere [Classificazione di dati](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Come cliente, è possibile aggiungere un secondo livello di classificazione specificando i livelli di riservatezza per i dati archiviati in campi standard e personalizzati. La classificazione di dati riservati assicura la conoscenza della posizione in cui sono mantenuti i dati personali nel sistema e rende più semplice rispondere alle richieste dagli oggetti dati. Ad esempio, se un contatto o un cliente chiede di esportare i relativi dati personali. Per ulteriori informazioni, vedere [Rispondere a richieste relative a dati personali](admin-responding-to-requests-about-personal-data.md).

> [!Important]  
> Microsoft fornisce tale funzione di classificazione di dati riservati solo per motivi di utilità. È responsabilità dell'utente classificare i dati in modo appropriato e rispettare le leggi e i regolamenti applicabili. Microsoft declina ogni responsabilità nei confronti di eventuali reclami relativi alla classificazione dei dati.  

Nella tabella seguente sono descritti i livelli di riservatezza dei dati che è possibile assegnare.

|Riservatezza|Description|
|----|----|
|Sensibili | Informazioni su origine razziale o etnica, opinioni politiche, credenze religiose, iscrizione a sindacati, salute fisica o mentale, orientamento sessuale o fedina penale di un oggetto dati. |
|Personale | Informazioni utilizzabili per identificare un oggetto dati, direttamente o in combinazione con altri dati o informazioni.|
|Riservato | Dati commerciali utilizzati a fini di contabilità o per altri scopi commerciali e che non si intende esporre a altre entità. Ad esempio, movimenti contabili.|
|Normale | Dati generali che non appartengono a nessun altra categoria.|

## <a name="how-do-i-classify-my-data"></a>Come si classificano i dati personali?

La classificazione dei livelli di riservatezza per ogni singolo campo potrebbe richiedere molto tempo. Per accelerare il processo, vengono forniti strumenti per classificare in blocco la riservatezza dei campi e ottimizzare le classificazioni per campi specifici. È possibile trovare strumenti nel foglio di lavoro Classificazione di dati, disponibile nella Gestione ruolo utente Amministrazione di utenti, gruppi di utenti e autorizzazioni. Per utilizzare questo foglio di lavoro è necessario essere un amministratore di sistema.
 
> [!Important]  
> Il foglio di lavoro di classificazione di dati è vuoto quando viene aperto per la prima volta. È necessario eseguire la guida di classificazione di dati per generare la lista di campi. Per avviare la guida, scegliere l'azione **Imposta classificazioni dati**.

Ad esempio, il foglio di lavoro di classificazione di dati consente di eseguire operazioni come:  

* Utilizzare la guida di classificazione di dati per esportare i campi in un foglio di lavoro di Excel dove è possibile classificarli in blocco. L'utilizzo di un foglio di lavoro Excel risulta particolarmente utile se si collabora con un partner Microsoft. Dopo che si aggiorna il foglio di lavoro, è possibile utilizzare la guida per importare e applicare le classificazioni. È inoltre possibile utilizzare la guida per classificare i campi manualmente.  
* Scegliere un campo e filtrare la lista per trovare campi simili che probabilmente appartengono alla stessa classificazione del campo su cui si è basata la ricerca.  
* Analizzare un campo visualizzandone il contenuto.  

> [!Tip]  
> Sono state definite classificazioni di sensibilità di esempio per le tabelle e i campi nella società demo Cronus. È possibile utilizzare queste classificazioni come esempio quando si classificano tabelle e campi.

## <a name="see-also"></a>Vedi anche

<!-- [Classifying Data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data) -->
[!INCLUDE[footer-include](includes/footer-banner.md)]

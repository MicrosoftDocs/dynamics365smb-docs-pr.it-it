---
title: Setup Relationship Management | Documenti di Microsoft
description: Viene descritto come impostare la gestione del marketing e dei contatti in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ba5ed3df4ddbf39863509528a667848015312ab0
ms.contentlocale: it-it
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-relationship-management"></a>Setup Relationship Management
Prima di iniziare a lavorare sui contatti e sugli interessi di marketing, è necessario prendere alcune decisioni e seguire alcuni passaggi per definire la modalità di gestione da parte dell'area marketing di alcuni aspetti dei contatti. Ad esempio, è possibile decidere se sincronizzare la scheda contatto con la scheda cliente, la scheda fornitore e la scheda conto corrente bancario, definire la numerazione o la formula di saluto standard per quando si scrive ai contatti.

La gestione corretta dei contatti e la messa a punto di una strategia per identificare, attirare e fidelizzare i clienti sono fondamentali per ottimizzare il business e aumentare la soddisfazione dei clienti. Anche l'utilizzo di un efficiente sistema di gestione dei contatti si rivelerà importante per stabilire e mantenere le relazioni con i clienti. La comunicazione è l'aspetto chiave di queste relazioni. Riuscire a comunicare con clienti esistenti e potenziali, fornitori e partner aziendali nel rispetto delle loro esigenze è fondamentale per garantire il successo delle società. Il passaggio principale consiste nel definire una strategia e la modalità di utilizzo delle informazioni di contatto della società. Queste informazioni verranno visualizzate da molti gruppi diversi all'interno della società, pertanto l'utilizzo di un ottimo sistema di gestione renderà tutti molto più produttivi.

Impostare la gestione dei contatti e del marketing dalla finestra **Setup marketing**. Per aprire la finestra **Setup marketing**, nell'angolo superiore destro selezionare l'icona **Cerca pagina o report** ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Setup marketing**, quindi selezionare il collegamento correlato.

## <a name="automatically-copy-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Copiare automaticamente informazioni specifiche dalle società contatto alle persone contatto.
Alcune informazioni relative alle società contatto sono identiche alle informazioni sulle persone contatto che lavorano all'interno di tali società, ad esempio i dettagli dell'indirizzo. Nella sezione **Eredità** della finestra **Setup marketing** è possibile impostare l'applicazione in modo che, ogni volta che si crea una persona contatto per una società contatto, alcuni campi specifici vengano copiati automaticamente dalla scheda della società contatto alla scheda della persona contatto. Ad esempio, è possibile scegliere di copiare il codice agente, i dettagli dell'indirizzo (indirizzo, indirizzo 2, città, CAP e provincia), i dettagli di comunicazione (numero di fax, telex di risposta e numero di telefono) e altro ancora.

Se si modifica uno di questi campi nella scheda della società contatto, viene modificato automaticamente anche il campo nella scheda della persona contatto, a meno che non sia stato modificato manualmente.

Per ulteriori informazioni, vedere [Procedura: creare contatti](marketing-how-create-contact-persons.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Utilizzare le impostazioni di default nei nuovi contatti
È possibile impostare l'applicazione in modo da assegnare automaticamente un codice lingua, un codice territorio, un codice agente e un codice paese specifici come default per ogni nuovo contatto creato. È inoltre possibile inserire un codice ciclo di vendita di default che verrà assegnato automaticamente a ogni nuova opportunità creata.

L'eredità dei campi viene sovrascritta ai valori di default impostati. Se ad esempio la lingua di default è stata impostata su Inglese ma la lingua della società contatto è Tedesco, quest'ultimo viene automaticamente assegnato come codice lingua per i contatti registrati relativi a tale società.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-record-interactions"></a>Registrare automaticamente le interazioni
[!INCLUDE[d365fin](includes/d365fin_md.md)] può registrare automaticamente documenti di vendita e di acquisto come interazioni, ad esempio ordini, fatture, carichi e così via, oltre a e-mail, telefonate e copertine.

Per ulteriori informazioni, vedere [Registrazione automatica delle interazioni con i contatti](marketing-auto-record-interactions.md).

## <a name="synchronize-contacts-with-customers-and-more"></a>Sincronizzare i contatti con i clienti e altri soggetti
Per sincronizzare la scheda contatto con la scheda cliente, la scheda fornitore e la scheda conto corrente bancario, è necessario selezionare un codice di relazione d'affari per clienti, fornitori e conti correnti bancari. È ad esempio possibile collegare un contatto a un cliente esistente solo se è stato selezionato un codice relazione d'affari per i clienti nella finestra **Setup marketing**.

Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assign-a-number-series-to-contacts-and-opportunities"></a>Assegnare una numerazione ai contatti e alle opportunità
È possibile impostare una numerazione per contatti e opportunità. Se si è impostata una numerazione per i contatti, quando si crea un contatto e si preme INVIO nel campo Nr. della scheda contatto, viene automaticamente inserito il numero del contatto successivo disponibile.

Per ulteriori informazioni sulla numerazione, vedere [Creazione di numerazioni](ui-create-number-series.md).

## <a name="search-for-duplicate-contacts-when-contacts-are-created"></a>Cercare i contatti duplicati quando vengono creati dei contatti
È possibile impostare il programma affinché vengano ricercati i duplicati ogni volta che si crea una società contatto; in alternativa, è possibile effettuare tale ricerca manualmente una volta completata la creazione dei contatti. È inoltre possibile aggiornare automaticamente le stringhe di ricerca ogni volta che le informazioni sui contatti vengono modificate o si crea un contatto. È possibile stabilire una percentuale di ricerca, ossia la percentuale di stringhe identiche che due contatti devono avere per essere considerati duplicati.

## <a name="set-up-email-logging"></a>Impostare il log delle e-mail
È possibile scambiare i messaggi e-mail con contatti, clienti, fornitori e così via. È possibile inviare e ricevere i messaggi e-mail utilizzando l'applicazione o Outlook. Prima di scambiare i messaggi e fare in modo che i messaggi vengano memorizzati e messi in coda nel sistema, è necessario impostare alcuni parametri, quali l'intervallo di tempo in base al quale viene eseguita la verifica della presenza di messaggi e-mail in attesa di elaborazione, il nome del profilo di registrazione e-mail e così via.

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


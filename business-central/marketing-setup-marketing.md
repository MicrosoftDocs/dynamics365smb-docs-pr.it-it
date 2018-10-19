---
title: Setup della gestione dei contatti e del marketing| Documenti Microsoft
description: "È possibile impostare la gestione dei contatti e del marketing in Business Central per ottimizzare relazioni con i clienti o i clienti potenziali e migliorare le campagne e le promozioni."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ac38294ce65d767133e70880b6104c7325d9bb3a
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-relationship-management"></a>Setup Relationship Management
Prima di iniziare a lavorare sui contatti e sugli interessi di marketing, è necessario prendere alcune decisioni e seguire alcuni passaggi per definire la modalità di gestione da parte dell'area marketing di alcuni aspetti dei contatti. Ad esempio, è possibile decidere se sincronizzare la scheda contatto con la scheda cliente, la scheda fornitore e la scheda conto corrente bancario, definire la numerazione o la formula di saluto standard per quando si scrive ai contatti.

La gestione corretta dei contatti e la messa a punto di una strategia per identificare, attirare e fidelizzare i clienti sono fondamentali per ottimizzare il business e aumentare la soddisfazione dei clienti. Anche l'utilizzo di un efficiente sistema di gestione dei contatti si rivelerà importante per stabilire e mantenere le relazioni con i clienti. La comunicazione è l'aspetto chiave di queste relazioni. Riuscire a comunicare con clienti esistenti e potenziali, fornitori e partner aziendali nel rispetto delle loro esigenze è fondamentale per garantire il successo delle società. Il passaggio principale consiste nel definire una strategia e la modalità di utilizzo delle informazioni di contatto della società. Queste informazioni verranno visualizzate da molti gruppi diversi all'interno della società, pertanto l'utilizzo di un ottimo sistema di gestione renderà tutti molto più produttivi.

Impostare la gestione dei contatti e del marketing dalla finestra **Setup marketing**. Per aprire la finestra **Setup marketing**, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup marketing** e quindi scegliere il collegamento correlato.

## <a name="automatically-copying-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Copiare automaticamente informazioni specifiche dalle società contatto alle persone contatto
Alcune informazioni relative alle società contatto sono identiche alle informazioni sulle persone contatto che lavorano all'interno di tali società, ad esempio i dettagli dell'indirizzo. Nella sezione **Eredità** della finestra **Setup marketing** è possibile impostare l'applicazione in modo che, ogni volta che si crea una persona contatto per una società contatto, alcuni campi specifici vengano copiati automaticamente dalla scheda della società contatto alla scheda della persona contatto. Ad esempio, è possibile scegliere di copiare il codice agente, i dettagli dell'indirizzo (indirizzo, indirizzo 2, città, CAP e provincia), i dettagli di comunicazione (numero di fax, telex di risposta e numero di telefono) e altro ancora.

Se si modifica uno di questi campi nella scheda della società contatto, viene modificato automaticamente anche il campo nella scheda della persona contatto, a meno che non sia stato modificato manualmente.

Per ulteriori informazioni, vedere [Creare contatti](marketing-how-create-contact-persons.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Utilizzare le impostazioni di default nei nuovi contatti
È possibile impostare l'applicazione in modo da assegnare automaticamente un codice lingua, un codice territorio, un codice agente e un codice paese specifici come default per ogni nuovo contatto creato. È inoltre possibile inserire un codice ciclo di vendita di default che verrà assegnato automaticamente a ogni nuova opportunità creata.

L'eredità dei campi viene sovrascritta ai valori di default impostati. Se ad esempio la lingua di default è stata impostata su Inglese ma la lingua della società contatto è Tedesco, quest'ultimo viene automaticamente assegnato come codice lingua per i contatti registrati relativi a tale società.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Interazioni di registrazioni automatiche
[!INCLUDE[d365fin](includes/d365fin_md.md)] può registrare automaticamente documenti di vendita e di acquisto come interazioni, ad esempio ordini, fatture, carichi e così via, oltre a e-mail, telefonate e copertine.

Per ulteriori informazioni, vedere [Registrazione automatica delle interazioni con i contatti](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Sincronizzare i contatti con i clienti e altri soggetti
Per sincronizzare la scheda contatto con la scheda cliente, la scheda fornitore e la scheda conto corrente bancario, è necessario selezionare un codice di relazione d'affari per clienti, fornitori e conti correnti bancari. È ad esempio possibile collegare un contatto a un cliente esistente solo se è stato selezionato un codice relazione d'affari per i clienti nella finestra **Setup marketing**.

Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Assegnare una numerazione ai contatti e alle opportunità
È possibile impostare una numerazione per contatti e opportunità. Se si è impostata una numerazione per i contatti, quando si crea un contatto e si preme INVIO nel campo Nr. della scheda contatto, viene automaticamente inserito il numero del contatto successivo disponibile.

Per ulteriori informazioni sulla numerazione, vedere [Creazione di numeri](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Cercare i contatti duplicati quando vengono creati dei contatti
È possibile impostare il programma affinché vengano ricercati i duplicati ogni volta che si crea una società contatto; in alternativa, è possibile effettuare tale ricerca manualmente una volta completata la creazione dei contatti. È inoltre possibile aggiornare automaticamente le stringhe di ricerca ogni volta che le informazioni sui contatti vengono modificate o si crea un contatto. È possibile stabilire una percentuale di ricerca, ossia la percentuale di stringhe identiche che due contatti devono avere per essere considerati duplicati.

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


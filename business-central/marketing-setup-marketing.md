---
title: Informazioni sul setup della gestione dei contatti e del marketing
description: È possibile impostare la gestione dei contatti e del marketing in Business Central per ottimizzare relazioni con i clienti o i clienti potenziali e migliorare le campagne e le promozioni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect, client, customer, campaign, promo'
ms.search.forms: '5172, 5173, 5170, 5094, 429'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-relationship-management"></a>Setup Relationship Management

Prima di iniziare a lavorare sui contatti e sugli interessi di marketing, è necessario prendere alcune decisioni e seguire alcuni passaggi per definire la modalità di gestione da parte dell'area marketing di alcuni aspetti dei contatti. Ad esempio, è possibile decidere se sincronizzare la scheda contatto con la scheda cliente, la scheda fornitore e la scheda conto corrente bancario, definire la numerazione o la formula di saluto standard per quando si scrive ai contatti.

La gestione corretta dei contatti e la messa a punto di una strategia per identificare, attirare e fidelizzare i clienti sono fondamentali per ottimizzare il business e aumentare la soddisfazione dei clienti. Anche l'utilizzo di un efficiente sistema di gestione dei contatti si rivelerà importante per stabilire e mantenere le relazioni con i clienti. La comunicazione è l'aspetto chiave di queste relazioni. Riuscire a comunicare con clienti esistenti e potenziali, fornitori e partner aziendali nel rispetto delle loro esigenze è fondamentale per garantire il successo delle società. Il passaggio principale consiste nel definire una strategia e la modalità di utilizzo delle informazioni di contatto della società. Queste informazioni verranno visualizzate da molti gruppi diversi all'interno della società, pertanto l'utilizzo di un ottimo sistema di gestione renderà tutti molto più produttivi.

Impostare la gestione dei contatti e del marketing dalla pagina **Setup marketing**. Per aprire la pagina **Setup marketing**, scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup marketing**, quindi scegli il collegamento correlato.

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Copiare automaticamente informazioni specifiche da Società contatto a Persone contatto
Alcune informazioni relative alle società contatto sono identiche alle informazioni sulle persone contatto che lavorano all'interno di tali società, ad esempio i dettagli dell'indirizzo. Nella sezione **Eredità** della pagina **Setup marketing** è possibile impostare l'applicazione in modo che, ogni volta che si crea una persona contatto per una società contatto, alcuni campi specifici vengano copiati automaticamente dalla scheda della società contatto alla scheda della persona contatto. Ad esempio, è possibile scegliere di copiare il codice agente, i dettagli dell'indirizzo (indirizzo, indirizzo 2, città, CAP e provincia), i dettagli di comunicazione (numero di fax, telex di risposta e numero di telefono) e altro ancora.

Se si modifica uno di questi campi nella scheda della società contatto, viene modificato automaticamente anche il campo nella scheda della persona contatto, a meno che non sia stato modificato manualmente.

Per ulteriori informazioni, vedi [Creare contatti](marketing-create-contact-companies.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Utilizzare le impostazioni predefinite nei nuovi contatti
È possibile impostare l'applicazione in modo da assegnare automaticamente un codice lingua, un codice territorio, un codice agente e un codice paese specifici come default per ogni nuovo contatto creato. È inoltre possibile inserire un codice ciclo di vendita di default che verrà assegnato automaticamente a ogni nuova opportunità creata.

L'eredità dei campi viene sovrascritta ai valori di default impostati. Se ad esempio la lingua di default è stata impostata su Inglese ma la lingua della società contatto è Tedesco, quest'ultimo viene automaticamente assegnato come codice lingua per i contatti registrati relativi a tale società.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Interazioni di registrazioni automatiche
[!INCLUDE[prod_short](includes/prod_short.md)] può registrare automaticamente documenti di vendita e di acquisto come interazioni, ad esempio ordini, fatture, carichi e così via, oltre a e-mail, telefonate e copertine.

Per ulteriori informazioni, vedere [Registrazione automatica delle interazioni con i contatti](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Sincronizzare i contatti con i clienti e altri soggetti
Per sincronizzare la scheda contatto con la scheda cliente, la scheda fornitore e la scheda conto corrente bancario, è necessario selezionare un codice di relazione d'affari per clienti, fornitori e conti correnti bancari. È ad esempio possibile collegare un contatto a un cliente esistente solo se è stato selezionato un codice relazione d'affari per i clienti nella pagina **Setup marketing**.

Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).  

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Assegnare una numerazione ai contatti e alle opportunità
È possibile impostare una numerazione per contatti e opportunità. Se hai impostato una numerazione per i contatti, quando crei un contatto e premi <kbd>INVIO</kbd> nel campo Nr. della scheda contatto, viene automaticamente inserito il numero del contatto successivo disponibile.

Per ulteriori informazioni sulla numerazione, vedere [Creazione di numeri](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Cercare i contatti duplicati quando vengono creati dei contatti
È possibile impostare l'applicazione affinché vengano ricercati i duplicati ogni volta che si crea una società contatto; in alternativa, è possibile effettuare tale ricerca manualmente una volta completata la creazione dei contatti. È inoltre possibile aggiornare automaticamente le stringhe di ricerca ogni volta che le informazioni sui contatti vengono modificate o si crea un contatto. È possibile stabilire una percentuale di ricerca, ossia la percentuale di stringhe identiche che due contatti devono avere per essere considerati duplicati.

## <a name="see-also"></a>Vedere anche
[Gestione dei contatti](marketing-contacts.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

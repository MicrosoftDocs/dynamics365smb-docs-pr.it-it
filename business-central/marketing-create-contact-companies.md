---
title: "Creare società contatto| Documenti Microsoft"
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: it-it
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Creazione di società contatto
La società si incontra regolarmente con altre società con le quali svilupperà in futuro relazioni commerciali. Quando si stabilisce un nuovo contatto, è necessario registrare queste informazioni affinché la comunicazione possa continuare.

L'assegnazione del numero più elevato possibile di dati su una determinata società è garanzia di una comunicazione efficiente. Ad esempio, assegnando il settore industriale rilevante, le società specifiche verranno incluse nelle comunicazioni pertinenti.

È inoltre possibile definire la relazione d'affari con un contatto. Ad esempio, un contatto potrebbe essere una banca, un potenziale cliente o un terzista.

## <a name="creatinge-contact-companies"></a>Creazione di società contatto
È possibile creare un contatto per ogni nuova società con cui si interagisce, ad esempio cliente, fornitore, potenziale cliente, banca, studio legale, consulente e così via.

Esistono due modi per creare un contatto: da zero o da un cliente, un fornitore o da un conto corrente bancario esistente.

Prima di creare un contatto, si consiglia di verificare le impostazioni nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Setup Relationship Management](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Per creare una società contatto da zero
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr. campo** inserire un numero per il contatto.

    In alternativa, se è stata impostata una numerazione per i contatti nella pagina **Setup marketing**, è possibile premere INVIO per selezionare il successivo numero di contatto disponibile.  
4. Impostare il **Tipo** su **Società**.
5. Compilare gli altri campi come necessario.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Per creare un contatto per una società da un cliente, fornitore o conto corrente bancario
Se è già stato impostato un numero di clienti, fornitori e conti correnti bancari, è possibile creare contatti sulla base dei dati esistenti. Quando si crea un contatto in questo modo, le informazioni di contatto verranno sincronizzate con clienti, fornitori, o le informazioni del conto corrente bancario.

> [!NOTE]  
>   Prima di creare la società contatto in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella pagina **Setup marketing**. Se verranno creati i contatti da conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella pagina **Setup contabilità generale**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immettere una delle seguenti opzioni, in base a dove si desidera creare contatti, quindi selezionare il collegamento correlato.
   * **Crea contatti da clienti**
   * **Crea contatti dai fornitori**
   * **Crea contatti da conti correnti**
2. Nella pagina del processo batch che si apre, nella sezione **Cliente**, **Fornitore** o **Conti correnti bancari**, impostare i filtri se si desidera creare contatti rispettivamente da clienti, fornitori o conti correnti bancari specifici.
3. Scegliere **OK** per avviare la creazione di contatti.

    Ai nuovi contatti verranno assegnati numeri contatto successivi all'interno della numerazione. Ai nuovi contatti creati verrà assegnata la relazione d'affari per i fornitori specificata nella pagina **Setup marketing**.

> [!TIP]  
>   È anche possibile creare un cliente, fornitore o conto corrente bancario da un contatto. Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari
Se alcuni contatti sono anche clienti, fornitori o conti correnti bancari, è possibile sincronizzare le informazioni di contatto con il relativo cliente, fornitore o conto corrente bancario. La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.  

Prima di effettuare tale operazione, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Setup Relationship Management](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Differenti modi di sincronizzare i contatti con clienti, fornitori e conti correnti bancari
È possibile sincronizzare i contatti con clienti, fornitori o i conti correnti bancari grazie a tre metodi:

* collegare i contatti con clienti, fornitori o conti correnti bancari esistenti dalla scheda contatto. Per ulteriori informazioni, vedere [Collegare i contatti con clienti, fornitori e conti correnti bancari](marketing-how-link-contact.md).
* Creare clienti, fornitori o conti correnti bancari dal contatto. Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* creare contatti da clienti, fornitori o conti correnti bancari. Per ulteriori informazioni, vedere [Creare un contatto per una società da un cliente, fornitore o conto corrente bancario](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Conseguenze della sincronizzazione
Quando il contatto è sincronizzato con il cliente, il fornitore, il conto corrente bancario:

* è necessario aggiornare le informazioni solo in una scheda. Se ad esempio si modifica il numero di telefono del contatto, viene effettuato automaticamente lo stesso aggiornamento nel cliente, nel fornitore o nel conto corrente bancario;
* se si è specificata una numerazione per i contatti, quando si crea una scheda cliente, una scheda fornitore o una scheda conto corrente bancario, viene creata automaticamente una scheda contatto per il cliente, il fornitore o il conto corrente bancario;
* dal contatto è possibile creare offerte e ordini di vendita, oltre a offerte e ordini di acquisto;
* è possibile registrare le interazioni quando si eseguono azioni specifiche, quali la stampa di ordini e ordini programmati, la creazione di ordini assistenza vendita, l'invio di e-mail e così via;
* se si elimina un contatto collegato a un cliente, un fornitore o un conto corrente bancario, viene eliminato solo il contatto; il cliente, il fornitore o il conto corrente bancario correlato non viene eliminato;
* se si elimina un cliente, un fornitore o un conto corrente bancario collegato a un contatto, il contatto non viene eliminato.

> [!NOTE]  
>   Alcuni dettagli, relativi ad esempio a fatturazione e registrazione, non vengono visualizzati nella scheda contatto. È quindi possibile aggiungerli manualmente alla scheda cliente, fornitore o conto corrente bancario quando si creano contatti come clienti, fornitori o conti correnti bancari.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Collegamento di contatti con clienti, fornitori e conti correnti bancari
Se è presente un contatto o un cliente, un fornitore o conto bancario per la medesima società, è possibile collegare le due entità. Collegare le due entità consente di sincronizzare i dati comuni in modo che siano identici in entrambe le aree.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente
1. Aprire il contatto che si desidera collegare.
2. Scegliere l'azione **Collega con esistente**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.
3. Selezionare il cliente, fornitore o conto bancario.

   In **Campi master correnti** specificare i campi a cui il programma deve assegnare priorità in caso di conflitto tra le informazioni riportate nei campi comuni al cliente, fornitore o conto. Ad esempio, se il codice agente è diverso tra il contatto e il cliente, è sufficiente selezionare **Contatto** per utilizzare le informazioni riportate nella scheda Contatto.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Creazione di un cliente, un fornitore o un conto corrente bancario da un contatto
   È possibile registrare alcuni contatti come clienti, fornitori oppure conti correnti bancari esistenti. La creazione di un cliente, un fornitore o un conto bancario da un contatto consente di utilizzare i dati esistenti. Quando si crea un cliente, un fornitore o un conto bancario in questo modo, le informazioni verranno sincronizzate con il contatto. La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.

   Prima di poter registrare i contatti in questo modo, è necessario specificare un codice relazione d'affari per clienti, fornitori e conti correnti bancari nella pagina **Setup marketing**. Se verranno registrati i contatti come conti bancari, sarà necessario specificare anche la serie di numeri di conti correnti bancari nella pagina **Setup contabilità generale**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Per creare un contatto come cliente, fornitore o conto corrente bancario.
   1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
   2. Selezionare il contatto che si desidera creare come cliente, fornitore o conto corrente bancario.
   3. Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.
   4. Scegliere Sì nel messaggio che verrà visualizzato.

   Le informazioni di contatto vengono trasferite dalla scheda **Contatto** alla scheda **C/C bancario**, alla scheda **Cliente** o alla scheda **Fornitore**. È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione.

## <a name="setting-up-business-relations-on-contact-companies"></a>Impostazione delle relazioni d'affari nelle società contatto
È possibile utilizzare le relazioni d'affari vengono utilizzate per indicare il tipo di relazione commerciale che intercorre con i contatti, ad esempio potenziale cliente, banca, consulente e fornitore di servizi e così via.

L'utilizzo delle relazioni d'affari nei contatti è un processo a due passaggi. Innanzitutto, occorre definire il codice relazioni d'affari. Questo passaggio deve essere eseguito una sola volta per ogni relazione d'affari. Dopo aver creato un codice di relazione d'affari, è possibile iniziare ad assegnarlo alle società.

> [!NOTE]  
>   Per sincronizzare i contatti con fornitori, clienti o conti correnti bancari in altre sezioni dell'applicazione, è consigliabile impostare una relazione d'affari.

### <a name="to-define-a-business-relation-code"></a>Per definire un codice relazioni d'affari
Il codice relazione d'affari definisce una categoria o un tipo della relazione d'affari, ad esempio BANCA o Legge. È possibile impostare più codici di relazione d'affari. Per definire la relazione d'affari, utilizzare la pagina **Relazioni d'affari**.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Relazioni d'affari** e quindi scegliere il collegamento correlato.
2. Selezionare l'azione **Nuovo** e immettere un codice e una descrizione. Il codice può avere un massimo di 11 caratteri e può essere qualsiasi combinazione di numeri o lettere.

### <a name="AssignBusRelContact"></a> Per assegnare relazioni d'affari a un contatto
Non è possibile assegnare relazioni d'affari a un contatto, ma solo alle società.

1. Aprire il contatto.
2. Scegliere l'azione **Società**, quindi l'azione **Relazioni d'affari**.

    Verrà aperta la pagina **Relazioni d'affari contatto**.
3. Nel campo **Codice relazione d'affari** selezionare la relazione d'affari da assegnare.

Ripetere questi passaggi per assegnare altre relazioni d'affari. È inoltre possibile assegnare altre relazioni d'affari dalla lista Contatti seguendo la stessa procedura.

Il numero di relazioni d'affari assegnate al contatto viene visualizzato nel campo **Nr. relazione d'affari** nella sezione **Segmentazione** nella pagina **Contatto**.

Una volta assegnate le relazioni d'affari ai contatti, è possibile utilizzare queste informazioni per selezionare i contatti per i segmenti. Per ulteriori informazioni, vedere [Aggiungere contatti ai segmenti](marketing-add-contact-segment.md).

## <a name="see-also"></a>Vedi anche
[Creazione di contatti](marketing-create-contact-persons.md)   
[Utilizzo di Business Central](ui-work-product.md)


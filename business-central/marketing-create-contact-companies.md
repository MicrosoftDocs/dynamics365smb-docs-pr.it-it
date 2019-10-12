---
title: Creare società contatto| Documenti Microsoft
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f4bf8e694a7b034eb601c3bf39bd420ff61ab73a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309318"
---
# <a name="create-contacts"></a>Crea contatti
Si incontrano regolarmente persone di altre società che possono diventare relazioni d'affari, ad esempio relazioni con i clienti. In caso di nuovo contatto, è necessario registrare il maggior numero di informazioni su una scheda contatti affinché la comunicazione possa continuare.

È possibile creare il contatto come tipo **Società**, ad esempio, se la relazione non è una singola persona ma un'entità, come un appaltatore o una banca. È inoltre possibile creare il contatto di tipo **Persona**. La funzionalità è più o meno la stessa per entrambi i tipi ed entrambi possono essere modificati con l'evoluzione della relazione.

Quando una scheda contatto viene convertita in una scheda cliente, ad esempio, la persona di contatto o la società di contatto diventa il nome del cliente. La scheda di contatto rimane e i dati sulle due schede verranno sincronizzati andando avanti se li colleghi.

## <a name="person-or-company"></a>Persona o società
È possibile decidere di configurare un contatto come persona o società, in genere a seconda se si conosce il nome della persona contatto al momento della creazione. Si esegue questa operazione quando si immette il valore del campo **Tipo** nella pagina **Scheda contatto**. È inoltre possibile mantenere schede contatti per una società e per una o più persone che lavorano nella società. Ciò avviene automaticamente quando si immette un valore nel campo **Nome Società** nella scheda contatti di tipo **Persona**.

La funzionalità è la stessa per entrambi i tipi, salvo che le opzioni per ulteriori informazioni cambiano a seconda del tipo. Ad esempio, è possibile assegnare solo ruoli professionali a una persona e un settore industriale a una società. Ciò è indicato nell'interfaccia utente mediante la disattivazione di campi e azioni non applicabili. Successivamente sarà possibile modificare il valore del campo **Type**, oppure utilizzare i campi nella Scheda dettaglio **Eredità** nella pagina **Setup marketing** per verificare quali dati sono condivisi tra una persona e la società ad essa correlata. Per ulteriori informazioni, vedere [Impostazione di contatti](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Per creare un contatto manualmente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr.** inserire un numero per il contatto.

    In alternativa, se è stata impostata una numerazione per i contatti nella pagina **Setup marketing**, è possibile premere INVIO per inserire il successivo numero di contatto disponibile.  
5. Compilare i rimanenti campi come necessario. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Per creare un contatto da un cliente, fornitore o conto corrente bancario
Se vi sono clienti, fornitori e conti bancari per i quali si intendono creare schede contatto, è possibile utilizzare i processi batch **Crea contatti dai** per creare contatti sulla base dei dati esistenti. Quando si crea un contatto in questo modo, le informazioni di contatto vengono successivamente sincronizzate con clienti, fornitori o informazioni di conto bancario correlati. Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Prima di creare contatti basati su dati esistenti, è necessario specificare un codice relazione d'affari per clienti, fornitori o conti bancari nella Scheda dettaglio **Interazioni** nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Impostare i contatti](marketing-setup-contacts.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immettere una delle seguenti opzioni, in base all'origine da cui si desidera creare contatti, quindi selezionare il collegamento correlato.
   * **Crea contatti dai clienti**
   * **Crea contatti dai fornitori**
   * **Crea contatti da conti correnti**
2. Nella pagina di richiesta che si apre, nella sezione **Cliente**, **Fornitore** o **Conti correnti bancari**, impostare i filtri se si desidera creare contatti rispettivamente da clienti, fornitori o conti correnti bancari specifici.
3. Scegliere **OK** per avviare la creazione di contatti.

Ai nuovi contatti verranno assegnati numeri contatto successivi all'interno della numerazione. Ai nuovi contatti creati verranno assegnate le relazioni d'affari specificate nella pagina **Setup marketing**.

> [!TIP]  
> È possibile eseguire questa operazione anche nell'altro senso, ossia creando un cliente, un fornitore o un conto corrente bancario da un contatto. Per ulteriori informazioni, vedere [Per creare un contatto come cliente, fornitore o conto corrente bancario.](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Per creare un cliente, un fornitore o un conto corrente bancario da un contatto
Se è presente un cliente, fornitore o conto bancario per la società per la quale si intende creare un contatto, è possibile utilizzare la funzione **Crea come**. Quando si crea un contatto in questo modo, le informazioni di contatto vengono successivamente sincronizzate con clienti, fornitori o informazioni di conto bancario correlati. Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Prima di creare contatti clienti, fornitori o conti bancari da contatti, è necessario specificare un codice relazione d'affari per clienti, fornitori o conti bancari nella Scheda dettaglio **Interazioni** nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Impostazione di contatti](marketing-setup-contacts.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Selezionare il contatto che si desidera creare come cliente, fornitore o conto corrente bancario.
3. Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.
4. Scegliere il pulsante **OK**.

Le informazioni di contatto vengono trasferite dalla scheda contatto a una nuova scheda cliente, fornitore o conto bancario. È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione. Per ulteriori informazioni, vedere, ad esempio, [Registrare nuovi clienti](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente
Se è presente un contatto e un cliente, un fornitore o conto bancario per la medesima società, è possibile collegare le due entità di modo che i dati comuni siano sincronizzati.

1. Aprire il contatto che si desidera collegare.
2. Scegliere l'azione **Collega con esistente**, quindi scegliere l'azione **Cliente**, **Fornitore** oppure **C.to/corrente**.
3. Nella pagina visualizzata, selezionare il cliente, il fornitore o il conto bancario da collegare.
4. Nel campo **Campi master correnti** specificare i campi a cui dare priorità in caso di conflitto tra le informazioni riportate nei campi comuni al cliente, fornitore o conto. Se ad esempio il codice agente nella scheda contatto è diverso da quello nella scheda cliente, è possibile scegliere di mantenere quello nella scheda contatto selezionando **Contatto**.
5. Scegliere il pulsante **OK**.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari
Se alcuni contatti sono anche clienti, fornitori o conti correnti bancari, è possibile sincronizzare le informazioni di contatto con il relativo cliente, fornitore o conto corrente bancario.

La sincronizzazione di un contatto con un cliente, fornitore o conto bancario comporta i seguenti vantaggi.

* è necessario aggiornare le informazioni solo in una scheda. Se ad esempio si modifica il numero di telefono del contatto, viene effettuato automaticamente lo stesso aggiornamento nel cliente, nel fornitore o nel conto corrente bancario;
* se si è specificata una numerazione per i contatti, quando si crea una scheda cliente, una scheda fornitore o una scheda conto corrente bancario, viene creata automaticamente una scheda contatto per il cliente, il fornitore o il conto corrente bancario;
* dal contatto è possibile creare offerte e ordini di vendita, oltre a offerte e ordini di acquisto;
* è possibile registrare le interazioni quando si eseguono azioni specifiche, quali la stampa di ordini e ordini programmati, la creazione di ordini assistenza vendita, l'invio di e-mail e così via;
* se si elimina un contatto collegato a un cliente, un fornitore o un conto corrente bancario, viene eliminato solo il contatto; il cliente, il fornitore o il conto corrente bancario correlato non viene eliminato;
* se si elimina un cliente, un fornitore o un conto corrente bancario collegato a un contatto, il contatto non viene eliminato.

> [!NOTE]  
> Alcuni dettagli, relativi ad esempio a fatturazione e registrazione, non vengono visualizzati nella scheda contatto. È quindi possibile aggiungerli manualmente alla scheda cliente, fornitore o conto corrente bancario quando si creano contatti come clienti, fornitori o conti correnti bancari.

La sincronizzazione di dati comuni tra contatti e i clienti, fornitori o conti bancari correlati può essere abilitata in tre modi:

* Quando si creano contatti da clienti, fornitori o conti correnti bancari. Vedere [Per creare un contatto da un cliente, fornitore o conto corrente bancario](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Quando si creano clienti, fornitori o conti correnti bancari da contatti. Vedere [Per creare un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Quando si collegano i contatti con clienti, fornitori o conti correnti bancari esistenti dalla scheda contatto. Vedere [Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Per visualizzare a quale cliente, fornitore o conto bancario è correlato un contatto
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Selezionare la riga per un contatto, scegliere l'azione **Informazioni correlate**, quindi l'azione **Cliente/Fornitore/Conto bancario**.

Viene visualizzata la pagina per la scheda relativa.

## <a name="see-also"></a>Vedere anche
[Gestione dei contatti](marketing-contacts.md)  
[Configurazione dei contatti](marketing-setup-contacts.md)  
[Utilizzo di Business Central](ui-work-product.md)

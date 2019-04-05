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
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: aaeb98aa5e3c48a92be71546be33b1494a751cb9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801002"
---
# <a name="creating-contacts"></a>Creazione di contatti
La società si incontra regolarmente con altre società con le quali svilupperà in futuro relazioni commerciali. Quando si stabilisce un nuovo contatto, è necessario registrare queste informazioni affinché la comunicazione possa continuare.

L'assegnazione del numero più elevato possibile di dati su una determinata società è garanzia di una comunicazione efficiente. Ad esempio, assegnando il settore industriale rilevante, le società specifiche verranno incluse nelle comunicazioni pertinenti. È inoltre possibile definire la relazione d'affari con un contatto. Ad esempio, un contatto potrebbe essere una banca, un potenziale cliente o un terzista.

> [!NOTE]
> Nel campo **Tipo** nella pagina **Scheda contatto**, è possibile impostare un contatto come persona o società, in genere a seconda se si conosce il nome della persona contatto al momento della creazione. La funzionalità è la stessa per entrambi i tipi, ad eccezione di alcuni tipi di informazioni aggiuntivi che è possibile assegnare. Successivamente sarà possibile modificare il valore del campo, oppure utilizzare i campi nella Scheda dettaglio **Eredità** nella pagina **Setup marketing** per verificare quali dati sono condivisi tra una persona e la società correlata.

È possibile creare una scheda contatto per ogni nuova persona o società con cui si interagisce, ad esempio cliente, fornitore, potenziale cliente, banca, studio legale, consulente e così via.

Un contatto può essere creato in due modi:
 * Manualmente.
 * Da un cliente, fornitore o conto bancario esistente.

## <a name="to-create-a-contact-manually"></a>Per creare un contatto manualmente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr.** inserire un numero per il contatto.

    In alternativa, se è stata impostata una numerazione per i contatti nella pagina **Setup marketing**, è possibile premere INVIO per inserire il successivo numero di contatto disponibile.  
5. Compilare i rimanenti campi come necessario. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Per creare un contatto da un cliente, fornitore o conto corrente bancario
Se vi sono clienti, fornitori e conti bancari per i quali si intendono creare schede contatto, è possibile utilizzare i processi batch **Crea contatti dai** per creare contatti sulla base dei dati esistenti. Quando si crea un contatto in questo modo, le informazioni di contatto vengono successivamente sincronizzate con clienti, fornitori o informazioni di conto bancario correlati. Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Prima di creare contatti basati su dati esistenti, è necessario specificare un codice relazione d'affari per clienti, fornitori o conti bancari nella Scheda dettaglio **Interazioni** nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Impostazione di contatti](marketing-setup-contacts.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immettere una delle seguenti opzioni, in base all'origine da cui si desidera creare contatti, quindi selezionare il collegamento correlato.
   * **Crea contatti dai clienti**
   * **Crea contatti dai fornitori**
   * **Crea contatti da conti correnti**
2. Nella pagina di richiesta che si apre, nella sezione **Cliente**, **Fornitore** o **Conti correnti bancari**, impostare i filtri se si desidera creare contatti rispettivamente da clienti, fornitori o conti correnti bancari specifici.
3. Scegliere **OK** per avviare la creazione di contatti.

Ai nuovi contatti verranno assegnati numeri contatto successivi all'interno della numerazione. Ai nuovi contatti creati verranno assegnate le relazioni d'affari specificate nella pagina **Setup marketing**.

> [!TIP]  
> È possibile eseguire questa operazione anche nell'altro senso, ossia creando un cliente, un fornitore o un conto corrente bancario da un contatto. Per ulteriori informazioni, vedere [Per creare un contatto come cliente, fornitore o conto corrente bancario.](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

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

* Quando si collegano i contatti con clienti, fornitori o conti correnti bancari esistenti dalla scheda contatto. Vedere [Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).
* Quando si creano clienti, fornitori o conti correnti bancari da contatti. Vedere [Per creare un contatto da un cliente, fornitore o conto corrente bancario](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Quando si creano contatti come clienti, fornitori o conti correnti bancari. Vedere [Per creare un contatto come cliente, fornitore o conto corrente bancario](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente
Se è presente un contatto e un cliente, un fornitore o conto bancario per la medesima società, è possibile collegare le due entità di modo che i dati comuni siano sincronizzati.

1. Aprire il contatto che si desidera collegare.
2. Scegliere l'azione **Collega con esistente**, quindi scegliere l'azione **Cliente**, **Fornitore** oppure **C.to/corrente**.
3. Nella pagina visualizzata, selezionare il cliente, il fornitore o il conto bancario da collegare.
4. Nel campo **Campi master correnti** specificare i campi a cui dare priorità in caso di conflitto tra le informazioni riportate nei campi comuni al cliente, fornitore o conto. Se ad esempio il codice agente nella scheda contatto è diverso da quello nella scheda cliente, è possibile scegliere di mantenere quello nella scheda contatto selezionando **Contatto**.
5. Scegliere il pulsante **OK**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Per creare un contatto come cliente, fornitore o conto corrente bancario.
Se è presente un cliente, fornitore o conto bancario per la società per la quale si intende creare un contatto, è possibile utilizzare la funzione **Crea come**. Quando si crea un contatto in questo modo, le informazioni di contatto vengono successivamente sincronizzate con clienti, fornitori o informazioni di conto bancario correlati. Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Prima di creare contatti clienti, fornitori o conti bancari da contatti, è necessario specificare un codice relazione d'affari per clienti, fornitori o conti bancari nella Scheda dettaglio **Interazioni** nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Impostazione di contatti](marketing-setup-contacts.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Selezionare il contatto che si desidera creare come cliente, fornitore o conto corrente bancario.
3. Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore** oppure **C.to/corrente**.
4. Scegliere il pulsante **OK**.

Le informazioni di contatto vengono trasferite dalla scheda contatto a una nuova scheda cliente, fornitore o conto bancario. È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione. Per ulteriori informazioni, vedere, ad esempio, [Registrare nuovi clienti](sales-how-register-new-customers.md).

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Configurazione dei contatti](marketing-setup-contacts.md)  
[Utilizzo di Business Central](ui-work-product.md)

---
title: Crea contatti business
description: Delinea le attività per creare contatti e definire le relazioni d'affari.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 01/05/2021
ms.author: edupont
ms.openlocfilehash: 42645a038c3937644fe90ce895ee454e1d1b5d5c
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827045"
---
# <a name="create-contacts"></a>Crea contatti
Quando si sviluppa una relazione d'affari con qualcuno in un'altra società, è possibile aggiungere questa persona come contatto in [!INCLUDE[prod_short](includes/prod_short.md)]. È anche possibile aggiungere qualsiasi informazione su tale contatto o sulla relativa azienda che possono rivelarsi utili per comunicazioni future. Nella pagina **Scheda contatto** è possibile creare i seguenti tipi di contatti:

* **Persona** - In genere si utilizza quando c'è già stato un contatto diretto con qualcuno e sono disponibili i dettagli del contatto.
* **Società** - Ad esempio, se il contatto non è una singola persona ma un'entità, come un appaltatore o una banca. 

Le informazioni rilevanti per ogni tipo di contatto sono diverse, quindi i campi e le azioni disponibili sono diversi. Ad esempio, è possibile assegnare solo ruoli professionali a una persona e un settore industriale a una società. 

È possibile modificare il valore del campo **Tipo** successivamente. In alternativa, utilizzare i campi nella Scheda dettaglio **Eredità** nella pagina **Setup marketing** per specificare i dati da condividere tra una persona e la sua società. Per ulteriori informazioni, vedere [Impostazione di contatti](marketing-setup-contacts.md).

Quando un contatto viene convertito in cliente, ad esempio, la persona di contatto o la società di contatto diventa il nome del cliente. Il record del contatto viene mantenuto ed è possibile collegare il contatto e il cliente in modo che i loro dati vengano sincronizzati in futuro.

## <a name="to-create-a-contact-manually"></a>Per creare un contatto manualmente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nel campo **Nr.** inserire un numero per il contatto.

    In alternativa, se è stata impostata una numerazione per i contatti nella pagina **Setup marketing**, è possibile premere **INVIO** per inserire il successivo numero di contatto disponibile.  
5. Compilare i rimanenti campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Per creare un contatto da un cliente, fornitore o conto corrente bancario
Se vi sono clienti, fornitori e conti bancari per i quali si intendono creare schede contatto, è possibile utilizzare i processi batch **Crea contatti dai** per creare contatti sulla base dei dati esistenti. Quando si crea un contatto in questo modo, le informazioni di contatto vengono successivamente sincronizzate con clienti, fornitori o informazioni di conto bancario correlati. Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Prima di creare contatti basati su dati esistenti, è necessario specificare un codice relazione d'affari per clienti, fornitori o conti bancari nella Scheda dettaglio **Interazioni** nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Impostare i contatti](marketing-setup-contacts.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere una delle seguenti opzioni, in base all'origine da cui si desidera creare contatti, quindi selezionare il collegamento correlato.
   * **Crea contatti dai clienti**
   * **Crea contatti dai fornitori**
   * **Crea contatti da conti correnti**
2. Nella pagina di richiesta che si apre, nella sezione **Cliente**, **Fornitore** o **Conti correnti bancari**, impostare i filtri se si desidera creare contatti rispettivamente da clienti, fornitori o conti correnti bancari specifici.
3. Scegliere **OK** per avviare la creazione di contatti.

Ai nuovi contatti verranno assegnati numeri contatto successivi all'interno della numerazione. Ai nuovi contatti creati verranno assegnate le relazioni d'affari specificate nella pagina **Setup marketing**.

> [!TIP]  
> È possibile eseguire questa operazione anche nell'altro senso, ossia creando un cliente, un fornitore o un conto corrente bancario da un contatto. Per ulteriori informazioni, vedere [Per creare un contatto come cliente, fornitore o conto corrente bancario.](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Per creare un cliente, un fornitore, un dipendente o un conto corrente bancario da un contatto
Se è presente un cliente, fornitore, dipendente o conto bancario per la società per la quale si intende creare un contatto, utilizzare l'azione **Crea come**. Quando si crea un contatto in questo modo, le informazioni di contatto vengono successivamente sincronizzate con clienti, fornitori, dipendenti o informazioni di conto bancario correlati. Per ulteriori informazioni, vedere [Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Prima di creare clienti, fornitori, dipendenti o C/C bancari dai contatti, è necessario specificare un codice relazione d'affari nella Scheda dettaglio **Interazioni** nella pagina **Setup marketing**. Per ulteriori informazioni, vedere [Impostazione di contatti](marketing-setup-contacts.md).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Selezionare il contatto che si desidera creare come cliente, fornitore, dipendente o conto corrente bancario.
3. Scegliere l'azione **Crea come**, quindi scegliere **Cliente**, **Fornitore**, **Banca** o **Dipendente**.
4. Scegliere il pulsante **OK**.

Le informazioni di contatto vengono trasferite dalla scheda contatto a una nuova scheda cliente, fornitore, dipendente o conto bancario. È possibile aggiungere informazioni specifiche a ciascuna delle schede, ad esempio dettagli di pagamento e fatturazione. Per ulteriori informazioni, vedere, ad esempio, [Registrare nuovi clienti](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Per collegare un contatto a un cliente, un fornitore, un dipendente o un conto corrente bancario esistente
Se è presente un contatto e un cliente, un fornitore, un dipendente o conto bancario per la medesima società, è possibile collegare le due entità per sincronizzare i dati.

1. Aprire il contatto che si desidera collegare.
2. Scegliere l'azione **Collega con esistente**, quindi scegliere l'azione **Cliente**, **Fornitore**, **Banca** o **Dipendente**.
3. Nella pagina visualizzata, selezionare il cliente, il fornitore, il dipendente o il conto bancario da collegare.
4. Nel campo **Campi master correnti** specificare i campi a cui dare priorità in caso di conflitto tra le informazioni riportate nei campi comuni al cliente, fornitore, dipendente o C/C bancario. Se ad esempio il codice agente è diverso per il contatto e il cliente, è possibile scegliere di mantenere quello nella scheda contatto selezionando **Contatto**.
5. Scegliere il pulsante **OK**.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Per rimuovere un collegamento tra un contatto e un cliente, un fornitore, un dipendente o un conto corrente bancario esistente

Se si è collegato erroneamente un contatto e un cliente, fornitore, dipendente o conto bancario, rimuovere il collegamento tra le entità in modo che i dati non vengano più sincronizzati.

1. Aprire il contatto con il collegamento errato.  
2. Scegliere l'azione **Relazione d'affari**.  
3. Nella pagina visualizzata, selezionare il cliente, il fornitore, il dipendente o il conto bancario da cui rimuovere il collegamento.  
4. Scegliere l'azione **Elimina**.  

> [!NOTE]  
> Non utilizzare la finestra **Relazioni d'affari** per modificare le relazioni esistenti. Rimuovere invece la relazione e utilizzare l'azione **Collega con esistente**. Per ulteriori informazioni, vedere la sezione [Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Sincronizzazione di contatti con clienti, fornitori, dipendenti e conti correnti bancari
Se alcuni contatti sono anche clienti, fornitori, dipendenti o conti correnti bancari, è possibile sincronizzare i dati del contatto e ottenere i seguenti vantaggi:

* È necessario aggiornare le informazioni solo in una scheda. Se ad esempio si modifica il numero di telefono del contatto, viene effettuato automaticamente l'aggiornamento del cliente, del fornitore. del dipendente o del conto corrente bancario.
* Se si è specificata una numerazione per i contatti, quando si crea una scheda cliente, una scheda fornitore, una scheda dipendente o una scheda conto corrente bancario, viene creato automaticamente un contatto.
* Dal contatto è possibile creare offerte e ordini di vendita, oltre a offerte e ordini di acquisto.
* È possibile registrare le interazioni, quali la stampa di ordini e ordini programmati, la creazione di ordini assistenza vendita, l'invio di e-mail e così via.
* se si elimina un contatto collegato a un cliente, un fornitore, un dipendente o un conto corrente bancario, viene eliminato solo il contatto. Il cliente, il fornitore, il dipendente o il conto corrente bancario correlato non viene eliminato.
* Se si elimina un cliente, un fornitore, un dipendente o un conto corrente bancario collegato a un contatto, il contatto non viene eliminato.

> [!NOTE]  
> Alcuni dettagli, relativi ad esempio a fatturazione e registrazione, non sono disponibili per i contatti. Quando si creano contatti come clienti, fornitori, dipendenti o conti bancari, si possono aggiungere manualmente.

Sono disponibili tre modi per abilitare la sincronizzazione di dati tra contatti e i clienti, fornitori, i dipendenti o conti bancari:

* Quando si creano contatti da clienti, fornitori, dipendenti o conti correnti bancari. Vedere [Per creare un contatto da un cliente, fornitore o conto corrente bancario](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Quando si creano clienti, fornitori, dipendenti o conti correnti bancari da contatti. Vedere [Per creare un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Quando si collegano i contatti con clienti, fornitori, dipendenti o conti correnti bancari esistenti dalla scheda contatto. Vedere [Per collegare un contatto a un cliente, un fornitore o un conto corrente bancario esistente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Per visualizzare a quale cliente, fornitore, dipendente o conto bancario è correlato un contatto
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Contatti** e quindi scegliere il collegamento correlato.
2. Selezionare la riga per un contatto, scegliere l'azione **Informazioni correlate**, quindi l'azione **Cliente/Fornitore/Conto bancario/Dipendente**.

## <a name="see-also"></a>Vedere anche
[Gestione dei contatti](marketing-contacts.md)  
[Configurazione dei contatti](marketing-setup-contacts.md)  
[Utilizzo di Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
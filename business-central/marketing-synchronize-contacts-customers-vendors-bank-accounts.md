---
title: Sincronizzare i contatti con clienti e fornitori| Documenti Microsoft
description: È possibile associare o sincronizzare le informazioni di contatto dei contatti che sono anche clienti, fornitori o conti correnti bancari, in modo da aggiornate le informazioni una volta sola.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 4785e0644e2cb4c615ed79fbd23bef74d25ca547
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801334"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizzazione di contatti con clienti, fornitori e conti correnti bancari
Se alcuni contatti sono anche clienti, fornitori o conti correnti bancari, è possibile sincronizzare le informazioni di contatto con il relativo cliente, fornitore o conto corrente bancario. La sincronizzazione rende uguali le informazioni comuni tra i contatti e clienti, fornitori o conti bancari.  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Differenti modi di sincronizzare i contatti con clienti, fornitori e conti correnti bancari
È possibile sincronizzare i contatti con clienti, fornitori o i conti correnti bancari grazie a tre metodi:

* collegare i contatti con clienti, fornitori o conti correnti bancari esistenti dalla scheda contatto. Per ulteriori informazioni, vedere [Collegare i contatti con clienti, fornitori e conti correnti bancari](marketing-how-link-contact.md).
* Creare clienti, fornitori o conti correnti bancari dal contatto. Per ulteriori informazioni, vedere [Creare un un cliente, un fornitore o un conto corrente bancario da un contatto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* creare contatti da clienti, fornitori o conti correnti bancari. Per ulteriori informazioni, vedere [Creare un contatto per una società da un cliente, fornitore o conto corrente bancario](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Conseguenze della sincronizzazione
Quando il contatto è sincronizzato con il cliente, il fornitore, il conto corrente bancario:

* è necessario aggiornare le informazioni solo in una scheda. Se ad esempio si modifica il numero di telefono del contatto, viene effettuato automaticamente lo stesso aggiornamento nel cliente, nel fornitore o nel conto corrente bancario;
* se si è specificata una numerazione per i contatti, quando si crea una scheda cliente, una scheda fornitore o una scheda conto corrente bancario, viene creata automaticamente una scheda contatto per il cliente, il fornitore o il conto corrente bancario;
* dal contatto è possibile creare offerte e ordini di vendita, oltre a offerte e ordini di acquisto;
* è possibile registrare le interazioni quando si eseguono azioni specifiche, quali la stampa di ordini e ordini programmati, la creazione di ordini assistenza vendita, l'invio di e-mail e così via;
* se si elimina un contatto collegato a un cliente, un fornitore o un conto corrente bancario, viene eliminato solo il contatto; il cliente, il fornitore o il conto corrente bancario correlato non viene eliminato;
* se si elimina un cliente, un fornitore o un conto corrente bancario collegato a un contatto, il contatto non viene eliminato.

> [!NOTE]  
>   Alcuni dettagli, relativi ad esempio a fatturazione e registrazione, non vengono visualizzati nella scheda contatto. È quindi possibile aggiungerli manualmente alla scheda cliente, fornitore o conto corrente bancario quando si creano contatti come clienti, fornitori o conti correnti bancari.

## <a name="see-also"></a>Vedi anche
[Gestione dei contatti](marketing-contacts.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

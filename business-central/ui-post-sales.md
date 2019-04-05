---
title: Informazioni sulle modalità di registrazione dei documenti vendita | Documenti Microsoft
description: Informazioni sulle diverse funzioni di registrazione per i documenti di vendita.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2019
ms.locfileid: "801497"
---
# <a name="posting-sales"></a>Registrazione di vendite
Nella **Categoria registrazione** in un documento di vendita, è possibile scegliere tra le seguenti funzioni di registrazione:

* **Registra**
* **Report test**
* **Registra e invia**
* **Registra e stampa**
* **Registra e invia tramite e-mail**
* **Registra batch**
* **Anteprima registrazione**

Una volta completate le righe e immesse tutte le informazioni nell'ordine di vendita, è possibile registrarlo. Vengono create una spedizione e una fattura.

Quando un ordine di acquisto viene registrato, il conto del cliente, la contabilità generale e i movimenti contabili articoli vengono aggiornati.

Per ciascun ordine di vendita viene creato un movimento di vendita nella tabella **Movimenti C/G**. Vengono inoltre creati un movimento nel conto del cliente nella tabella **Mov. contabili clienti** e un movimento C/G nel relativo conto crediti. Infine, la registrazione dell'ordine potrebbe generare un movimento IVA e un movimento di contabilità generale relativi all'importo dello sconto. La registrazione di un movimento relativo allo sconto dipende dal contenuto del campo **Registrazione sconti** della pagina **Setup contabilità clienti**.

Per ciascuna riga dell'ordine di vendita, verrà creato un movimento contabile articolo nella tabella **Mov. contabili articoli** (se le righe di vendita contengono numeri di articolo) oppure un movimento C/G nella tabella **Movimenti C/G** (se le righe di vendita contengono un conto C/G). Inoltre, gli ordini vendita vengono sempre registrati nelle tabelle **Testate sped. vendita** e **Testate Fatt. Vendita**.

> [!IMPORTANT]  
>   Quando si registra un ordine, è possibile creare sia una spedizione che una fattura. Ciò può avvenire in modo simultaneo oppure indipendente. Prima di effettuare la registrazione, è inoltre possibile creare una spedizione parziale e una fattura parziale immettendo le necessarie informazioni nei campi **Qtà da spedire** e **Qtà da fatturare** nelle singole righe dell'ordine di vendita. Si tenga presente che non è possibile creare una fattura per un articolo che non è stato spedito. Ciò significa che è necessario registrare una spedizione prima di emettere una fattura oppure la spedizione e la fattura devono essere contemporanee.

Una volta completata la registrazione, le righe di vendita registrate vengono rimosse dall'ordine. Un messaggio avviserà l'utente che la registrazione è completata. Dopodiché sarà possibile visualizzare i movimenti registrati nelle varie pagine che contengono movimenti registrati, ad esempio le pagine **Mov. contabili clienti**, **Movimenti C/G**, **Mov. contabili articoli**, **Spedizioni vendite registrate** e **Fatture di vendita registrate**.

## <a name="see-also"></a>Vedi anche
[Vendite](sales-manage-sales.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


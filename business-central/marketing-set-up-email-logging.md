---
title: Impostare il log delle e-mail | Documenti Microsoft
description: Informazioni su come trasformare le interazioni e-mail tra venditori e clienti in reali opportunità di vendita.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: e325cce98256b723c6fcfdf4d16068f852a2b032
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308742"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Tenere traccia degli scambi di messaggi e-mail tra venditori e contatti
Ottenere di più dalle comunicazioni tra i venditori e i tuoi clienti esistenti o potenziali monitorando gli scambi di e-mail e trasformandoli in opportunità fruibili. [!INCLUDE[d365fin](includes/d365fin_md.md)] può utilizzare Exchange Online per tenere un log dei messaggi in entrata e in uscita. È possibile visualizzare e analizzare i contenuti di ciascun messaggio nella pagina **Movimenti log interazione**.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a>Impostare [!INCLUDE[d365fin](includes/d365fin_md.md)] per registrare i messaggi e-mail
Iniziare la registrazione dei messaggi e-mail con due semplici passaggi:

1. Collegare [!INCLUDE[d365fin](includes/d365fin_md.md)]con Exchange Online per l'abbonamento di Office 365. Exchange Online gestisce i messaggi di posta elettronica. Questo passaggio è stato semplificato con una guida di installazione assistita. Sono solo necessarie le credenziali di amministratore per l'account amministratore in Office 365. Per iniziare la guida, andare a **Setup assistito** e quindi scegliere **Configurare la registrazione e-mail**. 
2. Assicurarsi che siano stati inseriti indirizzi email validi in [!INCLUDE[d365fin](includes/d365fin_md.md)] per gli addetti alle vendite e i contatti, a seconda che si tratti di clienti potenziali o esistenti. Per fare ciò, per ogni cliente o venditore, aprire la scheda **Contatto** o **Venditore/Acquirente** e osservare il campo **E-mail**.

> [!Tip]
> Dopo aver completato i passaggi nella guida, è possibile verificare se la connessione ha avuto esito positivo. Cercare **Impostazione marketing**, scegliere **Processi**, **Funzioni** e **Convalida configurazione registrazione email**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visualizzazione degli scambi di messaggi e-mail nel log delle interazioni
[!INCLUDE[d365fin](includes/d365fin_md.md)] crea una voce nella pagina **Log delle interazioni** ogni volta che un venditore e un contatto scambiano un messaggio di posta elettronica. Per visualizzare il log delle interazioni, aprire la scheda **Contatto** o **Venditore/Acquirente** per la persona, quindi scegliere **Naviga**, **Cronologia** e **Voci del registro delle interazioni**. Ci sono alcune cose che si possono fare con ogni voce del log, ad esempio:

* Visualizzare il contenuto del messaggio di posta elettronica che è stato scambiato facendo clic sull'azione **Mostra allegati**.
* Trasformare uno scambio di e-mail in un'opportunità di vendita: se una voce sembra promettente, è possibile trasformarla in un'opportunità e gestirne i progressi verso una vendita. A tale scopo, selezionare la voce e scegliere l'azione **Crea opportunità**. Per ulteriori informazioni, vedere [Gestire opportunità di vendita](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Vedere anche
[Gestione delle relazioni](marketing-relationship-management.md)


---
title: Assegnare layout di documenti speciali a clienti o fornitori | Microsoft Docs
description: Quando vengono definiti layout di report personalizzati, è possibile selezionarli da schede cliente e fornitore per specificare che i layout selezionati verranno utilizzati per documenti creati per il cliente o il fornitore in questione.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 493a801b381ef21a2f8265e3a59615fa21618fc1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385901"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definire layout di documenti per clienti e fornitori
Quando vengono definiti layout di report personalizzati, è possibile selezionarli da schede cliente e fornitore per specificare quali layout verranno utilizzati per differenti tipi di documenti creati per il cliente o il fornitore in questione. Il valore nel campo **Utilizzo**, definisce per quale processo verrà utilizzato il layout di documento, ad esempio **Sollecito**, **Spedizione** e **Conferma**.

Oltre a impostare quali layout utilizzare per quale documento, è possibile risparmiare tempo quando si inviano documenti a differenti contatti di clienti o fornitori impostando gli indirizzi e-mail di contatti specifici da utilizzare con documenti specifici. Ad esempio, gli estratti conto dei clienti verranno inviati ai contatti del commercialista, gli ordini di vendita agli acquirenti dei clienti e gli ordini di acquisto ai venditori o ai gestori degli account dei fornitori.

Quando si definisce un layout di documento per un cliente o un fornitore, è anche possibile specificare l'indirizzo e-mail della persona di contatto che deve ricevere il documento. È possibile eseguire rapidamente questa operazione con la funzione **Seleziona e-mail da contatti**, che filtra automaticamente gli indirizzi e-mail di contatto registrati per il cliente o il fornitore in questione.

Prima di poter definire quale layout di documento utilizzare per quali processi e a quale contatto inviare il documento, è necessario caricare tutti i report (documenti) disponibili dalla pagina **Selezioni report**. È possibile eseguire questa operazione rapidamente con la funzione **Copia da selezione report**.

Di seguito viene descritto come definire layout di documenti di vendita da una scheda cliente. I passaggi sono gli stessi per i layout di documenti di acquisto da una scheda fornitore.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Per abilitare tutti i documenti di vendita disponibili per un cliente
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.
2. Aprire la scheda del cliente per cui si desidera definire layout di documenti per processo aziendale.
3. Nella pagina **Scheda cliente** scegliere la pagina **Layout documento**.
4. Nella pagina **Layout documento**, scegliere l'azione **Copia da selezione report**.

La pagina **Layout documento** per il cliente in questione viene riempita con tutti i layout di report per le vendite esistenti nel sistema. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

Ora è possibile procedere alla modifica dell'elenco con qualsiasi layout di report personalizzato o indirizzo e-mail per i contatti a cui devono essere inviati i documenti.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Per selezionare un layout di report personalizzato da utilizzare per un layout di documento di vendita
Se uno o più dei layout di report definiti nella pagina **Layout documento** per il cliente non hanno un layout di report personalizzato definito, è possibile farlo rapidamente.

1. Nella pagina **Layout documento**, nella riga di un layout di report per il quale si desidera utilizzare un layout personalizzato, scegliere il campo **Descrizione layout personalizzato**. Il campo viene compilato se il layout del cliente è già selezionato o vuoto.
2. Nella pagina **Layout report personalizzati**, selezionare il layout di documento speciale che si desidera utilizzare per il tipo di documento di vendita in questione. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Per impostare quale contatto riceve quale layout di documento per un cliente
È possibile risparmiare tempo quando si inviano documenti a diversi clienti o contatti del fornitore specificando gli indirizzi e-mail dei contatti sulle diverse righe della pagina **Layout documento**. Ad esempio, gli estratti conto dei clienti possono essere inviati ai contatti del commercialista, gli ordini di vendita agli acquirenti dei clienti e gli ordini di acquisto ai venditori o ai gestori degli account dei fornitori.

1. Nella pagina **Layout documento** nella riga di un layout di report che si desidera inviare a un contatto specifico per il cliente, scegliere l'azione **Seleziona e-mail da contatti**.
2. Nella pagina **Contatti** selezionare la riga del contatto pertinente, quindi scegliere il pulsante **OK**.

L'indirizzo e-mail del contatto viene ora inserito nella riga del layout di documento di modo che il documento di vendita in questione, ad esempio i solleciti, sia sempre inviato a quel contatto presso la società del cliente.

## <a name="see-also"></a>Vedere anche  
[Aggiornare layout report personalizzati](ui-update-report-layouts.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  
[Utilizzo di report, processi batch e XMLport](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
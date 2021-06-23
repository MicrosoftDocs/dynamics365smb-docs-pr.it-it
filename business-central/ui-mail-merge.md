---
title: Utilizzo di modelli Word per comunicazioni in blocco | Microsoft Docs
description: I modelli di Word possono semplificare la creazione di massa di documenti personalizzati per entità specifiche.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110956"
---
# <a name="using-word-templates-for-bulk-communication"></a>Utilizzo di modelli Word per comunicazioni in blocco
I modelli di Microsoft Word possono semplificare le comunicazioni di massa con entità come clienti e fornitori. Ad esempio, è possibile creare brochure per avvisare i clienti di una campagna di vendita, lettere per informare i fornitori su una nuova politica di acquisto o inviti per attirare contatti a un evento imminente.

> [!NOTE]
> Puoi utilizzare i modelli di Word solo su dispositivi con Microsoft Word 2019 e il sistema operativo Windows installati.

Puoi usare entità in [!INCLUDE[prod_short](includes/prod_short.md)] come origine dati per il modello e aggiungi campi unione per personalizzare i documenti per ciascuna entità. I campi di unione provengono dall'entità in [!INCLUDE[prod_short](includes/prod_short.md)]. Quando si applica un modello di Word a un'entità, i dati dei campi unione vengono inseriti nel documento.

Nella pagina **Modelli di Word** è possibile utilizzare una guida alla configurazione assistita per scaricare un file ZIP contenente un file DataSource.txt e un file modello di Word per un'entità. Dopo aver impostato il modello e aggiunto i campi unione, utilizza la stessa guida per caricare il modello. Puoi utilizzare solo il modello di Word e i file di origine dati che scarichi da [!INCLUDE[prod_short](includes/prod_short.md)] ed è necessario archiviare i file nella stessa posizione.

> [!NOTE]
> Quando scegli un'entità per cui creare un modello, l'elenco mostra tutte le entità in formato [!INCLUDE[prod_short](includes/prod_short.md)]. Tuttavia, non è possibile creare modelli per tutte le entità. Se il nome di un'entità contiene caratteri speciali, come **/**, **.**, **_**, or **-**, non puoi creare un modello per esso. Il nome dell'entità è mostrato nella colonna **Didascalia oggetto**.

Quando si imposta il modello in Word, nella scheda **Corrispondenza** puoi aggiungere campi di unione scegliendo **Inserisci Campo Unione**.

> [!NOTE]
> Non è possibile utilizzare i campi unione se il nome del campo contiene 40 o più caratteri. Ad esempio, non è possibile utilizzare il campo Company__Information_Customs_Permit_Date perché contiene 40 caratteri. 

Quando il tuo modello di Word è pronto, nella pagina **Modelli di Word** puoi scegliere **Applica** per generare i documenti. Puoi creare un documento che contiene sezioni per ogni entità o dividere l'operazione per creare un nuovo documento per ogni entità.

## <a name="to-create-a-word-template"></a>Per creare un modello di Word
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Modelli di Word** e quindi scegli il collegamento correlato.
2. Segui i passaggi nella guida di setup assistito. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Vedere anche
[Gestione dei layout di report e documenti](ui-manage-report-layouts.md)  

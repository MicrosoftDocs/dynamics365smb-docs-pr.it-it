---
title: "Creare pacchetti di configurazione di società personalizzati | Documenti Microsoft"
description: "Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti. È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e26174fcf723e13ef5a9ed0b386006c0439e1c7a
ms.contentlocale: it-it
ms.lasthandoff: 09/28/2018

---
# <a name="create-custom-company-configuration-packages"></a>Creare pacchetti di configurazione di società personalizzati
Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti. È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo.  

In generale, creare un pacchetto di configurazione per area funzionale, ad esempio, creare un pacchetto per la propria funzionalità di produzione. Che consente di collegare e impostare nuove aree in una società in base alla necessità  

Un altro approccio consiste nel creare un pacchetto che include le tabelle che definiscono il setup, ad esempio:  

-   Setup cespiti  
-   Setup contabilità generale  
-   Setup magazzino  
-   Setup manufacturing  
-   Setup contabilità fornitori  
-   Setup marketing  
-   Setup assistenza  
-   Setup contabilità clienti  
-   Setup warehouse  
-   Setup registrazioni COGE  
-   Setup registrazioni IVA  
-   Setup registrazione magazzino  

Per visualizzare un elenco completo di tabelle di setup, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup** e quindi scegliere il collegamento correlato.  

## <a name="to-create-a-custom-company-configuration-package"></a>Per creare un pacchetto di configurazione di società personalizzato  
1.  Creare un nuovo [!INCLUDE[d365fin](includes/d365fin_md.md)] ***IMPOSSIBILE Collegamento alla Guida per "Creazione di un nuovo tenant"***.   
2.  Creare una nuova società per il modello della soluzione o del settore. Per ulteriori informazioni, vedere [Creare una nuova società](admin-how-to-create-a-new-company.md).  
3.  Impostare la nuova società nel modo desiderato. Compilare tutte le tabelle di setup necessarie.  
4.  Apre la nuova società.
5. Aprire la finestra **Foglio di lavoro configurazione**.  
6.  Aggiungere al prospetto le tabelle da trasferire a un'altra società. Assegnare le righe del prospetto al pacchetto.  
7.  Creare un questionario per le tabelle di setup utilizzate con maggiore frequenza.  
8.  Creare modelli di configurazione per facilitare la creazione di dati master, ad esempio clienti o articoli.  
9.  Esportare il pacchetto come file con estensione rapidstart.  

## <a name="see-also"></a>Vedi anche  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)


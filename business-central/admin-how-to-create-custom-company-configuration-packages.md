---
title: Creare pacchetti di configurazione di società personalizzati | Documenti Microsoft
description: Con la crescita della propria azienda, è probabile che ci si dovrà basare su un set di tipi di società utilizzati con la maggior parte dei clienti. È possibile perfezionare il processo di implementazione trasformando questi tipi in pacchetti di configurazione aziendali disponibili al riutilizzo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e6781b01a80acfd3431fc000069dd2c8b96dffc5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779909"
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

Per visualizzare un elenco completo di tabelle di setup, scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup manuale** e quindi scegliere il collegamento correlato.  

> [!IMPORTANT]
> Prestare attenzione se sono stati scelti campi o tabelle con lo stesso nome temporale ma differenziati da caratteri speciali, ad esempio %, &, <, >, ( e ). Ad esempio, la tabella "XYZ" potrebbe contenere i campi "Campo 1" e "Campo 1%".
>
> Il processore XML accetta solo alcuni caratteri speciali e rimuove quelli che non accetta. Se la rimozione di un carattere speciale, come il segno % in "Campo 1%", genera due o più tabelle o campi con lo stesso nome, si verificherà un errore durante l'esportazione o l'importazione di un pacchetto di configurazione.

## <a name="to-create-a-custom-company-configuration-package"></a>Per creare un pacchetto di configurazione di società personalizzato  
1.  Creare una nuova società. Per ulteriori informazioni, vedere [Creazione di nuove società in Business Central](about-new-company.md).  
3.  Impostare la nuova società nel modo desiderato. Compilare tutte le tabelle di setup necessarie.  
4.  Apre la nuova società.
5. Aprire la pagina **Foglio di lavoro configurazione**.  
6.  Aggiungere al prospetto le tabelle da trasferire a un'altra società. Assegnare le righe del prospetto al pacchetto.  
7.  Creare un questionario per le tabelle di setup utilizzate con maggiore frequenza.  
8.  Creare modelli di configurazione per facilitare la creazione di dati master, ad esempio clienti o articoli.  
9.  Esportare il pacchetto come file con estensione rapidstart.  

## <a name="see-also"></a>Vedere anche  
[Impostazione di una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
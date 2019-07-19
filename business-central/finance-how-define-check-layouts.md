---
title: Specificare il layout di un assegno| Documenti Microsoft
description: È possibile progettare e stampare gli assegni in modi diversi per conformità agli standard.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/24/2019
ms.author: edupont
ms.openlocfilehash: 6ba5b6f0f91e207ec8ffedf5b45003a5787b9e0f
ms.sourcegitcommit: 0854c074b500c3031eaf86fde9d452f93f238081
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2019
ms.locfileid: "1701131"
---
# <a name="select-a-check-layout"></a>Selezionare un layout degli assegni
È possibile progettare i controlli per assicurare la conformità agli standard definiti dalle autorità locali. Le immagini degli assegni possono essere stampati in inglese, francese, o spagnolo.

Gli assegni sono stati progettati per la stampa dei formati di immagine sia degli Stati Uniti che del Canada con formato assegno-matrice- assegno o matrice-matrice-assegno.

## <a name="to-select-a-check-layout"></a>Per selezionare un layout degli assegni
1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Selezioni report C/C bancari** e quindi scegliere il collegamento correlato.
2. Nella pagina **Selez. report - C/C bancario**, nel campo **Utilizzo** selezionare **Assegno**.
3. Selezionare uno dei seguenti ID report:

| ID report | Nome report | Descrizione |
| --- | --- | --- |
| 1401 |Seleziona |Questo è il report predefinito. |
| 10411 |Assegno (Matrice/Matrice/Assegno) |Il report è progettato per stampare gli assegni in formato Matrice/Matrice/Assegno. |
| 10412 |Assegno (Matrice/Assegno/Matrice) |Il report è progettato per stampare gli assegni in formato Matrice/Assegno/Matrice. |
| 10413 |Tre Assegni per pagina |Questo report è progettato per stampare tre assegni su ogni pagina. |

Dopo aver impostato i layout dell'asegno, è possibile stampare assegni nella pagina **Registrazioni pagamenti**. Per ulteriori informazioni, vedere [Utilizzo degli assegni](payables-how-work-checks.md).

Per modificare uno di questi layout degli assegni predefinito, utilizzare l'integrazione Word o RDLC. Per ulteriori informazioni, vedere [Creare e modificare un layout di documento o report personalizzato](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Vedere anche
[Creare e modificare un layout di documento o report personalizzato](ui-how-create-custom-report-layout.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Gestione di conti correnti bancari](bank-manage-bank-accounts.md)   
[Completare i processi di fine periodo](year-how-complete-period-end-processes.md)  
[Utilizzo di [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

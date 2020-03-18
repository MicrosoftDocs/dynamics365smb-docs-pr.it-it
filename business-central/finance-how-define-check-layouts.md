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
ms.date: 02/20/2020
ms.author: edupont
ms.openlocfilehash: df141f15eda20b1c3ce17e12e726f79a20532915
ms.sourcegitcommit: 35552b250b37c97772129d1cb9fd9e2537c83824
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "3097746"
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

Per modificare uno di questi layout degli assegni predefinito, utilizzare l'integrazione Word o RDLC. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Utilizzo dei caratteri MICR e di sicurezza
La versione online di [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene caratteri preinstallati sui server che possono essere utilizzati durante la definizione di layout di controllo. Di seguito vengono indicati i tipi di carattere disponibili con i collegamenti alle informazioni dettagliate di fornitori di terze parti dei caratteri.

> [!Important]
> I caratteri MICR e dei controlli di sicurezza in Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] sono concessi in licenza in un pacchetto di caratteri di IDAutomation.com, Inc. Questi prodotti possono essere utilizzati solo come parte e in connessione con Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].

Nell'aggiornamento 15.3 e successivi, i caratteri Magnetic Ink Character Recognition (MICR) sono installati e disponibili per l'uso. Sono supportati gli standard E-13B e CMC-7. Oltre ai caratteri MICR, sono disponibili caratteri di sicurezza speciali per generare testo, nomi, importi e i simboli di valuta dollaro, euro, sterlina e yen, che sono difficili da manomettere su un assegno stampato.

> [!NOTE]
> Per motivi legali e di sicurezza, non è possibile caricare i caratteri personalizzati nell'ambiente [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="micr-e-13b-specifications"></a>Specifiche MICR E-13B
Di seguito sono riepilogate le specifiche per i caratteri MICR E-13B che possono essere utili per la calibrazione dei caratteri per layout di controllo con specifiche stampanti MICR.

![Specifiche MICR E-13B](media/font_MICR_E-13B_Specifications.png "Specifiche MICR E-13B")

Le specifiche complete dei caratteri MICR E-13B sono disponibili nella documentazione del fornitore qui: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>Specifiche MICR CMC-7
I seguenti caratteri CMC-7 sono disponibili in [!INCLUDE[d365fin](includes/d365fin_md.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
-   IDAutomationCMC7n40

Di seguito sono riepilogate le specifiche per i caratteri MICR CMC-7 che possono essere utili per la calibrazione dei caratteri per layout di controllo con specifiche stampanti MICR.

![Specifiche MICR CMC-7](media/font_MICR_CMC-7_Specifications.png "Specifiche MICR CMC-7")

Le specifiche complete dei caratteri MICR CMC-7 sono disponibili nella documentazione del fornitore qui: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Specifiche dei caratteri di sicurezza
Di seguito sono riepilogate le specifiche per i caratteri dei controlli di sicurezza che possono essere utili per la calibrazione dei caratteri per layout di controllo con specifiche stampanti MICR.

![Specifiche dei caratteri dei controlli di sicurezza](media/font_check-security-font_Specifications.png "Specifiche dei caratteri dei controlli di sicurezza")

Le specifiche complete dei caratteri dei controlli di sicurezza sono disponibili nella documentazione del fornitore qui: (https://www.idautomation.com/security-fonts/).

I caratteri per altri scopi sono disponibili anche in [!INCLUDE[prodshort](includes/prodshort.md)]. Per ulteriori informazioni, vedere [Caratteri disponibili](ui-fonts.md)

## <a name="see-also"></a>Vedere anche
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Caratteri in Business Central](ui-fonts.md)  
[Gestione della contabilità fornitori](payables-manage-payables.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)   
[Completare i processi di fine periodo](year-how-complete-period-end-processes.md)  
[Utilizzo di [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)

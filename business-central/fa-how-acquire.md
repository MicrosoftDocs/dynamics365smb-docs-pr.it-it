---
title: Acquisire cespiti| Documenti Microsoft
description: È possibile impostare un cespite, assegnare un registro beni ammortizzabili e registrare il costo di acquisizione del cespite.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a8aa71492c307ba017b7ec3e2914e5f63e1dbefc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377774"
---
# <a name="acquire-fixed-assets"></a>Acquisire i cespiti
Per ogni cespite occorre impostare una scheda che ne riporti le relative informazioni. È possibile impostare edifici o attrezzature di produzione come bene principale con un elenco di componenti ed è possibile raggrupparli in vari modi, ad esempio per classe, reparto o ubicazione. Un registro beni ammortizzabili deve essere impostato e assegnato a ogni cespite prima di poterlo acquisire.

Quando un cespite è impostato e un registro beni ammortizzabili è assegnato, è necessario acquisire il cespite. Per acquisire un cespite, occorre registrare il costo di acquisizione nel relativo conto C/G, conto bancario o fornitore registrando una transazione di acquisizione dalla pagina **Registrazioni cespiti in C/G**. È possibile utilizzare la pagina **Acquisizione assistita cespiti** per creare e registrare le righe registrazioni COGE richieste automaticamente.

Il valore residuo di un cespite quando non può più essere utilizzato. È possibile registrare il valore di realizzo contemporaneamente alla registrazione del costo di acquisto. Per ulteriori informazioni, vedere [Ammortamento dei cespiti](fa-how-depreciate-amortize.md).

L'indicizzazione consente di correggere i valori per le modifiche generali a livello di prezzo. Il processo batch **Indice cespiti** consente di calcolare i costi di acquisto ai costi di sostituzione.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Per creare un cespite e acquisirlo automaticamente
Di seguito viene descritto come creare e acquisire un cespite utilizzando la pagina **Acquisizione assistita cespiti** per creare e registrare le righe registrazioni cespiti in C/G richieste. È inoltre possibile creare e registrare manualmente le righe di registrazione. Per ulteriori informazioni, vedere [Per registrare un'acquisizione di cespite manualmente con Registrazioni cespiti in C/G](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.  
2. Scegliere l'azione **Nuovo** e compilare i campi necessari della Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nella Scheda dettaglio **Registro beni ammortizzabili** compilare i campi secondo le necessità. In questo passaggio viene assegnato un registro beni ammortizzabili al cespite.  
4. Se è necessario assegnare più di un registro beni ammortizzabili al cespite, scegliere l'azione **Aggiungi più registri beni ammortizzabili**. Per ulteriori informazioni, vedere [Per assegnare un registro dei beni ammortizzabili a un cespite](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Quando tutti i campi necessari per acquisire un cespite vengono compilati, la notifica indicante che **si è pronti ad acquisire il cespite** viene visualizzata nella parte superiore della pagina.
5. Scegliere l'azione **Acquisisci** nella notifica.
6. Seguire i passaggi indicati nella pagina **Acquisizione assistita cespiti** per completare l'acquisizione automatica del cespite.

> [!NOTE]  
>   È inoltre possibile registrare i costi di acquisizione in Avere. In tal caso, ricordare che il valore nel campo **Costo di acquisizione IVA inclusa** deve avere il segno meno per indicare un credito.

Quando si sceglie **Fine**, il campo **Valore contabile** nella pagina **Scheda cespite** viene compilato per indicare che il cespite è stato acquisito al costo di acquisizione specificato.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Per impostare una lista di componenti per un bene principale
I cespiti possono essere raggruppati in beni principali e componenti. Un esempio è costituito da un macchinario di produzione composto da molte parti che si intendono raggruppare come segue.  

il bene principale e tutti i suoi componenti devono essere impostati come schede cespiti individuali. In seguito all'impostazione di una lista componenti, i campi **Bene Principale/Componente** e **Componenti di bene principale** nelle schede cespiti vengono compilati automaticamente da [!INCLUDE[prod_short](includes/prod_short.md)].

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Cespiti** e quindi scegliere il collegamento correlato.
2. Selezionare il cespite che costituisce il bene principale, quindi scegliere l'azione **Componenti bene principale**.
3. Nella pagina **Componenti bene principale** scegliere il campo **Nr. cespite**, quindi selezionare il cespite che si desidera aggiungere come componente del bene principale.
4. Chiudere la pagina.
5. Ripetere i passaggi 3 e 4 per ogni bene componente che si intende aggiungere.
6. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Setup cespiti** e quindi scegliere il collegamento correlato.
7. Selezionare la casella di controllo **Autorizza reg. in cespiti principali**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Per registrare manualmente un'acquisizione del cespite mediante Registrazioni cespiti in C/G
Di seguito viene descritto come acquistare manualmente un cespite creando e registrando le righe nella pagina **Reg. cespiti in G/L**. È inoltre possibile acquisire automaticamente un cespite utilizzando la pagina **Acquisizione assistita cespiti**. Per ulteriori informazioni, vedere il passaggio 5 in [Per creare un cespite e acquisirlo automaticamente](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   È inoltre possibile registrare i costi di acquisizione in Avere. In tal caso, ricordare che il valore nel campo **Importo** deve avere il segno meno per indicare un credito.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni cespiti in C/G** e quindi scegliere il collegamento correlato.
2. Nella pagina **Registrazioni cespiti in C/G**, nel campo **Tipo reg. cespite** selezionare **Costo di acquisto**.
3. Compilare i rimanenti campi, se necessario.
4. Scegliere l'azione **Registra**.  

> [!TIP]  
>   Se durante la registrazione di un costo di acquisto viene compilato il campo **Nr. Assicurazione**, il costo di acquisizione del cespite verrà registrato automaticamente da [!INCLUDE[prod_short](includes/prod_short.md)] nel registro di copertura assicurativa. Per ulteriori informazioni, vedere [Assicurazione di cespiti](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Per annullare una registrazione di costo di acquisto per un cespite
In caso di errore nella registrazione di un costo di acquisto, è possibile rimuovere il movimento con il processo batch **Rimuovi mov. cespiti** e registrare il movimento di acquisto corretto. I movimenti errati vengono trasferiti alla pagina **Mov. cont. cespiti errati**.

Ad esempio, se si registra un acquisto con la data errata, è necessario correggerla prontamente perché la data di registrazione del cespite viene utilizzata in diversi calcoli critici.

> [!IMPORTANT]  
>   Non è possibile utilizzare la funzione **Storno** per i movimenti di cespiti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Rimuovi mov. cespiti** e quindi scegliere il collegamento correlato.
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Scegliere **OK** per eseguire il processo batch.
4. Quando il movimento o i movimenti errati vengono annullati, continuare con la registrazione del costo di acquisto corretto.

Per annullare i movimenti contabili per più cespiti alla volta, utilizzare il processo batch **Annulla mov. contabili cespiti**.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Per registrare il valore di realizzo con il costo di acquisto
È possibile registrare il valore di realizzo insieme al costo di acquisto da Registrazioni Cespiti.

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Registrazioni cespiti** e quindi scegliere il collegamento correlato.
2. Nella pagina **Registrazioni cespiti**, creare la linea di acquisizione. Per ulteriori informazioni, vedere [Per registrare un'acquisizione di cespite manualmente con Registrazioni cespiti in C/G](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Immettere l'importo del valore di realizzo come avere (con il segno meno) nel campo **Valore di realizzo** nella riga di registrazione.
4. Scegliere l'azione **Registra**.

> [!NOTE]
> Se esiste un valore di recupero per un cespite, tale valore verrà utilizzato nella registrazione dell'ammortamento nel campo **Valore contabile finale** della pagina **Registro beni amm. cespiti**. Per ulteriori informazioni, vedere [Per gestire il valore contabile finale](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Vedere anche
[Cespiti](fa-manage.md)  
[Impostazione di cespiti](fa-setup.md)  
[Finanze](finance.md)  
[Introduzione](product-get-started.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
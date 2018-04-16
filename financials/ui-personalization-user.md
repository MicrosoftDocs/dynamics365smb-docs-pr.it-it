---
title: Personalizzazione delle pagine in Financials | Documenti Microsoft
description: Informazioni su come personalizzare l'interfaccia utente in base alle esigenze professionali.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: daf2a1349cc3e12e634324082d4e6507c5b312be
ms.contentlocale: it-it
ms.lasthandoff: 03/22/2018

---
# <a name="personalizing-your-workspace"></a>Personalizzazione dell'area di lavoro
<!--NAV in the Web client-->
È possibile *personalizzare* l'area di lavoro per adattarla alle esigenze professionali e alle preferenze modificando le pagine in modo da visualizzare solo le informazioni necessarie, quando necessario. Le modifiche di personalizzazione apportate influenzeranno solo ciò che vede l'utente che le ha effettuate, non quello che altri utenti vedono.

A seconda del tipo di pagina e del contenuto, è possibile:

-   Aggiungere, spostare e rimuovere i campi.
-   Aggiungere, spostare e rimuovere le colonne in un elenco.
-   Modificare il riquadro di blocco delle colonne in un elenco. Il riquadro blocca una o più colonne a sinistra di un elenco in modo che siano sempre presenti, anche quando si scorre orizzontalmente.
-   Spostare ed eliminare le pile (riquadri).
-   Spostare e rimuovere le parti. Le parti sono suddivisioni o aree in una pagina che contengono elementi quali più campi, un'altra pagina, un grafico o dei riquadri.  

## <a name="to-personalize-a-page"></a>Per personalizzare una pagina

1. Nell'angolo in alto a destra, selezionare l'icona ![Impostazioni](media/ui-experience/settings_icon_small.png "icona Impostazioni per Gestione ruolo utente") e quindi **Personalizza**.

    Viene visualizzato il banner **Personalizzazione** in alto per indicare che è possibile iniziare ad apportare le modifiche.

    ![Modalità di personalizzazione](media/ui_personalize_mode_small.png "Modalità di personalizzazione")

2. Andare alla pagina da personalizzare.

   Se è visualizzata un'icona di blocco sul banner, per ulteriori informazioni vedere [Perché la pagina è bloccata](ui-personalization-locked.md).

3. Specificare un'area che si desidera personalizzare, ad esempio un'intestazione di colonna o campo in un elenco. Tutti gli elementi che è possibile personalizzare vengono immediatamente evidenziati con una freccia o un bordo.
   <!--
   -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
   -   If the component is a part, the extent of the part is indicated by a border.
   -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
   -->

4. Utilizzare questa tabella per agevolare le modifiche:     <table>
       <tr><th>Operazione da eseguire</td><th>Procedura</th></tr>
       <tr><td>Spostare valori, come un campo, una colonna dell'elenco, un riquadro o una parte</td><td> Fare clic in un punto qualsiasi dell'elemento che si desidera spostare e trascinarlo nella nuova posizione. La posizione è indicata da una spessa linea orizzontale o verticale.</td></tr>
       <tr><td>Rimuovere un elemento</td><td>Selezionare la freccia e scegliere <b>Rimuovi</b>. </td></tr>
       <tr><td>Aggiungere un campo o una colonna</td><td>Nel banner <b>Personalizzazione</b> scegliere <b>Altro</b> quindi scegliere <b>Campo</b>.<br /></br>Si apre a destra il riquadro <b>Aggiungi campo a pagina</b>. Elenca i campi che possono essere aggiunti nella pagina. I campi contrassegnati come <b>posizionati</b> sono già nella pagina. I campi contrassegnati come <b>pronti</b> non sono già nella pagina.<br /></br>Per aggiungere un campo, trascinarlo dal riquadro alla posizione che si desidera. La posizione è indicata da una spessa linea orizzontale o verticale.</td></tr>
       <tr><td>Modificare il riquadro di blocco di un elenco in un'altra colonna</td><td>Selezionare la freccia della colonna che si desidera come ultima colonna del riquadro di blocco, quindi scegliere <b>Imposta Blocca riquadro</b>.<br /><br/>Se si desidera impostare il riquadro di blocco di nuovo sulla posizione originale, selezionare la freccia per la colonna corrente del blocco e scegliere <b>Cancella Blocca riquadro</b>. Nota: non è possibile rimuovere il riquadro di blocco.</td></tr>
     </table>

   > [!IMPORTANT]  
   >   Non è possibile apportare modifiche a un elenco se viene visualizzato come riquadro. È necessario innanzitutto passare alla vista elenco selezionando l'icona ![Mostra come lista](media/ui_show_as_list_icon.png "Freccia sinistra Mostra come lista").

5. È possibile continuare a modificare la stessa pagina o passare a un'altra pagina. Le modifiche vengono salvate automaticamente mentre le si apporta. Al termine, nel banner **Personalizzazione**, scegliere **Chiudi**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Annullare la personalizzazione per modificare una pagina e ripristinare il layout originale
In alcuni casi, potrebbe essere necessario annullare tutte le modifiche di personalizzazione effettuate nel tempo in una pagina per tornare all'aspetto della pagina in origine. Per effettuare questa operazione, nel banner **Personalizzazione** scegliere **Altro** e quindi **Cancella personalizzazione**.

## <a name="personalization-in-detail"></a>Personalizzazione in dettaglio
Per agevolare la comprensione della personalizzazione, di seguito sono elencati alcuni puntatori.  
-   Quando si apportano modifiche a una pagina schede avviata da un elenco, le modifiche diventeranno effettive in tutti i record a cui si accede dalla lista. Ad esempio, si apre un cliente specifico da una pagina elenco Clienti e quindi si personalizza la pagina aggiungendo un campo. Quando si aprono altri clienti dall'elenco, il campo aggiunto verrà visualizzato anche per questi clienti.
-   Le modifiche effettuate diventeranno effettive in tutte le Gestioni ruolo utente. Ad esempio, se si effettua una modifica all'elenco Cliente quando la Gestione ruolo utente è impostata su Manager aziendale, le modifiche verranno visualizzate anche nell'elenco cliente quando Gestione ruolo utente è impostata su Gestore ordini vendite.
-   Le modifiche a una pagina in un riquadro diventeranno effettive nella pagina ovunque viene visualizzata.  
-   È possibile aggiungere solo i campi e le colonne da una lista predefinita, che è basata sulla pagina. Non è possibile creare nuovi campi.

## <a name="see-also"></a>Vedi anche
[Gestione della personalizzazione](ui-personalization-manage.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modifica delle impostazioni di base](ui-change-basic-settings.md)  
[Personalizzazione dell'esperienza [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  


---
title: Impostare i dipendenti e modificare le informazioni
description: Descrive come utilizzare la funzionalità Risorse umane per registrare nuovo personale o modificare le informazioni sui dipendenti per il personale esistente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personnel, people, employee, staff, HR
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9f25ea61c41bfeb08b9283153a96b8a78ce7c9b7
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589284"
---
# <a name="register-employees"></a>Registrare i dipendenti
Per utilizzare la funzionalità Human Resources, devi prima aggiungere ogni dipendente compilando i campi nella pagina **Scheda dipendente** .

## <a name="adding-new-customers"></a>Aggiunta di nuovi clienti
Puoi aggiungere nuovi dipendenti manualmente, compilando i campi nella pagina **Scheda del dipendente**, oppure puoi usare dei modelli che contengono informazioni predefinite. Per esempio, è possibile creare un modello per diversi tipi di profili di dipendenti. L'uso di modelli fa risparmiare tempo quando si aggiungono nuovi dipendenti e aiuta a garantire che le informazioni siano corrette ogni volta. Se si creano modelli per più di un tipo di dipendente, è possibile scegliere il modello da utilizzare quando si aggiunge un dipendente. Se si crea un solo modello, questo sarà usato per tutti i nuovi dipendenti. Dopo aver creato un modello, si può usare l'azione **Applica modello** per applicarlo a uno o più dipendenti selezionati. Per creare un modello, si compilano le informazioni che si vogliono riutilizzare nella pagina della Scheda del dipendente, e poi si salva come modello.

> [!TIP]
> Può essere utile personalizzare la pagina **Modello dipendente** quando si crea un modello. Per esempio, potresti voler aggiungere un campo che non è già visualizzato nella pagina. Per ulteriori informazioni, vedi [Personalizzare lo spazio di lavoro](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

I dettagli di un impiegato possono essere modificati in qualsiasi momento. Mantenere aggiornati i registri dei dipendenti può semplificare i compiti relativi al personale. Per esempio, se l'indirizzo di un dipendente cambia, lo si registra nella pagina Scheda dipendente.

> [!NOTE]  
> È possibile rimborsare ai dipendenti le spese che hanno sostenuto durante le attività di lavoro. A questo scopo è necessario compilare i campi nella Scheda dettaglio **Pagamenti** nella pagina **Scheda impiegato**. Per altre informazioni, vedere [Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md).

## <a name="to-set-up-an-employee"></a>Per impostare un impiegato
1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dipendenti**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda impiegato** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-a-picture-of-an-employee"></a>Per inserire una foto di un impiegato
Se hai una foto di un dipendente, puoi inserirla nella scheda del dipendente.

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dipendenti**, quindi scegli il collegamento correlato.
2. Aprire la scheda dell'impiegato pertinente.
3. Nel riquadro Dettaglio informazioni **Immagine impiegato** scegliere il pulsante a discesa, quindi **Importa**.
4. Nella pagina **Selezionare un'immagine da caricare** scegliere il pulsante **Scegli**.
5. Selezionare il file quindi scegliere **Apri**.

L'immagine viene inserita nel riquadro Dettaglio informazioni **Immagine impiegato**.

## <a name="to-register-various-information-about-an-employee"></a>Per registrare varie informazioni relative a un dipendente
Nella scheda del dipendente, è possibile impostare informazioni, quali la tessera di sindacato, i parenti e in contratti dell'impiegato. Di seguito viene descritto come impostare un indirizzo alternativo. I passaggi sono simili per tutte le altre informazioni che è possibile impostare in una scheda relativa all'impiegato.

È possibile utilizzare gli indirizzi alternativi per tenere traccia delle località di domicilio degli impiegati, per esempio in caso di trasferta all'estero, di lunghi viaggi di lavoro oppure in caso di soggiorno in una residenza estiva.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Dipendenti**, quindi scegli il collegamento correlato.
2. Apri la scheda dell'impiegato pertinente.
3. Scegliere l'azione **Indirizzi alternativi**.
4. Nella pagina **Lista indirizzi alternativi** compilare i campi in base alle esigenze.
5. Ripetere il passaggio 4 per ogni indirizzo alternativo.

## <a name="see-also"></a>Vedi anche
[Registrare e rimborsare le spese dei dipendenti](finance-how-record-reimburse-employee-expenses.md)  
[Finanze](finance.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
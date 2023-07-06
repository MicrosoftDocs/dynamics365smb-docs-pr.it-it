---
title: Inizio rapido su Informazioni finanziarie
description: Prepara la tua azienda per il business impostando le informazioni finanziarie in Business Central.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a>Inizio rapido su Informazioni finanziarie

Dopo aver inserito le informazioni società di base in [!INCLUDE[prod_short](includes/prod_short.md)], uno dei passaggi successivi è il completamento della sezione finanziaria. Lo fai non solo per ricevere o effettuare pagamenti, ma anche per gestire e segnalare correttamente i numeri della tua attività.

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Il piano dei conti

Il piano dei conti (COA) offre una panoramica delle finanze dell'azienda, elencando i conti in gruppi strutturati come attività, passività, reddito, costo del venduto e spese. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard da personalizzare pronto per le procedure contabili aziendali.

## <a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a>Impostare un piano dei conti

Il seguente video mostra come impostare i piani dei conti in [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a>Aggiungi un account al piano dei conti

Per aggiungere un account non incluso per impostazione predefinita in [!INCLUDE[prod_short](includes/prod_short.md)], ad esempio, servizi di giardinaggio, basta seguire questi passaggi:

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Piano dei conti**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo** per aprire la pagina **Scheda conto C/G**.
3. Immettere i seguenti dati nei campi corrispondenti nella Scheda dettaglio **Generale**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Campo | Dati |
   | --- | --- |
   | **Nr.** | 61250 |
   | **Nome** | Servizi di giardinaggio |
   | **Economico/Patrimoniale** | Conto economico |
   | **Categoria conto** | Spese |
   | **Sottocategoria conto** | Spese riparazioni e manutenzione |
   | **Dare/Avere** | Entrambi |
   | **Tipo conto** | Registrazione |

4. Nella Scheda dettaglio **Registrazione** inserire i seguenti dati:

   | Campo | Dati |
   | --- | --- |
   | **Tipo reg. gen.** | Acquisti |
   | **Cat. Reg. Business** | Nazionale |
   | **Cat. Reg. Articolo/Servizio** | Servizi |

5. Compila i campi rimanenti nella pagina **Scheda contoC/G** secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a>Ottieni una panoramica del piano dei conti

Se è necessaria una visualizzazione più compatta del piano dei conti, senza colonne per gruppi di registrazione, tipo di registrazione o tipo di costo, ad esempio, **Panoramica del piano dei conti** elenca le informazioni principali per ciascun account in una tabella più piccola. Inoltre, puoi comprimere o espandere i gruppi per nascondere gli account al loro interno.

Per visualizzare la panoramica, scegli l'azione **Panoramica del piano dei conti** nella pagina **Piano dei conti** o cerca la funzione utilizzando ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare").

Ulteriori informazioni sul piano dei conti e sulla contabilità generale a [Comprensione della contabilità generale e del piano dei conti](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a>Impostare i conti correnti bancari

Conti bancari in [!INCLUDE[prod_short](includes/prod_short.md)] registrano le transazioni bancarie e sono associate a registrazioni nel piano dei conti. Il seguente video mostra come impostare i conti bancari.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Scegli la ![lampadina che apre la funzione Dimmi 1.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **C/C bancari**, quindi scegli il collegamento correlato.
2. Nella pagina **C/C bancari** scegliere l'azione **Nuovo**.
3. Nel campo **Nr.** campo, un identificatore come *B010* verrà inserito automaticamente se è stato impostato un elenco di serie numerate per i conti bancari. In caso contrario, immettere una combinazione univoca.

   Il campo è diverso dal campo **Nr. conto bancario** disponibile anche nella Scheda dettaglio **Generale**.
4. Compila i campi nella pagina **Scheda C/C bancari fornitori** secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Vedi le informazioni relative al training in [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Impostare un piano dei conti](finance-setup-chart-accounts.md)  
[Impostare i conti correnti bancari](bank-how-setup-bank-accounts.md)  
[Eseguire e stampare i report](ui-work-report.md)  
[Avviamento rapido di Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

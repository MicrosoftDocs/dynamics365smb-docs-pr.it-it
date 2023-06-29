---
title: 'Fatturazione elettronica [FatturaPA]'
description: Business Central supporta FatturaPA in modo da poter esportare fatture di vendita e note di credito come documenti elettronici secondo le regole italiane.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
---
# <a name="electronic-invoicing-fatturapa-in-the-italian-version"></a><a name="electronic-invoicing-fatturapa-in-the-italian-version"></a>Fatturazione Elettronica (FatturaPA) nella versione italiana

Questo articolo fornisce informazioni utili per iniziare a utilizzare la fatturazione elettronica per l'Italia in [!INCLUDE[prod_short](../../includes/prod_short.md)].
La fattura elettronica in Italia si chiama FatturaPA. **FatturaPA** significa **Fatturazione Elettronica verso la Pubblica Amministrazione** e tradotto significa: "Fatturazione elettronica alla pubblica amministrazione". Il termine comprende tutte le misure tecniche e organizzative per la fatturazione elettronica alla pubblica amministrazione. Le autorità accettano fatture elettroniche solo tramite la piattaforma Sistema di Interscambio (SDI), che è il sistema di scambio ufficiale.

## <a name="to-set-up-electronic-invoicing"></a><a name="to-set-up-electronic-invoicing"></a>Per configurare la fatturazione elettronica

1. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup fattura**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup fattura**, nella Scheda dettaglio **Generale**, nel campo **Gruppo business IVA fatturazione automatica**, specifica la **Categoria di registrazione business IVA** utilizzata per i movimenti IVA relativi ai documenti di autofatturazione.
3. Nel campo **Codice società PA**, specifica il codice da riportare nel nodo **CodiceDestinatario XML** per i documenti di fatturazione automatica.
4. Scegli la ![lampadina che apre la funzione Dimmi.](../../media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Lista tipi di documento Fattura**, quindi scegli il relativo collegamento.  
5. Creare i diversi tipi di documenti elettronici utilizzando le seguenti colonne:

   |Campo|Descrizione|  
   |------------------------------------|---------------------------------------|
   |**Nr.**| Specifica il codice del tipo di documento che verrà esportato nel file XML.|
   |**Descrizione**|Specifica una descrizione del tipo di documento. È possibile immettere un massimo di 250 caratteri, tra numeri e lettere.|
   |**Fattura**|Specifica il tipo di documento che rappresenta l'impostazione predefinita per le fatture.|
   |**Nota credito**|Specifica il tipo di documento che rappresenta l'impostazione predefinita per le note di credito.|
   |**Autofattura**|Specifica il tipo di documento che rappresenta l'impostazione predefinita per i documenti con autofattura.|
   |**Pagamento anticipato**|Specifica il tipo di documento che rappresenta l'impostazione predefinita per i pagamenti anticipati.|

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

## <a name="see-also"></a><a name="see-also"></a>Vedi anche

[Funzionalità locale per l'Italia](italy-local-functionality.md)

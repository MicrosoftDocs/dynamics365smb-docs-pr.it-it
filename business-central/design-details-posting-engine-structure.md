---
title: Dettagli di progettazione - Struttura del motore di registrazione
description: L'interfaccia di registrazione utilizza le funzioni del motore di registrazione per preparare e inserire record di movimenti di contabilità generale e IVA.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-posting-engine-structure" />Dettagli di progettazione: struttura del motore di registrazione
L'interfaccia di registrazione e alcune altre funzioni nella codeunit 12 utilizzare le funzioni del motore di registrazione e inseriscono record di movimenti di contabilità generale e IVA. Il motore di registrazione è inoltre responsabile della creazione del registro di contabilità generale.  
  
 Le funzioni nella seguente tabella forniscono una struttura standard per progettare le procedure di registrazione (ad esempio, Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry e Reverse) e l'accesso esclusivo alla tabella 17, movimenti C/G.  
  
|Ciclo|Description|  
|-------------|---------------------------------------|  
|StartPosting|Inizializza il buffer di registrazione TempGLEntryBuf, blocca le tabelle dei movimenti IVA e C/G e inizializza il periodo contabile, il registro C/G e il tasso di cambio. Se viene chiamato una sola volta, NextEntryNo è 0.|  
|ContinuePosting|Controlla e registra l''IVA ad esigibilità differita dell'incremento NextTransactionNo della transazione precedente e prepara la registrazione della riga successiva.|  
|FinishPosting|Completa la registrazione inserendo i movimenti di C/G dal buffer temporaneo nella tabella di database. Utilizzato sempre insieme a StartPosting. Verifica la presenza di incoerenze.|  
|InitGLEntry|Utilizzato per inizializzare nuovo movimento C/G per riga di registrazioni generali. Restituisce GLEntry come parametro.|  
|InitGLEntryVAT|Uguale a InitGLEntry, ma assegna anche contropartita e SummarizeVAT.|  
|InitGLEntryVATCopy|Simile a InitGLEntryVAT, ma copia anche i dati delle categorie di registrazione dal movimento IVA prima di SummarizeVAT.|  
|InsertGLEntry|L'unica funzione che inserisce movimenti C/G nella tabella globale di TempGLEntryBuf. Utilizzare sempre questa funzione per l'inserimento.|  
|CreateGLEntry|Esegue un InitGLEntry, assegna Importo in valuta addiz. ed esegue InsertGLEntry. Sostituisce molte righe di codice a una singola chiamata di funzione.|  
|CreateGLEntryBalAcc|Uguale a CreateGLEntry, ma assegna anche Tipo contropartita e Contropartita.|  
|CreateGLEntryVAT|Uguale a CreateGLEntry, ma con elaborazione addizionale delle categorie di registrazione e salvataggio nel buffer temporaneo IVA:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Uguale a CreateGLEntry, ma con raccolta addizionale di rettifiche e salvataggio nel buffer temporaneo IVA:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Uguale a CreateGLEntry, ma copia anche le categorie di registrazione dal movimento IVA.|  
  
## <a name="see-also" />Vedi anche
 [Dettagli di progettazione: Struttura dell'interfaccia di registrazione](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Trasferimento e registrazione di movimenti di costi
description: 'Prima di definire le allocazioni costi, è necessario comprendere le varie origini dei movimenti di costi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Trasferimento e registrazione di movimenti di costi

Prima di definire le allocazioni costi, è necessario comprendere come i movimenti di costi derivino dalle origini seguenti:  

- Trasferimento automatico dei movimenti C/G.  
- Registrazione manuale dei costi per i movimenti di costi puri, spese interne e allocazioni manuali.  
- Registrazioni automatiche delle allocazioni per i costi effettivi.  
- Trasferimento dei movimenti budget in costi effettivi.

## Criteri per trasferire movimenti C/G ai movimenti di costi

È importante comprendere i criteri per trasferire i movimenti C/G nei movimenti di costi. Durante il trasferimento, il processo batch **Trasferisci movimenti C/G a CA** utilizza i seguenti criteri per determinare se e come i movimenti C/G vengono trasferiti.  

I movimenti C/G vengono trasferiti nei seguenti casi:  

- Ai movimenti sono associati valori dimensioni che corrispondono a un centro di costo o un oggetto di costo.  
- Ai movimenti sono associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo. Per questi movimenti, il centro di costo ha la precedenza. Questo consente di evitare una situazione in cui un tipo di costo viene visualizzato sia in un oggetto di costo sia in un centro di costo, venendo pertanto conteggiato due volte nelle statistiche.  
- Il numero di documento nei movimenti è vuoto, pertanto verrà visualizzato con un numero di documento pari a 0000 nei movimenti di costo.  
- I movimenti vengono trasferiti in un tipo di costo che consente movimenti combinati e tali movimenti vengono trasferiti come movimento combinato mensilmente o giornalmente.  

I movimenti C/G non vengono trasferiti nei seguenti casi:  

- Ai movimenti sono associati valori dimensioni che non corrispondono a un centro di costo o un oggetto di costo.  
- Ai movimenti è associato un importo pari a zero.  
- Ai movimenti è associato un conto di contabilità generale che è stato eliminato.  
- Ai movimenti è associato un conto di contabilità generale che non è di tipo **Conto economico**.  
- Ai movimenti è associato un conto di contabilità generale a cui non è assegnato un tipo di costo.  
- I movimenti hanno una data di registrazione anteriore alla **Data inizio per trasferimento CG**.  
- Registrazione dei movimenti con data chiusura completata. Si tratta in genere di movimenti che reimpostano il saldo del conto economico alla fine dell'anno.

## Trasferire movimenti C/G ai movimenti di costi

I movimenti C/G possono essere trasferiti ai movimenti di costi.  

Prima di eseguire il processo per il trasferimento dei movimenti C/G ai movimenti di costi, è necessario preparare il trasferimento per evitare la registrazione manuale della correzione.  

### Per preparare il trasferimento  

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup contabilità industriale**, quindi scegli il collegamento correlato.  
2.  Nella pagina **Setup contabilità industriale** controllare che il campo **Data inizio per trasferimento C/G** sia impostato sul valore corretto.  
3.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei tipi di costo**, quindi scegli il collegamento correlato.  
4.  Nella pagina **Scheda tipo costo** verificare che il campo **Intervallo conti C/G** sia collegato correttamente per ogni tipo di costo per prelevare i movimenti dalla contabilità generale.  
5.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Piano dei conti**, quindi scegli il collegamento correlato.  
6.  Per ogni conto di contabilità generale pertinente, nella pagina **Scheda conto C/G** verificare che il campo **Nr. tipo di costo** sia collegato correttamente a un tipo di costo. Per ulteriori informazioni, vedere [Impostazione della contabilità industriale](finance-set-up-cost-accounting.md).  
7.  Verificare che a tutti i relativi movimenti C/G siano associati valori dimensioni che corrispondono a un centro di costo e a un oggetto di costo.  

### Per trasferire movimenti C/G a movimenti di costi

1.  Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Trasferisci movimenti C/G a CA**, quindi scegli il collegamento correlato.  
2.  Scegliere **Sì** per avviare il trasferimento. Con il processo vengono trasferiti tutti i movimenti C/G che non sono già stati trasferiti.  

Durante il trasferimento, con il processo vengono creati collegamenti nei movimenti nella tabella **Movimento di costo** e nella tabella **Registro costi**. In questo modo è possibile analizzare l'origine dei movimenti di costi.

## Trasferimento automatico e movimenti combinati

Nella contabilità industriale, è possibile trasferire i movimenti C/G in un tipo di costo utilizzando una registrazione combinata. È possibile specificare se il tipo di costo riceve i movimenti combinati nel campo **Cumula movimenti** nella definizione del tipo di costo. Nella seguente tabella vengono illustrate le diverse opzioni.  

|Cumula movimenti|Description|  
|---------------------|-----------------|  
|Nessuno|Ogni movimento C/G viene trasferito singolarmente al tipo di costo corrispondente.|  
|Giorno|I movimenti C/G con la stessa data di registrazione vengono trasferiti come un unico movimento nel tipo di costo corrispondente.|  
|Mese|Tutti i movimenti C/G dello stesso mese di calendario vengono trasferiti come un unico movimento nel tipo di costo corrispondente.|  

> [!IMPORTANT]  
>  Se si è selezionata la casella di controllo **Trasferimento automatico da CG** nella pagina **Setup contabilità industriale**, [!INCLUDE[prod_short](includes/prod_short.md)] aggiorna la contabilità dopo ogni registrazione nella contabilità generale. Le entità combinate non sono possibili.

## Risultati del trasferimento di movimenti C/G a movimenti di costi

Durante il trasferimento dei movimenti C/G ai movimenti di costo, in [!INCLUDE[prod_short](includes/prod_short.md)] vengono creati i collegamenti nei movimenti nelle tabelle **Movimento CG**, **Movimento di costo** e **Registro costi** per consentire di tenere traccia dei collegamenti tra i movimenti di costo e i movimenti C/G.  

### Movimenti C/G

Per ogni movimento C/G che viene trasferito alla contabilità industriale, in [!INCLUDE[prod_short](includes/prod_short.md)] viene compilato il campo **Nr. movimento** dei costi.  

### Movimenti di costi

Per ogni movimento di costo, [!INCLUDE[prod_short](includes/prod_short.md)] salva il numero del movimento C/G corrispondente nel campo **Nr. movimento C/G** della tabella **Movimento di costo**.  

Per i movimenti di costi combinati, in [!INCLUDE[prod_short](includes/prod_short.md)] viene salvato il numero dell'ultimo movimento C/G, vale a dire il movimento con il numero più alto.  

Nel campo **Conto C/G** della tabella **Movimento di costo** è contenuto il numero del conto di contabilità generale da cui deriva il movimento di costo.  

Per i singoli movimenti di costo, in [!INCLUDE[prod_short](includes/prod_short.md)] viene trasferito il testo della registrazione dal movimento C/G al campo di testo **Descrizione**. Per i movimenti combinati, il campo di testo mostra che questi movimenti vengono trasferiti come movimenti combinati. Ad esempio, per un movimento combinato per il mese di ottobre 2013, il testo può essere **Movimenti combinati, ottobre 2013**.  

### Registro costi

Nella tabella **Registro costi**, [!INCLUDE[prod_short](includes/prod_short.md)] crea un movimento con il trasferimento di origine dalla contabilità generale. Il movimento registra il primo e l'ultimo numero dei movimenti C/G trasferiti, oltre al primo e all'ultimo numero dei movimenti di costo creati.

## Vedere anche

 [Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)  
 [Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)  
 [Definizione e allocazione dei costi](finance-define-and-allocate-costs.md)  
 [Contabilizzazione dei costi](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

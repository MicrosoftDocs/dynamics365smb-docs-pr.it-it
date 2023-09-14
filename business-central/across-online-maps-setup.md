---
title: Impostare le mappe online
description: Scopri come configurare Business Central per offrire indicazioni stradali e informazioni sulla posizione con un servizio di mappe online.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.form: '800, 804'
ms.date: 07/15/2022
ms.author: bholtorf
---
# <a name="set-up-online-maps"></a>Impostare le mappe online

Quando si pianifica una visita a un indirizzo salvato su una scheda, ad esempio a un cliente oppure a un fornitore, è possibile ottenere una mappa da un servizio di mappa in linea in cui le direzioni del percorso sono indicate nella lingua selezionata dall'utente. Per assicurarsi che tale servizio possa individuare la mappa e le direzioni corrette, è necessario impostarlo in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-online-map-feature"></a>Impostare la funzionalità delle mappe online

1. Scegli la ![lampadina che apre la funzione Dimmi 1](media/ui-search/search_small.png "Dimmi cosa vuoi fare"). immetti **Setup mappa in linea**, quindi scegli il collegamento correlato.
2. Nella pagina **Setup mappa in linea** compila i campi. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Abilita l'interruttore **Abilitato**.

### <a name="customize-the-online-map-provider-features"></a>Personalizza le funzionalità del provider di mappe online

Per personalizzare la funzione della mappa online oltre alle opzioni elencate nella pagina **Setup mappa in linea** o per utilizzare un provider di mappe diverso, attieniti alla seguente procedura:

1. Nella pagina **Setup mappa in linea**, seleziona l'azione **Setup parametro**.
2. Nella pagina **Setup parametro mappa in linea**, seleziona l'azione **Nuovo**.
3. Compila i campi per personalizzare come [!INCLUDE[prod_short](includes/prod_short.md)] genererà gli URL per i servizi disponibili. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
   * Fare riferimento all'elenco **Parametro sostituzione Online Map** nel riquadro **Dettaglio informazioni** per i dati disponibili per generare gli URL.

## <a name="see-also"></a>Vedere anche

[Utilizzare le mappe online per trovare posizioni e indicazioni stradali](across-online-maps.md)  
[Prepararsi a fare affari](ui-get-ready-business.md)  
[Amministrazione](admin-setup-and-administration.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

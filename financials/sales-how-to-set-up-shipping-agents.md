---
title: 'Procedura: Impostare gli spedizionieri | Documenti Microsoft'
description: "È possibile impostare un codice per ciascuno degli spedizionieri di cui si avvale l'azienda e immettere informazioni relative a ognuno di essi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b6ab539048f3f802cc4575e023c43632025dccf5
ms.contentlocale: it-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-shipping-agents"></a>Impostare gli spedizionieri
È possibile impostare un codice per ciascuno degli spedizionieri di cui si avvale l'azienda e immettere informazioni relative a ognuno di essi.  

Se viene immesso l'indirizzo Internet di uno spedizioniere che fornisce servizi per rintracciare colli su Internet, è possibile utilizzare la funzione di tracciabilità automatica dei colli. Per ulteriori informazioni, vedere [Rintracciare i colli](sales-how-track-packages.md).

Quando sugli ordini di vendita vengono impostati i relativi spedizionieri è possibile specificare anche i servizi offerti da ciascuno spedizioniere.  
Per ciascuno di essi è possibile impostare un numero qualsiasi di servizi e per ogni servizio si può impostare il tempo di spedizione.  

Quando a una riga di ordine di vendita viene assegnato un servizio spedizioniere, il tempo di spedizione del servizio sarà compreso nel calcolo della promessa d'ordine relativa a quella riga. Per ulteriori informazioni, vedere [Calcolare le date per la promessa ordine](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Per impostare uno spedizioniere  
1.  Scegliere l'icona ![Cerca pagina o report](media/ui-search/search_small.png "icona Cerca pagina o report"), immettere **Spedizionieri**, quindi scegliere il collegamento correlato.  
2.  Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Scegliere l'azione **Servizi spedizioniere**.
4. In **Servizi spedizioniere** compilare tutti i campi in base alle esigenze.

> [!NOTE]  
>  Se uno spedizioniere viene eliminato dalla riga di ordine, verrà eliminato anche il codice di servizio spedizioniere. Il contenuto di campi parzialmente basato sul servizio spedizioniere verrà ricalcolato.  

## <a name="see-also"></a>Vedi anche
[Rintracciare i colli](sales-how-track-packages.md)    
[Gestione warehouse](warehouse-manage-warehouse.md)  
[Magazzino](inventory-manage-inventory.md)  
[Impostazione gestione warehouse](warehouse-setup-warehouse.md)     
[Gestione assemblaggio](assembly-assemble-items.md)    
[Dettagli di progettazione: Gestione warehouse](design-details-warehouse-management.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

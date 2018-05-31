---
title: Come chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino | Microsoft Docs
description: Utilizzare il campo **Collega da mov.** nella finestra **Registrazioni magazzino** per creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale. Ad esempio, per correggere la transazione in uscita o elaborare il suo reso.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879688bd458714f354b2e98e58ce78686cf79d9
ms.contentlocale: it-ch
ms.lasthandoff: 03/22/2018

---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino
Utilizzare il campo **Collega da mov.** nella finestra **Registrazioni magazzino** per creare un collegamento fisso tra una transazione in entrata e la transazione in uscita originale. Ad esempio, per correggere la transazione in uscita o elaborare il suo reso. Per ulteriori informazioni, vedere Collega da mov.  

> [!IMPORTANT]  
>  I collegamenti fissi creati in questo modo collegano solo il costo, non la quantità. Di conseguenza, il movimento contabile articoli positivo registrato non chiuderà il movimento in uscita collegato e rimarrà aperto. Ciò si applica anche quando si registra un collegamento fisso per un movimento positivo a un movimento negativo che non è stato chiuso da un movimento positivo normale, pertanto sia il movimento positivo che quello negativo rimarranno aperti.  
>   
>  Questo significa inoltre che non è possibile chiudere un periodo di magazzino se esiste tale movimento.  

La seguente procedura illustra come chiudere tali movimenti con due registrazioni correttive nelle registrazioni magazzino.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Per chiudere i movimenti contabili articoli aperti risultanti da un collegamento fisso nelle registrazioni magazzino  

1.  Utilizzare il campo **Collega-da mov.** per registrare una rettifica positiva con la quantità corrispondente. In questo modo si chiude il movimento negativo originale con un collegamento fisso.  
2.  Utilizzare il campo **Collega-da mov.** per registrare una rettifica negativa. In questo modo si chiude il movimento positivo correttivo originale con un collegamento fisso.  

## <a name="see-also"></a>Vedi anche  
[Rimuovere e ricollegare movimenti contabili articolo](finance-how-to-remove-and-reapply-item-entries.md)  
 [Elaborare i resi e gli annullamenti vendite](sales-how-process-sales-returns-cancellations.md)   
 [Impostazione della valutazione magazzino e i costi](finance-set-up-inventory-valuation-and-costing.md)   
 [Gestione dei costi di magazzino](finance-manage-inventory-costs.md)   
 [Dettagli di progettazione: Metodi di costing](design-details-costing-methods.md)

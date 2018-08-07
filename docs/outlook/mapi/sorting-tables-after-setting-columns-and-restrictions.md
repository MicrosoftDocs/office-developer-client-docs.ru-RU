---
title: Сортировка таблиц после установки столбцов и ограничений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812365"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Сортировка таблиц после установки столбцов и ограничений

  
  
**Относится к**: Outlook 
  
Если вам необходимо ограничить представление отсортированный таблицы, всегда следующие **IMAPITable** вызывается в следующем порядке: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) , чтобы наложить ограничение. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) для выполнения сортировки. 
    
Если к категории отсортированный таблице позвоните [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), в случае необходимости после вызова **SortTable** . В этом порядок вызовы важен, поскольку большинство поставщиков услуг отсортируйте таблицы в качестве последней задачи для достижения наилучшей производительности. Если, например поставщика хранилища сообщений необходимо классифицировать таблицу содержимого папки перед ограничение можно накладываемого, данная классификация удаляется во время обработки ограничение. Второй категоризации необходимо. 
  


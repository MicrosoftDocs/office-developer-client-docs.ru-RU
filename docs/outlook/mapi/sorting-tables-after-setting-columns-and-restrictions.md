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
ms.openlocfilehash: 9f975ed1b9036bce5ed225b2a9020262260f4f57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572146"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Сортировка таблиц после установки столбцов и ограничений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Если вам необходимо ограничить представление отсортированный таблицы, всегда следующие **IMAPITable** вызывается в следующем порядке: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) , чтобы наложить ограничение. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) для выполнения сортировки. 
    
Если к категории отсортированный таблице позвоните [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), в случае необходимости после вызова **SortTable** . В этом порядок вызовы важен, поскольку большинство поставщиков услуг отсортируйте таблицы в качестве последней задачи для достижения наилучшей производительности. Если, например поставщика хранилища сообщений необходимо классифицировать таблицу содержимого папки перед ограничение можно накладываемого, данная классификация удаляется во время обработки ограничение. Второй категоризации необходимо. 
  


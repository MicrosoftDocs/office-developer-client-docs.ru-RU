---
title: Определение конца таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420089"
---
# <a name="determining-a-tables-end"></a>Определение конца таблицы

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 Обычной ошибкой является предположить, что конец таблицы был достигнут, когда: 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) был вызван в цикле, а конец цикла определяется количеством строк, возвращенных [IMAPITable::GetRowCount](imapitable-getrowcount.md). Количество, которое **возвращает GetRowCount,** не всегда представляет точное количество строк в таблице; это примерный подсчет. 
    
- **QueryRows** был вызван с фиксированным числом строк и возвращается меньше строк. Только после того, как **QueryRows** возвращает набор строк с количеством строк, равным нулю, не будет больше строк для получения. 
    
> [!IMPORTANT]
> Единственный раз, когда вызываемая может предположить, что курсор находится в конце таблицы для положительного подсчета строк или в начале таблицы для отрицательного счета строк, это когда возвращается значение S_OK и нулевые строки. Значение, MAPI_E_NOT_FOUND никогда не возвращается. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)


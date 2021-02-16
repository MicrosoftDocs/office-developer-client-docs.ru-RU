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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 Распространенная ошибка предполагает, что конец таблицы достигается, когда: 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) был вызван в цикле, где конец цикла определяется количеством строк, возвращенных [IMAPITable::GetRowCount](imapitable-getrowcount.md). Число **возвращаемого GetRowCount** не всегда представляет точное количество строк в таблице; это приблизительное количество. 
    
- **QueryRows** был вызван с фиксированным числом строк, и возвращается меньше строк. Это не будет, пока **QueryRows** не возвращает набор строк со значением 0, что больше нет строк для извлечения. 
    
> [!IMPORTANT]
> Единственный раз, когда звонячая может предположить, что курсор находится в конце таблицы для положительного подсчета строк или в начале таблицы для отрицательного значения, возвращается значение S_OK и ноль строк. Значение, MAPI_E_NOT_FOUND не возвращается. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)


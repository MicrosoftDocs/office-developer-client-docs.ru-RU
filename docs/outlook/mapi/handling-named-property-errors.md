---
title: Обработка ошибок именованных свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 98b6adbc3a31994768a78b389e16eb3a6ece34bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429868"
---
# <a name="handling-named-property-errors"></a>Обработка ошибок именованных свойств
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
При запросе на [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs,](imapiprop-getnamesfromids.md) которые слишком большие для выполнения, возвращается значение MAPI_E_TOO_BIG ошибки. Звонители должны разделить запрос на несколько запросов, назвав соответствующий метод в цикле. 
  
Если вызов приводит к частичному успеху, например если запрос на имена, которые соотносят с определенными идентификаторами, и не удается найти одно или несколько имен, **GetNamesFromID возвращает** MAPI_W_ERRORS_RETURNED и помещает PT_ERROR в тип свойства для отсутствующих свойств в массиве тегов свойств. 
  
Иногда клиент звонит в **GetNamesFromIDs,** в результате чего свойства не возвращаются, например, когда в указанном наборе свойств нет свойств, или когда все указанные свойства имеют тип, исключаемый флагами. Клиенты могут ожидать от поставщиков услуг: 
  
- Возвращение S_OK.
    
- Установите содержимое указателя массива тегов свойств в недавно выделенный массив тегов свойств с его **членом cValues,** заниженным до нуля. 
    
- Установите содержимое массива [структуры MAPINAMEID](mapinameid.md) nULL. 
    
- Установите значение содержимого для подсчета структур **MAPINAMEID** до нуля. 
    
## <a name="see-also"></a>См. также

- [Именованные свойства MAPI](mapi-named-properties.md)


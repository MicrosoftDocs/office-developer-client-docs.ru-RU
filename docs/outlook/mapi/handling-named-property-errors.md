---
title: Свойство ошибки с именем обработки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f6c12973a3ee2f9842e74f6f01b94553659dc1ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583311"
---
# <a name="handling-named-property-errors"></a>Свойство ошибки с именем обработки
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При запросе [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или слишком велик для реализации обработки [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) MAPI_E_TOO_BIG возвращается ошибка. Абонентов необходимо разделить свой запрос на несколько запросов вызова соответствующего метода в цикле. 
  
Если не удается найти результаты вызовов в частичное успешно, например, когда запрос для имен, которые сопоставляют определенные идентификаторы и одно или несколько имен, **GetNamesFromIDs** возвращает MAPI_W_ERRORS_RETURNED и помещает PT_ERROR в тип свойства для отсутствующих свойство в массиве тега свойства. 
  
В некоторых случаях клиент вызывает **GetNamesFromIDs** , которая приводит к нет свойств, возвращаемых, например, когда нет свойств в наборе указанное свойство, или когда все именованные свойства типа исключены с флаги. Клиенты могут ожидать поставщиков услуг для: 
  
- Возвращает значение S_OK.
    
- Значение массива тег вновь выделенный свойства содержимое указателя свойство tag массива с его элементом **cValues** нулевое значение. 
    
- Содержимое массива структура [MAPINAMEID](mapinameid.md) значение NULL. 
    
- Задайте содержимое числа структур **MAPINAMEID** нулевое значение. 
    
## <a name="see-also"></a>См. также

- [Именованные свойства MAPI](mapi-named-properties.md)


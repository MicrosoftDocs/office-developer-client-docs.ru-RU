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
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При выполнении запроса к [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs,](imapiprop-getnamesfromids.md) которое слишком большое для реализации, возвращается значение MAPI_E_TOO_BIG ошибки. Вызывающие должны разделить свой запрос на несколько запросов, вызывая соответствующий метод в цикле. 
  
Если вызов приводит к частичному успеху, например когда запрос касается имен, которые соотнесются с определенными идентификаторами и не удается найти одно или несколько имен, **GetNamesFromIDs** возвращает MAPI_W_ERRORS_RETURNED и помещает PT_ERROR в тип свойства для отсутствующих свойств в массиве тегов свойств. 
  
Иногда клиент совершает вызов **GetNamesFromIDs,** что приводит к неудажным свойствам, таким как отсутствие свойств в указанном наборе свойств или когда все именуемые свойства имеют тип, исключенный флагами. Клиенты могут ожидать от поставщиков услуг: 
  
- Возврат S_OK.
    
- Установите для содержимого указателя массива тегов свойств только что выделенный массив тегов свойств, для его члена **cValues** установлено нулевое значение. 
    
- Установите для содержимого массива [структуры MAPINAMEID](mapinameid.md) NULL. 
    
- Задайте для содержимого подсчета структур **MAPINAMEID** нулевое значение. 
    
## <a name="see-also"></a>См. также

- [Именованные свойства MAPI](mapi-named-properties.md)


---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438850"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает выпадаемую таблицу управления списком, которая будет использоваться в диалоговом окне, построенной из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a>Элементы

 **ulFlags**
  
> Зарезервировано, должно быть ноль. 
    
 **ulPRDisplayProperty**
  
> Тег свойства для свойства типа PT_TSTRING. Это свойство является одним из столбцов в таблице, идентифицированной участником **ulPRTableName.** Значения этого свойства отображаются в списке. 
    
 **ulPRSetProperty**
  
> Тег свойства для свойства любого типа. Это свойство является одним из столбцов в таблице, идентифицированной участником **ulPRTableName.** Когда пользователь списка выбирает значение свойства для члена **ulPRDisplayProperty** из строк таблицы, идентифицированных участником **ulPRTableName,** устанавливается соответствующий член **ulPRSetProperty.** 
    
 **ulPRTableName**
  
> Тег свойства для свойства таблицы типа PT_OBJECT, который можно открыть с помощью **вызова OpenProperty.** В таблице должно быть два столбца: **ulPRDisplayProperty** и **ulPRSetProperty.** Строки таблицы должны соответствовать пунктам в списке.
    
## <a name="remarks"></a>Примечания

Структура **DTBLDDLBX** описывает элемент управления списком, отображаемый как единый элемент до тех пор, пока пользователь не выберет решение о его расширении. 
  
Три свойства, идентифицированные тегами свойств, работают вместе, чтобы отобразить сведения в списке и установить связанное свойство. Член **ulPRTableName** — это объект таблицы, к нему можно получить доступ по вызову [в IMAPIProp::OpenProperty.](imapiprop-openproperty.md) В таблице есть два столбца: один столбец для свойства, определенного участником **ulPRDisplayProperty,** а другой для свойства, определенного участником **ulPRSetProperty.** 
  
Свойство **ulPRDisplayProperty** диски отображения списка. Когда пользователь выбирает одно из значений из дисплея, MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить соответствующее свойство, определенное участником **ulPRSetProperty.** Это означает, что свойство в одной строке с выбранным свойством отображения. Нельзя установить для участника **ulPRSetProperty** **PR_NULL** [(PidTagNull).](pidtagnull-canonical-property.md)
  
Начальное значение отображается в списке, если MAPI извлекла свойство, представленное участником **ulPRSetProperty,** с помощью вызова [в IMAPIProp::GetProps](imapiprop-getprops.md) и расположена строка в таблице со значением для члена **ulPRSetProperty.** Начальное отображаемого значения — содержимое столбца **ulPRDisplayProperty** из этой строки, которое соответствует свойству в **члене структуры ulPRDisplayProperty.** Значение, возвращенное **GetProps** для свойства, определенного участником **ulPRDisplayProperty,** становится начальным значением, которое отображается при первом отображении списка. 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md) Сведения о типах свойств см. в [обзоре типов свойств MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Структуры MAPI](mapi-structures.md)
  
[Реализация таблицы отображения](display-table-implementation.md)
  
[Таблицы отображения](display-tables.md)
  
[Обзор типов свойств MAPI](mapi-property-type-overview.md)


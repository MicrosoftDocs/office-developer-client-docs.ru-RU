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
ms.openlocfilehash: 3307bb252ca4436999a541f85657fed9878c798a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579398"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывает элемент управления раскрывающегося списка, который будет использоваться в диалоговое окно, построенная на основе таблицы отображения.
  
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

## <a name="members"></a>Members

 **ulFlags**
  
> Зарезервированные, должен быть равно нулю. 
    
 **ulPRDisplayProperty**
  
> Свойство tag для свойства типа PT_TSTRING. Это свойство является одним из столбцов в таблице, определяемую средством члена **ulPRTableName** . Значения для этого свойства отображаются в списке. 
    
 **ulPRSetProperty**
  
> Свойство tag для свойства любого типа. Это свойство является одним из столбцов в таблице, определяемую средством члена **ulPRTableName** . Когда пользователь списка выбирает значение свойства для элемента **ulPRDisplayProperty** из строки в таблице, определяемую средством член **ulPRTableName** , соответствующего члена **ulPRSetProperty** имеет значение. 
    
 **ulPRTableName**
  
> Тег свойства для свойства в таблице типа PT_OBJECT, которая может быть открыта с помощью **OpenProperty** вызова. Таблица должна иметь два столбца: **ulPRDisplayProperty** и **ulPRSetProperty**. Строки в таблице должна соответствовать элементов в списке.
    
## <a name="remarks"></a>Замечания

Структура **DTBLDDLBX** описывает элемент управления раскрывающегося списка, который отображается в виде одного элемента, пока пользователь вручную развернуть его. 
  
Три свойства, определяемую средством теги свойства работают вместе для отображения сведений в списке и связанных с ними свойства. Член **ulPRTableName** — это объект таблицы, к которому осуществляется посредством вызова [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Таблица имеет два столбца: один столбец для свойства, определяемую средством член **ulPRDisplayProperty** , а другой для свойство, определяемое член **ulPRSetProperty** . 
  
Свойство **ulPRDisplayProperty** дисков Отображение списка. Когда пользователь выбирает одно из значений из отображения, MAPI вызывает [IMAPIProp::SetProps](imapiprop-setprops.md) для соответствующего свойства согласно процедуре участником **ulPRSetProperty** . Это означает, что свойство в той же строке выбранного отображаемое свойство. Член **ulPRSetProperty** не может иметь значение **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Начальное значение отображается в списке, если MAPI имеет извлекается свойство, представленное член **ulPRSetProperty** посредством вызова [IMAPIProp::GetProps](imapiprop-getprops.md) и находится строки в таблице со значением для элемента **ulPRSetProperty** . Начальное отображаемое значение находится содержимое столбца **ulPRDisplayProperty** из этой строки, соответствующее свойство в элемент **ulPRDisplayProperty** структуры. Значение, возвращаемое **GetProps** для свойства, определяемую средством член **ulPRDisplayProperty** становится начального значения, которая отображается при первом отображении списка. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см. Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Структуры MAPI](mapi-structures.md)
  
[Реализация таблицы отображения](display-table-implementation.md)
  
[Таблицы отображения](display-tables.md)
  
[Обзор типов свойств MAPI](mapi-property-type-overview.md)


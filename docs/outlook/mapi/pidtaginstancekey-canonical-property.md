---
title: Каноническое свойство PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396991"
---
# <a name="pidtaginstancekey-canonical-property"></a>Каноническое свойство PidTagInstanceKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, уникальным образом определяет строку в таблице. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_INSTANCE_KEY  <br/> |
|Идентификатор:  <br/> |0x0FF6  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Таблица  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство соответствует двоичное значение, которое однозначно определяет строку в представлении таблицы. Это обязательный столбец в большинстве таблиц. Если строка входит в два представления, есть два ключевых другой экземпляр. Ключ экземпляра строки, могут отличаться каждый раз при открытии таблицы, но остаются постоянными при таблице open. Строки, добавленные во время таблицы не повторного использования ключа экземпляра, который использовался ранее. 
  
Чтобы сопоставить все строки расширение с помощью **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или свойства **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Используйте **PR_INSTANCE_KEY** для указания конкретного экземпляра в развертывание. 
  
При развертывании свойством в таблице строка создается для каждого экземпляра расширения, то есть, для каждого значения этого свойства. Каждая строка имеет уникальное значение для свойства **PR_INSTANCE_KEY** , а все остальные столбцы сохранить исходные значения во всей расширения. 
  
В по категориям Сортировка таблицы строки, не соответствующие фактические данные можно добавить в результаты сортировки. Как и все строки во всех таблицах каждую строку, имеет свой собственный ключ уникальный экземпляр. 
  
 **PR_INSTANCE_KEY** также используется в таблице уведомления о событиях. **PropIndex** и **propPrior** элементы структуры [TABLE_NOTIFICATION](table_notification.md) — это [SPropValue](spropvalue.md) структуры, содержащие **PR_INSTANCE_KEY** значения. Элемент **propIndex** указывает строку, в которой были добавлены или изменены. Элемент **propPrior** указывает строку перед строкой добавленного или измененного (**PR_NULL** указывает на изменение в первую строку). 
  
Это значение не копируется как часть в таблице отображения. 
  
 **PR_INSTANCE_KEY** — это структура [MAPIUID](mapiuid.md) . Все экземпляр непосредственно сравнения ключей как двоичные значения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


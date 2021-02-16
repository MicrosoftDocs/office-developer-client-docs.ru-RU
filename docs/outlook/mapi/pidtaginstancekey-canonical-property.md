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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358513"
---
# <a name="pidtaginstancekey-canonical-property"></a>Каноническое свойство PidTagInstanceKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, однозначно определяя строку в таблице. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_INSTANCE_KEY  <br/> |
|Идентификатор:  <br/> |0x0FF6  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Table  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является двоичным значением, уникальным образом идентифицирует строку в представлении таблицы. В большинстве таблиц этот столбец является обязательной. Если строка включена в два представления, существует два разных ключа экземпляра. Клавиша экземпляра строки может отличаться при каждом открытие таблицы, но остается постоянной, пока таблица открыта. Строки, добавленные во время использования таблицы, не используют ранее использованный ключ экземпляра. 
  
Используйте свойства **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)или **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)для корреляции всех строк расширения. Используйте **PR_INSTANCE_KEY** для поиска определенного экземпляра в расширении. 
  
При расширении многоценного свойства в таблице создается строка для каждого экземпляра расширения, то есть для каждого значения этого свойства. Каждая строка имеет уникальное  значение для свойства PR_INSTANCE_KEY, а все остальные столбцы сохраняют исходные значения во время расширения. 
  
В классификации таблицы строки, не соответствующие фактическим данным, можно добавить в результат сортировки. Каждая такая строка, как и все строки во всех таблицах, имеет собственный уникальный ключ экземпляра. 
  
 **PR_INSTANCE_KEY** также используется в уведомлениях о событиях таблицы. The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values. Член **propIndex** указывает строку, которая была добавлена или изменена. Член **propPrior** указывает строку перед добавленной или измененной строкой **(PR_NULL** указывает на изменение первой строки). 
  
Это значение не копируется как часть отображаемой таблицы. 
  
 **PR_INSTANCE_KEY** является [структурой MAPIUID.](mapiuid.md) Все ключи экземпляра можно напрямую сравнить как двоичные значения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


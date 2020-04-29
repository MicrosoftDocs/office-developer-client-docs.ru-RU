---
title: Каноническое свойство PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433040"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Каноническое свойство PidTagMemberEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи объекта каталога для элемента таблицы списка управления доступом системы (SACL).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0FFF  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Правила на стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется интерфейсом [иексчанжемодифитабле](iexchangemodifytableiunknown.md) для уникальной идентификации пользователя или роли, к которым применяется SACL. После создания члена в таблице SACL изменить значение **EntryID** невозможно. Чтобы изменить его, необходимо удалить элемент Table и повторно создать его с другим идентификатором **EntryID**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


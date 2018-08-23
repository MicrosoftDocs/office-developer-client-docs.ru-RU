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
ms.openlocfilehash: 27659b69e0ae050206de18c1258ee593737fbd3b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592950"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Каноническое свойство PidTagMemberEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор каталога объект запись члена в таблице список управления ДОСТУПОМ системы доступа элемента управления.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0FFF  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Правила со стороны сервера  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) для уникальной идентификации лицо или роль, к которому относится список SACL. После создания члена в таблице SACL **ENTRYID** нельзя изменить. Чтобы изменить его, необходимо удалить элемент в таблице и повторно создать его с помощью различных **ENTRYID**.
  
## <a name="related-resources"></a>Связанные ресурсы

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


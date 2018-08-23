---
title: Каноническое свойство PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21fdff2aa713905a27a3d0cc5545ceb59f030378
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586860"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Каноническое свойство PidTagDefCreateMailuser

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи шаблона для обмена сообщениями объекта пользователя по умолчанию. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Идентификатор:  <br/> |0x3612  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Клиентские приложения используйте это свойство для создания объекта пользователя обмена сообщениями в контейнере. Поддержка создания записи является необязательным для контейнеров адресной книги; те, которые не поддерживают не требуется для предоставления этого свойства. 
  
Это свойство определяет записи, которые отображаются в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для обмена мгновенными сообщениями пользователей. После получения идентификатора клиента используется в вызов метода [IABContainer::CreateEntry](iabcontainer-createentry.md) . Операция представляет шаблон для обмена сообщениями пользователя по умолчанию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


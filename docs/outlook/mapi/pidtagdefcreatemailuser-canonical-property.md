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
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269988"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Каноническое свойство PidTagDefCreateMailuser

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор элемента шаблона для объекта пользователя, используемого по умолчанию для обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДЕФ_КРЕАТЕ_МАИЛУСЕР  <br/> |
|Идентификатор:  <br/> |0x3612  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Клиентские приложения используют это свойство, чтобы создать объект пользователя для обмена сообщениями в контейнере. Поддержка создания записей является необязательной для контейнеров адресных книг; те, которые не поддерживают эту возможность, не являются обязательными для предоставления этого свойства. 
  
Это свойство указывает запись, которая может отображаться в свойстве **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для пользователей системы обмена сообщениями. После получения идентификатора клиент использует его в вызове метода [иабконтаинер:: креатинтри](iabcontainer-createentry.md) . Запись представляет шаблон для пользователя обмена сообщениями по умолчанию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


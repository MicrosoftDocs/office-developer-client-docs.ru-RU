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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407482"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Каноническое свойство PidTagDefCreateMailuser

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи шаблона для объекта пользователя обмена сообщениями по умолчанию. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Идентификатор:  <br/> |0x3612  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Клиентские приложения используют это свойство для создания объекта пользователя обмена сообщениями в контейнере. Поддержка создания записей не является обязательной для контейнеров адресной книги; те, которые не поддерживают его, не требуются для того, чтобы получить доступ к этому свойству. 
  
Это свойство указывает запись, которая может отображаться в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)для пользователей сообщений. После получения идентификатора клиент использует его в вызове метода [IABContainer::CreateEntry.](iabcontainer-createentry.md) Запись представляет шаблон для пользователя обмена сообщениями по умолчанию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


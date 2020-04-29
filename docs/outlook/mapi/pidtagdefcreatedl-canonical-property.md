---
title: Каноническое свойство PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417793"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Каноническое свойство PidTagDefCreateDl

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор элемента шаблона для списка рассылки по умолчанию. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Идентификатор:  <br/> |0x3611  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Клиентские приложения используют это свойство для создания списка рассылки в контейнере. Поддержка создания записей является необязательной для контейнеров адресных книг; те, которые не поддерживают эту возможность, не являются обязательными для предоставления этого свойства. 
  
Это свойство указывает запись, которая может отображаться в свойстве **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) для списков рассылки. После получения идентификатора клиент использует его в вызове метода [иабконтаинер:: креатинтри](iabcontainer-createentry.md) . Запись представляет шаблон для списка рассылки по умолчанию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


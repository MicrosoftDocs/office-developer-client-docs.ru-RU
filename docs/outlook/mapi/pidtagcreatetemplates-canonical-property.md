---
title: Каноническое свойство PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811023"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Каноническое свойство PidTagCreateTemplates

  
  
**Относится к**: Outlook 
  
Содержит объект внедренных в таблице, который содержит идентификаторы записей шаблона поля диалогового окна. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Идентификатор:  <br/> |0x3604  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы узнать, какой шаблон объекты могут быть созданы в контейнере, вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на это свойство. Полученный объект является таблицей одноразовых, задающей идентификаторы записей для всех шаблонов, которые можно создавать внутри контейнера. 
  
Для создания объекта шаблона, вызовите метод **CreateEntry** объекта-контейнера на значения столбцов **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) в одноразовых TABLE.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


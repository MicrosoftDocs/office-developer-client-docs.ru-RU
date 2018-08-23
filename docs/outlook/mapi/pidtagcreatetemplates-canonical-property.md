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
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563361"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Каноническое свойство PidTagCreateTemplates

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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


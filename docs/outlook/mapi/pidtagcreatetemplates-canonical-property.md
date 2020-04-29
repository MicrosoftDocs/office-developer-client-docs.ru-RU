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
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438185"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Каноническое свойство PidTagCreateTemplates

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит объект внедренной таблицы, который содержит идентификаторы элементов шаблона диалогового окна. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Идентификатор:  <br/> |0x3604  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы узнать, какие объекты шаблонов можно создать в контейнере, вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для этого свойства. Полученный объект является одноразовой таблицей, которая предоставляет идентификаторы записей для всех шаблонов, которые можно создать в контейнере. 
  
Чтобы создать объекты шаблона, вызовите метод **креатинтри** объекта Container для значений столбца **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из таблицы с отправителями.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


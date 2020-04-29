---
title: Каноническое свойство PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419256"
---
# <a name="pidtagdetailstable-canonical-property"></a>Каноническое свойство PidTagDetailsTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит внедренный объект таблицы отображения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DETAILS_TABLE  <br/> |
|Идентификатор:  <br/> |0x3605  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

При передаче этого свойства методу [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для объекта возвращается интерфейс [IMAPITable](imapitableiunknown.md) , позволяющий создать таблицу отображения. MAPI использует эту таблицу для отображения страниц свойств для объекта адресной книги в ответ на вызов [IAddrBook::D етаилс](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Каноническое свойство PidTagSearch](pidtagsearch-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


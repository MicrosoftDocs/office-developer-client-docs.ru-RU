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
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585789"
---
# <a name="pidtagdetailstable-canonical-property"></a>Каноническое свойство PidTagDetailsTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит объект отображения внедренных в таблице.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DETAILS_TABLE  <br/> |
|Идентификатор:  <br/> |0x3605  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Передача этого свойства в метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для объекта возвращает [IMAPITable](imapitableiunknown.md) интерфейс, который позволяет создавать в таблице отображения. Эта таблица MAPI используется для отображения свойств для объекта адресной книги в ответ на вызов [IAddrBook::Details](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Каноническое свойство PidTagSearch](pidtagsearch-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


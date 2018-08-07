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
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811055"
---
# <a name="pidtagdetailstable-canonical-property"></a>Каноническое свойство PidTagDetailsTable

  
  
**Относится к**: Outlook 
  
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


---
title: Каноническое свойство PidTagLongTermEntryIdFromTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLongTermEntryIdFromTable
api_type:
- HeaderDef
ms.assetid: d9457fea-4b1e-4cf6-9c4b-14c98fbec2a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddec060af73d61a4a39c59b35f0442d6b9b1db66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590318"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a>Каноническое свойство PidTagLongTermEntryIdFromTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает идентификатор записи долгосрочного элемента.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LONGTERM_ENTRYID_FROM_TABLE  <br/> |
|Идентификатор:  <br/> |0x6670  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства таблицы  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство можно использовать в таблице содержимое для получения идентификатора запись элемента как долгосрочного идентификатор записи вместо краткосрочных идентификатор записи. Сведения об идентификаторах долгосрочных и краткосрочных содержатся **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


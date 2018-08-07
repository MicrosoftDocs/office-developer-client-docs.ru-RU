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
ms.openlocfilehash: ebb925ac1ff6507a5e686b769ba9d48b095fb527
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811340"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a>Каноническое свойство PidTagLongTermEntryIdFromTable

  
  
**Относится к**: Outlook 
  
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


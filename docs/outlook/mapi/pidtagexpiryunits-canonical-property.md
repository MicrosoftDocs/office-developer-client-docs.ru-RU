---
title: Каноническое свойство PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6aab4228af0f584d96a2a8cc02c5f36e05a01e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569605"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Каноническое свойство PidTagExpiryUnits

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описание единицы времени, когда умножает свойство **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Идентификатор:  <br/> |0x3FEE  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство, если значение, должно быть одно из следующих значений:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Описание (TimeOf)  <br/> |
|0x00000000  <br/> |Минут, например 60 секунд  <br/> |
|0x00000001  <br/> |Часов, например 60 x 60 секунд  <br/> |
|0x00000002  <br/> |День, например 24 x 60 x 60 секунд  <br/> |
|0x00000003  <br/> |Недели, например 7x24x60x60 секунд  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


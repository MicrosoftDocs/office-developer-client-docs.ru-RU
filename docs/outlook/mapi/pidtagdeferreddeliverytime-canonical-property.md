---
title: Каноническое свойство PidTagDeferredDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b6b5f5aa5c595fb0c19ca9b8a9f8aeb94a2c2725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811063"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a>Каноническое свойство PidTagDeferredDeliveryTime

  
  
**Относится к**: Outlook 
  
Содержит дату и время, когда отправитель сообщения запрашивает сообщение доставлено. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFERRED_DELIVERY_TIME  <br/> |
|Идентификатор:  <br/> |0x000F  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

MAPI не выполняет отложенная доставка; Это параметр базовой системы обмена сообщениями для обработки отложенной доставки.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые в сообщениях электронной почты.
    
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


---
title: Каноническое свойство PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590927"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>Каноническое свойство PidTagLatestDeliveryTime

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит последние дата и время, когда сообщение передачи (агента) необходимо доставить сообщение. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LATEST_DELIVERY_TIME  <br/> |
|Идентификатор:  <br/> |0x0019  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Если агента передачи сообщений не удается доставить сообщение, время, когда это свойство определяет, отменяет сообщение без доставки. 
  
## <a name="related-resources"></a>Связанные ресурсы

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


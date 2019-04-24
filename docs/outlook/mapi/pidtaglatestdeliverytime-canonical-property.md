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
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279854"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a>Каноническое свойство PidTagLatestDeliveryTime

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит последние дата и время, когда агент передачи сообщений (MTA) должен доставить сообщение. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ЛАТЕСТ_ДЕЛИВЕРИ_ТИМЕ  <br/> |
|Идентификатор:  <br/> |0x0019  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Если MTA не может доставить сообщение по времени, указанному этим свойством, оно отменяет сообщение без доставки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


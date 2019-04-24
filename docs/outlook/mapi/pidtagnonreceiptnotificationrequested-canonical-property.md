---
title: Каноническое свойство PidTagNonReceiptNotificationRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329311"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Каноническое свойство PidTagNonReceiptNotificationRequested

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если отправителю сообщения требуется уведомление о недоставке для указанного получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_НОН_РЕЦЕИПТ_НОТИФИКАТИОН_РЕКУЕСТЕД  <br/> |
|Идентификатор:  <br/> |0x0C06  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Комментарии

Если это свойство содержит значение FALSE, а свойство **пр_реад_рецеипт_рекуестед** ([PIDTAGREADRECEIPTREQUESTED](pidtagreadreceiptrequested-canonical-property.md)) содержит значение true, то поставщик услуг может переопределить свойство **пр_нон_рецеипт_нотификатион_рекуестед** и создать объект отчет о недоставке. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


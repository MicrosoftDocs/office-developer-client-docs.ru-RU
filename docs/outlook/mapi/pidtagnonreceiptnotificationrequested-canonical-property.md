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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419753"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Каноническое свойство PidTagNonReceiptNotificationRequested

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если отправителю сообщения нужно уведомление о нео получении для указанного получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Идентификатор:  <br/> |0x0C06  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство содержит значение FALSE, а свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)содержит значение TRUE, поставщик службы может переопредить свойство **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** и создать отчет о невыставке. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


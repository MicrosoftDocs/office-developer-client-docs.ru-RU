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
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811398"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Каноническое свойство PidTagNonReceiptNotificationRequested

  
  
**Относится к**: Outlook 
  
Содержит значение TRUE, если отправитель сообщения запрашивает уведомления без уведомления для указанного получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Идентификатор:  <br/> |0x0C06  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство содержит значение FALSE, а свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) значение TRUE, поставщик услуг можно переопределить свойство **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** и создать отчет о недоставке. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


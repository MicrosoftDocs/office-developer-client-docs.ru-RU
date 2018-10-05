---
title: Каноническое свойство PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391376"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a>Каноническое свойство PidTagOriginalDeliveryTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит копию исходного сообщения дату и время доставки в потоке. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_DELIVERY_TIME  <br/> |
|Идентификатор:  <br/> |0x0055  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство копируются из исходного свойства **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в последующих ответить или операции и в отчетах чтения и nonread. Отчеты о доставке используйте свойство **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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


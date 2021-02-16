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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355659"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a>Каноническое свойство PidTagOriginalDeliveryTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит копию даты и времени доставки исходного сообщения в потоке. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_DELIVERY_TIME  <br/> |
|Идентификатор:  <br/> |0x0055  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство копируется из исходного **свойства PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в последующих операциях ответа или переададации и используется в отчетах о прочтенных и непрочитаных сообщениях. В отчетах о доставке используется **свойство PR_DELIVER_TIME** ([PidTagDeliverTime).](pidtagdelivertime-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


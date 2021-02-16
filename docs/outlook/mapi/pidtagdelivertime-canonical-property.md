---
title: Каноническое свойство PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435280"
---
# <a name="pidtagdelivertime-canonical-property"></a>Каноническое свойство PidTagDeliverTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит дату и время доставки исходного сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELIVER_TIME  <br/> |
|Идентификатор:  <br/> |0x0010  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является свойством для каждого получателя в отчете о доставке, которое указывает время доставки исходного сообщения пользователю системы обмена сообщениями, для которого создается отчет о доставке.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


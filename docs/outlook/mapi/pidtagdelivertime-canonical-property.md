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
ms.openlocfilehash: 198e388f5cfb6ab0431e7b7a78b9a0be3d103597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582121"
---
# <a name="pidtagdelivertime-canonical-property"></a>Каноническое свойство PidTagDeliverTime

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит дату и время, когда исходное сообщение было доставлено. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELIVER_TIME  <br/> |
|Идентификатор:  <br/> |0x0010  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является свойством каждого получателя на отчетов о доставке, которое указывает время, когда исходное сообщение было доставлено обмена сообщениями пользователя, для которого создается отчет о доставке.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


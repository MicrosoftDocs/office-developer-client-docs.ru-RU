---
title: Каноническое свойство PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f636c0a49d6ad96ab157d00780fa6ffc5c8f3236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588274"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>Каноническое свойство PidTagDeferredSendTime

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает время, когда это клиент, предоставляемых отложите отправки сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|Идентификатор:  <br/> |0x3FEF  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Если присутствуют **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) и **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) свойства, значение этого свойства — это пересчитывать с помощью следующей формулы и Старое значение игнорируется.
  
 **PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** * TimeOf (**PR_DEFERRED_SEND_UNITS**)
  
Если значение **PR_DEFERRED_SEND_TIME** является более ранней, чем текущая время (в формате UTC), сообщение отправляется немедленно. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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


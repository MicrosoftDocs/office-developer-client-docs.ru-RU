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
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359880"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>Каноническое свойство PidTagDeferredSendTime

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает время, когда клиент хотел бы отложить отправку сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|Идентификатор:  <br/> |0x3FEF  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если **свойства PR_DEFERRED_SEND_UNITS** [(PidTagDeferredSendUnits)](pidtagdeferredsendunits-canonical-property.md)и **PR_DEFERRED_SEND_NUMBER** [(PidTagDeferredSendNumber)](pidtagdeferredsendnumber-canonical-property.md)присутствуют, значение этого свойства будет откормлено с помощью следующей формулы, а старое значение игнорируется.
  
 **PR_DEFERRED_SEND_TIME**  =  **PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** * TimeOf **(PR_DEFERRED_SEND_UNITS)**
  
Если **PR_DEFERRED_SEND_TIME** ниже текущего времени (в UTC), сообщение отправляется немедленно. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


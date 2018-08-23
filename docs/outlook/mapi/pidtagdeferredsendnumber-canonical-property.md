---
title: Каноническое свойство PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 30ee7c1a7eb86fd4cdfe90fb6711bd1b295fd5e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591088"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>Каноническое свойство PidTagDeferredSendNumber

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит номер, который можно использовать для вычисления отсрочке отправки сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Идентификатор:  <br/> |0x3FEB  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется для вычисления свойство **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)), когда она не существует. При отложенной отправки сообщения свойство **PR_DEFERRED_SEND_NUMBER** должно быть установлено вместе со свойством **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), если свойство **PR_DEFERRED_SEND_TIME** отсутствует. 
  
**PR_DEFERRED_SEND_NUMBER** должен иметь значение от 0 до 999. 
  
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


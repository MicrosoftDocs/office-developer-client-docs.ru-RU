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
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357738"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>Каноническое свойство PidTagDeferredSendNumber

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит номер, который можно использовать для вычисления отсрочки отправки сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|Идентификатор:  <br/> |0x3FEB  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для вычисления **свойства PR_DEFERRED_SEND_TIME** [(PidTagDeferredSendTime),](pidtagdeferredsendtime-canonical-property.md)когда оно не присутствует. При отложении отправки  сообщения свойство PR_DEFERRED_SEND_NUMBER должно быть задано вместе с свойством **PR_DEFERRED_SEND_UNITS** [(PidTagDeferredSendUnits),](pidtagdeferredsendunits-canonical-property.md)если свойство PR_DEFERRED_SEND_TIME отсутствует.  
  
Значение **PR_DEFERRED_SEND_NUMBER** должно быть установлено между 0 и 999. 
  
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


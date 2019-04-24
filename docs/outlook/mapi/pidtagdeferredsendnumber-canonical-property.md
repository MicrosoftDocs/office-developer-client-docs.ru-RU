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
  
Содержит номер, который можно использовать для вычисления дефермент отправки сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДЕФЕРРЕД_СЕНД_НУМБЕР  <br/> |
|Идентификатор:  <br/> |0x3FEB  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для вычисления свойства **пр_деферред_сенд_тиме** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)), если оно отсутствует. При отправке сообщения свойство **пр_деферред_сенд_нумбер** должно быть задано вместе со свойством **пр_деферред_сенд_унитс** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), если свойство **пр_деферред_сенд_тиме** отсутствует. 
  
Значение **пр_деферред_сенд_нумбер** должно быть задано в диапазоне от 0 до 999. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


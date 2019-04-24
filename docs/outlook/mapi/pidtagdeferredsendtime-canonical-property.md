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
  
Указывает время, в течение которого клиент хочет отложить отправку сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДЕФЕРРЕД_СЕНД_ТИМЕ  <br/> |
|Идентификатор:  <br/> |0x3FEF  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если присутствуют свойства **пр_деферред_сенд_унитс** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) и **пр_деферред_сенд_нумбер** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)), значение этого свойства пересчитывается с помощью следующей формулы и старое значение игнорируется.
  
 **Пр_деферред_сенд_тиме** = **пр_клиент_субмит_тиме** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **пр_деферред_сенд_нумбер** * тимеоф (**пр_деферред_сенд_унитс**)
  
Если значение **пр_деферред_сенд_тиме** более раннее, чем текущее время (в формате UTC), сообщение отправляется немедленно. 
  
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


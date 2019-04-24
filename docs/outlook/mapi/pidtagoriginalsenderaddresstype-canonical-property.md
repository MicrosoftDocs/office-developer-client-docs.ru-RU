---
title: Каноническое свойство PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342681"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a>Каноническое свойство PidTagOriginalSenderAddressType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит тип адреса отправителя первой версии сообщения, то есть сообщение перед пересылкой или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ОРИГИНАЛ_СЕНДЕР_АДДРТИПЕ, ПР_ОРИГИНАЛ_СЕНДЕР_АДДРТИПЕ_А, ПР_ОРИГИНАЛ_СЕНДЕР_АДДРТИПЕ_В  <br/> |
|Идентификатор:  <br/> |0x0066  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Комментарии

Эти свойства являются примерами свойств адреса для исходного отправителя сообщения. При первой отправке сообщения клиентскому приложению следует задать для этих свойств значение **пр_сендер_аддртипе** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)). Он никогда не изменяется при пересылке сообщения или ответе на него.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
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


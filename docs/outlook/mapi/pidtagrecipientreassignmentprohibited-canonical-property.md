---
title: Каноническое свойство PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341113"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Каноническое свойство PidTagRecipientReassignmentProhibited

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, запрещено ли добавлять дополнительных получателей сообщения электронной почты при пересылке сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Идентификатор:  <br/> |0x002B  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство задается на основе значения **PR_SENSITIVITYного** сообщения ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) сообщения электронной почты. Если для **PR_SENSITIVITY** задано значение "0x00000000" (обычная) или "0x00000003" (конфиденциально), для этого свойства должно быть задано значение "0x00" или отсутствует, что позволяет разрешить добавление дополнительных или других получателей сообщения электронной почты. Если для **PR_SENSITIVITY** объекта электронной почты задано значение "0x00000001" (личное) или "0x00000002" (личное), то для этого свойства необходимо задать значение "0x01", чтобы запретить добавление дополнительных или разных получателей этого сообщения через переадресацию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


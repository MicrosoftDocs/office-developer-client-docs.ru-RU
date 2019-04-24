---
title: Каноническое свойство PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356471"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a>Каноническое свойство PidTagReadReceiptRequested

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если отправителю требуется, чтобы система обмена сообщениями создавала отчет о прочтении, когда получатель прочитал сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕАД_РЕЦЕИПТ_РЕКУЕСТЕД  <br/> |
|Идентификатор:  <br/> |0x0029  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Примечания

Для этого свойства должно быть задано значение TRUE, чтобы проверить значения в свойствах **пр_реад_рецеипт_ентрид** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) и **пр_реад_рецеипт_сеарч_кэй** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)).
  
Если сообщение с набором **пр_реад_рецеипт_рекуестед** удаляется или истечет до тех пор, пока система обмена сообщениями не сможет создать отчет о прочтении, создается отчет о непрочтении. 
  
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


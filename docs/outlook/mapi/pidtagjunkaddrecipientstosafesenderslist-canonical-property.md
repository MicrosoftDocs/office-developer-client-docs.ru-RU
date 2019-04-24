---
title: Каноническое свойство PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282370"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Каноническое свойство PidTagJunkAddRecipientsToSafeSendersList

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли добавлять получателей почты в список надежных отправителей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ЖУНК_АДД_РЕЦИПС_ТО_ССЛ  <br/> |
|Идентификатор:  <br/> |0x6103  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Нежелательная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Если задано, для этого свойства должно быть задано значение 0 или 1. Значение 1 указывает, что почтовые получатели должны быть добавлены в список надежных отправителей. Значение 0 указывает, что получатели почты не добавляются в список надежных отправителей.
  
Если для этого свойства задано значение 1, SMTP-адреса получателей электронной почты необходимо добавить в предложение надежные отправители условия правила неЖелательной почты. Если это свойство равно 0, никаких действий не нужно.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.
    
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


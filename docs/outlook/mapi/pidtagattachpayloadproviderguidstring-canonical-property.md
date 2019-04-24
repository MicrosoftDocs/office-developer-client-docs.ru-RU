---
title: Каноническое свойство PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361105"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>Каноническое свойство PidTagAttachPayloadProviderGuidString

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка MIME X — полезных данных provider – GUID.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_ПАЙЛОАД_ПРОВ_ГУИД_СТР, ПР_АТТАЧ_ПАЙЛОАД_ПРОВ_ГУИД_СТР_А, ПР_АТТАЧ_ПАЙЛОАД_ПРОВ_ГУИД_СТР_В  <br/> |
|Идентификатор:  <br/> |0x3719  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Приложение Outlook  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать значение этих свойств, клиенты MIME должны записать поле заголовка X — полезных данных provider – GUID в сущность MIME, которая будет анализироваться как вложение.
  
Считыватели MIME должны скопировать значение поля заголовка в значение соответствующего свойства. Средства чтения MIME должны игнорировать это поле заголовка, если оно отображается в объекте MIME, анализируемом в виде сообщения или текста сообщения, а не вложения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
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


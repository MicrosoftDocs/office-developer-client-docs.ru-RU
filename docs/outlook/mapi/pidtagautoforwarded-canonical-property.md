---
title: Каноническое свойство PidTagAutoForwarded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326616"
---
# <a name="pidtagautoforwarded-canonical-property"></a>Каноническое свойство PidTagAutoForwarded

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если клиент запрашивает заглавное Exchange X-MS-Exchange-Organization-AutoForwarded.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AUTO_FORWARDED  <br/> |
|Идентификатор:  <br/> |0x0005  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общие отчеты  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство настроено на FALSE или не используется, не будет создано Exchange X-MS-Exchange-Organization-AutoForwarded header.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Определяет каждое свойство, которое используется в объектах, описанных в документах с префиксом MS-OXO.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных конвенций электронной почты в объекты сообщений.
    
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


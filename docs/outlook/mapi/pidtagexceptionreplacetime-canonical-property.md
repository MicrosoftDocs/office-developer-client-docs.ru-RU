---
title: Каноническое свойство PidTagExceptionReplaceTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExceptionReplaceTime
api_type:
- HeaderDef
ms.assetid: bd4d1311-15e4-4275-a967-c6d11d2e48d2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f255b91cbd428a2ceaa51140519b02d3f8a3b1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316389"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a>Каноническое свойство PidTagExceptionReplaceTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает исходную дату и время, когда экземпляр в шаблоне повторения произошел бы, если бы он не был исключением.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXCEPTION_REPLACETIME  <br/> |
|Идентификатор:  <br/> |0x7FF9  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Сообщение, определенное классом, не передается  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение должно быть указано в UTC.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


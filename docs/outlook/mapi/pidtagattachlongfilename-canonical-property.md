---
title: Каноническое свойство PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339328"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>Каноническое свойство PidTagAttachLongFilename

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит длинные имена файлов и расширения вложений, за исключением пути. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_ЛОНГ_ФИЛЕНАМЕ, ПР_АТТАЧ_ЛОНГ_ФИЛЕНАМЕ_А, ПР_АТТАЧ_ЛОНГ_ФИЛЕНАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x3707  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Комментарии

Эти свойства относятся к значениям АТТАЧ_БИ_ВАЛУЕ, АТТАЧ_БИ_РЕФЕРЕНЦЕ, АТТАЧ_БИ_РЕФ_РЕСОЛВЕ и АТТАЧ_БИ_РЕФ_ОНЛИ свойства **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). Платформы, поддерживающие длинные имена файлов, должны задавать свойства **пр_аттач_лонг_филенаме** и **пр_аттач_филенаме** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) при отправке, а также проверять **пр_аттач_лонг_филенаме** в начале луча. 
  
Клиентское приложение должно задать для этого свойства предложенное длинное имя файла, которое будет использоваться, если главный компьютер, принимающий сообщение, поддерживает длинные имена файлов. **Пр_аттач_лонг_филенаме** можно использовать в качестве имени файла для сохранения вложения, а также для предоставления расширения имени файла, если не указано свойство **пр_аттач_екстенсион** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). 
  
В отличие от имени файла, предоставленного **пр_аттач_филенаме**, это имя не ограничено именем, состоящего из восьми символов, и расширением, состоящего из трех символов. Длина этого параметра может доставлять до 256 символов, включая имя файла, расширение и разделительный период. 
  
MAPI работает только с именами файлов в наборе символов ANSI. Клиентские приложения, использующие имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства сообщений, закодированных с помощью управления правами.
    
[[MS — ОКСАУМ]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для представления голосовой почты и факсимильных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Ммапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


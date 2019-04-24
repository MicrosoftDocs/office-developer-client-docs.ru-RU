---
title: Каноническое свойство PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319224"
---
# <a name="pidtagattachfilename-canonical-property"></a>Каноническое свойство PidTagAttachFilename

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя и расширение основного файла вложения, за исключением пути.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_ФИЛЕНАМЕ, ПР_АТТАЧ_ФИЛЕНАМЕ_А, ПР_АТТАЧ_ФИЛЕНАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x3704  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется, чтобы объекты вложения раскрывают эти свойства, которые относятся к значениям **аттач_би_валуе**, **аттач_би_референце**, **аттач_би_реф_ресолве**и **аттач_би_реф_онли** объекта **пр_аттач_месод** Свойство ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). **Пр_аттач_филенаме** и связанные свойства являются обязательными при использовании любого из этих значений. 
  
Эти свойства можно использовать в качестве предлагаемого имени файла для сохранения вложения и для предоставления расширения имени файла, если не указано свойство **пр_аттач_екстенсион** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). 
  
Имя файла ограничено восемью символами и расширением из трех символов. Для платформы, поддерживающей длинные имена файлов, задайте для этого свойства и свойство **пр_аттач_лонг_филенаме** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
MAPI работает только с именами файлов и другими строками, передаваемыми в нее, в наборе символов ANSI национального института стандартизации (США). Клиентские приложения, использующие имена файлов в наборе символов ИВТ, должны преобразовать их в ANSI перед вызовом функции MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства сообщений, закодированных с помощью управления правами.
    
[[MS — ОКСОСМИМЕ]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Задает свойства подписанных и зашифрованных сообщений S/MIME.
    
[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.
    
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


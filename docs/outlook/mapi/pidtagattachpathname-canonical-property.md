---
title: Каноническое свойство PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327232"
---
# <a name="pidtagattachpathname-canonical-property"></a>Каноническое свойство PidTagAttachPathname

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит полный путь и имя файла вложения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_ПАСНАМЕ, ПР_АТТАЧ_ПАСНАМЕ_А, ПР_АТТАЧ_ПАСНАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x3708  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется предоставлять этим свойствам вложенные объекты вложений. Их установка указывает на то, что данные вложения не включены в сообщение, но доступны на общем файловом сервере. Эти свойства необходимы в сочетании с любыми флагами **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), которые указывают вложение по ссылке: **аттач_би_референце**, **аттач_би_реф_ресолве**или **аттач_би_реф_ ТОЛЬКО**. 
  
Имя каждого каталога или имени файла ограничено восемью символами и расширением из трех символов. Общий путь ограничен 256 символами. Для платформы, поддерживающей длинные имена файлов, установите оба этих свойства и **пр_аттач_лонг_паснаме** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Клиентские приложения должны использовать в большинстве случаев универсальное соглашение об именовании (UNC), если файл является общим, и использовать абсолютный путь, если файл является локальным.
  
MAPI работает только с путями и именами в наборе знаков ANSI. Клиенты, использующие пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства сообщений, закодированных с помощью управления правами.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


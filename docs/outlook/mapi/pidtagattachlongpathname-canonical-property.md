---
title: Каноническое свойство PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339370"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Каноническое свойство PidTagAttachLongPathname

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит полностью квалифицированный длинный путь вложения и имя файла. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Идентификатор:  <br/> |0x370D  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства применимы при использовании значений свойств **PR_ATTACH_METHOD** [(PidTagAttachMethod),](pidtagattachmethod-canonical-property.md)которые указывают на вложение по ссылке: **ATTACH_BY_REFERENCE,** **ATTACH_BY_REF_RESOLVE** или **ATTACH_BY_REF_ONLY**. Платформы, поддерживающие длинные имена **файлов,** должны задать как PR_ATTACH_LONG_PATHNAME, так и связанные свойства и **свойства PR_ATTACH_PATHNAME** [(PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)при отправке, **и** должны сначала проверять PR_ATTACH_LONG_PATHNAME или связанные свойства при получении. 
  
Клиентский приложение должно настроить эти свойства на предложенный длинный путь и имя файла, которые будут использоваться, если хост-машина, получающая сообщение, поддерживает длинные имена файлов. Настройка этих свойств указывает на то, что данные вложения не включены в сообщение, но доступны на общем файловом сервере. 
  
В отличие от каталогов и **имен** файлов, предоставляемых PR_ATTACH_PATHNAME, эти каталоги и имена файлов не ограничиваются восьмилиманным каталогом или файловым именом плюс расширением на три символа. Вместо этого каждый каталог или имя файла может иметь длину до 256 символов, включая период имени, расширения и сепаратора. Однако общий путь ограничен 256 символами. 
  
Клиенты должны использовать универсальную конвенцию именования (UNC) в большинстве случаев, когда файл является общим, и должны использовать абсолютный путь, когда файл локальный.
  
MAPI работает только с путями и именами файлов в наборе символов ANSI. Клиентские приложения, которые используют пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Указывает свойства зашифрованных сообщений с управляемым правами.
    
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


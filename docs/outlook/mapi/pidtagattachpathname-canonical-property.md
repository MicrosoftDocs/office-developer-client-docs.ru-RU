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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит полное имя и путь вложения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Идентификатор:  <br/> |0x3708  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы вложенные объекты вложения выдают эти свойства. Установка этих данных означает, что данные вложения не включены в сообщение, но доступны на общем файловом сервере. Эти свойства необходимы в сочетании с любым из флагов **PR_ATTACH_METHOD** ([PidTagAttachMethod),](pidtagattachmethod-canonical-property.md)которые указывают вложение по ссылке: **ATTACH_BY_REFERENCE,** **ATTACH_BY_REF_RESOLVE** или **ATTACH_BY_REF_ONLY**. 
  
Каждый каталог или имя файла ограничено восьмибуквенным и трехбуквенным расширением. Общий путь ограничен 256 символами. Для платформы, поддерживаю которой поддерживаются длинные имена файлов, установите эти свойства **и PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname).](pidtagattachlongpathname-canonical-property.md) 
  
Клиентские приложения должны использовать универсальное соглашение об именах (UNC) в большинстве случаев, когда файл является общим, и должны использовать абсолютный путь, если файл является локальным.
  
MAPI работает только с путями и именами файлов в наборе символов ANSI. Клиенты, которые используют пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI, прежде чем вызывать MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Указывает свойства сообщений в кодированной кодировки с управлением правами.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


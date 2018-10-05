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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389171"
---
# <a name="pidtagattachpathname-canonical-property"></a>Каноническое свойство PidTagAttachPathname

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит полный путь и имя файла вложения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Идентификатор:  <br/> |0x3708  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется, что вложения вложенных предоставлять эти свойства. Установки значения указывает, что данные вложения не включена в сообщение, но доступны в распространенных файлового сервера. Эти свойства требуются в сочетании с любым флаги **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), которые указывают вложения по ссылке: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**или **ATTACH_BY_REF_ ТОЛЬКО**. 
  
Каждый каталог или имя файла ограничен имени восьми символов, а также расширения-трех символов. Общий путь ограничен до 256 символов. Платформа, которая поддерживает длинные имена файлов задайте оба этих свойств и **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Клиентские приложения следует использовать универсальное соглашение об именах (UNC) в большинстве случаев, когда файл является общей и следует использовать абсолютный путь, если файл является локальным.
  
MAPI для работы только с пути и имена файлов в формате ANSI набор знаков. Клиенты, использующие пути и имена файлов в набор символов OEM необходимо преобразовать их в формате ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства управляемый правами закодированный сообщений.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


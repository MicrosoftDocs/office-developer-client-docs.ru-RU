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
  
Содержит длинное имя и расширение вложения, исключая путь. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Идентификатор:  <br/> |0x3707  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства относятся к значениям ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE и ATTACH_BY_REF_ONLY свойств[PR_ATTACH_METHOD (PidTagAttachMethod).](pidtagattachmethod-canonical-property.md)  Платформы, поддерживающие длинные имена  файлов, должны устанавливать свойства PR_ATTACH_LONG_FILENAME и **PR_ATTACH_FILENAME** [(PidTagAttachFilename)](pidtagattachfilename-canonical-property.md)при  отправке и проверять PR_ATTACH_LONG_FILENAME при получении. 
  
Клиентский приложение должно настроить это свойство на предложенное длинное имя файла, которое будет использоваться, если хост-компьютер, получающий сообщение, поддерживает длинные имена файлов. **PR_ATTACH_LONG_FILENAME** можно использовать в качестве имени файла для сохранения вложения и для обеспечения расширения **файла,** если свойство [PR_ATTACH_EXTENSION (PidTagAttachExtension)](pidtagattachextension-canonical-property.md)не предоставлено. 
  
В отличие от имени файла, предоставленного **PR_ATTACH_FILENAME,** это имя не ограничивается имям файла с восемью символами, а также расширением с тремя символами. Вместо этого может быть до 256 символов, включая имя файла, расширение и период сепаратора. 
  
MAPI работает только с именами файлов в наборе символов ANSI. Клиентские приложения, которые используют имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных конвенций электронной почты в объекты сообщений.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Указывает свойства зашифрованных сообщений с управляемым правами.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для представления голосовой почты и факсимили.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mmapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


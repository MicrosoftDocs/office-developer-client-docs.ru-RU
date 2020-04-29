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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит полный путь и имя файла для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Идентификатор:  <br/> |0x370D  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства применяются при использовании любых значений свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), указывающих на вложение по ссылке: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**или **ATTACH_BY_REF_ONLY**. Платформы, поддерживающие длинные имена файлов, должны устанавливать как **PR_ATTACH_LONG_PATHNAME** , так и связанные свойства и свойства **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) при отправке, а также должны сначала проверять **PR_ATTACH_LONG_PATHNAME** или связанные свойства при получении. 
  
Клиентское приложение должно задать для этих свойств предложенный длинный путь и имя файла, который будет использоваться, если хостный компьютер, принимающий сообщение, поддерживает длинные имена файлов. Задание этих свойств указывает на то, что данные вложения не включены в сообщение, но доступны на общем файловом сервере. 
  
В отличие от каталогов и имен файлов, предоставленных **PR_ATTACH_PATHNAME**, эти каталоги и имена файлов не ограничиваются каталогом из восьми символов, а имя файла и расширением из трех символов. Вместо этого длина имени каталога или имени файла может доставлять до 256 символов, в том числе имя, расширение и период разделения. Однако общий путь ограничен 256 символами. 
  
В большинстве случаев клиенты должны использовать соглашение об именовании (UNC), если файл является общим, и использовать абсолютный путь, если файл является локальным.
  
MAPI работает только с путями и именами в наборе знаков ANSI. Клиентские приложения, использующие пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства сообщений, закодированных с помощью управления правами.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


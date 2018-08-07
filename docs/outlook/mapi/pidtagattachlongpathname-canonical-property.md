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
ms.openlocfilehash: a2230f2c2b1d4793c425694f76bb79fb7284c479
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810842"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Каноническое свойство PidTagAttachLongPathname

  
  
**Относится к**: Outlook 
  
Содержит полное длинный путь и имя файла вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Идентификатор:  <br/> |0x370D  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства могут быть применены при использовании значения свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), которые указывают вложений с помощью ссылки: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**или **ATTACH_BY _REF_ONLY**. Платформы, поддерживающие длинные имена файлов следует устанавливать **PR_ATTACH_LONG_PATHNAME** или связанные свойства и свойства **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) при отправке и должен проверить, **PR_ATTACH_LONG_PATHNAME **или сначала связанные свойства при приеме. 
  
Клиентское приложение следует задать эти свойства предложенного длинный путь и имя файла для использования в том случае, если компьютер, появления сообщения об ошибке поддерживает длинные имена файлов. Установка этих свойств указывает, что данные вложения не включена в сообщение, но доступны в распространенных файлового сервера. 
  
В отличие от предоставлено **PR_ATTACH_PATHNAME**имен файлов и папок эти имен файлов и папок, не ограничены восьми символов каталог или имя файла, а также расширения-трех символов. Вместо этого каждого каталог или имя файла может быть длиной до 256 символов, включая имя, расширение и разделителя групп разрядов периода. Тем не менее общий путь — это более 256 символов. 
  
Клиенты должны использовать универсальное соглашение об именах (UNC) в большинстве случаев при файл является общей и следует использовать абсолютный путь, когда локальный файл.
  
MAPI для работы только с пути и имена файлов в формате ANSI набор знаков. Клиентские приложения, использующие пути и имена файлов в кодировке OEM необходимо преобразовать их в формате ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства управляемый правами закодированный сообщений.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


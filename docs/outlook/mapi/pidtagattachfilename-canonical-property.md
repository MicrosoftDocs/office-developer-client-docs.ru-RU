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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит базовое имя файла и расширение вложения, за исключением пути.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W  <br/> |
|Идентификатор:  <br/> |0x3704  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы объекты вложений выдают эти свойства, относящиеся к значениям **ATTACH_BY_VALUE,** **ATTACH_BY_REFERENCE,** **ATTACH_BY_REF_RESOLVE** и **ATTACH_BY_REF_ONLY** свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod).](pidtagattachmethod-canonical-property.md) **PR_ATTACH_FILENAME** и связанные свойства необходимы при любом из этих значений. 
  
Эти свойства можно использовать в качестве рекомендуемой имени файла для сохранения вложения и для обеспечения расширения имени **файла, если** свойство [PR_ATTACH_EXTENSION (PidTagAttachExtension)](pidtagattachextension-canonical-property.md)не предоставлено. 
  
Имя файла может быть ограничено восемью символами, а также трех символьным расширением. Для платформы, поддерживаю которой поддерживаются длинные имена файлов, установите как это свойство, так и **свойство PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename).](pidtagattachlongfilename-canonical-property.md) 
  
MAPI работает только с именами файлов и другими строками, переданными ему, в наборе символов Американского национального института стандартов (ANSI). Клиентские приложения, которые используют имена файлов в наборе символов изготовителя оборудования (OEM), должны преобразовывать их в ANSI, прежде чем вызывать MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Указывает свойства сообщений в кодированной кодировки с управлением правами.
    
[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Указывает свойства зашифрованных и подписанных сообщений S/MIME.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
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


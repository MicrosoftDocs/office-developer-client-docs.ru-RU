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
ms.openlocfilehash: c5354618383a97b362348b14aea174d6f2266d6c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583283"
---
# <a name="pidtagattachfilename-canonical-property"></a>Каноническое свойство PidTagAttachFilename

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит имя базового файла и расширение, исключая путь вложения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W  <br/> |
|Идентификатор:  <br/> |0x3704  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется, что объекты вложения предоставлять эти свойства, которые относятся к значениям **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**и **ATTACH_BY_REF_ONLY** **PR_ATTACH_METHOD** Свойство ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). Связанные свойства и **PR_ATTACH_FILENAME** необходимы, когда используется одно из следующих значений. 
  
Эти свойства можно использовать в качестве предлагаемого имени файла для сохранения вложения и добавьте расширение имени файла, если свойство **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) не указан. 
  
Имя файла ограничен восемь символов, а также расширения-трех символов. Платформа, которая поддерживает длинные имена файлов задайте это свойство и свойство **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
MAPI для работы только с имена файлов и другие строки, переданным в него, в наборе символов American National стандартов института (ANSI). Клиентские приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства управляемый правами закодированный сообщений.
    
[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Указывает, подписанной и зашифрованной свойства сообщений S/MIME.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
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


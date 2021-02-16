---
title: Каноническое свойство PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355778"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемую имя автора первой версии сообщения, то есть сообщение перед переадащением или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W  <br/> |
|Идентификатор:  <br/> |0x004D  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства являются примерами свойств адреса для автора сообщения. При первой отправке сообщения клиентский приложение должно установить для этих свойств значение **PR_SENDER_NAME** ([PidTagSenderName).](pidtagsendername-canonical-property.md) Оно никогда не меняется, когда сообщение переадовыно или отвечает на него.
  
Исходные свойства автора позволяют сохранить информацию из-за пределов локального домена обмена сообщениями. Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, эти свойства обеспечивают способ обеспечения того, чтобы исходная информация не была потеряна.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


---
title: Каноническое свойство PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385650"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Каноническое свойство PidTagSubjectPrefix

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит префикс темы, который указывает на то, какие-либо действия в окне сообщения, например, «по: "для пересылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Идентификатор:  <br/> |0x003D  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства, рекомендуется использовать для всех объектов сообщения. 
  
Префикс Тема состоит из одного или нескольких буквенно-цифровых символов, за которым следует двоеточие и пробелом (который входят в состав префикс). Не должно содержать все символы перед двоеточием. Отсутствие префикса может быть представлена с пустой строке или это свойство не задано. 
  
Если эти свойства задаются явно, строка может быть любой длины и использовать любой буквенно-цифровых символов, но он должен соответствовать подстроки в начале свойство **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Если эти свойства не заданы отправителем и вычисляемые, их содержимое более ограничены. — Это правило вычислений префикс, что **PR_SUBJECT** должен начинаться с один, два или три буквы (к буквам и цифрам только) за которым следует двоеточие и пробел. При обнаружении таких подстроки в начале **PR_SUBJECT**его при этом становится строка для этих свойств (и не используется в начале **PR_SUBJECT**). В противном случае эти свойства остаются неопределенные. 
  
Эти свойства и **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) следует вычисляется как часть реализации [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Клиент должен не запрашивать пользователя [IMAPIProp::GetProps](imapiprop-getprops.md) для их значения до их фиксации вызовом **IMAPIProp::SaveChanges** . 
  
Свойства темы — это обычно коротких строк менее 256 символов и поставщика хранилища сообщений не обязаны поддержки интерфейса OLE **IStream** на них. Клиент должен всегда сначала попытаться доступ через интерфейс **IMAPIProp** и прибегать к **IStream** только в том случае, если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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


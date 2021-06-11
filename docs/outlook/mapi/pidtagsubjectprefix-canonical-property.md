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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339230"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Каноническое свойство PidTagSubjectPrefix

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит префикс субъекта, который обычно указывает какое-либо действие на сообщение, например "FW: " для переададки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Идентификатор:  <br/> |0x003D  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства рекомендуется использовать во всех объектах сообщений. 
  
Префикс субъекта состоит из одного или нескольких букв, за которыми следуют двоеточие и пространство (которые являются частью префикса). Он не должен содержать никаких неальфанумерных символов перед двоеточием. Отсутствие префикса может быть представлено пустой строкой или не заданной этим свойством. 
  
Если эти свойства задаются явно, строка может иметь любую длину и использовать любые буквенные символы,  но она должна соответствовать подстройке в начале свойства[PR_SUBJECT (PidTagSubject).](pidtagsubject-canonical-property.md) Если эти свойства не установлены отправительом и должны быть вычислены, их содержимое более ограничено. Правило вычисления префикса: PR_SUBJECT  должны начинаться с одной, двух или трех букв (только в алфавитном порядке), а затем двоеточия и пространства. Если такое подстройка найдена в начале **PR_SUBJECT,** она становится строкой для этих свойств (а также остается в **начале PR_SUBJECT).** В противном случае эти свойства остаются неустановленным. 
  
Эти свойства и **PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)должны быть вычислены в рамках реализации [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Клиент не должен вызывать [IMAPIProp::GetProps](imapiprop-getprops.md) для своих значений, пока они не были совершены **вызовом IMAPIProp::SaveChanges.** 
  
Свойства субъекта обычно являются небольшими строками менее 256 символов, и поставщик магазина сообщений не обязан поддерживать интерфейс OLE **IStream** на них. Клиент всегда должен сначала попытаться получить доступ через **интерфейс IMAPIProp** и прибегать к **IStream** только MAPI_E_NOT_ENOUGH_MEMORY **возвращается.** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые на объектах сообщений электронной почты.
    
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


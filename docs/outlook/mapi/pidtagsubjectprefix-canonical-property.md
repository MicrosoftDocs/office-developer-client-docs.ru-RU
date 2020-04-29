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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит префикс темы, который обычно указывает на некоторые действия с сообщением, например "FW:" для переадресации. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A PR_SUBJECT_PREFIX_W  <br/> |
|Идентификатор:  <br/> |0x003D  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства рекомендуются для всех объектов Message. 
  
Префикс темы состоит из одного или нескольких буквенно-цифровых символов, за которыми следует двоеточие и пробел (часть префикса). Он не должен содержать небуквенно-цифровых символов перед двоеточием. Отсутствие префикса может быть представлено пустой строкой или это свойство не задается. 
  
Если эти свойства заданы явно, строка может иметь любую длину и использовать любые буквенно-цифровые символы, но она должна соответствовать подстроке в начале свойства **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Если эти свойства не заданы отправителем и должны быть вычислены, их содержимое будет более ограниченным. Правило для вычисления префикса состоит в том, что **PR_SUBJECT** должен начинаться с одной, двух или трех букв (только алфавит), за которыми следует двоеточие и пробел. Если такая подстрока найдена в начале **PR_SUBJECT**, она становится строкой для этих свойств (а также остается в начале **PR_SUBJECT**). В противном случае эти свойства будут неопределенными. 
  
Эти свойства и **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) должны вычисляться как часть реализации [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Клиент не должен запрашивать [IMAPIProp::/PROPS](imapiprop-getprops.md) для их значений до тех пор, пока они не будут зафиксированы вызовом **IMAPIProp:: SaveChanges** . 
  
В свойствах subject обычно используются небольшие строки менее 256 символов, а поставщик хранилища сообщений не обязан поддерживать интерфейс OLE **IStream** . Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** , а затем последовательно прибегнуть к **IStream** , только если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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


---
title: Каноническое свойство PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339258"
---
# <a name="pidtagsubject-canonical-property"></a>Каноническое свойство PidTagSubject

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит полный текст сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Идентификатор:  <br/> |0x0037  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства рекомендуется использовать во всех объектах сообщений. 
  
Эти свойства всегда являются полным текстом темы, т. е. консатация префикса и нормализуемого субъекта. Если префикса нет, то нормализуемая тема должна быть такой же, как и субъект. Хранилище сообщений или поставщик транспорта использует как эти свойства, так и **свойства PR_SUBJECT_PREFIX** [(PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md)для вычисления нормализуемого субъекта с помощью правила, описанного в **PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject).](pidtagnormalizedsubject-canonical-property.md)
  
Свойства субъекта обычно являются небольшими строками менее 256 символов, и поставщик магазина сообщений не обязан поддерживать интерфейс **IStream** на них. Клиент всегда должен сначала попытаться получить доступ через **интерфейс IMAPIProp** и прибегать к **IStream** только MAPI_E_NOT_ENOUGH_MEMORY **возвращается.** 
  
Для отчета это свойство содержит объект исходного сообщения, предшествующий строке, указывающей, что произошло с сообщением.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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


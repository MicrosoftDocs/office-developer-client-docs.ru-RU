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
  
Содержит полную тему сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СУБЖЕКТ, ПР_СУБЖЕКТ_А, ПР_СУБЖЕКТ_В  <br/> |
|Идентификатор:  <br/> |0x0037  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Комментарии

Эти свойства рекомендуются для всех объектов Message. 
  
Эти свойства всегда являются полным текстом темы, то есть объединением префикса и нормализованной темы. Если префикс отсутствует, нормализованная тема должна совпадать с темой. Хранилище сообщений или поставщик транспорта используют как эти свойства, так и свойства **пр_субжект_префикс** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) для вычисления нормализованной темы с использованием правила, описанного в разделе **пр_нормализед_субжект** ([ PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
В свойствах subject обычно используются небольшие строки менее 256 символов, а поставщик хранилища сообщений не обязан поддерживать интерфейс **IStream** . Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** , а в **** случае возврата мапи_е_нот_енаугх_мемори — только при возвращении **** . 
  
Для отчета это свойство содержит тему исходного сообщения, которая предшествует строке, указывающей на то, что произошло с сообщением.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


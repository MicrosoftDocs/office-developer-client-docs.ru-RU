---
title: Каноническое свойство PidTagSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358914"
---
# <a name="pidtagsenderentryid-canonical-property"></a>Каноническое свойство PidTagSenderEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи отправителя сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕНДЕР_ЕНТРИД  <br/> |
|Идентификатор:  <br/> |0x0C19  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса отправителя сообщения. Он должен быть задан поставщиком исходящей транспортировки, который никогда не должен распространять какие бы то ни было существующие значения.
  
Если поставщик транспорта не предоставил свойства адреса отправителя, то диспетчер очереди MAPI пытается заполнить их, вызвав метод [IMAPISession:: куеридентити](imapisession-queryidentity.md) для идентификатора записи. Если не указаны никакие идентификаторы записей, диспетчер очереди MAPI имеет идентификатор, соответствующий строке "Unknown" в этом свойстве. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСОРСС]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Задает свойства и операции, представляющие элементы RSS.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
[[MS — ОКСОПОСТ]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов POST.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


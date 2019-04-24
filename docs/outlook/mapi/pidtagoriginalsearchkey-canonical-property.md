---
title: Каноническое свойство PidTagOriginalSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d106a216e8d72c126f3293f9d492db73992c3872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355295"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a>Каноническое свойство PidTagOriginalSearchKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит исходный ключ поиска для записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ОРИГИНАЛ_СЕАРЧ_КЭЙ  <br/> |
|Идентификатор:  <br/> |0x3A14  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств, содержащих сведения о первоначальном источнике скопированной записи.
  
Для отчета о непрочтении это свойство содержит копию ключа поиска исходного получателя сообщения, для которого создается отчет. Когда исходный получатель входит в список рассылки, ключ поиска списка рассылки сохраняется для отчета.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
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


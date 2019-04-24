---
title: Каноническое свойство PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360944"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>Каноническое свойство PidNameAcceptLanguage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка [RFC3282] Accept. Language.
  
|||
|:-----|:-----|
|Понятные имена:  <br/> |Акцептлангуаже  <br/> |
|Набор свойств:  <br/> |ПС_ИНТЕРНЕТ_ХЕАДЕРС  <br/> |
|Имя свойства:  <br/> |Accept-Language  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать значение этого свойства, клиенты с многоцелевыми расширениями Интернет-сообщений (MIME) должны записать поле заголовка Accept-Language с желаемым значением. Клиенты MIME могут создавать вместо этого поле заголовка X — Accepting. Считыватели MIME должны скопировать значение любого поля заголовка в значение этого свойства. Если оба поля заголовков присутствуют, то для средств чтения MIME необходимо использовать поле заголовка Accept – Language.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


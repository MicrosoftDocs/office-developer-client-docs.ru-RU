---
title: Каноническое свойство PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279631"
---
# <a name="pidtaglisthelp-canonical-property"></a>Каноническое свойство PidTagListHelp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка справки для многоцелевого почтового расширения в Интернете (MIME).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ЛИСТ_ХЕЛП, ПР_ЛИСТ_ХЕЛП_А, ПР_ЛИСТ_ХЕЛП_В  <br/> |
|Идентификатор:  <br/> |0x1043  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы создать поле заголовка списка справки, клиентам необходимо задать для свойства **пр_лист_хелп** или связанного свойства нужное значение. Модули записи MIME должны скопировать это значение в поле заголовка List – Help. 
  
Чтобы задать значение этих свойств, связанных с сервером, клиенты MIME должны записать поля заголовков, как указано в следующей таблице:
  
|**Property**|**Имя основного поля заголовка**|**Имя поля альтернативного заголовка**|
|:-----|:-----|:-----|
|**ПР_ЛИСТ_ХЕЛП** <br/> |List – Справка  <br/> |Список "X" — Справка  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
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


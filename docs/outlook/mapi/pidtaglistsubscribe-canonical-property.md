---
title: Каноническое свойство PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279659"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>Каноническое свойство PidTagListSubscribe

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка List-Subscribe-почтовые расширения для многоцелевого протокола (MIME).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A PR_LIST_SUBSCRIBE_W  <br/> |
|Идентификатор:  <br/> |0x1044  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Для создания поля заголовка List – Subscribe клиенты должны присвоить значениям этих свойств нужное значение. Записи MIME должны копировать значения этих свойств в поле заголовка List – Subscribe.
  
Чтобы задать значения свойств, связанных с сервером, клиенты MIME должны записать поля заголовков, как указано в следующей таблице.
  
|**Свойство**|**Имя основного поля заголовка**|**Имя поля альтернативного заголовка**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |List – Subscribe  <br/> |X – List — Subscribe  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
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


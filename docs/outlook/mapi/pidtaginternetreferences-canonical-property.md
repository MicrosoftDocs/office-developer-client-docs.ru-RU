---
title: Каноническое свойство PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360412"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Каноническое свойство PidTagInternetReferences

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка REFERENCES для многоцелевого почтового расширения Интернета (MIME).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A PR_INTERNET_REFERENCES_W  <br/> |
|Идентификатор:  <br/> |0x1039  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы создать поле заголовка References, клиенты должны задать для этих свойств нужное значение. Записи MIME должны копировать значения этих свойств в поле заголовка References.
  
Чтобы задать значение этих свойств, клиенты MIME должны записать нужное значение в поле заголовка References. Устройства чтения MIME должны копировать значение поля заголовка References в эти свойства. Средства чтения MIME могут усечь значение этих свойств, если длина превышает 64 КБ.
  
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


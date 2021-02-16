---
title: Каноническое свойство PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344977"
---
# <a name="pidlidcategories-canonical-property"></a>Каноническое свойство PidLidCategories

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает список категорий для элемента.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidCategories  <br/> |
|Набор свойств:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00002328  <br/> |
|Тип данных:  <br/> |PT_MV_UNICODE  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы создать поле загона ключевых слов, клиенты должны установить для этого свойства нужные значения. Это свойство имеет несколько строк; каждая категория должна быть соедина с одним ключевым словом.
  
Авторы MIME должны скопировать каждое под значение этого свойства в отдельное ключевое слово в поле "Ключевые слова" с запятой (U+002C) и пробелом (U+0020), отделяющие каждое ключевое слово. MIME writers may drop this property instead of copying it to the keywords header field, to avoid conflict among different sets of categories in different organizations.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


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
ms.openlocfilehash: 6893afa11cc08b335b0ffb39b725e26478dae22f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574841"
---
# <a name="pidlidcategories-canonical-property"></a>Каноническое свойство PidLidCategories

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает список категорий для элемента.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidCategories  <br/> |
|Набор свойств:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00002328  <br/> |
|Тип данных:  <br/> |PT_MV_UNICODE  <br/> |
|Область:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы создать поле заголовка ключевые слова, клиенты необходимо присвоить значение этого свойства необходимые значения. Это свойство имеет несколько строк; каждой категории должна быть сопоставлена с одного ключевого слова.
  
Записи Multipurpose Internet Mail Extensions (MIME) следует скопировать каждого подменю значение этого свойства для отдельных ключевое слово в поле Заголовок ключевые слова с запятой (U + 002 C) и разделения пространства (U + 0020) каждого ключевого слова. Записи MIME может удалить это свойство вместо копирования поле заголовка ключевые слова, чтобы избежать конфликтов между различными наборами категорий в различных организациях.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


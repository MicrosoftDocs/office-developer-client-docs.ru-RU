---
title: Каноническое свойство PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 91eb93c9cf3afcecef698e27791c06831c13624d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589100"
---
# <a name="pidnamecontentbase-canonical-property"></a>Каноническое свойство PidNameContentBase

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка [RFC3282] Content-Base.
  
|||
|:-----|:-----|
|Понятные имена:  <br/> |BodyContentBase  <br/> |
|Набор свойств:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Имя свойства:  <br/> |Content-Base  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) необходимо создать нужное значение в поле Заголовок Content-Base в сущности MIME, которая сопоставлена с текст сообщения. Читатели MIME необходимо скопировать значение в поле Заголовок Content-Base в сущности MIME значение этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
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


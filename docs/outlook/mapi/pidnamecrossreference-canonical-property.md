---
title: Каноническое свойство PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382500"
---
# <a name="pidnamecrossreference-canonical-property"></a>Каноническое свойство PidNameCrossReference

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка перекрестные ссылки на модель [RFC3282].
  
|||
|:-----|:-----|
|Понятные имена:  <br/> |Отсутствует  <br/> |
|Набор свойств:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Имя свойства:  <br/> |Перекрестные ссылки на модель  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) необходимо создать нужное значение в поле Заголовок перекрестные ссылки на модель. Читатели MIME необходимо скопировать значение поля заголовка перекрестные ссылки на модель значение этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


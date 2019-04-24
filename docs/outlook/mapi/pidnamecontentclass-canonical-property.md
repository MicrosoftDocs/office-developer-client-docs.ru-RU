---
title: Каноническое свойство PidNameContentClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356352"
---
# <a name="pidnamecontentclass-canonical-property"></a>Каноническое свойство PidNameContentClass

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка Content – class [RFC3282].
  
|||
|:-----|:-----|
|Понятные имена:  <br/> |Нет  <br/> |
|Набор свойств:  <br/> |ПС_ИНТЕРНЕТ_ХЕАДЕРС  <br/> |
|Имя свойства:  <br/> |Content – class  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать значение этого свойства, клиенты с многоцелевыми расширениями Интернет-сообщений (MIME) должны записать поле заголовка Content-class с требуемым значением. Считыватели MIME должны скопировать значение поля заголовка Content – class в значение этого свойства. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства сообщений, закодированных с помощью управления правами.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


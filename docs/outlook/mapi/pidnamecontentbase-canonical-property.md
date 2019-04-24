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
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331502"
---
# <a name="pidnamecontentbase-canonical-property"></a>Каноническое свойство PidNameContentBase

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка Content — Base (RFC3282]).
  
|||
|:-----|:-----|
|Понятные имена:  <br/> |Бодиконтентбасе  <br/> |
|Набор свойств:  <br/> |ПС_ИНТЕРНЕТ_ХЕАДЕРС  <br/> |
|Имя свойства:  <br/> |Content — Base  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы задать значение этого свойства, клиенты с многоцелевыми расширениями Интернет-сообщений (MIME) должны записать нужное значение в поле заголовка Content-Base для объекта MIME, который сопоставляется с текстом сообщения. Считыватели MIME должны скопировать значение поля заголовка Content – Base для такой сущности MIME в значение этого свойства.
  
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


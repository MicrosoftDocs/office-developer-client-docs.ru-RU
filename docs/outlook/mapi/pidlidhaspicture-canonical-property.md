---
title: Каноническое свойство PidLidHasPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357752"
---
# <a name="pidlidhaspicture-canonical-property"></a>Каноническое свойство PidLidHasPicture

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, существует ли вложение с фото для контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидхаспиктуре  <br/> |
|Набор свойств:  <br/> |Псетид_аддресс  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008015  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство существует и имеет значение TRUE, таблица вложений контакта содержит вложение со свойством **пр_аттачмент_контактфото** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)), для которого установлено значение true.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


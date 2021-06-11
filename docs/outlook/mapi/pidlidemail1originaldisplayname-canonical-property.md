---
title: Каноническое свойство PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335044"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a>Каноническое свойство PidLidEmail1OriginalDisplayName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает имя первого отображения, соответствующее указанному для контакта адресу электронной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidEmail1OriginalDisplayName  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008084  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Если значение свойства **dispidEmail1AddrType** [(PidLidEmail1AddressType)](pidlidemail1addresstype-canonical-property.md)является "SMTP", значение соответствующего свойства **dispidEmail1OriginalDisplayName** должно равняться значению соответствующего свойства **dispidEmail1EmailAddress** [(PidLidEmail1EmailAddress).](pidlidemail1emailaddress-canonical-property.md) Это свойство отображает альтернативный удобным для пользователя адрес, эквивалентный адресу в **свойстве dispidEmail1EmailAddress.** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


---
title: Каноническое свойство PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338075"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a>Каноническое свойство PidLidEmail3OriginalDisplayName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает третье имя отображения, соответствующее адресу электронной почты, указанному для контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidEmail3OriginalDisplayName  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x000080A4  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Если значение свойства **dispidEmail3AddrType** [(PidLidEmail3AddressType)](pidlidemail3addresstype-canonical-property.md)является "SMTP", значение соответствующего свойства **dispidEmail3OriginalDisplayName** должно равняться значению соответствующего **dispidEmail3EmailAddress** [(PidLidEmail3EmailAddress).](pidlidemail3emailaddress-canonical-property.md) Целью этого свойства является отображение альтернативного удобного для пользователя адреса, эквивалентного адресу **dispidEmail3EmailAddress.**
  
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


---
title: Каноническое свойство PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337963"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>Каноническое свойство PidLidEmail2OriginalDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает второе отображаемого имени, соответствующее адресу электронной почты, указанному для контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008094  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если свойство **dispidEmail2AddrType** ([PidLidEmail2AddressType)](pidlidemail2addresstype-canonical-property.md)имеет значение "SMTP", значение соответствующего свойства **PidLidEmail2OriginalDisplayName** должно быть равно значению соответствующего свойства **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress).](pidlidemail2emailaddress-canonical-property.md) Это свойство предназначено для отображения альтернативного удобного адреса, эквивалентного адресу **dispidEmail2EmailAddress.**
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


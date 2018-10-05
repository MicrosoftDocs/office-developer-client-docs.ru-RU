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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397774"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>Каноническое свойство PidLidEmail2OriginalDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает второй отображаемое имя, соответствующий адрес электронной почты, указанный для этого контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008094  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение свойства **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) «SMTP», значение соответствующего свойства **PidLidEmail2OriginalDisplayName** должно быть равно значение соответствующих ** dispidEmail2EmailAddress** свойство ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)). Это свойство предназначено для отображения альтернативный понятное адрес, который соответствует тому в **dispidEmail2EmailAddress**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


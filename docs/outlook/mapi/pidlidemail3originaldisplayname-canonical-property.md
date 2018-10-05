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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389080"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a>Каноническое свойство PidLidEmail3OriginalDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, третий отображаемое имя, соответствующий адрес электронной почты, указанный для этого контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidEmail3OriginalDisplayName  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x000080A4  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение свойства **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) «SMTP», значение свойства соответствующих **dispidEmail3OriginalDisplayName** должно быть равно значение соответствующих ** dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)). Это свойство предназначено для отображения альтернативный понятное адрес, который соответствует тому в **dispidEmail3EmailAddress**.
  
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


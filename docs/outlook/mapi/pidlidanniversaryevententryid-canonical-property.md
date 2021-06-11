---
title: Каноническое свойство PidLidAnniversaryEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335576"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a>Каноническое свойство PidLidAnniversaryEventEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает идентификатор записи встречи, которая представляет годовщину контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidAnniversaryEventEID  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x0000804E  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Назначение, указанное свойством **dispidAnniversaryEventEventEID,** должно быть связано с этим контактом с помощью **dispidContactLinkEntry** [(PidLidContactLinkEntry),](pidlidcontactlinkentry-canonical-property.md) **dispidContactLinkSearchKey** [(PidLidContactLinkSearchKey)](pidlidcontactlinksearchkey-canonical-property.md)и **dispidContactLinkLinkName** [(PidLidContactLinkLinkName](pidlidcontactlinkname-canonical-property.md)) свойств, как описано [в [MS-OXCMSG].](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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


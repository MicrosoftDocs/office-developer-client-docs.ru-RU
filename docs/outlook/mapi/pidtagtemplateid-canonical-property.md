---
title: Каноническое свойство PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396395"
---
# <a name="pidtagtemplateid-canonical-property"></a>Каноническое свойство PidTagTemplateid

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), выраженное как формат идентификатора навсегда.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TEMPLATEID  <br/> |
|Идентификатор:  <br/> |0x3902  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |�������� ����� MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это значение должно присутствовать для всех объектов адресной книги на сервере интерфейса поставщика имя службы (NSPI), его различающееся имя (DN) должен совпадать со значением **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и его различающееся имя необходимо следовать формату различающееся имя Спецификация определенный тип объекта. 
  
Это свойство не указан на объекты в автономной адресной книги.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


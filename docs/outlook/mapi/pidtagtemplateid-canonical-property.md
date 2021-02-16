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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358823"
---
# <a name="pidtagtemplateid-canonical-property"></a>Каноническое свойство PidTagTemplateid

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит **PR_ENTRYID** ([PidTagEntryId),](pidtagentryid-canonical-property.md)выраженный в виде формата постоянной записи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TEMPLATEID  <br/> |
|Идентификатор:  <br/> |0x3902  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |�������� ����� MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение должно присутствовать для всех объектов адресной книги на сервере интерфейса поставщика службы имен (NSPI), его различается имя должно соответствовать значению **PR_EMAIL_ADDRESS** ([PidTagEmailAddress),](pidtagemailaddress-canonical-property.md)а его DN должно соответствовать спецификации формата DN, определенного типу объекта. 
  
Это свойство не присутствует для объектов в автономной адресной книге.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


---
title: Каноническое свойство PidTagGovernmentIdNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGovernmentIdNumber
api_type:
- HeaderDef
ms.assetid: fa265d37-a1ea-4812-8fe9-21dac374cd7c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4b7ce4620f224597e753fb05ec377461b4c19c9a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398453"
---
# <a name="pidtaggovernmentidnumber-canonical-property"></a>Каноническое свойство PidTagGovernmentIdNumber

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор государственных организаций для получателя. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_GOVERNMENT_ID_NUMBER, PR_GOVERNMENT_ID_NUMBER_A, PR_GOVERNMENT_ID_NUMBER_W  <br/> |
|Идентификатор:  <br/> |0x3A07  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства предоставляют идентификации и доступа к сведениям о получателе. Они определены получателя и организации получателя. 
  
Эти свойства часто устанавливаются номер паспорта, граждане номер или номер налогоплательщика, такие как номера социального страхования. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


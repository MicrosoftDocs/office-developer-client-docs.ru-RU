---
title: Каноническое свойство PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55db507055692c9e929b0125abf719d8c03ac967
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811416"
---
# <a name="pidtagnull-canonical-property"></a>Каноническое свойство PidTagNull

  
  
**Относится к**: Outlook 
  
Представляет значение null или параметры свойства или резервирует массива.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NULL  <br/> |
|Идентификатор:  <br/> |0x0000  <br/> |
|Тип данных:  <br/> |PT_NULL  <br/> |
|Область:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется для сохранения места в массивах структур [SPropValue](spropvalue.md) . Используется в массив структур [SPropTagArray](sproptagarray.md) определить метод для сохранения места в возвращаемый массив структур **SPropValue** . Это позволяет вычисленные свойства следует реализовать в недорогим способом. 
  
Для получения дополнительных сведений см [MAPI свойство типа](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые на контакты и списки рассылки.
    
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


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
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329269"
---
# <a name="pidtagnull-canonical-property"></a>Каноническое свойство PidTagNull

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет значение null или параметр пространства массива свойств или резервов.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NULL  <br/> |
|Идентификатор:  <br/> |0x0000  <br/> |
|Тип данных:  <br/> |PT_NULL  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для резерва пространства в массивах [структур SPropValue.](spropvalue.md) Он используется в массиве [структур SPropTagArray,](sproptagarray.md) чтобы сообщить методу, чтобы зарезервировать пространство в возвращаемом массиве **структур SPropValue.** Это позволяет недорого заполнять вычислительные свойства. 
  
Дополнительные сведения см. в обзоре типов [свойств MAPI.](mapi-property-type-overview.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


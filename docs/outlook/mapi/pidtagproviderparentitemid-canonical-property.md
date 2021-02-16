---
title: Каноническое свойство PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433418"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Каноническое свойство PidTagProviderParentItemId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает идентификатор родительского элемента папки или элемента в хранилище.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Идентификатор:  <br/> |0x0EA4  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MAPI, не передаваемый  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщики магазина могут указать значение для этого свойства для родительского элемента папки или элемента, но должны сохранять одинаковое значение между сеансами. Поставщики магазина используют это свойство для идентификации результатов поиска, возвращаемой поисковой системы.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


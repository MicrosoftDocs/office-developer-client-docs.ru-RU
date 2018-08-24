---
title: Каноническое свойство PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572839"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Каноническое свойство PidTagProviderItemId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает идентификатор для папки или элемента в хранилище.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Идентификатор:  <br/> |0x0EA3  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщики хранилища можно указать значение для этого свойства для папки или элемента, но необходимо учитывать значения, то же самое, между сеансами. Это свойство использовать поставщиков хранилища для идентификации результаты поиска, возвращаемые из поисковой системы.
  
## <a name="related-resources"></a>Связанные ресурсы

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


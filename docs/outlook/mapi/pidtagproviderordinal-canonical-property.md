---
title: Каноническое свойство PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438353"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Каноническое свойство PidTagProviderOrdinal

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит нулевой индекс позиции поставщика услуг в таблице поставщика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Идентификатор:  <br/> |0x300D  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI общие  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство вычисляется MAPI.
  
Получение таблицы поставщика с помощью метода [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Сортировка таблицы поставщика в этом свойстве для отображения порядка транспортировки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


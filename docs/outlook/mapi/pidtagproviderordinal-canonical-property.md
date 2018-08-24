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
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573812"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Каноническое свойство PidTagProviderOrdinal

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит начинающийся с нуля индекс положения поставщика услуг в таблице поставщика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Идентификатор:  <br/> |0x300D  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Распространенные MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство вычисляется путем MAPI.
  
В таблице поставщика получите путем вызова метода [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) . Сортировка в таблице поставщика для данного свойства для отображения порядка транспорта. 
  
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


---
title: Каноническое свойство PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c024f71279fac5dbb3d771442d9fbfb8a50e0f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578873"
---
# <a name="pidtagformhostmap-canonical-property"></a>Каноническое свойство PidTagFormHostMap

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит карты узла из доступных форм. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FORM_HOST_MAP  <br/> |
|Идентификатор:  <br/> |0x3306  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Распространенные MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Клиентское приложение следует обновить это свойство, а также свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), при изменении базовой структуры в интерфейсе **IMAPIFormProp** . 
  
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


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
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433768"
---
# <a name="pidtagformhostmap-canonical-property"></a>Каноническое свойство PidTagFormHostMap

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит карту узла Доступные формы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ФОРМ_ХОСТ_МАП  <br/> |
|Идентификатор:  <br/> |0x3306  <br/> |
|Тип данных:  <br/> |ПТ_МВ_ЛОНГ  <br/> |
|Область:  <br/> |Общие протоколы MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Клиентское приложение должно обновлять это свойство вместе со свойством **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) при изменении базовой структуры в интерфейсе **имапиформпроп** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


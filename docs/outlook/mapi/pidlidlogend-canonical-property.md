---
title: Каноническое свойство PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336927"
---
# <a name="pidlidlogend-canonical-property"></a>Каноническое свойство PidLidLogEnd

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет дату и время окончания сообщения журнала.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидложенд  <br/> |
|Набор свойств:  <br/> |PSETID_Log  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008708  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Журнал  <br/> |
   
## <a name="remarks"></a>Примечания

Время окончания действия в формате UTC (UTC), которое должно совпадать со свойством **диспидкоммоненд** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) и большим или равным значению свойства **диспидлогстарт** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОЖРНЛ]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для журналов.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


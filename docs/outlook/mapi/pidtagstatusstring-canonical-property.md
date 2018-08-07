---
title: Каноническое свойство PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811954"
---
# <a name="pidtagstatusstring-canonical-property"></a>Каноническое свойство PidTagStatusString

  
  
**Относится к**: Outlook 
  
Содержит сообщение, указывающее текущее состояние сеанса ресурсов. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Идентификатор:  <br/> |0x3E08  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства предоставьте поставщиков услуг и MAPI возможность предоставить определенные сведения о состоянии сеанса ресурса, например интегрированной адресной книги или поставщик конкретной службы. Это свойство объясняется, а также предоставляются дополнительные сведения о код состояния или свойство **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). В то время как **PR_STATUS_CODE** является обязательным для всех объектов состояния, **PR_STATUS_STRING** и связанные свойства являются необязательными. Когда поставщика транспорта не задано значение, диспетчер очереди MAPI предоставляет значение по умолчанию. 
  
Строка создается в части удаленный вызов процедур, как диспетчер очереди MAPI; он проходит через общей памяти, а не выполняется упаковать через границы процессов.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


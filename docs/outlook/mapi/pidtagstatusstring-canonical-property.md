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
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421566"
---
# <a name="pidtagstatusstring-canonical-property"></a>Каноническое свойство PidTagStatusString

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сообщение с указанием текущего состояния ресурса сеанса. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СТАТУС_СТРИНГ, ПР_СТАТУС_СТРИНГ_А, ПР_СТАТУС_СТРИНГ_В  <br/> |
|Идентификатор:  <br/> |0x3E08  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства предоставляют поставщикам услуг и MAPI возможность предоставлять конкретные сведения о состоянии ресурса сеанса, например интегрированной адресной книге или определенном поставщике услуг. Это свойство объясняет и предоставляет дополнительные сведения о коде состояния или свойстве **пр_статус_коде** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). В то время как **пр_статус_коде** является обязательным для всех объектов status, **пр_статус_стринг** и связанные свойства являются необязательными. Когда поставщик транспорта не предоставляет значение, диспетчер очереди MAPI предоставляет значение по умолчанию. 
  
Строка создается на той же стороне удаленного вызова процедуры, что и Диспетчер очереди MAPI; он перемещается через общую память, а не упаковывается в пределах границы процесса.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


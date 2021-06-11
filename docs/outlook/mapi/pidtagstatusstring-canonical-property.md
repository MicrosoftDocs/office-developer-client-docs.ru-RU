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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сообщение, которое указывает текущее состояние ресурса сеанса. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Идентификатор:  <br/> |0x3E08  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства дают поставщикам услуг и MAPI возможность предоставить конкретные сведения о состоянии ресурса сеанса, например интегрированной адресной книги или конкретного поставщика услуг. Это свойство объясняет и предоставляет дополнительные сведения о коде состояния или **свойстве PR_STATUS_CODE** [(PidTagStatusCode).](pidtagstatuscode-canonical-property.md) Если **PR_STATUS_CODE** требуется для всех объектов **состояния,** PR_STATUS_STRING и связанные свойства необязательны. Если поставщик транспорта не обеспечивает значение, шпалер MAPI поставляет значение по умолчанию. 
  
Строка создается на той же стороне удаленного вызова процедуры, что и шпалер MAPI; он проходит через общую память, а не проходит через границу процесса.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


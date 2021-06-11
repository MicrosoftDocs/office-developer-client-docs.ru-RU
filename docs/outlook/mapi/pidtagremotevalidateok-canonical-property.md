---
title: Каноническое свойство PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424226"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Каноническое свойство PidTagRemoteValidateOk

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит TRUE, если удаленному зрителю разрешено вызывать [метод IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Идентификатор:  <br/> |0x3E0D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство отображается в таблице состояния и обеспечивает определенный контроль над производительностью транспорта. Это можно рассматривать как еще один способ направлять удаленного зрителя на простое. Если установлено true, удаленный зритель может вызывать **IMAPIStatus::ValidateState** так часто, как нужно. Значение FALSE указывает на то, что удаленный зритель не может больше звонить. 
  
Поставщик транспорта обычно задает это свойство динамически, установив значение FALSE для отключения дополнительных вызовов, если поставщик транспорта имеет достаточный объем обработки для выполнения. После этого поставщик транспорта задает значение TRUE, позволяя клиентской приложению делать дополнительные вызовы **IMAPIStatus::ValidateState.** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


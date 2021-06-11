---
title: Каноническое свойство PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426529"
---
# <a name="pidtagserviceuid-canonical-property"></a>Каноническое свойство PidTagServiceUid

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит [структуру MAPIUID](mapiuid.md) для службы сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_UID  <br/> |
|Идентификатор:  <br/> |0x3D0C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство вычисляется MAPI на объектах раздела профилей. MAPI использует его для группировки всех поставщиков, принадлежащих к одной и той же службе сообщений. Это свойство предоставляется в качестве параметра для большинства методов [IMsgServiceAdmin.](imsgserviceadminiunknown.md) Он не должен отображаться в Mapisvc.inf. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


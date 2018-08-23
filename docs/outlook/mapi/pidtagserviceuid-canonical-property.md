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
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582254"
---
# <a name="pidtagserviceuid-canonical-property"></a>Каноническое свойство PidTagServiceUid

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит структуру [MAPIUID](mapiuid.md) для службы сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_UID  <br/> |
|Идентификатор:  <br/> |0x3D0C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство вычисляется путем MAPI на объекты раздела профиля. MAPI используется для группирования всех поставщиков, относящихся к одной службы сообщений. Это свойство предоставляется в качестве параметра Большинство методов [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Он должен отображаться в Mapisvc.inf. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


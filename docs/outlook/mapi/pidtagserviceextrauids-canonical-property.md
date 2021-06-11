---
title: Каноническое свойство PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422308"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Каноническое свойство PidTagServiceExtraUids

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список структур [MAPIUID,](mapiuid.md) которые определяют дополнительные разделы профилей для службы сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Идентификатор:  <br/> |0x3D0D  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Для каждого фильтра сообщений могут быть созданы новые разделы профилей. При копировании сведений о службе сообщений в другой профиль важно также скопировать дополнительные разделы профилей для фильтров. Поставщик услуг, использующий дополнительные разделы профилей, может хранить структуры **MAPIUID** этих разделов профилей в **PR_SERVICE_EXTRA_UIDS,** что позволяет MAPI скопировать дополнительные сведения службы сообщений.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


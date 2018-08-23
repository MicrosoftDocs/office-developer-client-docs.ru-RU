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
ms.openlocfilehash: 0deb1b34a437d47ab53cdb2e13cda006d9116f65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570123"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Каноническое свойство PidTagServiceExtraUids

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит список структур [MAPIUID](mapiuid.md) , чтобы указать дополнительный профиль разделы для службы сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Идентификатор:  <br/> |0x3D0D  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Можно создавать новые разделы профиль для каждого фильтра сообщений. При со сведениями о службе сообщений для копирования в другой профиль необходимость копирования в разделах дополнительный профиль для фильтров также. Поставщик службы, который использует разделах дополнительных профилей можно хранить структур **MAPIUID** разделам профилей в **PR_SERVICE_EXTRA_UIDS**, что позволяет MAPI для копирования сведений о службе дополнительное сообщение.
  
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


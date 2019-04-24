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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328730"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Каноническое свойство PidTagServiceExtraUids

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список структур [мапиуид](mapiuid.md) , которые определяют дополнительные разделы профиля для службы сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕРВИЦЕ_ЕКСТРА_УИДС  <br/> |
|Идентификатор:  <br/> |0x3D0D  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Для каждого фильтра сообщений можно создавать новые разделы профилей. Когда информация о службе сообщений копируется в другой профиль, важно также скопировать дополнительные разделы профиля для этих фильтров. Поставщик услуг, использующий дополнительные разделы профилей, может хранить структуры **мапиуид** в разделах профилей в **пр_сервице_екстра_уидс**, что позволяет MAPI копировать дополнительные сведения о службе сообщений.
  
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


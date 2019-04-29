---
title: Каноническое свойство PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438962"
---
# <a name="pidtagservicename-canonical-property"></a>Каноническое свойство PidTagServiceName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя службы сообщений, заданной пользователем в файле MapiSvc. INF.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕРВИЦЕ_НАМЕ, ПР_СЕРВИЦЕ_НАМЕ_А, ПР_СЕРВИЦЕ_НАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x3D09  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Имя, которое хранится в этих свойствах, относится только к службе сообщений. Он поступает из раздела [Services] в MapiSvc. INF.
  
Эти свойства отображаются в виде столбца в таблице службы сообщений и могут использоваться для фильтрации служб. Так как он используется для идентификации и фильтрации служб, значение не должно быть локализовано.
  
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


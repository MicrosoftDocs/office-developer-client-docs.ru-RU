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
ms.openlocfilehash: d950ee21c0c4c41e84c0fe1f8104219e63f84cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592677"
---
# <a name="pidtagservicename-canonical-property"></a>Каноническое свойство PidTagServiceName

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит имя службы сообщение как набор пользователем в файла MapiSvc.inf.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3D09  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Имя, содержащихся в этих свойств для службы сообщений. Текст поступает из раздела [Services] в MapiSvc.inf.
  
Эти свойства отображаются в виде столбцов в таблице службы сообщений и может использоваться для фильтрации служб. Так как она используется для идентификации и фильтрации служб, значение не должно быть локализовано.
  
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


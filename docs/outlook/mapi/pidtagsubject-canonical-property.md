---
title: Каноническое свойство PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386308"
---
# <a name="pidtagsubject-canonical-property"></a>Каноническое свойство PidTagSubject

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит полный темы сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Идентификатор:  <br/> |0x0037  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства, рекомендуется использовать для всех объектов сообщения. 
  
Эти свойства, всегда текст полного темы, то есть, объединение префикс и нормализованный темы. Если префикс отсутствует, нормализованный темы должны совпадать с темы. Сообщение хранения или транспорта используется поставщик, как эти свойства, так и для свойства **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) для вычисления нормализованный темы, с помощью правила, описанные в разделе **PR_NORMALIZED_SUBJECT** ([ PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
Свойства темы — это обычно коротких строк менее 256 символов и поставщика хранилища сообщений не обязаны поддержки интерфейса **IStream** на них. Клиент должен всегда сначала попытаться доступ через интерфейс **IMAPIProp** и прибегать к **IStream** только в том случае, если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** . 
  
Для отчета это свойство содержит стоять строка, указывающая, что произошло с сообщением темы исходного сообщения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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


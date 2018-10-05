---
title: Каноническое свойство PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 889b43bb606cbe9c96d52c8a21ffda5dfcebb1da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383508"
---
# <a name="pidtagreportsearchkey-canonical-property"></a>Каноническое свойство PidTagReportSearchKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для получателя, должны получить отчеты для данного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REPORT_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x0054  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является одним из свойств адреса для получателя, который имеет делегированное отправителя для получения отчетов, созданных для данного сообщения.
  
Клиентское приложение, которое направлять отчеты другому пользователю следует устанавливать это свойство во время отправки сообщения. Если не указано, отчеты, передаются в отправителя сообщения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые в сообщениях электронной почты.
    
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


---
title: Каноническое свойство PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811723"
---
# <a name="pidtagreportname-canonical-property"></a>Каноническое свойство PidTagReportName

  
  
**Относится к**: Outlook 
  
Содержит отображаемое имя для получателя, должны получить отчеты для данного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W  <br/> |
|Идентификатор:  <br/> |0x003A  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойства адреса для получателя, который имеет делегированное отправителя для получения отчетов, созданных для данного сообщения.
  
Клиентское приложение, которое направлять отчеты другому пользователю необходимо задать эти свойства во время отправки сообщения. Если они не заданы, отчеты, передаются в отправителя сообщения.
  
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

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
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422315"
---
# <a name="pidtagreportname-canonical-property"></a>Каноническое свойство PidTagReportName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя получателя, который должен получить отчеты для этого сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕПОРТ_НАМЕ, ПР_РЕПОРТ_НАМЕ_А, ПР_РЕПОРТ_НАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x003A  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства являются примерами свойств адреса получателя, которым отправитель делегирован для получения любых отчетов, созданных для этого сообщения.
  
Клиентское приложение, которое должно маршрутизировать отчеты другому пользователю, должно задавать эти свойства во время отправки сообщения. Если они не заданы, отчеты отправляются отправителю сообщения.
  
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


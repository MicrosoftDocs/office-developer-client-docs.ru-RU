---
title: Каноническое свойство PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437863"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a>Каноническое свойство PidTagOriginatorRequestedAlternateRecipient

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи для альтернативного получателя, назначенного отправителем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ОРИГИНАТОР_РЕКУЕСТЕД_АЛТЕРНАТЕ_РЕЦИПИЕНТ  <br/> |
|Идентификатор:  <br/> |0x0C09  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется в перенаправляемых сообщениях. Если не разрешено использование пересылки или не назначен альтернативный получатель, следует создать отчет о недоставке.
  
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


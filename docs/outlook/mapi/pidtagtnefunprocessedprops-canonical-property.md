---
title: Каноническое свойство PidTagTnefUnprocessedProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9ea9938ca9f8dd0b25cf2de5199178a76e17b6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431325"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>Каноническое свойство PidTagTnefUnprocessedProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Serializes properties when filtering Transport Neutral Encapsulation Format (TNEF).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|Идентификатор:  <br/> |0x0E9C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MAPI, не передаваемая  <br/> |
   
## <a name="remarks"></a>Примечания

Используется корпорацией Майкрософт Outlook и Outlook веб-доступа (OWA) для сохранения исходного TNEF в случаях, когда TNEF содержит именные свойства, которые невозможно создать в магазине.
  
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


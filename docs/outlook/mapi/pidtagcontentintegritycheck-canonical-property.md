---
title: Каноническое свойство PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 53226daafd1c0a53f96db5af3432d6f34738fd93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585811"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Каноническое свойство PidTagContentIntegrityCheck

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение проверки целостности контента ASN.1, обеспечивающий отправителя сообщения для защиты содержимого сообщения от раскрытия несанкционированного получателям.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Идентификатор:  <br/> |0x0c00  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство предоставляет неотрекаемые содержимого сообщения. В сочетании с **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) гарантирует, что содержимое сообщения достигает места назначения без изменений.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


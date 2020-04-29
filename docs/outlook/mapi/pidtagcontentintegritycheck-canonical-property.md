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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415728"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Каноническое свойство PidTagContentIntegrityCheck

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение проверки целостности содержимого ASN. 1, позволяющее отправителю сообщения защитить содержимое сообщения от разглашения неавторизованным получателям.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Идентификатор:  <br/> |0x0C00  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет неподдельность содержимого сообщения. В сочетании с **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) это гарантирует, что содержимое сообщения поступает в свое место назначения без изменений.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


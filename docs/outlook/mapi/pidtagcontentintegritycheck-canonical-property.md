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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение проверки целостности контента ASN.1, которое позволяет отправителю сообщений защищать содержимое сообщения от раскрытия неавторизованным получателям.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Идентификатор:  <br/> |0x0C00  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство обеспечивает неопубликовку контента сообщений. В сочетании **с PR_MESSAGE_TOKEN** [(PidTagMessageToken)](pidtagmessagetoken-canonical-property.md)оно гарантирует, что содержимое сообщения поступает в пункт назначения без изменений.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


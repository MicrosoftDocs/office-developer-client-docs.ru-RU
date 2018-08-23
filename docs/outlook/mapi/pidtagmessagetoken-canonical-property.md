---
title: Каноническое свойство PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b5def94096f7664169935a062d3b28171fb2919
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578432"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Каноническое свойство PidTagMessageToken

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит маркер безопасности ASN.1 для сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Идентификатор:  <br/> |0x0C03  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Безопасного обмена сообщениями свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство передает защищенный конфиденциальные данные из его инициатор его получателю. В сочетании со свойством **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) это гарантирует метки связь с содержимым сообщения. В сочетании со свойством **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) проверяется, что содержимое сообщения не изменяется.
  
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


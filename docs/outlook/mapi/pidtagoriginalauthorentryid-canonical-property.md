---
title: Каноническое свойство PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425591"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи автора первой версии сообщения, то есть сообщения перед его переададрещением или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x004C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адресов для автора сообщения. При первой отправке сообщения клиентская заявка должна установить это свойство к значению **PR_SENDER_ENTRYID** [(PidTagSenderEntryId).](pidtagsenderentryid-canonical-property.md) Он никогда не меняется, когда сообщение переададовыв или отвечает на него. 
  
Исходное свойство автора позволяет сохранить сведения из локального домена обмена сообщениями. Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, это свойство предоставляет способ убедиться, что исходные сведения не будут потеряны.
  
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


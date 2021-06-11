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
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408189"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Каноническое свойство PidTagMessageToken

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит маркер безопасности ASN.1 для сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Идентификатор:  <br/> |0x0C03  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Безопасные свойства обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство передает защищенные сведения, связанные с безопасностью, от его источника до получателя. В сочетании с **свойством PR_MESSAGE_SECURITY_LABEL** [(PidTagMessageSecurityLabel)](pidtagmessagesecuritylabel-canonical-property.md)он гарантирует связь метки с содержимым сообщения. В сочетании с **свойством PR_CONTENT_INTEGRITY_CHECK** [(PidTagContentIntegrityCheck)](pidtagcontentintegritycheck-canonical-property.md)оно проверяет, что содержимое сообщения остается неизменным.
  
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


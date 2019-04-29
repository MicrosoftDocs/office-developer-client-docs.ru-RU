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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит маркер безопасности ASN. 1 для сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МЕССАЖЕ_ТОКЕН  <br/> |
|Идентификатор:  <br/> |0x0C03  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства безопасного обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство передает защищенные сведения о безопасности от инициатора получателю. В сочетании со свойством **пр_мессаже_секурити_лабел** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) она гарантирует связь метки с содержимым сообщения. В сочетании со свойством **пр_контент_интегрити_чекк** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) он проверяет, не изменилось ли содержимое сообщения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


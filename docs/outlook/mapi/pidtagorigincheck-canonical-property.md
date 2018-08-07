---
title: Каноническое свойство PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811499"
---
# <a name="pidtagorigincheck-canonical-property"></a>Каноническое свойство PidTagOriginCheck

  
  
**Относится к**: Outlook 
  
Содержит значение двоичные проверки, которая позволяет получателя отчета доставки для проверки origin исходного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Идентификатор:  <br/> |0x0027  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство предоставляет средства для сторонних производителей, такие как сообщения передачи (агента) или обмена мгновенными сообщениями пользователя получения отчетов о доставке, чтобы проверить источник отправляемого сообщения. Если этот параметр указан, для полученного сообщения, это свойство должен быть скопирован на любой отчетов о доставке, возникающие в ответ на сообщение.
  
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


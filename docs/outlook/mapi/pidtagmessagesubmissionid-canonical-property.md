---
title: Каноническое свойство PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a26a8483e584ccc5cf9f33e0dbd75f379c01633
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569668"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a>Каноническое свойство PidTagMessageSubmissionId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор система передачи сообщений для передачи сообщений (агента).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_SUBMISSION_ID  <br/> |
|Идентификатор:  <br/> |0x0047  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Данное свойство возвращает агента передачи сообщений при успешном выполнении отправки сообщений. Дальнейших контактов с помощью агента передачи сообщений о сообщении, например запрашивающая отмены используется идентификатор MTS в этом свойстве.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
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


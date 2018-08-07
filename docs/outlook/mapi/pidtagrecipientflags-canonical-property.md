---
title: Каноническое свойство PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811648"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Каноническое свойство PidTagRecipientFlags

  
  
**Относится к**: Outlook 
  
Задает битовое поле, которое описывает состояние получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Идентификатор:  <br/> |0x5FFD  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не требуется. Ниже приведены отдельные флаги, которые можно задать.
  
|**Значение**|**Описание**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |Получатель является **Sendable** Attendee. Этот флаг используется только в свойстве **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |**RecipientRow** , на котором установлен этот флаг представляет организатора собрания.  <br/> |
|Аварийного восстановления (recipExceptionalResponse 0x00000010)  <br/> |Указывает, что участник предоставили ответа для исключения, на котором находится в этом **RecipientRow** . Этот флаг используется только в **RecipientRow** объекта внедренных сообщений исключения объекта организатора собрания.  <br/> |
|ED (recipExceptionalDeleted 0x00000020)  <br/> |Указывает, что несмотря на то, что существует **RecipientRow** , его следует рассматривать как, если соответствующий получателя не поддерживает. Этот флаг используется только в **RecipientRow** объекта внедренных сообщений исключения объекта организатора собрания.  <br/> |
|X (зарезервирован, 0x00000040)  <br/> |Не должно быть задано.  <br/> |
|X (зарезервирован, 0x00000080)  <br/> |Не должно быть задано.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Указывает, что получатель является исходного участника. Этот флаг используется только в свойстве **dispidApptUnsendableRecips** .  <br/> |
|X (зарезервирован, 0x00000200)  <br/> |Зарезервировано.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


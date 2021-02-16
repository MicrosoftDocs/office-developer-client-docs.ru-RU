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
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356702"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Каноническое свойство PidTagRecipientFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает битовую область, описываемую состояние получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Идентификатор:  <br/> |0x5FFD  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не требуется. Ниже следующую помету можно установить отдельные флаги.
  
|**Значение**|**Описание**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |Получателем является **отправимый** участник. Этот флаг используется только в свойстве **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients).](pidlidappointmentunsendablerecipients-canonical-property.md)  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |**RecipientRow,** для которого установлен этот флаг, представляет организатор собрания.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Указывает, что участник ответил на исключение, в котором находится **этот RecipientRow.** Этот флаг используется только в **Объекте RecipientRow** объекта внедренного сообщения исключения объекта собрания организатора.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Указывает, что, хотя **RecipientRow существует,** его следует рассматривать как если бы соответствующий получатель этого не сделал. Этот флаг используется только в **Объекте RecipientRow** объекта внедренного сообщения исключения объекта собрания организатора.  <br/> |
|X (зарезервировано, 0x00000040)  <br/> |Не должно быть установлено.  <br/> |
|X (зарезервировано, 0x00000080)  <br/> |Не должно быть установлено.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Указывает, что получатель является исходным участником. Этот флаг используется только в свойстве **dispidApptUnsendableRecips.**  <br/> |
|X (зарезервировано, 0x00000200)  <br/> |Зарезервировано.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


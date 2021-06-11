---
title: Каноническое свойство PidTagRecipientProposedEndTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332776"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a>Каноническое свойство PidTagRecipientProposedEndTime

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает предлагаемое время окончания собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_PROPOSEDENDTIME  <br/> |
|Идентификатор:  <br/> |0x5FE4  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Примечания

Когда значение свойства **PR_RECIPIENT_PROPOSED** [(PidTagRecipientProposed)](pidtagrecipientproposed-canonical-property.md)задано значение TRUE, значение этого свойства указывает значение, запрашиваемое участниками, чтобы установить как значение свойства **dispidApptEndWhole** [(PidLidAppointmentEndWhole)](pidlidappointmentendwhole-canonical-property.md)для объекта собрания одного экземпляра или объекта исключения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
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


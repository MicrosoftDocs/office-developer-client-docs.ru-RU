---
title: Каноническое свойство PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345761"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Каноническое свойство PidLidResponseStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние ответа участника.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidResponseStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008218  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Собрания  <br/> |
   
## <a name="remarks"></a>Примечания

Состояние ответа должно быть одним из значений в приведенной ниже таблице.
  
|**Состояние ответа**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Отклик для этого объекта не требуется. Это касается объектов встреч и объектов ответа на собрания.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Это собрание принадлежит организатору.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Это значение на собрании участника указывает, что участник принял приглашение на собрание под вопросом.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Это значение в собрании участника не указывает, что участник принял приглашение на собрание.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Это значение в собрании участника указывает, что участник отклонил запрос на собрание.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Это значение на собрании участника указывает, что участник еще не ответил. Это значение занося в запрос на собрание, обновление собрания и отмену собрания.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


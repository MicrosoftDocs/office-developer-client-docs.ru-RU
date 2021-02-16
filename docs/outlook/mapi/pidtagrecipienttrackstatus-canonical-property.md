---
title: Каноническое свойство PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355288"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>Каноническое свойство PidTagRecipientTrackStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние ответа, возвращенного участником.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Идентификатор:  <br/> |0x5FFF  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Примечания

Если это значение не установлено, его необходимо считать respNone. В противном случае должно быть одно из следующих:
  
|**Состояние ответа**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Отклик для этого объекта не требуется. Это касается объектов встреч и объектов ответа на собрания.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Это значение в объекте собрания участника указывает, что участник предварительно принял объект запроса на собрание.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Это значение в объекте собрания участника указывает, что участник принял объект запроса на собрание.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Это значение в объекте собрания участника указывает, что участник отклонил объект запроса на собрание.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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


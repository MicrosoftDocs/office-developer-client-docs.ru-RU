---
title: Каноническое свойство PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386945"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a>Каноническое свойство PidLidNonSendableBccTrackStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение для каждого участника, указанный в свойстве **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidNonSendBccTrackStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008545  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является обязательным только в том случае, если свойство **dispidNonSendableBCC** имеет значение. Количество значений в это свойство должно быть равно значений в **dispidNonSendableBCC**. Каждое значение в это свойство соответствует участника в свойстве **dispidNonSendableBCC** с таким же индексом. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


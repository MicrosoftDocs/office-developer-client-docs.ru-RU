---
title: Каноническое свойство PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf9d11b7a53ee0b9911e32cb3c3e2a0a490e4729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592789"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a>Каноническое свойство PidLidNonSendToTrackStatus

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение для каждого участника, перечисленные в свойстве **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidNonSendToTrackStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008543  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является обязательным только в том случае, если свойство **dispidNonSendableTo** имеет значение. Количество значений в это свойство должно быть равно значений в **dispidNonSendableTo**. Каждое значение PT_LONG в это свойство соответствует участника в свойстве **dispidNonSendableTo** с таким же индексом. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


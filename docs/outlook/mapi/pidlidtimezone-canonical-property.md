---
title: Каноническое свойство PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810638"
---
# <a name="pidlidtimezone-canonical-property"></a>Каноническое свойство PidLidTimeZone

  
  
**Относится к**: Outlook 
  
Задает сведения о часовом поясе повторяющееся собрание.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |LID_TIME_ZONE  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000000C  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство читаются только в том случае, если свойство **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) не установлено, но если свойство **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) имеет значение TRUE и **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) свойство имеет значение FALSE. Снижение WORD задает индекс в таблицу, содержащую сведения о часовом поясе. Из верхней WORD читать только высший бит. Если этот бит задан, выберите часовой пояс по ссылке не увидите, что следует делать летнего времени (летнее время), в противном случае — подробное описание даты перехода на летнее время в [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
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


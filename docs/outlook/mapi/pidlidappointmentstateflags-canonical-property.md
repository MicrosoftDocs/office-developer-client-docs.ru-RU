---
title: Каноническое свойство PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810182"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a>Каноническое свойство PidLidAppointmentStateFlags

  
  
**Применимо к**: Outlook 
  
Задает битовое поле, которое описывает состояние объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptStateFlags  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008217  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Области:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не требуется. Ниже приведены отдельные флаги, которые можно задать.
  
M (asfMeeting, 0x00000001)
  
> Этот флаг указывает, что объект является собрания объектов или объектов, относящихся к собранию.
    
R (asfReceived 0x00000002)
  
> Этот флаг указывает, что представляемого объекта было получено из другого пользователя.
    
C (asfCanceled 0x00000004)
  
> Этот флаг указывает, что объект собрания, представленного объектом была отменена.
    
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
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)


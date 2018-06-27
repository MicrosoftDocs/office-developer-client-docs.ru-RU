---
title: Каноническое свойство PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: cac9c735403e6cb65dfe3111a2246a8387339339
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810092"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Каноническое свойство PidLidAppointmentAuxiliaryFlags

  
  
**Применимо к**: Outlook 
  
Задает битовое поле, которое описывает дополнительный состояние объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptAuxFlags  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008207  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Области:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не требуется. Ниже приведены отдельные флаги, которые можно задать.
  
C (auxApptFlagCopied, 0x00000001)
  
> Этот флаг указывает, что объект календаря, скопированный из другой папки календаря.
    
R (auxApptFlagForceMtgResponse 0x00000002)
  
> Этот флаг на приглашения на собрание указывает, что клиент или сервер следует отправить ответ на приглашение к организатора, при выборе ответа.
    
F (auxApptFlagForwarded 0x00000004)
  
> Этот флаг на приглашения на собрание указывает, что оно было перенаправлено (включая переадресацию организатором), а не приглашение из картинок.
    
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

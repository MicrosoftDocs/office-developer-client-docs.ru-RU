---
title: Каноническое свойство PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341995"
---
# <a name="pidlidcalendartype-canonical-property"></a>Каноническое свойство PidLidCalendarType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает значение поля CalendarType из свойства **dispidApptRecur** ([PidLidAppointmentRecur).](pidlidappointmentrecur-canonical-property.md)
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |LID_CALENDAR_TYPE  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x0000001C  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Собрания  <br/> |
   
## <a name="remarks"></a>Примечания

Когда запрос на собрание представляет повторяющийся ряд или исключение, это значение поля CalendarType из свойства **dispidApptRecur.** В противном случае это свойство не устанавливается и считается 0. 
  
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


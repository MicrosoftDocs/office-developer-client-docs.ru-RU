---
title: Каноническое свойство PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342030"
---
# <a name="pidlidbusystatus-canonical-property"></a>Каноническое свойство PidLidBusyStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет доступность пользователя для встречи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidBusyStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008205  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает доступность пользователя для события, описанного объектом, и должно быть одним из значений, указанных ниже.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Пользователь доступен.  <br/> |
|0x00000001  <br/> |У пользователя запланировано предварительное событие.  <br/> |
|0x00000002  <br/> |Пользователь занят.  <br/> |
|0x00000003  <br/> |Пользователь находится вне офиса.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)


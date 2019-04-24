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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345362"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a>Каноническое свойство PidLidAppointmentStateFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает битовое поле, описывающее состояние объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидапптстатефлагс  <br/> |
|Набор свойств:  <br/> |Псетид_аппоинтмент  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008217  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство не является обязательным. Ниже приводятся отдельные флаги, которые можно задать.
  
M (Асфмитинг, 0x00000001)
  
> Этот флаг указывает, что объект является объектом собрания или объектом, связанным с собранием.
    
R (Асфрецеивед, 0x00000002)
  
> Этот флаг указывает, что предоставленный объект был получен от другого пользователя.
    
C (Асфканцелед, 0x00000004)
  
> Этот флаг указывает, что объект собрания, представленный объектом, был отменен.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


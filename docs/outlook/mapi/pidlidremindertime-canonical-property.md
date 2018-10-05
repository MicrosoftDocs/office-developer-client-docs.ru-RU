---
title: Каноническое свойство PidLidReminderTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382472"
---
# <a name="pidlidremindertime-canonical-property"></a>Каноническое свойство PidLidReminderTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает время первоначальной сигнал напоминания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidReminderTime  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008502  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Замечания

Для объектов, календарь это свойство представляет время, когда пользователь может быть позднее которого является время начала встречи. Клиенты необходимо задать значение в формате UTC.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


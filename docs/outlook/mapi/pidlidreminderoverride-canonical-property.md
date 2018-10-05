---
title: Каноническое свойство PidLidReminderOverride
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4956ce33d00135c34193dec3df832c6878b2c6db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385965"
---
# <a name="pidlidreminderoverride-canonical-property"></a>Каноническое свойство PidLidReminderOverride

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, будет ли клиента должны учитывать значения свойства **dispidReminderFileParam** ( [PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) и **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidReminderOverride  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000851C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Замечания

Клиент может использовать значения по умолчанию вместо значений свойств **dispidReminderPlaySound** и **dispidReminderFileParam** . 
  
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


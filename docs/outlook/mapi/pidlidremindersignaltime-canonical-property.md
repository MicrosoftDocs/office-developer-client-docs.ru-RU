---
title: Каноническое свойство PidLidReminderSignalTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350857"
---
# <a name="pidlidremindersignaltime-canonical-property"></a>Каноническое свойство PidLidReminderSignalTime

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает момент времени, в течение которого напоминание переходит из состояния ожидания в статус просрочено.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидреминдернексттиме  <br/> |
|Набор свойств:  <br/> |Псетид_коммон  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008560  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Напоминание  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть задано, если свойство **диспидреминдерсет** ([PIDLIDREMINDERSET](pidlidreminderset-canonical-property.md)) имеет значение true. Клиенты должны задать значение в формате UTC.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


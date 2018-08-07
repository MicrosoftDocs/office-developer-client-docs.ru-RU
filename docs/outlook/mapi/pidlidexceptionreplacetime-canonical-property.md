---
title: Каноническое свойство PidLidExceptionReplaceTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2292d53997fd4d54e9272789be83ea94a93c6a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810291"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a>Каноническое свойство PidLidExceptionReplaceTime

  
  
**Относится к**: Outlook 
  
Указывает дату и время в рамках повторов, которое заменит исключение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidExceptionReplaceTime  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008228  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Значением должен быть указан в формате UTC. Это свойство позволяет найти для конкретного экземпляра объект исключения вложения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств.
    
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


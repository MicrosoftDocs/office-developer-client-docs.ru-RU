---
title: Каноническое свойство PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390851"
---
# <a name="pidlidisrecurring-canonical-property"></a>Каноническое свойство PidLidIsRecurring

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, связан ли объект с серии повторяющихся.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |LID_IS_RECURRING  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00000005  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Значение TRUE указывает, что объект представляет серии повторяющихся или исключение (включая потерянного экземпляра). Значение FALSE или отсутствие этого свойства указывает, что объект представляет один экземпляр. Обратите внимание на разницу между этого свойства и свойства **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


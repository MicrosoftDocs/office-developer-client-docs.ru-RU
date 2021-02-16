---
title: Каноническое свойство PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357962"
---
# <a name="pidlidtaskordinal-canonical-property"></a>Каноническое свойство PidLidTaskOrdinal

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет помощь в пользовательских задачах сортировки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskOrdinal  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008123  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может не быть заданной. Если установлено значение, значение должно быть больше 0x800186A0 (-2 147 383 648) и меньше значения 0x7FFE7960 (2 147 383 648) и должно быть уникальным для задач в одной папке.
  
Каждый раз, когда клиент задает для этого свойства число, меньшее, чем отрицательное текущее значение свойства **PR_ORDINAL_MOST** ([PidTagOrdinalMost)](pidtagordinalmost-canonical-property.md)папки, клиент также должен обновить PR_ORDINAL_MOST в папке.  
  
Свойство **PR_ORDINAL_MOST** папки обеспечивает эффективный способ определения уникального значения между задачами в одной папке. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач. 
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


---
title: Каноническое свойство PidLidTaskOwnership
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332111"
---
# <a name="pidlidtaskownership-canonical-property"></a>Каноническое свойство PidLidTaskOwnership

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает роль текущего пользователя относительно задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskOwnership  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008129  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно иметь одно из следующих значений.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Задача не назначена.  <br/> |
|0x00000001  <br/> |Задача является копией задачи, которая является копией задачи.  <br/> |
|0x00000002  <br/> |Задача является копией задачи, которую назначает его.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
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


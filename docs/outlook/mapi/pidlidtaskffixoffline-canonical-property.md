---
title: Каноническое свойство PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303040"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>Каноническое свойство PidLidTaskFFixOffline

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает точность свойства **dispidTaskOwner** ([PidLidTaskOwner).](pidlidtaskowner-canonical-property.md)
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskFFixOffline  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x0000812C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Примечания

Если свойство **dispidTaskFFixOffline** имеет значение FALSE или не замечено, значение свойства **dispidTaskOwner** является правильным. Если **для dispidTaskFFixOffline** установлено значение TRUE, клиент не может определить точное значение **для dispidTaskOwner.** В этом случае клиент может установить **для dispidTaskOwner** универсальное имя владельца, например "Unknown". Однако если клиент сталкивается со значением **dispidTaskFFixOffline** true и может определить точное имя владельца, клиент должен обновить **dispidTaskOwner** и установить **для dispidTaskFFixOffline** значение FALSE. 
  
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


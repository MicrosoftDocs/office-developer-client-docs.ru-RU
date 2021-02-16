---
title: Каноническое свойство PidLidTaskLastDelegate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355673"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a>Каноническое свойство PidLidTaskLastDelegate

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 Имя пользователя, который недавно был назначен или назначен задаче. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskLastDelegate  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008125  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Примечания

Перед отправкой запроса задачи клиент присваивает этому свойству имя назначения задачи. Перед отправкой ответа на задачу клиент присваивает этому свойству имя его.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
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


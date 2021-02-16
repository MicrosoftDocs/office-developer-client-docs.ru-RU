---
title: Каноническое свойство PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356495"
---
# <a name="pidlidtaskversion-canonical-property"></a>Каноническое свойство PidLidTaskVersion

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, какая копия является последним обновлением задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskVersion  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008112  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Примечания

Обновления с более низкими версиями, чем задача, игнорируются. 
  
При внедрении задачи в связь с задачей клиент также задает текущую версию внедренной задачи для связи с задачей.
  
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


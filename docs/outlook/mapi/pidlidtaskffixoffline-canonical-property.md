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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает точность свойства **диспидтасковнер** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидтаскффиксоффлине  <br/> |
|Набор свойств:  <br/> |Псетид_таск  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x0000812C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Замечания

Если свойство **диспидтаскффиксоффлине** имеет значение false или не задано, то значение свойства **диспидтасковнер** является правильным. Если для **диспидтаскффиксоффлине** задано значение true, клиент не может определить точное значение для **диспидтасковнер**. В этом случае клиент может задать **диспидтасковнер** в качестве имени универсального владельца, например "Unknown". Тем не менее, если клиент встречает значение **диспидтаскффиксоффлине** в true и может определить точное имя владельца, клиент должен обновить **диспидтасковнер** и задать для **диспидтаскффиксоффлине** значение false. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач. 
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


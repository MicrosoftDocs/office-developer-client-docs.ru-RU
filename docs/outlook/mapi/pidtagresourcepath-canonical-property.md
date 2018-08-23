---
title: Каноническое свойство PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a00abec7627eb12e23e7b76f5d0900514d710ffb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593097"
---
# <a name="pidtagresourcepath-canonical-property"></a>Каноническое свойство PidTagResourcePath

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит путь к серверу поставщика услуг.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Идентификатор:  <br/> |0x3E07  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Путь, содержащийся в эти свойства представляет предложенный путь, где пользователь может найти ресурсы. Определение этих свойств зависит от поставщика. Например планирования приложение использует эти свойства для указания предложенного расположения для ее планирования файлы приложения.
  
Эти свойства предоставляющей обмена сообщениями профилей пользователей для удобства, чтобы клиентского приложения не нужно запрашивать обмена сообщениями для сетевой путь или сетевого диска.
  
MAPI работает только с именами файлов в набор знаков American National стандартов института (ANSI). Приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)


---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566665"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Проверяет две структуры [MAPIUID](mapiuid.md) определяет, содержат ли они тот же идентификатор. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Параметры

 _lpuid1_
  
> Указатель на структуру первого **MAPIUID** , который необходимо проверить. 
    
 _lpuid2_
  
> Указатель на структуру второй **MAPIUID** , который необходимо проверить. 
    
## <a name="remarks"></a>Замечания

Макрос **IsEqualMAPIUID** возвращает значение TRUE, если две структуры **MAPIUID** содержат тот же идентификатор и значение FALSE, если это не так. 
  
Макрос **IsEqualMAPIUID** необходимо включить файл заголовка Memory.h. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)


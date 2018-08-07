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
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809580"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Относится к**: Outlook 
  
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

